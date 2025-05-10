graph TD
    A[Start: Personal Center Page] --> B[Click "Edit Personal Info" Button]
    B --> C[Enter Personal Info Modification Page]
    
    C --> D[Modify Nickname]
    D --> D1[Show Current WeChat Nickname as Default]
    D1 --> D2[User Edits Nickname or Retains Default]
    
    C --> E[Modify Avatar]
    E --> E1[Click Avatar Frame]
    E1 --> E2[Select Image from Album or Camera]
    E2 --> E3[Upload Image to Aliyun Server]
    E3 -->|Success| E4[Return Image Path & Display Preview]
    E3 -->|Failure| E5[Show "Image Upload Failed, Please Retry"]
    E5 --> E2
    
    D2 --> F[Click "Save" Button]
    E4 --> F
    F --> F1[Save Nickname & Avatar Path to Local Server]
    F1 -->|Success| F2[Complete Modification & Return to Personal Center]
    F1 -->|Failure| F3[Show "Save Failed, Please Try Again Later"]
    F3 --> C
    
    F2 --> G[End]
