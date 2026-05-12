---
layout: default
title: "Learning Analytics and Institutional Operations"
nav_order: 5
parent: "Core Topics"
description: "Educational data mining, learning analytics, course scheduling optimization, operational efficiency, and institutional technology strategy."
---
## Overview

Learning analytics and institutional operations represent a rapidly evolving domain at the intersection of computer science, education, and statistics. The field encompasses how higher education institutions collect, analyze, and act on data to improve student outcomes, optimize resource allocation, and navigate digital transformation. From predictive models that identify at-risk students to optimization algorithms that streamline course scheduling and faculty assignment, data-driven approaches are reshaping how institutions operate.

A central theme emerging from the research is that operational efficiency and student outcomes need not trade off against each other. Computational optimization of course scheduling and faculty assignment can generate significant cost savings -- in documented cases, on the order of six figures annually per institution -- while simultaneously improving instructional quality indicators such as full-time faculty coverage, workload equity, and section availability (Xue et al., 2024; Domenech & Lusa, 2016). The guiding principle is **outcome neutrality**: efficiency gains achieved through better data use and structural optimization are strategically sound; efficiency gains that degrade the learning environment are not.

Yet adoption remains uneven. While 93% of chief online learning officers agree that data analytics is a strategic priority for improving online learning (Simunich et al., 2025), only 40% say online learning data is well-defined and understood at their institution. Technology solutions that collect data can help advisors identify and address risks early, but integration across systems remains a persistent pain point (Axim Strategy Briefing). The field continues to grapple with how technology should be deployed -- whether it will replace or empower human workers -- and how to bridge the silos that separate technology leaders from educators and policymakers.

## Key Concepts and Definitions

**Educational Data Mining (EDM)** refers to the application of data mining techniques to data from educational environments to address important educational questions. EDM emphasizes developing new methods and algorithms for exploring the unique types of data that come from educational settings (Romero & Ventura, 2024).

**Learning Analytics (LA)** is defined as the measurement, collection, analysis, and reporting of data about learners and their contexts, for purposes of understanding and optimizing learning and the environments in which it occurs. LA emphasizes three crucial elements: data, analysis, and action (Romero & Ventura, 2024; Mukred et al., 2024).

**Academic Analytics and Institutional Analytics** focus on the collection, analysis, and visualization of academic program activities for institutional-level insight, oriented toward political and economic decision-making rather than individual learner outcomes (Romero & Ventura, 2024).

**Teaching Analytics** involves the analysis of teaching activities and performance data from the instructor's point of view, supporting pedagogical improvement.

**Learning Analytics Technology (LAT)** refers to the integrated systems and platforms institutions deploy to operationalize learning analytics at scale, including dashboards, early warning systems, and predictive models (Mukred et al., 2024).

**University Course Timetabling Problem (UCTP)** is the complex, multi-dimensional assignment problem involving students, instructors, courses, timeslots, and classrooms. It has been proven to be NP-complete, requiring decomposition or heuristic approaches for practical solutions (Xue et al., 2024).

**Hybrid Campus** transcends the current idea of blended education into a more holistic vision for delivering everything an institution offers, integrating in-person, online, and technology-mediated experiences across academic and support services (Axim Strategy Briefing).

## Current State of Research

### Learning Analytics and Data Mining

The EDM and LA research communities have grown rapidly since their formalization in the late 2000s. EDM emerged from its first dedicated conference in 2008, while the first Learning Analytics and Knowledge (LAK) conference was held in 2011. By 2018, both fields had produced thousands of papers, with LA publications slightly outpacing EDM (Romero & Ventura, 2024). Two dedicated open-access journals -- the Journal of Educational Data Mining and the Journal of Learning Analytics -- serve as primary venues alongside high-impact outlets such as Computers and Education and the British Journal of Educational Technology.

The methods used across the field span a wide range: prediction (classification and regression), clustering, relationship mining, process mining, social network analysis, text mining, knowledge tracing, visualization, and recommendation systems (Romero & Ventura, 2024). Current topics of particular interest include early warning systems for at-risk students, multimodal learning analytics that draw on sensor and behavioral data, dashboards and visual analytics for instructors, deep learning approaches, and transfer learning to enable models to generalize across courses and institutions.

A bibliometric analysis of 2,779 publications from 2018 to 2023 across Scopus and Web of Science found that LA research trends have fluctuated, with a gradual decline in Web of Science publications since 2020 (Bunsu & Abd Halim, 2023). Despite fluctuations in publication volume, the research base has proven robust. Post-pandemic studies continue to demonstrate the value of LA for tackling online learning challenges, with prediction and clustering remaining the most commonly used techniques. Recent work includes models for early dropout detection, student engagement profiling, and team cohesion analysis using online trace data.

A significant trend in the post-pandemic era is the integration of artificial intelligence with learning analytics. Researchers have combined AI-based performance prediction models with LA approaches such as social network analysis and content analysis to generate real-time feedback in collaborative learning contexts, leading to measurable improvements in student engagement (Bunsu & Abd Halim, 2023). Natural language processing has been incorporated into peer assessment systems to improve feedback quality and grading accuracy.

**Predictive Analytics and Early Warning Systems.** Predicting student performance and identifying at-risk learners remains a central application. Techniques range from traditional classification models to neural network approaches for early prediction in self-paced courses. Multi-class phased prediction models have been developed to detect students at risk of dropping out at progressive stages of their academic journey (Bunsu & Abd Halim, 2023). The Axim Strategy Briefing confirms that technology solutions collecting data can help advisors identify and address risks early, though system integration remains a barrier to effective deployment.

### Institutional Optimization and Scheduling

Operational efficiency in higher education extends beyond analytics on learning data to encompass the optimization of course scheduling, faculty assignment, and resource allocation. These problems are computationally complex but have significant financial and pedagogical implications.

**Course Scheduling Optimization.** Xue et al. (2024) developed a decision support system that decomposes the NP-complete University Course Timetabling Problem into two hierarchical sub-models: one integrating course schedule planning with instructor assignment, and a second handling timeslot and classroom allocation. Using historical data from a department at Kent State University encompassing 20 full-time faculty and 45 undergraduate plus 17 graduate courses, the model achieved a 14% reduction in course sections (from 178 to 153), translating to approximately $130,000 in annual savings. The proportion of sections taught by full-time faculty rose from 57% to 65%, meeting accreditation thresholds. New course assignments to instructors were reduced by up to 81%, and distinct course sections per instructor decreased by 29%, freeing faculty time for deeper course preparation and research.

The model uses demand forecasting based on historical enrollment and registration patterns to determine optimal section counts, then assigns instructors using mixed integer linear programming (MILP) with a tunable parameter balancing the competing goals of minimizing new course preparations versus minimizing distinct course assignments. Solving time was under five seconds for the full model with over 9,000 integer variables and nearly 17,000 constraints.

**Teacher Assignment Models.** Domenech and Lusa (2016) formalized the Teacher Assignment Problem as a MILP model that simultaneously optimizes teacher satisfaction (through preference honoring) and workload balance (through equitable distribution across categories). Applied to real data from a department at the Universitat Politecnica de Catalunya with 30 teachers and approximately 80 course groups, the model improved teacher preference satisfaction by approximately 30% compared to manual assignment while substantially reducing workload imbalance. A calibration methodology using normalized objectives identified a weight parameter around 0.7-0.8 as providing the best trade-off. Most instances solved to optimality within minutes, with gaps below 1%.

Both scheduling studies demonstrate that operations research methods can replace time-consuming manual processes with transparent, fair, and financially beneficial automated solutions, though real-world adoption requires interactive decision support tools that departmental administrators can use without specialized expertise.

**Efficiency Without Compromising Outcomes: A Guiding Principle.** A critical finding from the scheduling literature is that operational optimization need not trade off against student experience. In fact, poor scheduling decisions can actively harm outcomes. Ran and Sanders (2020) demonstrated that the widely cited negative effect of part-time faculty on student persistence is largely a scheduling artifact: adjunct instructors disproportionately teach at non-traditional times (evenings, weekends) that are independently associated with lower subsequent enrollment. When scheduling is controlled, the direct effect of part-time faculty status on outcomes largely disappears. This reframes the "adjunct effect" as a scheduling problem rather than a quality problem -- and one that optimization tools are well-positioned to address.

The principle that emerges is straightforward: technology-driven efficiency gains should be pursued when they are student-neutral or student-positive. Reducing course sections to match actual demand (rather than historical habit) is student-neutral. Reallocating qualified instructors across time slots more equitably is student-positive. Eliminating courses that serve small but high-need populations to cut costs is neither. Institutions should evaluate operational optimization proposals against this standard, and prioritize reinvesting realized savings into the direct student supports -- advising, tutoring, financial aid -- that the research consistently shows drive persistence and completion.

### Technology Strategy and Digital Transformation

Institutional technology strategy in higher education is increasingly shaped by the twin forces of AI adoption and the transition toward hybrid campus models.

**AI Strategy and Investment.** According to the CHLOE 10 survey of chief online learning officers (Simunich et al., 2025), only 23% of institutions report having an institution-wide AI strategy, while 66% describe localized efforts across individual units. However, expectations for AI's importance are rising sharply: currently 56% rate AI as "somewhat" important, but looking two years ahead, 39% expect it to be "very" important and 33% "extremely" important. Top AI investment goals include preparing students for the workforce (77%), improving student learning (67%), and exploring new instructional methods (59%). Current AI tool usage spans workload efficiency (49%), course preparation (46%), accessibility (37%), learning analytics (27%), and predictive analytics (21%).

**The Hybrid Campus Transformation.** The Axim Strategy Briefing describes a hybrid campus that transcends current blended education models into a holistic vision for delivering everything an institution offers. Infrastructure for hybrid pathways has improved, but universities will require support to transition to student-centered hybrid models. Evolved institutional capacity is needed.

The CHLOE 10 data illustrates how COLOs envision the student experience evolving over the next five years. For traditional-age undergraduates, keywords like "physical classroom" are expected to decline sharply (from 70% to 32%), while "AI support services" is projected to surge from 1% to 43% and "AI tutoring" from 2% to 31%. Adaptive learning is expected to grow from 2% to 21%, and competency-based approaches from 3% to 18%. For adult undergraduates, AI support services are projected to jump from 2% to 51%. These projections suggest a fundamental restructuring of how institutions deliver education, with technology playing a central rather than supplementary role.

**Data Strategy and Governance.** While 93% of COLOs agree that data analytics is a strategic priority and 96% consider it essential for decision-making, implementation lags behind aspiration. Only 40% report that online learning data is well-defined and understood, and only 52% agree that effective data governance policies are in place (Simunich et al., 2025). Data privacy is recognized as a strategic priority by 85%, and 89% evaluate data privacy during technology procurement.

## Challenges and Barriers

**System Integration and Interoperability.** Many technology solutions in higher education are independently implemented, and lack of integration is a key challenge to adoption (Axim Strategy Briefing). Data portability standards such as Experience API (xAPI) and IMS Caliper are important for enabling data sharing across systems, but adoption remains inconsistent (Romero & Ventura, 2024).

**Adoption Barriers.** A study of learning analytics technology adoption in Saudi higher education institutions using an extended Technology Acceptance Model found that perceived usefulness, top management support, financial support, and government policy are the primary drivers of adoption intention (Mukred et al., 2024). Notably, perceived ease of use did not significantly influence adoption intention, suggesting that stakeholders accept complexity if the system demonstrably improves their work. This finding underscores that organizational and environmental factors -- leadership commitment, funding, and policy frameworks -- may matter more than technical usability for analytics adoption.

**Faculty Readiness.** Only 28% of institutions rate their faculty as fully prepared for online course design, and 77% of faculty are not fully prepared for online teaching in 2025, virtually unchanged from 75% in 2020 (Simunich et al., 2025). Adjunct faculty carry the largest share of online teaching, with nearly half of COLOs reporting adjuncts in the large or very large category of online teaching distribution.

**Digital Equity.** The digital divide persists as a barrier: 88% of COLOs say it affects at least some online students, with community colleges reporting the greatest impact (38% say it affects many students) (Simunich et al., 2025). The Axim Strategy Briefing reports that 40% of students still experience stress due to unstable internet and 22% lack access to a computer or tablet. Access disparities for AI tools compound existing inequities, with 57% of COLOs reporting that at least some online learners are impacted by differences in AI tool access.

**Privacy and Ethics.** EDM and LA raise significant concerns around data privacy, informed consent, and ethical use. Preprocessing and anonymization of data consume substantial effort, and guidelines about ethical issues require ongoing attention (Romero & Ventura, 2024). Challenges include making LA initiative goals transparent, ensuring privacy of all parties involved, defining data lifetime policies, and meeting high ethical standards that produce beneficial outcomes for all stakeholders.

**Siloed Conversations.** Conversations between technology leaders and educators or policymakers remain in silos, impeding the integrated approach needed for effective institutional transformation (Axim Strategy Briefing).

**Institutional Preparedness.** Only 28% of institutions have a documented academic continuity plan, and only 37% are fully prepared to address the digital divide with resources (Simunich et al., 2025). Revenue-sharing models for online programs remain contentious, with only 37% of COLOs saying their models work well.

## Best Practices and Recommendations

**Adopt a Multi-Level Approach to Analytics Implementation.** Successful LA adoption requires alignment across individual perceptions (perceived usefulness), organizational support (top management commitment and financial resources), and governmental or regulatory frameworks (Mukred et al., 2024). Institutions should secure visible leadership support before investing in technical infrastructure.

**Invest in Training and Professional Development.** Training significantly influences both perceived usefulness and perceived ease of use of analytics systems (Mukred et al., 2024). Faculty development programs should emphasize practical benefits and applications rather than technical complexity. Given that faculty preparedness has stagnated over five years, new approaches to professional development are needed.

**Ensure Adequate Technical Infrastructure.** Cloud computing ability and big data facility availability enhance the usefulness and ease of use of analytics platforms (Mukred et al., 2024). Institutions should build or procure adequate infrastructure -- including cloud services and data warehousing -- before deploying analytics tools at scale.

**Pursue System Integration Over Point Solutions.** Rather than deploying independent technology solutions, institutions should prioritize interoperability and integration across data systems. Adoption of data portability standards (xAPI, IMS Caliper) can facilitate cross-system analytics and reduce the integration pain points identified in the Axim Strategy Briefing.

**Use Optimization Models for Scheduling and Assignment.** MILP-based decision support systems for course scheduling and instructor assignment can generate substantial financial savings (14% section reduction, approximately $130,000 annually in one case) while improving fairness, faculty satisfaction, and accreditation compliance (Xue et al., 2024; Domenech & Lusa, 2016). These models should be developed as interactive tools accessible to department administrators.

**Develop Comprehensive Data Governance.** With only 52% of institutions reporting effective data governance, there is significant room for improvement. Institutions should establish clear policies for data definition, ownership, privacy, and ethical use, particularly as AI tools become more prevalent.

**Address Digital Equity Proactively.** Mitigation strategies for the digital divide include loaner technology programs, online readiness assessments, on-campus computer labs, grants for technology costs, Universal Design for Learning principles, digital literacy workshops, and open educational resources (Simunich et al., 2025).

**Plan for the Hybrid Campus Strategically.** The transition to a student-centered hybrid model requires evolved institutional capacity and deliberate planning, not ad hoc adoption. Institutions should develop institution-wide AI strategies (currently only 23% have one) and prepare for a future where AI tutoring, adaptive learning, and AI support services are central to the student experience.

## Implications for Practice

The convergence of learning analytics, operational optimization, and digital transformation creates both opportunities and imperatives for higher education institutions:

1. **Cost management under pressure.** Institutions face continued pressure for more affordable learning with demonstrable ROI and growing need for lifelong learning pathways (Axim Strategy Briefing). Course scheduling optimization alone can yield six-figure annual savings while maintaining or improving instructional quality.

2. **From data collection to data action.** The field has matured beyond questions of whether to collect data toward questions of how to act on it effectively. The knowledge discovery cycle -- from data collection through preprocessing, analysis, interpretation, and action -- requires institutional commitment at every stage (Romero & Ventura, 2024).

3. **AI as a transformative force.** Generative AI is only beginning to show its potential in higher education (Axim Strategy Briefing), but COLOs project dramatic shifts in the student experience within five years. Institutions that develop AI strategies now will be better positioned than those pursuing localized, uncoordinated efforts.

4. **Nondegree and alternative credentials.** Investment in nondegree offerings has surged, with 65% of COLOs reporting significant investment, up from 29% in 2019 (Simunich et al., 2025). Analytics and scheduling systems will need to accommodate these expanding program portfolios.

5. **Empowering rather than replacing.** The field continues to grapple with whether technology will replace or empower human workers (Axim Strategy Briefing). The most effective implementations use analytics and optimization to augment human decision-making -- helping advisors identify risks, helping department heads make fair assignments, helping faculty focus on teaching rather than administration -- rather than automating away human judgment.

## Related Topics

- [Academic Readiness and Course Design](academic-readiness-and-course-design.md)
- [Student Support, Belonging, and Persistence](student-support-belonging-persistence.md)
- [Credentials, Pathways, and the Labor Market](credentials-pathways-labor-market.md)
- [Workforce Development and Career Navigation](workforce-development-career-navigation.md)

## Sources

- Bunsu, C., & Abd Halim, N. D. (2023). A Review of Trends and Applications of Learning Analytics in Higher Education in the Post-Pandemic Era. *Innovative Teaching and Learning Journal*, 7(2), 19-24.
- Domenech, B., & Lusa, A. (2016). A MILP Model for the Teacher Assignment Problem Considering Teachers' Preferences. *European Journal of Operational Research*, 249, 1153-1160.
- Mukred, M., Mokhtar, U. A., Hawash, B., AlSalman, H., & Zohaib, M. (2024). Learning Analytics Technology Adoption in Saudi Higher Learning Institutions: An Extended TAM Study. *Heliyon*, 10, e26315.
- Romero, C., & Ventura, S. (2024). Educational Data Mining and Learning Analytics: An Updated Survey. *WIREs Data Mining and Knowledge Discovery*.
- Simunich, B., Garrett, R., Fredericksen, E. E., & Gay, K. (2025). CHLOE 10: Meeting the Moment -- Navigating Growth, Competition, and AI in Online Higher Education. Quality Matters.
- Xue, G., Offodile, O. F., Razavi, R., Kwak, D.-H., & Benitez, J. (2024). Addressing Staffing Challenges Through Improved Planning: Demand-Driven Course Schedule Planning and Instructor Assignment in Higher Education. *Decision Support Systems*, 187, 114345.
- Axim Strategy Briefing (internal strategy document).
