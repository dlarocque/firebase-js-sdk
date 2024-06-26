Project: /docs/reference/js/_project.yaml
Book: /docs/reference/_book.yaml
page_type: reference

{% comment %}
DO NOT EDIT THIS FILE!
This is generated by the JS SDK team, and any local changes will be
overwritten. Changes should be made in the source code at
https://github.com/firebase/firebase-js-sdk
{% endcomment %}

# @firebase/messaging/sw

## Functions

|  Function | Description |
|  --- | --- |
|  <b>function(app, ...)</b> |
|  [getMessaging(app)](./messaging_sw.md#getmessaging_cf608e1) | Retrieves a Firebase Cloud Messaging instance. |
|  <b>function(messaging, ...)</b> |
|  [experimentalSetDeliveryMetricsExportedToBigQueryEnabled(messaging, enable)](./messaging_sw.md#experimentalsetdeliverymetricsexportedtobigqueryenabled_f3e53bd) | Enables or disables Firebase Cloud Messaging message delivery metrics export to BigQuery. By default, message delivery metrics are not exported to BigQuery. Use this method to enable or disable the export at runtime. |
|  [onBackgroundMessage(messaging, nextOrObserver)](./messaging_sw.md#onbackgroundmessage_b9887da) | Called when a message is received while the app is in the background. An app is considered to be in the background if no active window is displayed. |
|  <b>function()</b> |
|  [isSupported()](./messaging_sw.md#issupported) | Checks whether all required APIs exist within SW Context |

## Interfaces

|  Interface | Description |
|  --- | --- |
|  [FcmOptions](./messaging_sw.fcmoptions.md#fcmoptions_interface) | Options for features provided by the FCM SDK for Web. See [WebpushFcmOptions](https://firebase.google.com/docs/reference/fcm/rest/v1/projects.messages#webpushfcmoptions)<!-- -->. |
|  [GetTokenOptions](./messaging_sw.gettokenoptions.md#gettokenoptions_interface) | Options for [getToken()](./messaging_.md#gettoken_b538f38)<!-- -->. |
|  [MessagePayload](./messaging_sw.messagepayload.md#messagepayload_interface) | Message payload that contains the notification payload that is represented with [NotificationPayload](./messaging_.notificationpayload.md#notificationpayload_interface) and the data payload that contains an arbitrary number of key-value pairs sent by developers through the [Send API](https://firebase.google.com/docs/reference/fcm/rest/v1/projects.messages#notification)<!-- -->. |
|  [Messaging](./messaging_sw.messaging.md#messaging_interface) | Public interface of the Firebase Cloud Messaging SDK. |
|  [NotificationPayload](./messaging_sw.notificationpayload.md#notificationpayload_interface) | Display notification details. Details are sent through the [Send API](https://firebase.google.com/docs/reference/fcm/rest/v1/projects.messages#notification)<!-- -->. |

## function(app, ...)

### getMessaging(app) {:#getmessaging_cf608e1}

Retrieves a Firebase Cloud Messaging instance.

<b>Signature:</b>

```typescript
export declare function getMessagingInSw(app?: FirebaseApp): Messaging;
```

#### Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  app | [FirebaseApp](./app.firebaseapp.md#firebaseapp_interface) |  |

<b>Returns:</b>

[Messaging](./messaging_.messaging.md#messaging_interface)

The Firebase Cloud Messaging instance associated with the provided firebase app.

## function(messaging, ...)

### experimentalSetDeliveryMetricsExportedToBigQueryEnabled(messaging, enable) {:#experimentalsetdeliverymetricsexportedtobigqueryenabled_f3e53bd}

Enables or disables Firebase Cloud Messaging message delivery metrics export to BigQuery. By default, message delivery metrics are not exported to BigQuery. Use this method to enable or disable the export at runtime.

<b>Signature:</b>

```typescript
export declare function experimentalSetDeliveryMetricsExportedToBigQueryEnabled(messaging: Messaging, enable: boolean): void;
```

#### Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  messaging | [Messaging](./messaging_.messaging.md#messaging_interface) | The <code>FirebaseMessaging</code> instance. |
|  enable | boolean | Whether Firebase Cloud Messaging should export message delivery metrics to BigQuery. |

<b>Returns:</b>

void

### onBackgroundMessage(messaging, nextOrObserver) {:#onbackgroundmessage_b9887da}

Called when a message is received while the app is in the background. An app is considered to be in the background if no active window is displayed.

<b>Signature:</b>

```typescript
export declare function onBackgroundMessage(messaging: Messaging, nextOrObserver: NextFn<MessagePayload> | Observer<MessagePayload>): Unsubscribe;
```

#### Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  messaging | [Messaging](./messaging_.messaging.md#messaging_interface) | The [Messaging](./messaging_.messaging.md#messaging_interface) instance. |
|  nextOrObserver | [NextFn](./util.md#nextfn)<!-- -->&lt;[MessagePayload](./messaging_.messagepayload.md#messagepayload_interface)<!-- -->&gt; \| [Observer](./util.observer.md#observer_interface)<!-- -->&lt;[MessagePayload](./messaging_.messagepayload.md#messagepayload_interface)<!-- -->&gt; | This function, or observer object with <code>next</code> defined, is called when a message is received and the app is currently in the background. |

<b>Returns:</b>

[Unsubscribe](./util.md#unsubscribe)

To stop listening for messages execute this returned function

## function()

### isSupported() {:#issupported}

Checks whether all required APIs exist within SW Context

<b>Signature:</b>

```typescript
export declare function isSwSupported(): Promise<boolean>;
```
<b>Returns:</b>

Promise&lt;boolean&gt;

a Promise that resolves to a boolean.

