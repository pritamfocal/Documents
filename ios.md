## Integration

> **Note**: 
-  Focalx.ai supports os versions from iOS 10 and above!
- You can install the Focalx.ai iOS SDK manually.



### Via Manual

1. Follow the below link to download
- [Download (For Swift 5.2 or above)](http://focalx.ai)

2. Unzip the file and drag the `FocalxAi.xcframework` directory to the “Frameworks” in your XCode project tree.
3. In your Xcode project, select your application project in the Project Navigator (blue project icon) to navigate to the target configuration window and select the application target under the `Targets` heading in the sidebar.
4. In the tab bar at the top of that window, open the `General` panel.
5. Click on the + button under the `Frameworks, Library and Embedded Content` section.
6. You will see `FocalxAi.xcframework` nested inside a `Frameworks`.
7. Select the `FocalxAi.xcframework` and click `Add` and make sure to select `Embed and Sign` option.
8. In your app where every you want to present damage detectiopn model, include:

-  For Objective-C
    
            @import FocalxAi;

-  For Swift

            import FocalxAi


9. Before showing FocalX.ai damage Guide, please create a token and supply it to 


-   Please check the API documentation to create Token to supply to our SDK


-   For Objective-C

             
        [FocalxAi showDamageGuide:self token:@"Token you get from API call from your backend"];
    -   **Note**

         self here is the current controller  from where you want to  present DamageGuide


-  For Swift

            FocalxAi.showDamageGuide(caller:self,token:"Token you get from API call from your backend")
            
    -   **Note**

   
          self here is the current controller  from where you want to present DamageGuide

And that's it!


## What is NSAllowsArbitraryLoads?

A Boolean value used to disable App Transport Security for any domains not listed in the NSExceptionDomains dictionary. Listed domains use the settings specified for that domain. The default value of NO requires the default App Transport Security behavior for all connections.



