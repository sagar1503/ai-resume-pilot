# Resume Automation Workflow

Whenever the user mentions they have added a "new JD", "new CV", or new job description, you **MUST** automatically execute the following workflow without needing further explicit instructions:

1. **Identify the New JD**: Check the `JD/` directory for new job description files and cross-reference them with `Resume_Tracker.md` to identify untailored roles.
2. **Read the JD & Configuration**:
   - Read the job description file to understand the key skills, requirements, and keywords.
   - Read `config.yaml` for candidate metadata, naming conventions, and sync settings.
   - Read `.agents/rules/candidate-profile.md` for candidate-specific verified metrics, career boundaries, and feasibility checks (e.g., clearance, driving license, work authorization).
3. **Feasibility Pre-Check**:
   - If the role strictly requires qualifications, clearances, or licenses the candidate does not have (as defined in `candidate-profile.md`), mark as "Skipped" with reason in `Resume_Tracker.md` and state this in the 1-line response.
4. **Tailor the Resume**:
   - Use `CV_Base.tex` (or the candidate's designated master `.tex` file) as the baseline.
   - Apply guidelines from `resume-tailor` and `resume-bullet-writer` skills (in `.agents/skills/`) to strategically reorder skills/bullets and rigorously enforce the Google XYZ formula (`Accomplished [X] as measured by [Y] by doing [Z]`) using **only verified metrics** from `candidate-profile.md`.
   - Create a new `.tex` file following the naming convention in `config.yaml` (e.g., `[cv_prefix]_[CompanyName].tex`).
5. **Chat Response**:
   - Respond with **ONLY 1 single line** stating whether the JD is suitable for the resume/profile and confirming the tailored file creation. Do **NOT** provide lengthy summaries, breakdowns, or conversational filler in the chat.
6. **Update the Tracker**:
   - Automatically update `Resume_Tracker.md` by appending a row for the newly created resume (Company name, JD file path, Tailored Resume file path, Status, Date).
7. **Sync to Overleaf (Optional)**:
   - If `overleaf_sync.enabled` is `true` in `config.yaml`, automatically copy the new `.tex` file into the designated sync folder, commit, and push via git. If disabled, skip this step without error.

---

## Strict Resume Rules & Constraints

- **NEVER Include JD Logistics/Schedule Details**: Under no circumstances should job-specific work patterns, client office locations, day counts, or commute notes (e.g., "(2 days/week) in Ashton", "3 days/week on-site", "travel 3x/month", "commutable to X") be written in any resume. The `AVAILABILITY & WORK AUTHORISATION` section (specifically `Location`) MUST strictly remain general and candidate-centric as established in `config.yaml` and `CV_Base.tex`.
- **Anti-Hallucination**: Never fabricate numbers, percentages, company names, or dates not documented in `candidate-profile.md` or `CV_Base.tex`.
- **One-Page ATS Architecture**: Keep layouts clean, single-column, with standardized LaTeX geometry and standard sections (`PROFESSIONAL SUMMARY`, `CORE SKILLS`, `PROFESSIONAL EXPERIENCE`, `KEY ACHIEVEMENTS`, `EDUCATION`, `AVAILABILITY & WORK AUTHORISATION`).
