# Release Notes

## Version 1.11
- Added option to save id's of triggered builds in an environment variable so subsequent tasks can use this info (e.g. for downloading artifacts etc.) ([Save resulting build ID in environment ](https://github.com/huserben/TfsExtensions/issues/15))
- Changed output so that a link to the triggered build is displayed ([Feature request: when a build is queued, include a link or the full name of the new build](https://github.com/huserben/TfsExtensions/issues/16))

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@garuma**](https://github.com/garuma)  
- [**@shmatkotija**](https://github.com/shmatkotija)

## Version 1.10
- Added support to select which source branch shall be used - either the same as the source build or it can be specified freely ([Unable to specify git sourceBranch for triggered build](https://github.com/huserben/TfsExtensions/issues/14))
- Added option to wait for triggered builds to complete - this enables to run builds on a different agent and continue with the build just when they have finished. User can decide in which intervall the triggered builds shall be checked and if the build should fail if one of the builds was not completed successfully.
- Added handling that if for some reason we get en already escaped string we do not encode it a second time ([Double encoding of URL with space in collection name](https://github.com/huserben/TfsExtensions/issues/12))

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@shmatkotija**](https://github.com/shmatkotija)  
- [**@viperx77**](https://github.com/viperx77)  

## Version 1.9
- Added support to trigger multiple builds at once via a comma-separated list

## Version 1.8.5
- Fixed bug that caused Task to fail when using Current Source Version on Git Repositories [The latest version throw 409 conflict error](https://github.com/huserben/TfsExtensions/issues/7)

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@nobitagamaer**](https://github.com/nobitagamer)  

## Version 1.8
- Added option to use the same source version for the triggered builds. If enabled, when a build is triggered for a specific changeset, the triggered build will use the same source version.
- Added option to pass parameters to triggered build. Build Parameters like *BuildPlatform* or *BuildConfiguration* can be specified as part of the Build Task. It is possible to use hardcoded values or reuse the variables from the original build. A detailed description can be found in the overview.

## Version 1.7
- Added option that you can choose if the builds that are triggered are run now for the same user that triggered the first build. This means if a CI build is kicked off by a check-in from a specific user, the triggered builds will be queued for that user as well. This enables that queries based on the user name will work properly (e.g. customized dashboards, email-alerts etc.) - based on feedback from [Dependent Build Timestamp Not Updated ](https://github.com/huserben/TfsExtensions/issues/6)

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@bdwellborn**](https://github.com/bdwellborn)  

## Version 1.6
- SourceBranch is now included when triggering a build 
- Fixed issue that exception was thrown when Blocking Build Condition was enabled with the current build selected, but no additional builds selected [(see Issue)](https://github.com/huserben/TfsExtensions/issues/4)

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@nobitagamaer**](https://github.com/nobitagamer)  

## Version 1.5
- Added new Condition to check if last build of a definition failed. This enables to queue for example a scheduled build automatically if it failed last time and all dependent builds are now fixed.

## Version 1.4
- Added support for Personal Access Token and OAuth System Token Authentication ([Invalid Web Request results on a default VSTS environment](https://github.com/huserben/TfsExtensions/issues/2))

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@nobitagamaer**](https://github.com/nobitagamer)  
- [**@lukx**](https://github.com/lukx)

## Version 1.3.16
- Fixed Issue that Trigger did not work when building in Release Mode ([Trigger Build out of a release build does not resolve BUILD_REPOSITORY_URI](https://github.com/huserben/TfsExtensions/issues/1))

### Acknowledgements
Thank you goes to all of the following users, who contributed feedback, bug reports, code submissions, testing, and reviews which helped in this release.  
- [**@lukx**](https://github.com/lukx)