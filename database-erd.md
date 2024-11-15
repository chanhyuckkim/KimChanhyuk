# Database ERD Diagram

```mermaid
%%{init: {'theme': 'neutral', 'htmlLabels': true, 'securityLevel': 'loose', 'themeVariables': {'fontSize': '16px'}, 'flowchart': {'htmlLabels': true, 'rankSpacing': 80, 'nodeSpacing': 120}}}%%
erDiagram
    user_info {
        string(20) UserID PK
        string(50) UserPW
        string(20) Role
    }

    Files {
        string(255) FileID PK
        string(255) FileName
        string(20) UserID FK
    }

    SectionData {
        int SectionID PK
        string(255) FileID FK
        string(20) UserID FK
        text Content
        int PageLimit
    }

    TableOfContents {
        int TOCID PK
        string(255) FileID FK
        string(20) UserID FK
        string(50) Chapter
        string(255) MainTopic
        string(255) SubTopic
    }

    Proposals {
        int ProposalID PK
        string(255) FileID FK
        string(20) UserID FK
        string(255) SubTopic
        text Content
        text Headline
    }

    TokenUsage {
        int TokenID PK
        string(20) UserID FK
        float CostKRW
    }

    ChatHistory {
        int ChatID PK
        string(255) FileID FK
        string(20) UserID FK
        int SectionIndex
        text Message
        string(20) Sender
    }

    TokenUsageHistory {
        int HistoryID PK
        string(20) UserID FK
        float CostKRW
        string(50) Model
        int UsageMonth
        int UsageYear
    }

    image {
        int ImageID PK
        string(20) UserID FK
        string(255) FileID
        int ImageIndex
        string(255) ImageUrl
        string(255) SubTopic
    }

    user_info ||--o{ Files : "has"
    user_info ||--o{ SectionData : "creates"
    user_info ||--o{ TableOfContents : "manages"
    user_info ||--o{ Proposals : "writes"
    user_info ||--o{ TokenUsage : "tracks"
    user_info ||--o{ ChatHistory : "participates"
    user_info ||--o{ TokenUsageHistory : "records"
    user_info ||--o{ image : "uploads"
    
    Files ||--o{ SectionData : "contains"
    Files ||--o{ TableOfContents : "has"
    Files ||--o{ Proposals : "includes"
    Files ||--o{ ChatHistory : "relates"
