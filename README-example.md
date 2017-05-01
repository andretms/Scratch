Microsoft Authentication Library for Apple
=====================================

The MSAL library for iOS and macOS gives your app the ability to sign in to Microsoft Azure Active Directory and Microsoft Accounts and begin using the Microsoft Cloud. This library uses industry standard protocols such as OAuth2 and OpenID Connect, provides web API integration with user level consent, and two factor authentication support among many other features.

## Example

`     if let application = try? MSALPublicClientApplication.init(clientId: kClientID, authority: kAuthority) {

        application.acquireToken(forScopes: kScopes) { (result, error) in
            if result != nil {

                    // Set up your app for the user
          } else {
                print(error?.localizedDescription)
            }
        }
    }
        
    else {
            print(Unable to create application.)
        }`

## Installation

* Using Cocoapods

You can use [CocoaPods](https://cocoapods.org) to remain up to date with MSAL within a specific major version. Include the following line in your podfile:

`pod 'MSAL'`

You then you can run either `pod install` (if it's a new PodFile) or `pod update` (if it's an existing PodFile) to get the latest version of MSAL. Subsequent calls to pod update will update to the latest released version of MSAL as well.

* Using Git Submodule

If your project is managed in a git repository you can include MSAL as a git submodule. First check the GitHub Releases Page for the latest release tag. Replace <latest_release_tag> with that version.

`git submodule add https://github.com/AzureAD/azure-activedirectory-library-for-objc msal`
`cd msal`
`git checkout tags/<latest_release_tag>`
`cd ..`
`git add msal`
`git commit -m "Use ADAL git submodule at <latest_release_tag>"`
`git push`

## Samples and Documentation

We provide a full suite of [documentation](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-developers-guide) and [sample applications](https://github.com/Azure-Samples) to help you get started with the Azure Identity system. We also provide docs for authentication flows such as OAuth2, OpenID Connect, Graph API, and other awesome features. 

## Community Help and Support

We leverage [Stack Overflow](http://stackoverflow.com/questions/tagged/msal) with the community to provide support. We highly recommend you ask your questions on Stack Overflow first and browse existing issues to see if someone has asked your question before. 

If you find and bug or have a feature request, please raise the issue on GitHub Issues for this repo.

## Contribute

We enthusiastically welcome contributions and feedback. You can clone the repo and start contributing now. Read our [Contribution Guide](Contributing.md) for more information.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

### Security Reporting

If you find a security issue with our libraries or services please report it to [secure@microsoft.com](mailto:secure@microsoft.com) with as much detail as possible. Your submission may be eligible for a bounty through the [Microsoft Bounty](http://aka.ms/bugbounty) program. Please do not post security issues to GitHub Issues or any other public site. We will contact you shortly upon receiving the information. We encourage you to get notifications of when security incidents occur by visiting [this page](https://technet.microsoft.com/en-us/security/dd252948) and subscribing to Security Advisory Alerts.


Copyright (c) Microsoft Corporation.  All rights reserved. Licensed under the MIT License (the "License");
