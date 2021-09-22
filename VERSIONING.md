# VERSIONING

For my applications we follow Semantic Versioning as defined on [http://semver.org/](http://semver.org).

## Interpretation of SemVer for the App

### PATCH

A release only containing backwards-compatible bug fixes. A patch is meant to fix a particular issue without "chroming the bumpers" or adding additional functionality. "Fix only what's broken!"

#### Example of a Bug Fix

In version 1.0.0 we deployed a textbox. We forgot to validate the textbox for data insertion, and it is allowing bogus data.  We need to fix this fast. The resulting 1.0.1 would fix this by adding textbox validation that was missed.

### MINOR

If a release adds functionality in a backwards-compatible manner and contains backwards-compatible bug fixes it will bea minor release.

#### Example of a new Feature

In version 1.0.0 we added a textbox that had character length validation.  We want to provide additional validation to strip special character and show a message indicating character filtering has occurred. The result doesn't break anything and is not an immediate need It would be version 1.1.0.

### MAJOR

Any non-backward compatible changes lead to a major version bump. This includes:

- Any change to the output that changes the behavior of existing application that could require newer versions of browsers.
- Any change to the output that prevents you from deploying over an existing application.
- Any core functionality changed in a way that requires data transformation if reporting to say an endpoint
- Any change that changes an endpoint location or required input params when reporting output to an endpoint

#### What is considered a breaking change?

- Everything which requires a different operating environment or removes previously required functionality
  + Makes use of newer browser technologies requiring a new version of a browser causing older browsers to no longer be supported
  + Anything that integrates with operating system specific items such as cameras or USB device interfaces and requires a different version of an OS than prior versions of tha application.
  + Endpoint for data storage changes
  + ...
- Anything that could impact security or privacy
  + Breaks existing data for things such as analytics or EULAs
  + Transient data which is available during runtime is changed
  + ...

#### Example of a Breaking Change

If change the network address to an end point that scores questionnaires. This would  be a breaking change and would change our version from 1.0.0 to 2.0.0

### FAQ

1. Is it okay to mark a feature as deprecated in version 1.4.0 and then remove it in 1.8.0

No, since this is a breaking change it should trigger a major version bump to 2.0.0

2. Can we change everything in a major version bump?

Yes, this is the purpose of major version bumps. Ideally every breaking change has a clear and well documented migration path. In the best case the features were already introduced earlier and upgrading is not a deal breaker.

3. Can we do a major version bump without a breaking change?

No, as we strictly follow Semantic Versioning. The suggested strategy is to add features with minor releases and only do major version bumps when we take out deprecated features. Sometimes this is not possible, but as suggested above then a well documented migration path should come with the release.
