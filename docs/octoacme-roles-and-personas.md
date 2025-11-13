# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

### Interactions with Other Roles
- **Product Managers**: Clarify feature requirements and provide technical feasibility input
- **Project Managers**: Share progress updates, raise blockers, and participate in planning
- **Business Analyst**: Ask questions about requirements and acceptance criteria during implementation
- **UX/UI Lead**: Collaborate on design implementation and provide feedback on feasibility
- **DevOps Specialist**: Work together on CI/CD improvements and deployment issues
- **Quality Assurance Lead**: Collaborate on testability, fix bugs, and improve test coverage

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

### Interactions with Other Roles
- **Developers**: Provide feature requirements and context for technical trade-offs
- **Project Managers**: Align on priorities, timelines, and scope decisions
- **Business Analyst**: Collaborate on defining customer needs and validating solutions
- **UX/UI Lead**: Partner on feature definition and ensure designs solve customer problems
- **DevOps Specialist**: Support feature flagging and phased rollout strategies
- **Quality Assurance Lead**: Define acceptance criteria and validate solutions meet quality standards

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

### Interactions with Other Roles
- **Product Managers**: Align on priorities and communicate trade-offs between scope, timeline, and resources
- **Developers**: Facilitate planning, track progress, and remove blockers
- **Business Analyst**: Coordinate requirements gathering and scope definition
- **UX/UI Lead**: Track design timelines and dependencies
- **DevOps Specialist**: Coordinate deployment schedules and manage infrastructure dependencies
- **Quality Assurance Lead**: Monitor testing progress and manage release readiness

---

## Business Analyst

### Role Summary
Business Analysts bridge the gap between business needs and technical solutions. They analyze requirements, model business processes, and ensure that solutions align with organizational goals and user needs.

### Responsibilities
- Elicit and document business requirements from stakeholders
- Create process flows, user stories, and acceptance criteria
- Analyze data to identify trends, gaps, and opportunities
- Facilitate requirements workshops and stakeholder interviews
- Validate that delivered solutions meet business objectives
- Maintain requirements traceability matrices and documentation

### Goals
- Ensure solutions address actual business problems
- Reduce rework through clear, complete requirements
- Improve decision-making through data analysis and insights
- Foster alignment between business and technical teams

### Typical Communication
- Requirements documentation and user stories
- Stakeholder interviews and workshops
- Process diagrams and business models
- Data analysis reports and recommendations

### Interactions with Other Roles
- **Product Managers**: Collaborate on feature prioritization and customer value; translate product vision into detailed requirements
- **Developers**: Clarify requirements, answer questions during implementation, and provide context for technical decisions
- **Project Managers**: Support scope definition, identify dependencies, and assist in planning and tracking
- **UX/UI Lead**: Work together to ensure requirements align with user experience goals
- **Quality Assurance Lead**: Define acceptance criteria and validate test scenarios match business needs

---

## UX/UI Lead

### Role Summary
UX/UI Leads design intuitive, accessible user experiences and interfaces. They advocate for users, create design systems, and ensure consistency across products while balancing user needs with business goals.

### Responsibilities
- Conduct user research and usability testing
- Create wireframes, prototypes, and high-fidelity designs
- Develop and maintain design systems and style guides
- Collaborate with developers to ensure design implementation fidelity
- Advocate for accessibility and inclusive design practices
- Measure and improve user satisfaction and experience metrics

### Goals
- Create delightful, intuitive user experiences
- Reduce user friction and support costs
- Ensure consistency across product touchpoints
- Make products accessible to all users

### Typical Communication
- Design mockups and interactive prototypes
- User research findings and personas
- Design reviews and critique sessions
- Accessibility audits and recommendations

### Interactions with Other Roles
- **Product Managers**: Partner on feature definition and user needs; validate designs solve customer problems
- **Developers**: Provide design specifications, answer implementation questions, and review final UI
- **Business Analyst**: Ensure designs support business processes and requirements
- **Quality Assurance Lead**: Collaborate on usability testing and visual regression testing
- **Project Managers**: Communicate design timelines and dependencies

---

## DevOps Specialist

### Role Summary
DevOps Specialists enable fast, reliable software delivery through automation, infrastructure management, and platform engineering. They build CI/CD pipelines, maintain production systems, and foster a culture of continuous improvement.

### Responsibilities
- Design and maintain CI/CD pipelines and deployment automation
- Manage cloud infrastructure and container orchestration
- Implement monitoring, logging, and observability solutions
- Ensure security, compliance, and disaster recovery capabilities
- Optimize build and deployment performance
- Support incident response and post-mortem analysis

### Goals
- Minimize deployment time and risk
- Maximize system reliability and uptime
- Enable developer productivity through automation
- Maintain secure, compliant infrastructure

### Typical Communication
- Infrastructure-as-code and pipeline configurations
- Incident reports and post-mortems
- Runbooks and operational documentation
- Metrics dashboards and performance reports

### Interactions with Other Roles
- **Developers**: Provide CI/CD support, troubleshoot build/deployment issues, and optimize developer workflows
- **Quality Assurance Lead**: Integrate automated testing into pipelines and support test environment management
- **Project Managers**: Communicate deployment schedules, risks, and infrastructure dependencies
- **Product Managers**: Support feature flagging strategies and phased rollouts
- **Security Teams**: Collaborate on security scanning, vulnerability management, and compliance

---

## Quality Assurance Lead

### Role Summary
Quality Assurance Leads ensure product quality through comprehensive testing strategies, automation, and process improvements. They advocate for quality throughout the development lifecycle and help teams deliver reliable software.

### Responsibilities
- Develop test strategies and plans for features and releases
- Create and maintain automated test suites (unit, integration, e2e)
- Perform manual testing for exploratory and edge cases
- Track and triage bugs, manage defect lifecycle
- Define quality metrics and monitor test coverage
- Facilitate quality reviews and test planning sessions

### Goals
- Prevent defects from reaching production
- Increase test coverage and automation rates
- Reduce time-to-market while maintaining quality
- Build quality awareness across the team

### Typical Communication
- Test plans and coverage reports
- Bug reports and regression analysis
- Quality metrics dashboards
- Test automation frameworks and documentation

### Interactions with Other Roles
- **Developers**: Collaborate on testability, review code for test coverage, and pair on complex test scenarios
- **Product Managers**: Validate acceptance criteria, provide quality feedback on features, and assess release readiness
- **Business Analyst**: Ensure test cases align with business requirements and user scenarios
- **UX/UI Lead**: Conduct usability testing and validate UI consistency
- **DevOps Specialist**: Integrate automated tests into CI/CD pipelines and maintain test environments
- **Project Managers**: Report on testing progress, risks, and release readiness

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- For role-specific onboarding and collaboration examples, see [role-onboarding-checklist.md](role-onboarding-checklist.md) and [sample-collab-scenarios.md](sample-collab-scenarios.md).

