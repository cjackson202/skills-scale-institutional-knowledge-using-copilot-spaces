# Sample Collaboration Scenarios

This document provides real-world examples of how different roles at OctoAcme collaborate to deliver successful projects. These scenarios illustrate typical interactions, responsibilities, and communication patterns.

---

## Scenario 1: New Feature Development - E-commerce Checkout Optimization

### Context
The Product Manager has identified through analytics that cart abandonment rates are high. The team needs to redesign the checkout flow to improve conversion rates.

### Role Interactions

**Product Manager (Sarah)**
- Analyzes data showing 65% cart abandonment rate
- Defines success metrics: Reduce abandonment to <40%, increase checkout completion by 30%
- Creates problem statement and prioritizes in the roadmap
- Communicates to stakeholders: "We're tackling checkout friction in Q2"

**Business Analyst (Marcus)**
- Conducts stakeholder interviews with sales and customer support
- Documents current checkout process flow
- Gathers requirements: guest checkout, saved payment methods, progress indicator
- Creates user stories with acceptance criteria
- Validates requirements with Sarah and key stakeholders

**UX/UI Lead (Priya)**
- Reviews Marcus's process flows and user stories
- Conducts user research: 5 usability tests on current checkout
- Creates wireframes for simplified 3-step checkout
- Designs high-fidelity mockups with progress indicator
- Presents designs to team, iterates based on feedback
- Collaborates with Marcus to ensure design meets business requirements

**Developer (Alex)**
- Reviews Priya's designs and Marcus's acceptance criteria in sprint planning
- Asks clarifying questions about edge cases (expired cards, address validation)
- Implements frontend checkout components using design system
- Works with backend team on payment API integration
- Reviews code with team, addresses feedback

**Quality Assurance Lead (Jordan)**
- Reviews user stories and designs to plan test strategy
- Creates test cases for happy path and edge cases (payment failures, timeouts)
- Develops automated e2e tests for checkout flows
- Performs exploratory testing on staging environment
- Identifies usability issue: error messages unclear - works with Priya to improve
- Reports readiness: "All critical tests passing, 95% coverage"

**DevOps Specialist (Taylor)**
- Sets up feature flag for gradual rollout
- Configures monitoring for checkout completion metrics
- Creates alerts for payment gateway errors
- Supports deployment to staging and production
- Monitors rollout, ensures no performance degradation

**Project Manager (Lisa)**
- Facilitates sprint planning, ensuring everyone understands the scope
- Tracks progress on project board, identifies blocker with payment provider API
- Coordinates stakeholder demo
- Ensures documentation is updated
- Facilitates retrospective to capture learnings

### Key Touchpoints
1. **Kickoff Meeting**: Lisa facilitates, Sarah presents problem statement, all roles discuss approach
2. **Design Review**: Priya presents designs, Marcus validates against requirements, Jordan identifies testability concerns
3. **Sprint Planning**: Lisa facilitates, team breaks down work, Jordan defines testing approach
4. **Daily Standups**: Brief updates, blockers discussed (e.g., Alex blocked on API docs, Taylor helps)
5. **Demo**: Sarah, Priya, and Alex demonstrate completed feature to stakeholders
6. **Retrospective**: Lisa facilitates, team discusses what went well (early collaboration) and improvements (need earlier DevOps involvement)

### Outcome
- Feature deployed with 90% success rate initially, scaled to 100% after monitoring period
- Checkout abandonment reduced to 38%, exceeding target
- Team velocity maintained with minimal bugs in production

---

## Scenario 2: Critical Production Bug - Data Export Timeout

### Context
A critical bug is reported: enterprise customers cannot export large datasets. The export times out after 30 seconds, impacting 15% of paid customers.

### Role Interactions

**Quality Assurance Lead (Jordan)**
- Triages incoming bug report as P0-Critical
- Reproduces issue with datasets >10,000 rows
- Documents steps to reproduce and affected versions
- Escalates to development team and Project Manager

**DevOps Specialist (Taylor)**
- Reviews production logs and identifies timeout in API gateway
- Checks monitoring dashboards for related errors
- Provides log snippets and error patterns to developers
- Temporarily increases timeout as interim mitigation

**Developer (Alex)**
- Reviews logs and code, identifies N+1 query problem
- Proposes solution: implement pagination and background job processing
- Creates hotfix for immediate relief: optimize query with database indexes
- Works with Taylor to test hotfix in staging

**Product Manager (Sarah)**
- Assesses customer impact and urgency
- Communicates with affected customers: "We've identified the issue and are deploying a fix within 4 hours"
- Prioritizes long-term solution (background jobs) in next sprint
- Updates stakeholders on resolution timeline

**Project Manager (Lisa)**
- Coordinates rapid response across team
- Tracks progress of hotfix deployment
- Documents incident timeline for post-mortem
- Schedules post-mortem meeting

**Business Analyst (Marcus)**
- Documents current export process and failure scenarios
- Gathers requirements for improved export feature
- Identifies similar patterns in other reporting features that may need review

### Key Touchpoints
1. **Incident Declaration**: Jordan declares P0, notifies team via Slack
2. **War Room**: Lisa creates ad-hoc sync, Taylor shares logs, Alex proposes fix
3. **Hotfix Review**: Quick PR review by senior developer, Jordan validates fix in staging
4. **Deployment**: Taylor deploys hotfix with monitoring, confirms resolution
5. **Customer Communication**: Sarah notifies affected customers of resolution
6. **Post-Mortem**: Lisa facilitates, team identifies action items (add export timeout monitoring, implement background jobs)

### Outcome
- Hotfix deployed in 3 hours, resolving immediate issue
- Background job processing added in next sprint
- Monitoring improved to catch similar issues earlier
- Customer satisfaction maintained through proactive communication

---

## Scenario 3: New Product Initiative - Mobile App Launch

### Context
OctoAcme is launching its first mobile app. This is a multi-quarter initiative requiring coordination across multiple teams.

### Role Interactions

**Product Manager (Sarah)**
- Defines mobile app vision and target user segments
- Creates roadmap with phased rollout: MVP (Q1), Enhanced Features (Q2), Full Parity (Q3)
- Prioritizes features based on customer research and competitive analysis
- Defines success metrics: 50K downloads in first quarter, 4.5+ app store rating

**Business Analyst (Marcus)**
- Conducts gap analysis between web and mobile requirements
- Documents mobile-specific workflows (push notifications, offline mode)
- Creates user stories for MVP features
- Works with Sarah to define minimum viable feature set

**UX/UI Lead (Priya)**
- Conducts mobile user research: 10 user interviews, competitive analysis
- Creates mobile design system following iOS/Android guidelines
- Designs native mobile interfaces optimized for touch
- Conducts usability testing with clickable prototypes
- Creates design specifications for iOS and Android

**Developer (Alex - now mobile dev team)**
- Sets up React Native project structure
- Implements core features following Priya's designs
- Integrates with existing APIs
- Optimizes for mobile performance (offline caching, lazy loading)
- Conducts code reviews with mobile team

**Quality Assurance Lead (Jordan)**
- Develops mobile testing strategy: device matrix, OS versions
- Sets up automated testing framework (Detox for React Native)
- Performs manual testing on physical devices (iOS/Android)
- Conducts accessibility testing for mobile screen readers
- Coordinates beta testing program with 100 early users

**DevOps Specialist (Taylor)**
- Sets up mobile CI/CD pipelines with Fastlane
- Configures app store deployment processes (Apple App Store, Google Play)
- Implements mobile-specific monitoring and crash reporting (Firebase)
- Manages code signing certificates and provisioning profiles
- Sets up staged rollouts for safe production releases

**Project Manager (Lisa)**
- Creates multi-quarter project plan with milestones
- Tracks dependencies: API changes, app store review timelines
- Coordinates weekly syncs across mobile, backend, and design teams
- Manages risks: app store rejection, feature creep, resource constraints
- Reports progress to executive stakeholders monthly

### Key Touchpoints
1. **Project Kickoff**: Lisa facilitates, Sarah presents vision, all roles align on MVP scope
2. **Design Workshop**: Priya presents mobile designs, Marcus validates requirements, developers assess feasibility
3. **Technical Architecture Review**: Alex presents technical approach, Taylor reviews infrastructure needs, Jordan identifies testing requirements
4. **Sprint Planning (Bi-weekly)**: Lisa facilitates, team commits to sprint goals
5. **Beta Launch**: Taylor deploys to TestFlight/Google Play Beta, Jordan coordinates tester feedback
6. **App Store Submission**: Taylor submits, team monitors review process, addresses feedback
7. **Public Launch**: Coordinated announcement, Taylor monitors metrics, Sarah tracks adoption
8. **Retrospectives**: Monthly retrospectives to improve collaboration across teams

### Outcome
- MVP launched on time with 35 key features
- Achieved 60K downloads in first quarter, exceeding goal
- 4.6 app store rating with positive reviews
- Identified areas for improvement in cross-platform testing

---

## Scenario 4: Process Improvement - Reducing Build Times

### Context
The team notices build and test times have increased from 15 minutes to 45 minutes over the past year, slowing down development velocity.

### Role Interactions

**Developer (Alex)**
- Raises concern in retrospective: "Slow builds are impacting productivity"
- Shares data: PR feedback time increased 3x
- Volunteers to help investigate and optimize

**DevOps Specialist (Taylor)**
- Analyzes build metrics and identifies bottlenecks
- Finds issues: large Docker images, sequential test execution, no caching
- Proposes solutions: parallel test runs, layer caching, incremental builds
- Creates proof-of-concept showing 60% reduction in build time

**Quality Assurance Lead (Jordan)**
- Reviews test suite performance
- Identifies slow integration tests that could be parallelized
- Refactors tests to support parallel execution
- Works with Taylor to optimize test data setup

**Project Manager (Lisa)**
- Recognizes this as a process improvement initiative
- Allocates 20% of sprint capacity for build optimization
- Tracks progress and ROI (developer hours saved)
- Communicates improvements to leadership

**Product Manager (Sarah)**
- Supports prioritization of technical debt work
- Approves time investment based on velocity impact
- Celebrates improvement with team

### Key Touchpoints
1. **Retrospective**: Alex raises issue, team discusses impact
2. **Investigation**: Taylor and Jordan analyze bottlenecks
3. **Proposal Review**: Taylor presents optimization plan to team
4. **Implementation**: Alex, Taylor, and Jordan collaborate on changes
5. **Validation**: Team measures actual improvement
6. **Communication**: Lisa shares results with stakeholders

### Outcome
- Build time reduced from 45 minutes to 18 minutes
- Developer productivity increased: faster PR feedback
- Team morale improved through addressing pain point
- Process documented for future optimization efforts

---

## Scenario 5: Accessibility Compliance - WCAG 2.1 AA Certification

### Context
OctoAcme needs to achieve WCAG 2.1 AA compliance to meet enterprise customer requirements and improve accessibility for all users.

### Role Interactions

**Product Manager (Sarah)**
- Identifies accessibility as a customer requirement and market differentiator
- Defines success criteria: Achieve WCAG 2.1 AA certification within 6 months
- Prioritizes accessibility work alongside feature development
- Communicates commitment to accessibility in product roadmap

**UX/UI Lead (Priya)**
- Conducts accessibility audit of existing product
- Identifies issues: color contrast, keyboard navigation, screen reader support
- Updates design system with accessible components
- Creates accessibility guidelines for future designs
- Tests with assistive technologies (JAWS, NVDA, VoiceOver)

**Business Analyst (Marcus)**
- Documents accessibility requirements for new features
- Creates acceptance criteria that include accessibility standards
- Ensures user stories consider users with disabilities
- Validates that solutions meet accessibility needs

**Developer (Alex)**
- Remediates accessibility issues in existing code
- Implements ARIA labels and semantic HTML
- Ensures keyboard navigation works across all features
- Integrates automated accessibility testing (axe-core)
- Attends accessibility training to build expertise

**Quality Assurance Lead (Jordan)**
- Adds accessibility testing to test plans
- Performs manual testing with screen readers
- Sets up automated accessibility scans in CI/CD pipeline
- Creates regression test suite for accessibility features
- Validates fixes with users who use assistive technologies

**DevOps Specialist (Taylor)**
- Integrates accessibility scanning tools into CI/CD pipeline
- Configures automated checks to fail builds on critical violations
- Sets up accessibility monitoring in production
- Creates dashboards to track accessibility metrics over time

**Project Manager (Lisa)**
- Creates project plan for accessibility initiative
- Tracks progress against WCAG 2.1 AA criteria
- Coordinates with legal and compliance teams
- Schedules third-party accessibility audit
- Facilitates certification process

### Key Touchpoints
1. **Accessibility Kickoff**: Lisa facilitates, Priya presents audit findings, team commits to remediation
2. **Design System Update**: Priya updates components, Alex implements, Jordan validates
3. **Training Sessions**: External accessibility expert trains team on best practices
4. **Sprint Planning**: Accessibility work integrated into each sprint
5. **Testing Reviews**: Jordan demonstrates accessibility testing, team learns to use screen readers
6. **Third-Party Audit**: External auditor reviews application, team addresses findings
7. **Certification**: Team celebrates achieving WCAG 2.1 AA compliance

### Outcome
- WCAG 2.1 AA certification achieved in 5 months
- Accessibility became part of standard development process
- Product opened to new market segment requiring accessibility compliance
- Team gained valuable accessibility expertise

---

## Common Collaboration Patterns

### Pattern 1: Requirements to Design to Code
1. **Business Analyst** documents requirements and acceptance criteria
2. **UX/UI Lead** creates designs based on requirements
3. **Developer** implements code based on designs
4. **Quality Assurance Lead** validates against requirements
5. **Product Manager** confirms solution meets customer needs

### Pattern 2: Production Issue Resolution
1. **DevOps Specialist** identifies issue in monitoring
2. **Developer** investigates root cause
3. **Quality Assurance Lead** validates fix
4. **DevOps Specialist** deploys hotfix
5. **Product Manager** communicates to affected customers
6. **Project Manager** facilitates post-mortem

### Pattern 3: Feature Planning
1. **Product Manager** defines problem and success metrics
2. **Business Analyst** gathers detailed requirements
3. **UX/UI Lead** creates user experience design
4. **Developer** estimates effort and identifies technical risks
5. **Quality Assurance Lead** defines testing strategy
6. **DevOps Specialist** identifies infrastructure needs
7. **Project Manager** creates timeline and coordinates delivery

### Pattern 4: Continuous Improvement
1. **Team Members** identify improvement opportunities
2. **Project Manager** facilitates retrospective discussion
3. **Roles** collaborate on solutions (e.g., Developer + DevOps on build times)
4. **Product Manager** supports prioritization of improvements
5. **Team** implements changes and measures impact

---

## Tips for Effective Collaboration

### For All Roles
- **Communicate Early and Often**: Share information proactively, don't wait to be asked
- **Ask Questions**: Clarify assumptions before making decisions
- **Respect Expertise**: Trust team members in their areas of expertise
- **Be Solution-Oriented**: Focus on solving problems together
- **Document Decisions**: Capture important decisions and rationale

### Cross-Role Collaboration
- **Business Analyst + UX/UI Lead**: Align on user needs vs. business requirements early
- **Developer + DevOps Specialist**: Involve DevOps in architecture decisions
- **QA Lead + UX/UI Lead**: Collaborate on usability testing
- **Product Manager + Project Manager**: Balance feature scope with timeline constraints
- **Developer + Business Analyst**: Clarify requirements during implementation, not after

### Meeting Effectiveness
- **Daily Standups**: Quick updates, identify blockers, coordinate for the day
- **Sprint Planning**: Detailed discussion, ensure shared understanding, commit to goals
- **Design Reviews**: Gather diverse perspectives, iterate on feedback
- **Retrospectives**: Safe space for honest feedback, focus on actionable improvements

---

## Additional Resources

- [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) - Detailed role definitions
- [role-onboarding-checklist.md](role-onboarding-checklist.md) - Onboarding guides for each role
- [octoacme-project-management-overview.md](octoacme-project-management-overview.md) - Overall project management framework
- [octoacme-risks-and-communication.md](octoacme-risks-and-communication.md) - Communication best practices

---

**Last Updated**: 2025-11-13

---

## Feedback

These scenarios are based on common OctoAcme situations. If you have suggestions for additional scenarios or improvements:

1. Open an issue using the [Process Doc Update template](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml)
2. Share real examples from your projects that could benefit the team
3. Contribute scenarios that highlight successful collaboration patterns
