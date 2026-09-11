# Features and specification

## Context
Researchers publishing novel methodologies face pushback proving the validity data to reviewers (JOB-01, JOB-02). Currently, authors must either spend hours manually assembling raw files, execution logs, and READMEs before initial submission (INT-01), or risk long and costly delays conducting external validation reruns when reviewers challenge custom parameters (INT-02). 

To eliminate this obstacle, the proposed system is an automated data provenance and audit trail generator. The system integrates into existing scientific processing pipelines to capture hashes of raw inputs, script parameters, and execution logs. It enables researchers to instantly export standardized, immutable manifests that prove data integrity and pipeline execution without exposing proprietary source code or requiring manual work.
## Users
Profiles and evidence in USERS.md:
**PROFILE-01 (Early-Career Academic Researcher):** Undergraduate researchers using custom data pipelines (such as cell segmentation scripts) face issues preparing files prior to journal submission (INT-01). They require an automated mechanism to log script parameters and generate standardized provenance packages (JOB-01) so they can eliminate manual file packaging without interrupting lab work.
* **PROFILE-02 (Senior R&D Lead & Industry Executive):** Senior research leads publishing unconventional findings face skepticism regarding data integrity (INT-02). They require verifiable audit trails and raw baseline exports (JOB-02) to validate experimental integrity without delays or external validation reruns.
## Scope
### Included Behavior (In-Scope)
* **Automated Logging:** Log raw data, pipeline parameters, and execution environments automatically during script runs
* **Manifest Export:** Generate provenance manifests and audit trails for manuscript submission.
* **Verification:** Produce hashes for raw inputs and outputs to prove data remains unaltered.

### Explicit Non-Goals (Out-of-Scope)
* **Heavy Raw Data Storage:** Storing large datasets directly.
* **Code Debugging:** Validating or fixing runtime errors in algorithms.
* **Electronic Lab Notebook Replacement:** Acting as a general Electronic Lab Notebook for text notes or inventory.
### Kano hypotheses
Provide at least six features. For each, name the user segment, date, category, and evidence-based reasoning. These are tentative hypotheses, not validated survey findings.

| Feature ID | Feature | Kano hypothesis | Segment / date | Evidence and reasoning |
|---|---|---|---|---|
| F-01 | Digital Data Seal & Verification | Must-have | PROFILE-01 / PROFILE-02<br>September 10, 2026 | Without this guarantee of the security of data, the manifest cannot prove data integrity. It is a core expected functionality. |
| F-02 | Simple Export to JSON/PDF Manifest | Performance | PROFILE-01<br>September 10, 2026 | Cuts manual packaging time (INT-01 lost 10+ hours). Faster exports and ease of use make the system more desirable. |
| F-03 | Automatic script tracker | Performance | PROFILE-01<br>September 10, 2026 | Easier setup for those not accustomed to software. Easier integration increases satisfaction. |
| F-04 | Live result testing tool | Attractive | PROFILE-02<br>September 10, 2026 | Lets reviewers provide feedback avoiding reruns (INT-02). Unexpected feature that will provide satisfaction. | |
| F-05 | Custom UI | Indifferent | PROFILE-01 / PROFILE-02<br>September 10, 2026 | Visual styling does not help pass peer review or verify data. Users might not care. | |
| F-06 | Mandatory Code Sharing | Reverse | PROFILE-02<br>September 10, 2026 | Forcing industry users to share any type of data drives them away. | |

## Behavior
(Sequence & Trigger) When a researcher attaches the one line integration hook to a Python or MATLAB script and executes the pipeline, (Action) the system logs settings and timestamps while computing for all raw inputs, (Visible Outcome) outputting a confirmation without disrupting execution.

(Sequence & Trigger) Upon script completion, (Action) the system automatically packages parameters and logs into a JSON or PDF Data Manifest, (Visible Outcome) saving the manifest directly to the project directory, ready for journal submission.

(Sequence & Condition) When reviewers access the manifest, (Action) the system verifies data integrity, (Visible Outcome) displaying a verified status badge alongside parameter controls that allow reviewers to test results
## Constraints
Platform: Operates as a background utility compatible with standard scientific execution environments (Python, MATLAB, Jupyter) across Windows, macOS, and Linux.
Data: Captures and stores execution data, pipeline parameters, runtime logs, and SHA-256 hashes only; raw binary datasets remain on external user storage.
Privacy & Security: Encrypts local manifest exports and execution logs; operates without transmitting source code or underlying algorithms to external servers.
Scope Limits: Handles data tracking and manifest generation. Does not provide cloud data hosting, code debugging, or full ELN project management features.

## Acceptance
Replace examples with criteria for your feature. Choose the pattern that fits; HW2 does not require both WHEN and IF.

- Ubiquitous: The system shall compute SHA-256 hashes for all input files and package parameters into a JSON/PDF manifest.
- Event-driven: When a user executes a tracked script, the system shall compute hashes and record environment settings in the background.
- State-driven: While tracking is active, the system shall execute with low performance overhead.
- Unwanted: If a raw data file is modified post execution, then the system shall display a warning.
- Optional: Where the parameter sandbox is enabled, the system shall allow online threshold adjustments without exposing source code.
## Handoff reflection
An external peer reviewer evaluated this to verify scope boundaries and confirm that technical requirements were verifiable. The review identified two main issues: the original criteria failed to specify how hash mismatches were displayed, and background tracking boundaries were unclear for nonstandard scripts. In response, the it was revised to require a warning badge on the manifest and to limit automated logging to scripts containing the integration hook. A remaining limit is that while the tool guarantees file integrity, it cannot validate whether initial raw input data contained experimental errors, and it doesn't deal with hardware driver dependencies in the parameter sandbox.
## AI assistance
I used AI to understand what a lot of the question were asking. I also used it for a ton of syntax help, like bullet points and stuff. I put my original draft in to gemini to see what issues there were and if i missed anything the assignment asked for. It pointed out some stuff and I took it into consideration. 
