# Policy

## New member workflow

```mermaid
flowchart TD
    A([New member Joined]) --> B[Direct to #Welcome] --> C[Choose Roles]
    C --> D{Did member choose roles}
    D -->|Yes| E[Can see channels for selected roles]
    D -->|No| F[Send automated message to remind to choosing roles] --> C
    E --> H[Hide Other channels by default]
    H --> I[Show liaise-projects and others after a few days] --> Q([END])
```

## New Idea/Project 

### Submit the idea/project

```mermaid
flowchart TD
    A([Go to Submit a New Idea/Project]) --> B[Open a Ticket]
    B --> C[Mee6 Creates a ticket and display the template]
    C --> D{The Project needs PM?}
    D -->|Yes| E[Ping PM channel] --> H[PM assigned and claim the ticket] --> I[PM setup a meeting with the owner] --> J[PM discuss the decision to _new_project_reviewer]
    D --> |No| F[_new_project_reviewer create a post in #new-ideas]
    J --> L{Project Accepted?} --> |Yes| F
    F --> G([Close the ticket])
    L --> |No| G
```
> Note: A better template with specific details is required.

### Onboard the new idea/project
```mermaid
flowchart TD
    A([New Idea/Project Post]) --> B[Add tags and owner to the post]
    B --> C{{status = new}} --> D[_new_project_reviewer/PM send Bot command for requests]
    D --> E{Volunteer responded} 
    E --> |Yes| F{{Status = In Progress}} ---> G[Remove the corresponding tag]
    E --> |No| H[Wait 24 hours] --> I[Send new Bot Command] --> D
    G --> J{All Requests Fulfilled?}
    J --> |No| E
    J --> |Yes| K[Send Thank you and closing message] --> L{{Status == Complete}} --> Q
    Q([Close the Post])
```

## Collaborator Matching

**Bot Command**:An existing project
