## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/106

**Issue title:** Shared test fixture for a sample user profile is missing from `tests/fixtures/`

**Tier:** [x] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
Several test and evaluation flows expect a sample profile at `tests/fixtures/sample_profiles/basic_profile.json`, but that fixture is missing from the repository. Without it, tests that need a realistic portfolio cannot run against consistent input and may be skipped or fail before exercising the application behavior. The change is limited to restoring well-formed test data containing a GitHub username, resume information, and two repositories. A successful fix will give the test suite a stable, reusable profile that matches the project's expected data shape.

**Branch name:** `test/106-restore-sample-profile-fixture`

**Setup confirmation:** [x] App runs locally at localhost:5173

**Cohort ledger:** [x] Issue added to cohort ledger

### Selection notes — “Is this issue right for me?” checklist

- **Understanding:** I can explain the missing behavior and define “done” as adding a valid, realistic JSON fixture that can be reused by the affected test and evaluation flows.
- **Tier fit:** I chose a Tier 1 issue because this is my first contribution to this large codebase. The work is localized to one new fixture file, does not require an architectural change, and the issue estimates only 1–2 hours of implementation work.
- **Codebase readiness:** I confirmed that the target fixture is absent, found the reference to sample profiles in `scripts/run_evals.py`, reviewed the profile fields in `api/schemas/profile.py`, and read the existing fixture and test patterns in `tests/conftest.py` and `tests/unit/test_review_service.py`.
- **Scope and time:** I checked the issue comments and the cohort ledger's claim count. Claims are non-exclusive, the issue has no listed blockers or unresolved dependencies, and the small file scope is realistic to complete and test before the Week 9 deadline.
