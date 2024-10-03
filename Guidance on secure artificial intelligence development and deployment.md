

Document version 1.0
Published October 2024<p></p>

**Authors**
Darren Christopher Furacão Pereira
Anand Gunti

<div style="page-break-after: always;"></div>


### <font color="#7030a0">Table of contents:</font>
<p></p>

##### [[Guidance on secure artificial intelligence development and deployment#<font color=" 7030a0">1. Introduction</font>|1. Introduction]]  

###### [[Guidance on secure artificial intelligence development and deployment#1.1 What is the scope of this document?|1.1 What is the scope of this document?]]

##### [[Guidance on secure artificial intelligence development and deployment#<font color=" 7030a0">2. Core principles</font>|2. Core principles]] <p></p>

###### [[Guidance on secure artificial intelligence development and deployment#**2.1 Responsible AI principles**|2.1 Responsible AI principles]] <p></p>

 ##### [[Guidance on secure artificial intelligence development and deployment#<font color=" 7030a0">3. Guidelines</font>|3. Guidelines]]

###### [[Guidance on secure artificial intelligence development and deployment#3.1 Secure design |3.1 Secure design]] <p></p>

###### [[Guidance on secure artificial intelligence development and deployment#3.2 Secure development|3.2 Secure development]] <p></p>

###### [[Guidance on secure artificial intelligence development and deployment#3.3 Secure deployment|3.3 Secure deployment]] <p></p>

###### [[Guidance on secure artificial intelligence development and deployment#3.4 Secure operation and maintenance|3.4 Secure operations and maintenance]] <p></p>

##### [[Guidance on secure artificial intelligence development and deployment#<font color=" 7030a0">4. References</font>|4. References]] <p></p> 


<div style="page-break-after: always;"></div>

### <font color="#7030a0">1. Introduction</font>


This document has been developed to provide a general frame work for the development and deployment of artificial intelligence or automation 
at **Mednet Health**. 

The content in this document does not endorse or recommend any third party organisation, product or service. Any links or references to websites and third party materials are provided for information only.

The guidelines follow a ‘secure by default’ approach to processes and is aligned closely with practices defined in the NCSC’s **[Secure Development and Deployment Guidance](https://www.ncsc.gov.uk/collection/developers-collection/principles/secure-development-is-everyones-concern)**<sup>1</sup>, NIST’s **[Secure Software Development Framework](https://csrc.nist.gov/Projects/ssdf)**<sup>2</sup>, and **[Secure by Design Principles](https://www.cisa.gov/sites/default/files/2023-10/SecureByDesign_1025_508c.pdf)**<sup>3</sup> published by CISA, the NCSC and international cyber agencies. 

<p></p>

#### 1.1 What is the scope of this document?

In this document we use ‘AI’ to refer specifically to systems that involve machine learning (ML) or related applications. ML applications are defined but not restricted to any program, protocol, algorithm or similar project that does the following:

 - Involve software components (models) that allow computers to recognise and bring context to patterns in data without the rules having to be explicitly programmed by a human

- Generates predictions, recommendations, or decisions based on statistical or programmed reasoning

> [!info] > Machine learning models tend to use or work with sensitive information for training or functional purposes. This creates a vulnerability for misuse of sensitive or protected data that can far exceed standard GDPR concerns. 

As well as existing cyber security threats, AI systems are subject to new types of vulnerabilities. The term ‘adversarial machine learning’ (AML), is used to describe the exploitation of fundamental vulnerabilities in ML components, including hardware, software, workflows and supply chains.

These models may be further used to perform malicious tasks using this data like:<sup>4</sup>

- Affecting the model’s classification or regression performance

- Allowing users to perform unauthorised actions

-  Extracting sensitive model information

>**The scope of this document in a nutshell is to address concepts and considerations to ensure that ML models remain secure.**

<div style="page-break-after: always;"></div>

### <font color="#7030a0">2. Core principles</font>

At Mednet Health, we endeavour to follow core principles while building processes that aim to support and enhance tasks, rather than replace people.

- The application of artificial intelligence (AI) processes and automation within Mednet Health (or when provided to other organisations via Mednet Health), is dependent on creating a secure user experience. All parts of the process must be evaluated and designed to facilitate this principle both in practice and spirit.<p></p>

-  Service end users may not possess the expertise or the visibility to fully engage with risks associated with the systems they may be using. This means that it is the responsibility of the developer/deployer to ensure that the there is end-to-end security and that the service user cannot be held responsible for any breaches of data or compliance.<p></p>

- The purpose of these tools or processes is generally to create a useful solution to a problem or to create a better way of working. However the use of these tools at the time of publication of this document has a significant impact on energy consumption, natural resources and climate. Where possible, the cost of tool development, deployment and maintenance should be measured against the cost/benefit ratio of having the task performed manually on all fronts.<p></p>

- Bias and discrimination can be both implicit and explicit, all systems built should aim to ensure that there is no propagation of discrimination based on race,gender, socioeconomic aspects or similar social constructs. Testing phases should be varied and aim to offset any unconscious developer bias that may be present.<p></p>

- AI systems should be transparent and explainable, meaning that users and stakeholders should understand how AI decisions are made. This principle is essential to building trust and accountability in AI systems, especially in sensitive areas like healthcare, finance, or legal decisions.<p></p>

- Privacy and data protection of all user data should be a priority that must be considered during any planning phase. Safeguarding information using encryption, permissions or other limitations must be undertaken alongside any other necessities to comply with legal frameworks like [General Data Protection Regulation (Regulation (EU) 2016/679)](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02016R0679-20160504).<sup>5</sup> <p></p>

##### **2.1 Responsible AI principles**
<p></p>

We recognise Responsible Artificial Intelligence (RAI) as an approach to developing, assessing, and deploying AI systems in a safe, trustworthy, and ethical way. To this end we aim to uphold the following principles: 

- Accurate and reliable: Develop AI systems to achieve the highest levels of accuracy and reliability.

- Accountable and transparent: Establish clear oversight over the full AI lifecycle, and provide transparency and evidence of decision making processes

- Fair and human-centric: Design AI systems with human oversight and diverse perspectives to avoid unfair discrimination and harmful bias.

- Safe and ethical: Prioritise the safety of human life, health, property, and the environment when designing, developing, and deploying AI systems.

- Secure and resilient: Proactively mitigate potential cyber threats and vulnerabilities to ensure the robustness and resilience of AI systems.

- Interpretable and documented: Design AI systems to be interpretable, allowing humans to understand their operations and the meaning and limitation of their outputs. Document design decisions, development protocols, and alignment with RAI principles.

- Privacy-enhanced and data governed: Develop AI systems with careful attention to privacy, security, confidentiality, and intellectual property ownership considerations around the data used.

- Vendor and partner selection: Exercise diligence and ongoing oversight when selecting third-party vendors involved in AI system development (eg, data brokers, cloud service providers).

- Ongoing monitoring: Establish standards for continuous monitoring and evaluation of AI systems to uphold ethical, legal, and social standards and performance benchmarks.

- Continuous learning & development: Commit to continuous learning and development of AI systems, adapting through adaptive training, feedback loops, user education, and regular compliance auditing to remain aligned with ethical, legal, and societal standards.

**In addition to the above principles, we will not design or deploy AI in the following application areas: ** 
  
- Technologies or systems that cause or are likely to cause overall harm.  <p></p>
  
- Technologies or systems that gather or use information for surveillance in violation of the law. <p></p>
  
- Technologies or systems that violate principles of international human rights.  <p></p>
  
>[!info] > We reserve the right to expand on the definition of this list or add to it in the future.

>[!example|purple.red] **Within the framework of Mednet Health specifically, when using Microsoft integrations or affiliated product we shall align with the [Microsoft responsible AI standard](https://cdn-dynmedia-1.microsoft.com/is/content/microsoftcorp/microsoft/final/en-us/microsoft-brand/documents/Microsoft-Responsible-AI-Standard-General-Requirements.pdf?culture=en-us&country=us)**.

<div style="page-break-after: always;"></div>

### <font color="#7030a0">3. Guidelines</font>

The guidelines approach four key areas within the AI system development life cycle in line with NCSC recommendation and borrows heavily from their publications.<sup>1</sup> 

| <font color="#002060">**Considerations:**</font> |
| :--- |
|Secure Design|
| Secure Development |
| Secure Deployment |
| Secure Operation and Maintenance  |

For each area, there are specific considerations and mitigations that will help reduce the overall risk to the organisational AI system development process. These areas prioritise:

- Taking ownership of security outcomes for end users

- Embracing transparency and accountability

- Building secure organisational structures and leadership 

> [!info] > Note that while these are not exhaustive, they should be considered as the tenets for wider decision making. 

##### 3.1 Secure design

This section contains guidelines that apply to the design stage of the AI system development life cycle. It covers understanding risks and threat modelling, as well as specific topics and trade-offs to consider when it comes to system and model design.

<font color="#000000">**Raise staff awareness of threats and risks**</font>

- Ensure senior leaders are aware of and understand the threats and mitigations involved in projects.
- Developers and data scientists should maintain an up-to-date understanding of security threats and failure modes to help risk owners to make informed decisions. 
- Always provide users with guidance on the unique security risks facing AI systems and provide functionality guides to minimise unforeseen outcomes.

<font color="#000000">**Model the threats to systems**</font>

- As part of the risk management process, a holistic assessment of the system should be undertaken. This includes understanding the potential impact to the system, users, organisations and wider society if an AI component is compromised or behaves unexpectedly. 

- This process should involve assessing the impact of AI-specific threats<sup>6</sup> and documenting the decision making against this. 

<font color="#000000">**Incorporate security as well as functionality and performance**</font>

- Due diligence on supply chain security when choosing whether to develop in house or use external processes.
- Integrate AI software system development into existing secure development and operations.
- Ensure appropriate restrictions and failsafes (including manual failsafes) for processes that affect or change files or data
- User interaction should be a key consideration when developing secure methods of process use.

<font color="#000000">**Consider security benefits and trade-offs**</font>

- Consider the need for complexity and the amount of training data required.
- Consider the appropriateness of the model for the use case and/or feasibility of adapting it to specific needs (for example by fine-tuning).
- Consider the impact of functions like debugging, audit or regulatory compliance.
- Consider the characteristics of training dataset(s), including size, integrity, quality, sensitivity, age, relevance and diversity.
- Consider the value of using model hardening (such as adversarial training), regularisation and/or privacy-enhancing techniques.

>[!info] > For more information about how many of these factors impact security outcomes, refer to the NCSC’s [Principles for the Security of Machine Learning](https://www.ncsc.gov.uk/files/Principles-for-the-security-of-machine-learning.pdf)

##### 3.2 Secure development

This section contains guidelines that apply to the development stage of the AI system development lifecycle, including supply chain security, documentation, and asset and technical debt management.

<font color="#000000">**Secure the supply chain**</font>

-  Assess and monitor the security of the AI supply chains across a system’s life cycle, and require suppliers to adhere to the same standards the organisation applies to other software. 

- Where not produced in-house, acquire and maintain well-secured and well-documented hardware and software components (for example, models, data, software libraries, modules, middleware, frameworks, and external APIs) from verified commercial, open source, and other third-party developers to ensure robust security in systems.

- Consistency planning using alternate solutions for mission-critical systems, if security criteria are not met.

<font color="#000000">**Identify, track and protect assets**</font>

- All logs, repositories and archives are sensitive data and controls must be implemented to protect their confidentiality, integrity and availability.
- Know where all assets are stored after assessing and accepting any associated risks. 
-  Maintain processes and tools to track, authenticate, version control and secure assets, 
- Ensure that the assets can be restored to a known good state in the event of compromise.

<font color="#000000">**Document data, models and prompts**</font>

- Document the creation, operation, and life cycle management of any models, datasets and meta-or system-prompts. 
- Document security-relevant information such as the sources of training data (including fine-tuning data and human or other operational feedback), intended
scope and limitations, guardrails, cryptographic hashes or signatures, retention time, suggested review frequency and potential failure modes. 

>[!info] > The production of comprehensive documentation supports transparency and accountability.

<font color="#000000">**Manage technical debt**</font> ^c6421a

- Identify, track and manage areas where time or resources has forced deviation from best practice or ideal solutions.
- Maintain documentation of actions leading to short term goal completion at the expense of long term goals. These should be followed up on to update when possible.

##### 3.3 Secure deployment

This section contains guidelines that apply to the deployment stage of the AI system development lifecycle, including protecting infrastructure and models from compromise, threat or loss, developing incidents,management processes, and responsible release.

>[!example|purple.red] **Within the framework of Mednet Health specifically, this should be done in partnership with our compliance partners <font color="#7030a0">(INFOSecurity People)</font>**.

<font color="#000000">**Secure the infrastructure**</font>

- Apply good infrastructure security principles to the infrastructure used in every part of the system’slife cycle. 
- Apply appropriate access controls to APIs, models and data, and to their training and processing pipelines, in research and development as well as deployment. 
- This includes appropriate **segregation of environments** holding sensitive code or data. 

<font color="#000000">**Protect the model continuously**</font>

- Implementing standard cyber security best practices.
- Implementing controls on the query interface to detect and prevent attempts to access, modify, and exfiltrate confidential information.
- If appropriate, privacy-enhancing technologies (such as differential privacy or homomorphic encryption) can be used to explore or assure levels of risk associated with consumers, users and attackers having access to models and outputs.

<font color="#000000">**Develop incident management procedures**</font>

- Have processes in place for incident response, escalation and remediation plans. 
- Store critical company digital resources in offline backups and archive regularly.
- Keep high-quality audit logs and other security features or information 

<font color="#000000">**Ease of use for end user**</font>

- Ideally, the most secure setting should be integrated into a system as the only option. 
- When configuration is necessary, the default option should be broadly secure against common threats (that is, secure by default). 
- Controls should be deployed to prevent the use or deployment of systems in malicious ways.
- Guides or handbooks should be provided with details around functionality to ensure that users are less likely to deviate from appropriate process.

##### 3.4 Secure operation and maintenance

This section contains guidelines that apply to the secure operation and maintenance stage of the AI system development life cycle. It provides guidelines on actions particularly relevant once a system has been deployed, including logging and monitoring, update management and information sharing.

<font color="#000000">** Monitor system behaviour**</font>

- Measure the outputs and performance of models or systems to keep an eye out for  changes in behaviour affecting security. Account for and identify potential intrusions and compromises, as well as natural data drift.

<font color="#000000">** Monitor system inputs**</font>

- In line with privacy and data protection requirements, monitor and log inputs to the system (such as inference requests, queries or prompts) to enable compliance obligations, audit, investigation and remediation in the case of compromise or misuse. 

<font color="#000000">**Follow a secure by design approach to updates**</font>

- Include automated updates by default in every product and use secure, modular update procedures.
- Attempt to address  **[[Guidance on secure artificial intelligence development and deployment#^c6421a|technical debt]]** when possible as part of larger updates.
- Keep systems current to avoid vulnerability.
 
<font color="#000000">**Keep track of best practice**</font>

- Participate in information-sharing communities, collaborating across the global ecosystem of industry, academia and governments to share best practice as appropriate. 
- Maintain open lines of communication for feedback regarding system security, both internally and externally to the organisation, including providing consent to security researchers to research and report vulnerabilities.
- When needed, escalate issues to the wider community, for example publishing bulletins responding to vulnerability disclosures, including detailed and complete common vulnerability enumeration (without compromising data). 


<div style="page-break-after: always;"></div>

### <font color="#7030a0">4. References</font>

1. **Secure Development and Deployment Guidance** published by the National Cyber Security Centre (NCSC), accessed at: https://www.ncsc.gov.uk/collection/developers-collection/principles/secure-development-is-everyones-concern <p></p>
2. **Secure Software Development Framework** published by National Institute of Standards and Technology, accessed at: https://csrc.nist.gov/Projects/ssdf <p></p>

3. **Secure by Design Principles** published by CISA, the NCSC and international cyber agencies, accessed at: https://www.cisa.gov/sites/default/files/2023-10/SecureByDesign_1025_508c.pdf <p></p>

4. **AI Security Concerns in a Nutshell**, published by the German Federal Office for Information Security (BSI), accessed at: https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/KI/Practical_Al-Security_Guide_2023.pdf?__blob=publicationFile&v=5 <p></p>

5.  **General Data Protection Regulation (Regulation (EU) 2016/679)**, published by the European Parliament and Council of the European Union, accessed at: https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02016R0679-20160504 <p></p>

6. **AI Security 101**, published by MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems), accessed at: https://atlas.mitre.org/resources/ai-security-101 <p></p>



