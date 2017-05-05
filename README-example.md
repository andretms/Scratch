Microsoft Authentication Library for Apple
=====================================

| [Get Started](https://aka.ms/aaddev)| [Docs](https://aka.ms/aaddev) | [API Reference](http://cocoadocs.org/docsets/MSAL/) | [Support](README.md#community-help-and-support) | [Releases](../../releases)
| --- | --- | --- | --- | --- |


The MSAL library for macOS and iOS gives your app the ability to begin using the [Microsoft Cloud](https://cloud.microsoft.com) by supporting [Microsoft Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory/) and [Microsoft Accounts](https://account.microsoft.com) in a converged experience using industry standard OAuth2 and OpenID Connect. The library also supports [Microsoft Azure B2C](https://azure.microsoft.com/services/active-directory-b2c/) for those using our hosted identity management service.

[![Build Status](https://travis-ci.org/AzureAD/microsoft-authentication-library-for-objc.svg?branch=dev)](https://travis-ci.org/AzureAD/microsoft-authentication-library-for-objc)

## Important Note about the MSAL Preview

These libraries are suitable to use in a production environment. We provide the same production level support for these libraries as we do our current production libraries. During the preview we reserve the right to make changes to the API, cache format, and other mechanisms of this library without notice. For instance, a change to the cache format may impact your users, such as requiring them to sign in again and an API change may require you to update your code. When we provide our General Availability release later, we will require you to update your application to our General Availabilty version to continue to get support. 

## Example

```swift
     if let application = try? MSALPublicClientApplication.init(clientId: kClientID, authority: kAuthority) {
        application.acquireToken(forScopes: kScopes) { (result, error) in
            if result != nil {
                    // Set up your app for the user
          } else {
                print(error?.localizedDescription)
            }
        }
    }
    else {
            print("Unable to create application.")
        } 
```

## Installation

### Using Cocoapods

You can use [CocoaPods](https://cocoapods.org) to remain up to date with MSAL within a specific major version. Include the following line in your podfile:

`pod 'MSAL'`

You then you can run either `pod install` (if it's a new PodFile) or `pod update` (if it's an existing PodFile) to get the latest version of MSAL. Subsequent calls to pod update will update to the latest released version of MSAL as well.

### Using Git Submodule

If your project is managed in a git repository you can include MSAL as a git submodule. First check the GitHub Releases Page for the latest release tag. Replace <latest_release_tag> with that version.

* `git submodule add https://github.com/AzureAD/microsoft-authentication-library-for-objc msal`
* `cd msal`
* `git checkout tags/<latest_release_tag>`
* `cd ..`
* `git add msal`
* `git commit -m "Use ADAL git submodule at <latest_release_tag>"`
* `git push`

## Community Help and Support

We use [Stack Overflow](http://stackoverflow.com/questions/tagged/msal) with the community to provide support. We highly recommend you ask your questions on Stack Overflow first and browse existing issues to see if someone has asked your question before. 

If you find and bug or have a feature request, please raise the issue on [GitHub Issues](../../issues). 

To provide a recommendation, visit our [User Voice page](https://feedback.azure.com/forums/169401-azure-active-directory).

## Contribute

We enthusiastically welcome contributions and feedback. You can clone the repo and start contributing now. Read our [Contribution Guide](Contributing.md) for more information.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Security Library

This library controls how users sign-in and access services. We recommend you always take the latest version of our library in your app when possible. We use [semantic versioning](http://semver.org) so you can control the risk associated with updating your app. As an example, always downloading the latest minor version number (e.g. x.*y*.x) ensures you get the latest security and feature enhanements but our API surface remains the same. You can always see the latest version and release notes under the Releases tab of GitHub.

### Security Reporting

If you find a security issue with our libraries or services please report it to [secure@microsoft.com](mailto:secure@microsoft.com) with as much detail as possible. Your submission may be eligible for a bounty through the [Microsoft Bounty](http://aka.ms/bugbounty) program. Please do not post security issues to GitHub Issues or any other public site. We will contact you shortly upon receiving the information. We encourage you to get notifications of when security incidents occur by visiting [this page](https://technet.microsoft.com/en-us/security/dd252948) and subscribing to Security Advisory Alerts.



Copyright (c) Microsoft Corporation.  All rights reserved. Licensed under the MIT License (the "License");
