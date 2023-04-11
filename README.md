# onboarding-1

Run on a not-onboarded repo using new logic.

## Expectations:
  - Creates onboarding Pr
  - Creates onboarding cache
  - On second run updates the cache
  
## Observations:
  - Creates onboarding Pr ✅
  - Creates onboarding cache ✅
  -  On second run updates the cache ✅
## Relevant Logs
### First Run
```log
DEBUG: Create Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-1)
       "onboardingCache": {
         "defaultBranchSha": "ede1592fa1f26a98af1ea5c1e0d91ad8e3bc6a37",
         "onboardingBranchSha": "9c7af2c45636235eca3352be86dc35ebd64ddb4a",
         "isConflicted": false
       }
```
### Second Run 
*note: actually 3rd run because I updated baseBranch before running which invalidated the cache
```log
DEBUG: checkOnboarding() (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: isOnboarded() (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: Onboarding cache is valid. Repo is not onboarded (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: Repo is not onboarded (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: getBranchPr(renovate/configure) (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: findPr(renovate/configure, undefined, open) (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: getPrList success (repository=RahulGautamSingh-testing/onboarding-1)
       "pullsTotal": 1,
       "requestsTotal": 1,
       "apiQuotaAffected": true
DEBUG: Found PR #1 (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: Onboarding PR already exists (repository=RahulGautamSingh-testing/onboarding-1)
DEBUG: Merge onboarding branch in default branch (repository=RahulGautamSingh-testing/onboarding-1)
... clones ...
DEBUG: Update Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-1)
       "onboardingCache": {
         "defaultBranchSha": "0a30f967577b454d5aa5f012c9fe0c1f1f46ab19",
         "onboardingBranchSha": "9c7af2c45636235eca3352be86dc35ebd64ddb4a",
         "isConflicted": false
       }
```
