# SMAX Aviator Prospect Presentation - Design Document

**Date:** 2025-11-10
**Format:** HTML Presentation (reveal.js)
**Target Audience:** IT Managers
**Length:** 25 slides maximum
**Duration:** 20-30 minutes with demo capability

## Presentation Objectives

Create a prospect-oriented presentation that:
- Demonstrates SMAX Aviator's value across multiple personas (end-users, agents, administrators)
- Showcases real-world scenarios with practical use cases
- Highlights security and architecture (private LLM, data isolation)
- Features the custom IVR workflow as a hero scenario
- Includes latest 25.4 updates

## Audience Profile

**Primary:** IT Managers
**Focus:** Balance of business benefits and implementation considerations
**Priorities:**
- ROI and productivity gains
- Security and compliance
- Practical use cases and scenarios
- Integration with existing SMAX environment

## Structure Approach

**Selected:** Role-Based Journey
- Natural workflow progression from end-user → agent → backend
- Easy for prospects to relate to their organization
- Builds narrative continuity
- Architecture/trust established early, reinforced throughout

## Detailed Slide Breakdown

### Opening Section (Slides 1-4)

**Slide 1: Title Slide**
- Title: "SMAX Aviator: AI-Powered Service Management"
- Subtitle: Intelligent Virtual Assistant for Enterprise IT
- Branding elements

**Slide 2: The Challenge**
- Common IT service desk pain points:
  - Long resolution times
  - Knowledge buried in silos
  - Agent burnout from repetitive questions
  - Inconsistent service quality
  - Difficulty scaling support

**Slide 3: Meet SMAX Aviator**
- One-slide overview
- Key differentiators:
  - Private LLM (Llama 3 or Google Gemini)
  - Enterprise-ready security
  - Multi-persona support (Portal, Agent, Mobile, Teams, UCMDB)
  - Real-time enterprise data integration
- Value proposition statement

**Slide 4: Architecture & Privacy Overview**
- Architecture diagram showing:
  - AWS infrastructure (OpenText Public Cloud)
  - Vector database (Milvus) with tenant isolation
  - API gateway
  - Connection to ESM SaaS tenants
- Key security features:
  - Data processing and isolation
  - Tenant-specific context
  - Private LLM options

### End-User Journey (Slides 5-9)

**Slide 5: Service Portal Experience Overview**
- What end-users can do:
  - Natural language Q&A
  - Knowledge base search
  - Request/incident handling
  - Multi-conversation management
- Screenshot: Aviator chat interface in Service Portal

**Slide 6: Demo Scenario 1 - Knowledge Q&A**
- Scenario: "How do I connect to a printer?"
- Shows:
  - Natural language query
  - Aviator response with context
  - Reference links (knowledge articles, news)
  - Like/Dislike feedback
- [Screenshot placeholder: Service Portal chat with references expanded]

**Slide 7: Demo Scenario 2 - Intent & Offering Suggestions**
- Scenario: User asks about password reset
- Shows:
  - Aviator provides answer
  - Suggests relevant offerings
  - "Suggested next steps" section
  - One-click request creation
- [Screenshot placeholder: Aviator suggesting intents and offerings]

**Slide 8: Demo Scenario 3 - Multi-Conversation Management**
- Shows:
  - "Start new topic" within conversation
  - "Start new conversation" icon
  - Conversation history panel
  - Ability to switch between 20 conversations
  - Rename/delete options
- [Screenshot placeholder: Conversation history panel open]

**Slide 9: End-User Value Summary**
- Metrics and benefits:
  - Increased self-service rate
  - Reduced ticket volume
  - Faster time to resolution
  - Improved user satisfaction
  - 24/7 availability

### Agent Journey (Slides 10-16)

**Slide 10: Agent Interface Experience Overview**
- What agents can do:
  - Ticket summarization
  - Solution suggestions
  - Auto-generate content (emails, knowledge articles)
  - Risk assessment
  - Sentiment analysis
- Screenshot: Aviator panel in Agent Interface

**Slide 11: Demo Scenario 1 - Ticket Summarization**
- Scenario: Complex incident with long description and multiple updates
- Shows:
  - "Summarize this incident" button
  - Concise summary generated
  - Ability to ask follow-up questions
  - Context from title, description, updates, comments
- [Screenshot placeholder: Agent interface with summarized ticket]

**Slide 12: Demo Scenario 2 - Solution Suggestions**
- Scenario: Recurring incident type
- Shows:
  - "Suggest a solution" option
  - Aviator analyzes incident details
  - Provides solution based on knowledge base
  - Solution saved to Solution field
  - Agent can refine and apply
- [Screenshot placeholder: Solution suggestion interface]

**Slide 13: Demo Scenario 3 - Auto-Generate Knowledge Articles**
- Scenario: Incident marked as "Knowledge candidate"
- Shows:
  - Checkbox selection triggers Aviator
  - Draft article title generated
  - Draft article content created
  - New Article record linked to incident
  - Agent reviews and publishes
- [Screenshot placeholder: Generated knowledge article draft]

**Slide 14: Demo Scenario 4 - Change Risk Assessment**
- Scenario: Change request evaluation
- Shows:
  - "Analyze risk" button in Change form
  - AI generates descriptive risk assessment
  - Numerical risk score (0-4 scale)
  - Risk score displayed in fields:
    - AI risk assessment (text)
    - AI risk score (0=none, 1=low, 2=moderate, 3=high, 4=very high)
- [Screenshot placeholder: Change form with risk assessment]

**Slide 15: Demo Scenario 5 - UCMDB CI Summarization**
- Scenario: Analyzing configuration item
- Shows:
  - CI detail page with Aviator icon
  - "Summarize this CI" option
  - Summary of CI details and relationships
  - Follow-up questions (e.g., "What software is installed?")
- [Screenshot placeholder: UCMDB with CI summary]

**Slide 16: Agent Value Summary**
- Metrics and benefits:
  - Productivity gains (time saved per ticket)
  - Faster mean time to resolution (MTTR)
  - Improved first-call resolution
  - Reduced agent training time
  - Knowledge capture automation

### Backend Automation (Slides 17-22)

**Slide 17: Intelligent Automation Behind the Scenes**
- Overview of Aviator business rules
- How they work:
  - Triggered by record events
  - Aviator processes data
  - Automated actions taken
  - Full audit trail in History tab
- Benefits: Workflow automation without manual intervention

**Slide 18: Business Rule Scenarios Grid**
- Four key scenarios:
  1. **Sentiment Analysis**
     - Analyzes request text for sentiment
     - Categories: positive, neutral, negative
     - Auto-escalates negative requests to service desk
  2. **Privacy Detection**
     - Identifies PII, financial, health data
     - Auto-routes to "HR Private Sensitive" group
     - Marks Privacy field with justification
  3. **Knowledge Candidate Detection**
     - Detects incidents suitable for KB
     - Auto-generates draft articles
     - Links to incident record
  4. **Change Risk Assessment**
     - Evaluates change details
     - Generates risk score and description
     - Updates AI risk fields

**Slide 19: Business Rule Architecture**
- Visual diagram showing:
  - Trigger: Record created/updated
  - Process: Aviator analyzes content
  - Action: Fields updated, workflows triggered
  - Audit: History tab shows "Updated by: Aviator"
- Customization capability highlighted

**Slide 20: Featured Scenario - Angry Customer Auto-Response**
- **Setup:**
  - Customer submits ticket with angry/negative language
  - Example: "This is ridiculous! I've been waiting 3 days for help!"
- **Challenge:**
  - Need immediate response to prevent escalation
  - Must triage priority appropriately
  - Agent time wasted on detection vs resolution

**Slide 21: The Workflow - Visual Flow**
- Step-by-step flow diagram:
  1. **Ticket Created** - Request submitted with negative content
  2. **Aviator Analysis** - Intent analysis + sentiment detection
  3. **5-Word Summary** - "Customer frustrated with delayed response"
  4. **Sentiment Result** - Marked as "negative"
  5. **IVR Trigger** - Custom workflow automatically initiated
  6. **Automated Actions:**
     - Priority escalation
     - Assignment to senior team
     - Auto-response email sent
     - Manager notification
- [Workflow diagram placeholder with icons and arrows]

**Slide 22: Impact & Results**
- **Quantifiable Benefits:**
  - Response time: Hours → Minutes
  - Escalation rate: -40%
  - Customer satisfaction: +25%
  - Agent focus: 100% on resolution
- **Flexibility:**
  - Customizable for different severity levels
  - Configurable workflows per business rules
  - Integration with existing IVR systems
  - Adaptable to organizational needs

### What's New & Closing (Slides 23-25)

**Slide 23: What's New in SMAX 25.4**
- **Aviator Agents** (Left side):
  - Create task plans (serial or parallel execution)
  - Execute all standard tasks:
    - Manual and automatic tasks
    - Calls to Aviator
    - Orchestration flows
    - Integration Studio
  - Initiated via Business rule process
  - Creates Aviator Agent Session record
  - Full audit history of all actions
- **Google Gemini Option** (Right side):
  - Alternative LLM backend (SaaS only)
  - Enhanced multilingual support
  - Larger general knowledge corpus
  - Advanced language understanding
  - Choice based on data processing preferences:
    - Private Llama 3: Maximum data privacy
    - Google Gemini: Enhanced capabilities
- Visual: Split screen with icons/diagrams

**Slide 24: Key Takeaways**
- **Three Pillars:**
  1. **Private & Secure**
     - AWS-hosted infrastructure
     - Tenant data isolation
     - Data privacy guaranteed
     - Compliance-ready
  2. **Multi-Persona Value**
     - End-users: Self-service empowerment
     - Agents: Productivity boost
     - IT: Workflow automation
  3. **Enterprise Ready**
     - Proven architecture
     - Extensible business rules
     - Scales across service desk
     - Integration with Microsoft Teams, Mobile, UCMDB

**Slide 25: Next Steps**
- **Call to Action:**
  - Schedule live demo
  - Pilot program options
  - Tenant activation process
- **Contact Information:**
  - Sales contact
  - Technical resources
- **Resources:**
  - QR code for documentation
  - Link to SMAX Aviator docs
  - Customer success stories

## Technical Implementation Details

### HTML Framework
- **Platform:** reveal.js
- **Why:**
  - Professional presentation framework
  - Smooth transitions and animations
  - Keyboard navigation
  - Speaker notes support
  - Responsive design
  - PDF export capability

### Design System
- **Color Scheme:**
  - Primary: OpenText/Micro Focus blue
  - Accent: Modern gradients for AI/tech feel
  - Backgrounds: Clean white/light gray
  - Text: High contrast for readability

- **Typography:**
  - Headers: Sans-serif, bold
  - Body: Sans-serif, readable at distance
  - Code/technical: Monospace where appropriate

- **Layout Patterns:**
  - Opening/closing: Centered, minimal
  - Content slides: Left-aligned headings, structured content
  - Demo slides: Large screenshot area with caption
  - Flow diagrams: Horizontal left-to-right progression

### Screenshot Placeholders
Each placeholder will include:
- Descriptive border/frame
- Clear label indicating what should be captured
- Suggested dimensions
- Context notes for presenter

### Speaker Notes
Each slide includes talking points covering:
- Key message for the slide
- Demo instructions (if applicable)
- Transition to next slide
- Common questions to anticipate

### Navigation Features
- Progress bar at bottom
- Slide numbers
- Keyboard shortcuts reference (? key)
- Touch/swipe support for tablets

### Accessibility
- High contrast text
- Alt text for images
- Keyboard navigation
- Screen reader compatible structure

## Demo Preparation Notes

### Required Screenshots
1. Service Portal chat with references
2. Intent/offering suggestions
3. Conversation history panel
4. Agent interface ticket summary
5. Solution suggestion interface
6. Generated knowledge article
7. Change risk assessment
8. UCMDB CI summary
9. Business rule workflow diagram (can be created)

### Demo Flow Options
- **Quick path:** Slides 1-4, 6, 11, 12, 20-22, 24-25 (10 min)
- **Comprehensive:** All slides with pauses for questions (30 min)
- **Custom:** Modular design allows skipping sections based on interest

### Key Messages by Section
- **Opening:** Trust and security first
- **End-user:** Empowerment and self-service
- **Agent:** Productivity and efficiency
- **Backend:** Intelligence and automation
- **Closing:** Enterprise readiness and next steps

## Success Criteria

The presentation will be successful if it:
1. Clearly demonstrates value for each persona
2. Addresses security/privacy concerns upfront
3. Shows practical, relatable scenarios
4. Features the IVR workflow as a differentiator
5. Positions SMAX Aviator as enterprise-ready
6. Generates interest in demo/pilot
7. Can be delivered in 25-30 minutes with flexibility

## Next Steps

1. Create HTML presentation file
2. Generate placeholder graphics/diagrams
3. Add speaker notes to each slide
4. Test on presentation hardware
5. Capture actual screenshots from SMAX environment
6. Review with stakeholders
7. Practice delivery with demo flow
