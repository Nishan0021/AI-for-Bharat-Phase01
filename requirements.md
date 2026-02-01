# Requirements Document

## Introduction

The AI-Powered Government Scheme Eligibility & Explainer System is a citizen-centric decision support platform designed to help users discover government schemes they qualify for and understand how to apply for them. The system focuses on eligibility logic, plain-language explanations, and actionable guidance, addressing key barriers such as low digital literacy, complex government language, and fragmented information. Artificial Intelligence is used only for simplification, translation, and explanation, while all eligibility decisions are based on transparent, rule-based logic.

## Glossary

- **System**: AI-Powered Government Scheme Eligibility & Explainer System
- **User**: A citizen seeking government scheme information
- **Scheme**: A government welfare program or benefit
- **Eligibility_Engine**: Rule-based component that evaluates scheme eligibility
- **Explanation_Engine**: AI component that simplifies scheme information into plain language
- **Guidance_Engine**: Component that provides step-by-step application guidance
- **User_Input**: Information provided by the user through forms or voice input
- **Confidence_Score**: Percentage indicating how strongly a user matches a scheme
- **Scheme_Database**: Curated dataset of government schemes with verified rules
- **Low_Bandwidth_Mode**: UI mode optimized for slow or limited internet connections

## Requirements

### Requirement 1: User Input Collection

**User Story:** As a citizen, I want to answer a few simple questions, so that the system can identify government schemes relevant to me.

#### Acceptance Criteria

1. WHEN a user starts the assessment, THE System SHALL collect 5–8 basic inputs (age, state, income range, education, occupation, gender, category)
2. THE System SHALL avoid requesting complex or sensitive data not required for eligibility
3. WHEN inputs are incomplete, THE System SHALL prompt the user clearly for missing information
4. THE System SHALL support form-based input optimized for mobile devices
5. WHERE enabled, THE System SHALL allow voice input for basic responses

### Requirement 2: Eligibility-Based Scheme Matching

**User Story:** As a citizen, I want the system to clearly tell me which schemes I qualify for, so that I don't miss benefits I am eligible for.

#### Acceptance Criteria

1. WHEN user input is submitted, THE Eligibility_Engine SHALL evaluate eligibility using predefined rule sets
2. THE Eligibility_Engine SHALL NOT use AI to make eligibility decisions
3. THE System SHALL support state-specific and category-based eligibility rules
4. WHEN eligibility conditions conflict, THE System SHALL apply exclusion criteria transparently
5. THE System SHALL return only schemes that meet mandatory eligibility requirements

### Requirement 3: Confidence Scoring and Transparency

**User Story:** As a citizen, I want to know why a scheme was suggested to me, so that I can trust the system's recommendations.

#### Acceptance Criteria

1. THE System SHALL assign a Confidence_Score to each matched scheme
2. THE System SHALL display reasons for eligibility in simple bullet points
3. WHEN a scheme is partially matched, THE System SHALL indicate missing or weak criteria
4. THE System SHALL avoid misleading certainty or promises of approval
5. THE System SHALL clearly distinguish eligibility from final government approval

### Requirement 4: Plain-Language Scheme Explanation

**User Story:** As a citizen with limited technical or legal knowledge, I want schemes explained in simple language, so that I can understand them easily.

#### Acceptance Criteria

1. WHEN displaying scheme details, THE Explanation_Engine SHALL simplify content to Class-6 language level
2. THE System SHALL avoid copying government PDF language verbatim
3. EACH scheme explanation SHALL include: What the scheme is, Who gets it, Benefits, Who should not apply
4. THE System SHALL use short sentences and active voice
5. AI usage SHALL be limited to simplification and explanation only

### Requirement 5: Step-by-Step Application Guidance

**User Story:** As a citizen, I want clear steps to apply for a scheme, so that I can complete the process without confusion.

#### Acceptance Criteria

1. WHEN a scheme is selected, THE Guidance_Engine SHALL show a structured application flow
2. THE Application_Guide SHALL divide the process into stages (Preparation, Application, Verification, Disbursement)
3. THE System SHALL list required documents in checklist format
4. THE System SHALL highlight common mistakes to avoid
5. THE System SHALL provide realistic timelines for each stage

### Requirement 6: Local Language Support

**User Story:** As a citizen more comfortable in my local language, I want content in my language, so that I can fully understand the information.

#### Acceptance Criteria

1. THE System SHALL support English and Hindi at minimum
2. WHEN language is switched, THE System SHALL update all UI labels and content
3. Scheme explanations and eligibility criteria SHALL be available in selected languages
4. THE System SHALL prioritize clarity over literal translation
5. WHERE feasible, THE System SHALL support one additional regional language

### Requirement 7: Low-Bandwidth and Accessibility Design

**User Story:** As a citizen with limited internet access, I want the system to work smoothly on slow networks.

#### Acceptance Criteria

1. THE System SHALL provide a Low_Bandwidth_Mode
2. THE UI SHALL avoid heavy images, videos, or animations
3. Pages SHALL load within 2 seconds on 3G networks
4. THE System SHALL function on basic smartphones and older browsers
5. THE System SHALL follow accessibility best practices for readability

### Requirement 8: Scheme Data Management

**User Story:** As a system administrator, I want scheme data to be accurate and controlled, so that users receive correct information.

#### Acceptance Criteria

1. THE Scheme_Database SHALL contain only curated and verified schemes
2. EACH scheme SHALL have clearly defined eligibility rules
3. THE System SHALL NOT scrape live government websites during runtime
4. Scheme data SHALL be stored in structured JSON format
5. Updates to scheme data SHALL be logged and versioned

### Requirement 9: Responsible AI Usage

**User Story:** As a citizen, I want AI to help me understand schemes without making unreliable decisions.

#### Acceptance Criteria

1. AI SHALL NOT determine eligibility or approval outcomes
2. AI SHALL be used only for: Simplification, Translation, Explanation
3. THE System SHALL avoid hallucinated or speculative information
4. AI outputs SHALL be grounded in curated scheme data
5. THE System SHALL disclose how AI is used

### Requirement 10: Demonstration and Reliability

**User Story:** As a judge or evaluator, I want a stable and realistic system, so that I can assess its real-world usefulness.

#### Acceptance Criteria

1. THE System SHALL function without crashes during demo flow
2. THE System SHALL use pre-loaded scheme data
3. Language switching SHALL work instantly
4. Eligibility results SHALL be consistent and explainable
5. THE System SHALL clearly state its scope and limitations