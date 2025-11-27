# Non-Functional Requirements

The project must also meet these non-functional requirements:

1. **Performance**
   - Scans should complete within reasonable time (e.g., full Nmap scan ≤ 30 minutes for the target VM).

2. **Security**
   - Testing must be performed in an isolated environment to prevent unintended impacts.
   - Sensitive data (credentials, hashes) must be stored securely.

3. **Usability**
   - Documentation must be clear and structured.
   - Reports must be readable for both technical and non-technical stakeholders.

4. **Reliability**
   - Tools and scripts should run consistently without crashing the VM.
   - Snapshots must be taken to restore the environment if errors occur.

5. **Maintainability**
   - Code and documentation should follow consistent naming conventions and formatting.
   - Updates to the methodology should be easy to incorporate.
