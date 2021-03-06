# Microsoft Office 365 Connect Sample for iOS Using Microsoft Graph (Swift)

Connecting to Microsoft Office 365 is the first step every iOS app must take to start working with Office 365 services and data. This sample shows how to connect and then call one API through Microsoft Graph (previously named Office 365 unified API).

> Note: For the Objective-C version of this sample, see [O365-iOS-Microsoft-Graph-Connect](https://github.com/OfficeDev/O365-iOS-Microsoft-Graph-Connect). Also, try out the [Get started with Office 365 APIs](http://dev.office.com/getting-started/office365apis?platform=option-ios#setup) page, which simplifies registration so you can get this sample running faster.
 
## Prerequisites
* [Xcode](https://developer.apple.com/xcode/downloads/) from Apple
* Installation of [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)  as a dependency manager.
* An Office 365 account. You can sign up for [an Office 365 Developer subscription](https://portal.office.com/Signup/Signup.aspx?OfferId=6881A1CB-F4EB-4db3-9F18-388898DAF510&DL=DEVELOPERPACK&ali=1#0) that includes the resources that you need to start building Office 365 apps.

     > Note: If you already have a subscription, the previous link sends you to a page with the message *Sorry, you can’t add that to your current account*. In that case, use an account from your current Office 365 subscription.Mic
* A Microsoft Azure Tenant to register your application. Microsoft Azure Active Directory (AD) provides identity services that applications use for authentication and authorization. A trial subscription can be acquired here: [Microsoft Azure](https://account.windowsazure.com/SignUp).

     > Important: You'll also need to ensure your Azure subscription is bound to your Office 365 tenant. To do this, see the Active Directory Team's Blog post, [Creating and Managing Multiple Windows Azure Active Directories](http://blogs.technet.com/b/ad/archive/2013/11/08/creating-and-managing-multiple-windows-azure-active-directories.aspx). The **Adding a new directory** section will explain how to do this. You can also see [Set up your Office 365 development environment](https://msdn.microsoft.com/office/office365/howto/setup-development-environment#bk_CreateAzureSubscription) and the section **Associate your Office 365 account with Azure AD to create and manage apps** for more information.
      
* A Client Id and Redirect Uri values of an application registered in Azure. This sample application must be granted the **Send mail as user** permission for **Microsoft Graph**. To create the registration, see **Register your native app with the Azure Management Portal** in [Manually register your app with Azure AD so it can access Office 365 APIs](https://msdn.microsoft.com/en-us/office/office365/howto/add-common-consent-manually) and [grant proper permissions](https://github.com/OfficeDev/O365-iOS-Microsoft-Graph-Connect/wiki/Grant-permissions-to-the-Connect-application-in-Azure) in the sample wiki to apply the proper permissions to it.


       
## Running this sample in Xcode

1. Clone this repository
2. Use CocoaPods to import the Active Directory Authentication Library (ADAL) iOS dependency:
        
	     pod 'ADALiOS', '= 1.2.4'

 This sample app already contains a podfile that will get the ADAL components (pods) into  the project. Simply navigate to the project from **Terminal** and run: 
        
        pod install
        
   For more information, see **Using CocoaPods** in [Additional Resources](#AdditionalResources)
  
3. Open **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**
4. Open **AuthenticationConstants.swift**. You'll see that the **ClientID** and **RedirectUri** values can be added to the top of the file. Supply the necessary values here:

        // You will set your application's clientId and redirect URI.
    	static let ClientId = "ENTER_YOUR_CLIENT_ID"
    	static let RedirectUri = NSURL.init(string: "ENTER_YOUR_REDIRECT_URI")
    	static let Authority = "https://login.microsoftonline.com/common"
    	static let ResourceId = "https://graph.microsoft.com"
    
    > Note: If you don't have CLIENT_ID and REDIRECT_URI values, [add a native client application in Azure](https://msdn.microsoft.com/library/azure/dn132599.aspx#BKMK_Adding) and take note of the CLIENT\_ID and REDIRECT_URI.

5. Run the sample.


## Questions and comments

We'd love to get your feedback about the Office 365 iOS Microsoft Graph Connect Swift project. You can send your questions and suggestions to us in the [Issues](https://github.com/OfficeDev/O365-iOS-Microsoft-Graph-Connect-Swift/issues) section of this repository.

Questions about Office 365 development in general should be posted to [Stack Overflow](http://stackoverflow.com/questions/tagged/Office365+API). Make sure that your questions or comments are tagged with [Office365] and [MicrosoftGraph].


## Additional resources

* [Office Dev Center](http://dev.office.com/)
* [O365-iOS-Microsoft-Graph-Connect-Obj-C](https://github.com/OfficeDev/O365-iOS-Microsoft-Graph-Connect)
* [Microsoft Graph overview page](https://graph.microsoft.io)
* [Using CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)

## Copyright
Copyright (c) 2016 Microsoft. All rights reserved.

