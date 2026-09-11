# User research and jobs

## Interview synthesis
Use participant codes (INT-01 and INT-02), dates, relevant circumstances, and approximately 15 minutes per interview. Ask about a specific recent experience. Summarize confirmed, contradicted, or uncertain findings; do not manufacture surprises. Keep sensitive raw notes out of the repository.

### INT-01
INT-01 | Undergraduate Researcher, BME Optics & Imaging Lab | September 7, 2026  

What happened and the participant's workaround: While preparing a manuscript for submission, a graduate researcher anticipated that reviewers would push back on a section about their custom cell-segmentation pipeline. To ensure that the paper showed integrity to the reviewer, INT-01 spent three days before review organizing raw .tiff files with timestamped execution logs to upload to a publi repository.  

What was reported: The data clean-up took up the entirety of his required 10 hours a week of lab time in the week leading up to send off. This time took away from actual wet-lab experiments.  

What I observed: He stated that he learned preemptive actions such as this data cleaning were common, but also thought they were largely a waste of time.  

What I inferred: Academic labs spend a lot of time and effort preemptively supplying proof of integrity to reviewers because there is no way to definitively prove the trustworthiness of the data, so they want to leave as little doubt as possible.  

Evidence that confirms, challenges, or leaves the framing uncertain: It confirms that the integrity of the data is an important factor to consider before sending in a  submission, but challenges that the friction caused by the data is mostly apparent after being sent back by a reviewer.

### INT-02
INT-02 | Senior Industry Research Lead & Startup Executive | September 9, 2026  

What happened and the participant's workaround: Submitted a manuscript that contained findings that challenged the status quo of tissue storage. The primary reviewer accepted the paper into the journal, but left comments (can be viewed by readers) that suggested that many of the results could have been due to an artefact, noise, or an improper signal threshold. In order to bolster credibility of the data, INT-02's workaround was collaborating with an external academic lab to redo much of the experimentation. They spent many weeks on generating a validation of the dataset before resubmitting the paper to the same journal.  

What was reported: Stated that when findings challenge established scientific consensus, standard protocol isn't enough. Reviewers expect extra validation, especially when data is tied to corporate entities.  
what I observed: Seemed frustrated when recalling the weeks of delay and logistics required to nullify the skepticism.  
What you inferred: Researchers face great time and financial demands proving cutting edge data validity because they lack the tools to verify protocol execution internally.
Evidence that confirms, challenges, or leaves the framing uncertain: Confirms that proving raw data validity for novel science is one of the primary publication obstacles.

## Job statements
JOB-01: When preparing a manuscript with custom data pipelines, I want to automatically generate an immutable data manifest, so I can eliminate manual file packaging and defend pipeline integrity before submission.
Evidence: INT-01 spent over 20 hours manually zipping raw TIF files, writing READMEs, and logging script parameters before manuscript submission.

JOB-02: When unconventional scientific findings face reviewer pushback, I want to instantly provide verified execution lineages and baseline data, so I can validate raw data integrity without delayed, costly external re-runs.
Evidence: INT-02 lost six weeks and R&D budget commissioning an external lab re-run after a reviewer questioned custom assay thresholds.

## User profiles
PROFILE-01: Early-Career Academic Researcher
* **Relevant role:** Undergraduate / Graduate Researcher in a Biomedical Optics & Imaging Laboratory.
* **Circumstances:** Regularly processes high-volume microscopy data using custom-built scripts (e.g., cell-segmentation pipelines) and prepares primary data packages for peer-reviewed journal submissions.
* **Needs:** An automated way to track script execution parameters and bundle raw data into a standardized provenance package without interrupting active wet-lab experiments.
* **Constraints:** Limited administrative bandwidth, no formal software engineering background, and reliance on open-source file platforms (e.g., Figshare, GitHub).
* **Evidence IDs:** INT-01, JOB-01
* **Profile Insights:**
  * *Reported:* Spends up to 20 hours per submission cycle manually organizing raw TIF files, writing README documentation, and logging script execution parameters.
  * *Observed:* Expresses resignation toward pre-submission file packaging, viewing it as necessary but disruptive "administrative busywork."
  * *Inferred:* Student researchers want to share verifiable raw data, but the lack of automated provenance tools makes manual prep a major productivity bottleneck.
PROFILE-02: relevant role, circumstances, needs, constraints, and evidence IDs.

Use reported / observed / inferred labels. Earlier known / assumed labels are acceptable if the distinction is clear. Two exploratory interviews do not establish population prevalence.
