# Example of using PaynetEasyReader library to integrate Miura or Spire mPOS

[![Build Status](https://travis-ci.org/payneteasy/ReaderExampleSwift.svg?branch=master)](https://travis-ci.org/payneteasy/ReaderExampleSwift)

## How to build this project

#### Set up the project dependencies

```
pod install
```

#### Open workspace

open ReaderExampleSwift.xcworkspace

## How to integrate the SDK to your swift project

* Create `Podfile` and add *PaynetEasyReader* podspec to it
* Run `pod install`
* Run `open your-project.xcworkspace`
* Add *Bridging-Header.h* file to your project

```obj-c
#ifndef Bridging_Header_h
#define Bridging_Header_h


#import <PaynetEasyReader/PNEReaderFactory.h>
#import <PaynetEasyReader/PNEReaderInfo.h>
#import <PaynetEasyReader/PNEReaderManager.h>
#import <PaynetEasyReader/PNEReaderPresenter.h>
#import <PaynetEasyReader/PNEProcessingEvent.h>
#import <PaynetEasyReader/PNEProcessingContinuation.h>
#import <PaynetEasyReader/PNECard.h>
#import <PaynetEasyReader/PNECardError.h>
#import <PaynetEasyReader/PNEReaderEvent.h>
#import <PaynetEasyReader/PNEConfigurationContinuation.h>
#import <PaynetEasyReader/PNEConfigurationContinuationBuilder.h>

#endif /* Bridging_Header_h */
```

* Drug the *Bridging-Header.h* file to *Build Settings / Objective-C Bridging Header*
* Add to your *-Info.plist
```xml
<key>UISupportedExternalAccessoryProtocols</key>
<array>
  <string>com.miura.shuttle</string>
  <string>com.thyron</string>
</array>
```
  


