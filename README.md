# HttpSession

[![](https://img.shields.io/badge/Twitter-O--Liker%20Error-blue.svg)](https://twitter.com/O_Linker_Error)
[![](https://img.shields.io/badge/lang-swift4.0-ff69b4.svg)](https://developer.apple.com/jp/swift/)
[![](https://img.shields.io/badge/licence-MIT-green.svg)](https://github.com/keisukeYamagishi/HttpRequest/blob/master/LICENSE)

### Overview

TCP / IP based HTTP communication can be simplified
and Twitter OAuth

***API Server:*** http://153.126.160.55/

## Installation

### Cocoapods

[CocoaPods](https://cocoapods.org/pods/HttpSession) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```
To integrate GMSDirection into your Xcode project using CocoaPods, specify it in your `Podfile`:

```
vi ./Podfile 
```

If you do not have the google map SDK for iOS

```
target 'Target Name' do
  use_frameworks!
  pod 'HttpSession'
end
```
Then, run the following command:

```bash
$ pod setup
$ pod install
```

## Use it

***Via SSH***: For those who plan on regularly making direct commits, cloning over SSH may provide a better experience (which requires uploading SSH keys to GitHub):

```
$ git clone git@github.com:keisukeYamagishi/HttpSession.git
```
***Via https***: For those checking out sources as read-only, HTTPS works best:

```
$ git clone https://github.com/keisukeYamagishi/HttpSession.git
```

## Sample code

POST http method

```swift

HttpSession(url: "http://153.126.160.55/postApi.json",method: .post)
            .postHttp(param: ["http_post":"Http Request POST 😄"],
                      completionHandler: { (data, responce, error) in
                        
                        let responceStr = String(data: data!, encoding: .utf8)
                        print ("session: \(responceStr)")
            })

```

