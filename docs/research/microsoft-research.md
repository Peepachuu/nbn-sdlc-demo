
# Source Note — [Microsoft]

**Author:** Chirag Wadehra

**Date:** 22 August, 2026

**Time spent:** 

## 1. Sources

| # | Source | Type | Date accessed |
|---|---|---|---|
| S1 | https://www.microsoft.com/en-us/power-platform/topics/phases-of-the-software-development-lifecycle | Documentation | 22 August, 2026|
| S2 | https://learn.microsoft.com/en-us/compliance/assurance/assurance-security-development-and-operation | Documentation | 22 August, 2026|
| S3 | https://learn.microsoft.com/en-us/compliance/assurance/assurance-microsoft-security-development-lifecycle | Documentation | 22 August, 2026|
| S4 | | | |
| S5 | | | |

## 2. The lifecycle stages, in their words
S1 is the official documentation from Microsoft describing the Software Development Life Cycle (SDLC). Microsoft defines the SDLC as a structured methodology for developing software that meets quality standards and security requirements. 


Microsoft divides the SDLC into seven stages:

### Planning
Microsoft describes planning as the phase that lays the foundation for the entire project. During this stage, the development team defines the goals for the project and identifies what is required to achieve them.

The team must consider stakeholder needs and expectations, as well as the overall feasibility of the project. This includes determining how the application will be built, when it should be deployed, and whether the required resources, such as time and budget, are available.

Microsoft considers this stage crucial because effective planning helps ensure that everyone involved understands what the software is expected to provide and reduces the risk of technical problems, unexpected costs, or delays later in the development stage.

### Analysis
Microsoft describes Analysis as the stage where the project plan and software requirements, derived during planning, are examined in more detail to determine how the solution should function.

The findings from this analysis are then used to create detailed system specifications, which help guide the later stages of the SDLC.

Microsoft also suggests using tools such as use-case diagrams and data-flow diagrams to visually represent the software's functionality and structure. These diagrams can help the development team better understand how the proposed solution should operate and verify that it aligns with stakeholder requirements before development begins. This reduces the likelihood of misunderstandings and costly rework during later stages of the SDLC.

### Design
Microsoft describes Design as the phase where the requirements identified during the earlier stages are used to define the overall architecture of the software and determine how its key components will interact.

The team creates detailed system designs and models to help check whether the proposed solution is likely to satisfy user and stakeholder expectations, while also uncovering possible problems before implementation begins.

Microsoft also suggests using established design patterns to speed up this phase by providing proven solutions to common design problems. In addition, prototyping tools can be used to visualise the user interface and system functionality before development begins.

### Development
Microsoft describes Development as the stage where the requirements and designs produced during the earlier phases are translated into actual code. By the end of this stage, the implementation should be complete and functional, ensuring that it is ready for testing and deployment.

Microsoft explains that development is usually iterative, meaning developers may repeatedly revisit and refine their code to fix technical issues or respond to changes in requirements.

Microsoft also recommends close collaboration within the development team, supported by coding standards and guidelines that help keep the code consistent, readable, and maintainable. In addition, version control systems can be used to track and manage changes made throughout development.

### Testing
Microsoft describes Testing as the phase where the software produced during development is evaluated before it can move toward deployment. This helps the team determine whether the solution satisfies user needs, stakeholder expectations and security requirements.

Microsoft notes that the exact testing approach depends on the project, but common forms of testing include:
- Unit Testing
- Integration Testing
- System Testing
- User Testing

Microsoft also recommends preparing a testing plan that defines what will be tested, when testing will occur and what each test is intended to verify. This ensures that the testing process remain organised and focused.


### Deployment
This stage takes place after testing has confirmed that the software meets the necessary requirements and standards.

Microsoft suggests starting by compiling the final build of the software and preparing the production environment. The resources and tasks required for deployment should then be coordinated to support a smooth release.

Microsoft also recommends having rollback strategies in place so that, if problems occur during deployment, the system can be restored to a previous stable state.


### Maintenance
Microsoft describes Maintenance as a continuous phase that begins after the software has been deployed. The purpose of this stage is to keep the software working correctly, secure and aligned with changing user needs over time.

Microsoft identifies several key activities during this phase:
- Monitoring system performance
- Gathering user feedback to identify possible improvements
- Fixing bugs
- Providing updates, including new features and security improvements
- Offering support to help users understand and use the software


## 3. Human approval gates
Microsoft documentation identifies multiple points where human approval is required before software changes are allowed to progress.

### Code review before integration
Microsoft's Security Development Lifecycle (SDL) requires code to undergo manual review by someone other than the engineer who wrote the code before it can be checked into a release branch. The reviewer checks whether the change meets the relevant SDL and design requirements and whether the required functional and security tests have been passed.

If problems are identified, the reviewer can request changes or block the code from progressing. Once the code is considered satisfactory, approval from the reviewer is required before it can move to the next deployment phase.

### Final security and privacy review
Microsoft also states that new features and material changes undergo a final security and privacy review before release to confirm that the required security and privacy requirements have been satisfied.

## 4. Mechanics inside each stage

### Planning and Analysis
During Planning and Analysis, the project goals, stakeholder expectations, feasibility, resources and software requirements are established. These requirements are then translated into more detailed system specifications that guide the later stages of the development.

During this phase, Microsoft also adds security and privacy requirements. These are determined based on various factors such as the type of data being handled, known threats, regulations, industry requirements and lessons learned from previous incidents.

### Design
During Design, the architecture and interaction between the different components of the system are defined.

Microsoft's SDL create threat modelling during this stage. Through this modelling, the development teams can identify important components of the system and examine how they interact during critical scenarios such as Authentication, in order to identify possible security threats. Microsoft also recommends to create Data-flow diagrams to represent how the information moves through the system, allowing for easier identification of threats.

Any threats that are identified during this stage are evaluated and appropriate mitigations are added to the system's security requirements. Microsoft also requires threat models to be reviewed before a product is released.

### Development
During Development, developers implement the requirements and designs produced during the earlier stages.

Microsoft provides developers with approved development tools, such as compilers, development environments and built-in security checks. These tools are intended to help developers implement the functional and security requirements of the software.

Microsoft also performs automated checks while code is being committed and builds are being created. These checks can identify issues such as exposed credentials, vulnerabilities in source code and problems in third-party or open-source components.

### Testing
Testing is used to determine whether the implementation adheres to the required functional, user and security expectations.

Microsoft's SDL adds several verification mechanisms to this stage. The code is independently reviewed by someone who did not write the code. 

Automated security tools are also used to perform checks such as:
- Static code analysis
- Binary analysis
- Credential and secret scanning
- Encryption checks
- Fuzz testing
- Configuration validation
- Open-source component and vulnerability checking

If the reviewer or the automated tools identify a problem, the developer responsible for writing the code must address the issue before resubmitting the code for review again.

Microsoft also uses penetration testing as an additional method of identifying security weaknesses that may not have been detected through the other verification methods.

### Deployment
Once the required testing and reviews have been completed, the software can progress towards release.

For the deployment, Microsoft uses a Safe Deployment Process (SDP), where the software is not immediately available to every customer. Instead, the build is gradually released to larger and larger groups. The release begins with the development team, followed by Microsoft employees, selected external users and eventually the wider customer base.

This staged approach allows Microsoft to observe the behaviour and stability of the software on a smaller scale before expanding the release to more users.

### Maintenance
After deployment, Microsoft continues monitoring its services to identify security incidents and other issues that may occur after the release.

This complements the general SDLC maintenance activities, such as performance monitoring, bug fixing, updates and user support.

## 5. Where AI appears and where it does not

Microsoft's SDLC documentation does not explicitly identify specific lifecycle stages where AI must or must not be used. Instead, Microsoft describes AI as a way to improve efficiency across the software development lifecycle.

Microsoft explains that AI tools and agents can analyse information from sources such as user feedback, performance metrics and testing results, allowing the teams to identify potential issues earlier and support decision-making throughout the lifecycle.

Moreover, Microsoft states that AI can automate repetitive and time-consuming development activities, allowing the development teams to spend more time on complex and creative aspects of software development.

Microsoft provides examples of AI generating development plans, code and pull requests. These examples suggest that AI may contribute to activities within stages such as planning and development, but the documentation does not assign AI to a fixed set of SDLC stages.

Additionally, Microsoft's Security Development Lifecycle (SDL) documentation does not describe AI as replacing the required human approval processes. Although Microsoft uses various automated security tools during verification, these tools are not explicitly described as AI in the documentation and operate alongside independent manual code review.

Microsoft still requires the code to be reviewed by someone other than the engineer who developed it. Furthermore, problems identified through manual review or automated checks must be resolved before the code can progress. Microsoft also documents a final security and privacy review before new features and material changes can be released.

Therefore, Microsoft's documentation suggests that AI can assist with creating, analysing and planning software development work, while automated tools can assist with verification. However, required human review and approval still remains an explicit control before software changes are allowed to progress towards release.

## 6. What the papers say

## 7. Borrow
At least two ideas we should take into our model, each with a reason.

1.
2.

## 8. Reject

## 9. Open questions


