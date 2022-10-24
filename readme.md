```mermaid
sequenceDiagram
    participant SWARM 
    participant GitHub Workflow
    participant p4setup
    participant test_cppcheck
    participant comment
    participant P4
    SWARM->>GitHub Workflow: review, change, update
    GitHub Workflow->>p4setup: change, PORT,USER,PASSWD
    p4setup->>GitHub Workflow: files
    Github Workflow->>test_cppcheck:./temp
    test_cppcheck->GitHub Workflow: result_cppcheck.txt
    GitHub Worflow->>commment:update,review,result_cppcheck.txt
    comment->>SWARM: comment
```
