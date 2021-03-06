[![License MIT](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/wangshiyu13/Lothar/blob/master/LICENSE)
[![CI Status](https://img.shields.io/badge/build-1.0.6-brightgreen.svg)](https://travis-ci.org/wangshiyu13/Lothar)
[![CocoaPods](https://img.shields.io/badge/platform-iOS-lightgrey.svg)](http://cocoapods.org/?q=Lothar)
[![Support](https://img.shields.io/badge/support-iOS%208%2B-blue.svg)](https://www.apple.com/nl/ios/)
#### 基于[CTMediator](https://github.com/casatwy/CTMediator)的组件化中间件

## 特点
相对于CTMediator，增加了一些功能

1. 增加容错处理
2. 增加短链映射处理
3. 提供基于user:password的鉴权方案

====

## 使用方法
**具体使用方法请看[我的简书](http://www.jianshu.com/p/568e875abd48)**

***AppDelegate application:didFinishLaunchingWithOptions:***

```objective-c
[Lothar setupConfig:^(LotharConfig * _Nonnull config) {
        config.URLScheme = @"lothar";
        config.URLVerifySkip = YES;
        config.URLRouteMapFilePath = [[NSBundle mainBundle] pathForResource:@"RouteMapTemplate" ofType:@"plist"];
    }];
```

***AppDelegate application:openURL:options:***

```objective-c
return [[LotharMediator performActionWithUrl:url completion:nil] boolValue];
```


## 环境要求

该库需运行在 iOS 8.0 和 Xcode 7.0以上环境.

## 集成方法

Lothar is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "Lothar"
```

## 更新日志


## 作者

wangshiyu13, wangshiyu13@163.com

## 开源协议

HLNetworking is available under the MIT license. See the LICENSE file for more info.
