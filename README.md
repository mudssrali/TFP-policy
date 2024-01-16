# Policy

## New member workflow

```mermaid
flowchart TD
    A[New member Joined] --> B( Direct to #Welcome) --> C(Choose Roles)
    C --> D{Did member choose roles}
    D -->|Yes| E[Can see channels for selected roles]
    D -->|No| F[Send automated message to remind to choosing roles] --> C
    E --> H[Hide Other channels by default]
    H --> I[Show liaise-projects and others after a few days]
```

## New Idea/Project 

### Submit the idea/project

```mermaid
flowchart TD
    A(Go to Submit a New Idea/Project) --> B(Open a Ticket)
    B --> C[Mee6 Creates a ticket and display the template]
    C --> D{The Project needs PM?}
    D -->|Yes| E[Ping PM channel] --> H[PM assigned and claim the ticket] --> I[PM setup a meeting with the owner] --> J[PM discuss the decision to _new_project_reviewer]
    D --> |No| F[_new_project_reviewer create a post in #new-ideas]
    J --> L{Project Accepted?} --> |Yes| F
    L --> |No| G
    F --> G[Close the ticket]

```
> Note: A better template with specific details is required.

### Onboard the new idea/project
- Close the post once the ask is addressed
- Need status tags for each collaborative
- Limit the time (24 hours) to reply back to the interested volunteer.

## Collaborator Matching

**Bot Command**:An existing project
