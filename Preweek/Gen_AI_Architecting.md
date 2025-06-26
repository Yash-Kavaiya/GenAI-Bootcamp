# Week 1 Architectural Diagramming Notes
*Instructor: Angie Brown*

https://youtu.be/94ESD5pP1oE?si=z-KExHkAiIIoVa8X

## Assignment Overview
- **Goal**: Create an architectural diagram for week 1 submission
- **Scope**: Keep it simple and manageable for first week
- **Tools**: Use any diagramming software (Lucid Charts, PowerPoint, Draw.io, Excel, or pen and paper)
- **Deliverables**: 
  - Architectural diagram (recreate the simplified version shown)
  - Optional: README.md with requirements and considerations

## Core Components to Include

### 1. Study Activity
- **Example**: Sentence Constructor
- Represents the main application functionality

### 2. Model API
- **Component**: LLM (Large Language Model)
- **Specification**: 70 billion parameter model
- **Function**: Generation of responses
- **Flow**: User query → Model → Response

### 3. User Interaction
- **Components**: User/Users
- **Flow**: 
  - User sends query
  - System processes through various components
  - User receives response

### 4. RAG Implementation (Retrieval Augmented Generation)
- **Purpose**: Fetch data from external sources before generation
- **Sources**: Internet, databases, vector databases
- **Flow**: Query → RAG → External source → Back to model
- **Use Cases**: 
  - Practice sentences based on favorite movies (from database)
  - Practice with latest news (from internet)

### 5. Security Components
- **Input Guard Rails**: Filter and validate incoming queries
- **Output Guard Rails**: Filter and validate model responses
- **Placement**: Near the model in the workflow

### 6. Performance Optimization
- **Prompt Caching**: Cache frequently used prompts/responses
- **Multiple Cache Options**:
  - Between RAG and user input
  - Between user and RAG
  - Various other strategic locations
- **Trade-offs**: Different caching strategies have different benefits

### 7. Database Components
- **Type**: Vector database (specialized for AI applications)
- **Purpose**: Store training materials, user data, or reference content

## Components NOT Included (Simplified Version)
- ❌ Payment Gateway
- ❌ Scoring (LLMs don't return confidence scores)
- ❌ Routing (too complex for this scope)
- ❌ Write Actions (keep simple for now)

## Technical Considerations

### Business Requirements Example
- **Hardware Investment**: $10-15K budget
- **User Base**: 300 active students
- **Location**: Students located in specific city (e.g., Nagasaki)
- **Infrastructure**: Company wants to own infrastructure for:
  - Privacy concerns with user data
  - Cost control (avoiding expensive managed services)

### Assumptions
- Open source LLMs will be powerful enough for the hardware budget
- Single server in office can handle bandwidth for 300 students
- Local hosting is sufficient (not global market)

### Data Strategy Concerns
- **Copyright Issues**: Must purchase and supply materials
- **Storage**: Materials stored in local database for RAG access
- **Privacy**: Keep data on-premises for security

### Model Selection Considerations
- **Preference**: IBM Granite
- **Reasons**:
  - Truly open source
  - Traceable training data
  - Avoids copyright issues
  - Full understanding of model components

## Submission Requirements

### File Structure
```
/gen-architecting/
  ├── [diagram-file].png or .jpeg
  └── README.md (optional)
```

### Diagram Requirements
- **Format**: PNG or JPEG for easy viewing
- **Folder Name**: Must be exactly "gen-architecting"
- **Content**: Should look different from instructor's example but include same components
- **Completeness**: Focus on core components, complexity is optional

### Optional README Content
- Functional requirements
- Non-functional requirements
- Assumptions
- Technical considerations
- Data strategy

## Key Takeaways
1. **Keep it simple** - This is week 1, complexity can come later
2. **Focus on communication** - Diagram should clearly show system components to stakeholders
3. **Understand trade-offs** - Each component has cost, complexity, and reliability considerations
4. **Document assumptions** - Important for stakeholder discussions
5. **Consider business context** - Technical decisions should align with business constraints

## Next Steps
- Create your architectural diagram using preferred tool
- Save as PNG/JPEG in correct folder structure
- Optional: Add README with technical considerations
- Submit for week 1 along with sentence construction assignment
