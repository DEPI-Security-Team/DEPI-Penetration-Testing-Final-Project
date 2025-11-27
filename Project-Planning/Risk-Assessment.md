# Risk Assessment & Mitigation Plan

| Risk Description                                   | Likelihood | Impact | Mitigation / Action                                      |
|----------------------------------------------------|------------|--------|-----------------------------------------------------------|
| Lab not isolated and tests accidentally escape     | Medium     | High   | Ensure Host-only network setup and verify before testing |
| VM corruption or loss of progress                  | Low        | High   | Create snapshots before each major stage                 |
| Tool failures or incompatible versions             | Medium     | Medium | Use stable versions and test tools beforehand            |
| Exploits causing service crashes                   | Low        | Medium | Test on isolated VM and keep snapshots ready             |
| Insufficient logs or incomplete evidence           | Medium     | Medium | Enable logging and capture all outputs/screenshots       |

## Contingency Plans
- Restore VM using snapshots if any major issue occurs.  
- Maintain timestamped notes for each experiment.  
- Escalate unusual behavior to the project supervisor immediately when needed.
