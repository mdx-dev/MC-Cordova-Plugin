# Salesforce Marketing Cloud Cordova Plugin

Use this plugin to implement the Marketing Cloud MobilePush SDK for your [iOS](https://salesforce-marketingcloud.github.io/MarketingCloudSDK-iOS/) and [Android](http://salesforce-marketingcloud.github.io/JB4A-SDK-Android/) applications.

## Release Notes

Release notes for the plugin can be found [here](CHANGELOG.md)

## Installation

#### 1. Add plugin to your application via [npm](https://www.npmjs.com/package/cordova-plugin-marketingcloudsdk)

```shell
cordova plugin add cordova-plugin-marketingcloudsdk
```

#### 2. Modify your application's `config.xml` to configure the plugin

```xml
<!-- Required -->
<preference name="com.salesforce.marketingcloud.app_id" value="{Marketing Cloud application id}" />
<preference name="com.salesforce.marketingcloud.access_token" value="{Marketing Cloud access token}" />

<!-- Required - Android Only -->
<platform name="android">
  <preference name="com.salesforce.marketingcloud.notification_small_icon" value="ic_notification" />
</platform>

<!-- Optional - Will soon be required -->
<preference name="com.salesforce.marketingcloud.tenant_specific_endpoint" value="{URL retrieved from Marketing Cloud adminstration page}" />

<!-- Optional -->
<preference name="com.salesforce.marketingcloud.analytics" value="{true|false}" />
```

#### 3. Provide FCM credentials

To enable push support for the Android platform you will need to include the google-services.json file.  

1. Download the file from your application's [Firebase console](https://console.firebase.google.com/) and place it in your project's root folder.  
2. Add following to Android element in your `config.xml`:

```xml
<platform name="android">
  <resource-file src="google-services.json" target="app/google-services.json" />
</platform>
```

## API Reference <a name="reference"></a>

{{#orphans~}}
{{>member-index}}
{{/orphans}}

---

{{#modules~}}
{{>header~}}
{{>body~}}
{{>members~}}

---

{{/modules}}