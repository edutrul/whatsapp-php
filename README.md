# OpenAPIClient-php

The SDK allows you to receive and send messages through your WhatsApp account. [Sign up now](https://app.chat-api.com/)  The Chat API is based on the WhatsApp WEB protocol and excludes the ban both when using libraries from mgp25 and the like. Despite this, your account can be banned by anti-spam system WhatsApp after several clicking the \"block\" button.

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: instanceId
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('instanceId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('instanceId', 'Bearer');

// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\Class1InstanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->expiry();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling Class1InstanceApi->expiry: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.chat-api.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Class1InstanceApi* | [**expiry**](docs/Api/Class1InstanceApi.md#expiry) | **POST** /expiry | Updates the QR code after its expired
*Class1InstanceApi* | [**getQRCode**](docs/Api/Class1InstanceApi.md#getqrcode) | **GET** /qr_code | Direct link to QR-code in the form of an image, not base64.
*Class1InstanceApi* | [**getSettings**](docs/Api/Class1InstanceApi.md#getsettings) | **GET** /settings | Get settings
*Class1InstanceApi* | [**getStatus**](docs/Api/Class1InstanceApi.md#getstatus) | **GET** /status | Get the account status and QR code for authorization.
*Class1InstanceApi* | [**logout**](docs/Api/Class1InstanceApi.md#logout) | **POST** /logout | Logout from WhatsApp Web to get new QR code.
*Class1InstanceApi* | [**reboot**](docs/Api/Class1InstanceApi.md#reboot) | **POST** /reboot | Reboot your whatsapp instance.
*Class1InstanceApi* | [**retry**](docs/Api/Class1InstanceApi.md#retry) | **POST** /retry | Repeat the manual synchronization attempt with the device
*Class1InstanceApi* | [**setSettings**](docs/Api/Class1InstanceApi.md#setsettings) | **POST** /settings | Set settings
*Class1InstanceApi* | [**takeover**](docs/Api/Class1InstanceApi.md#takeover) | **POST** /takeover | Returns the active session if the device has connected another instance of Web WhatsApp
*Class2MessagesApi* | [**forwardMessage**](docs/Api/Class2MessagesApi.md#forwardmessage) | **POST** /forwardMessage | Forwarding messages to a new or existing chat.
*Class2MessagesApi* | [**getMessages**](docs/Api/Class2MessagesApi.md#getmessages) | **GET** /messages | Get a list of messages.
*Class2MessagesApi* | [**sendContact**](docs/Api/Class2MessagesApi.md#sendcontact) | **POST** /sendContact | Sending a contact or contact list to a new or existing chat.
*Class2MessagesApi* | [**sendFile**](docs/Api/Class2MessagesApi.md#sendfile) | **POST** /sendFile | Send a file to a new or existing chat.
*Class2MessagesApi* | [**sendLink**](docs/Api/Class2MessagesApi.md#sendlink) | **POST** /sendLink | Send text with link and link&#39;s preview to a new or existing chat.
*Class2MessagesApi* | [**sendLocation**](docs/Api/Class2MessagesApi.md#sendlocation) | **POST** /sendLocation | Sending a location to a new or existing chat.
*Class2MessagesApi* | [**sendMessage**](docs/Api/Class2MessagesApi.md#sendmessage) | **POST** /sendMessage | Send a message to a new or existing chat.
*Class2MessagesApi* | [**sendPTT**](docs/Api/Class2MessagesApi.md#sendptt) | **POST** /sendPTT | Send a ptt-audio to a new or existing chat.
*Class2MessagesApi* | [**sendVCard**](docs/Api/Class2MessagesApi.md#sendvcard) | **POST** /sendVCard | Sending a vcard to a new or existing chat.
*Class3ChatsApi* | [**addGroupParticipant**](docs/Api/Class3ChatsApi.md#addgroupparticipant) | **POST** /addGroupParticipant | Adding participant to a group
*Class3ChatsApi* | [**demoteGroupParticipant**](docs/Api/Class3ChatsApi.md#demotegroupparticipant) | **POST** /demoteGroupParticipant | Demote group participant
*Class3ChatsApi* | [**getChats**](docs/Api/Class3ChatsApi.md#getchats) | **GET** /dialogs | Get the chat list.
*Class3ChatsApi* | [**group**](docs/Api/Class3ChatsApi.md#group) | **POST** /group | Creates a group and sends the message to the created group.
*Class3ChatsApi* | [**promoteGroupParticipant**](docs/Api/Class3ChatsApi.md#promotegroupparticipant) | **POST** /promoteGroupParticipant | Make participant in the group an administrator
*Class3ChatsApi* | [**readChat**](docs/Api/Class3ChatsApi.md#readchat) | **POST** /readChat | Open chat for reading messages
*Class3ChatsApi* | [**removeGroupParticipant**](docs/Api/Class3ChatsApi.md#removegroupparticipant) | **POST** /removeGroupParticipant | Remove participant from a group
*Class4WebhooksApi* | [**setWebhook**](docs/Api/Class4WebhooksApi.md#setwebhook) | **POST** /webhook | Sets the URL for receiving webhook
*Class5QueuesApi* | [**clearActionsQueue**](docs/Api/Class5QueuesApi.md#clearactionsqueue) | **POST** /clearActionsQueue | Clear outbound actions queue.
*Class5QueuesApi* | [**clearMessagesQueue**](docs/Api/Class5QueuesApi.md#clearmessagesqueue) | **POST** /clearMessagesQueue | Clear outbound messages queue.
*Class5QueuesApi* | [**showActionsQueue**](docs/Api/Class5QueuesApi.md#showactionsqueue) | **GET** /showActionsQueue | Get outbound messages queue.
*Class5QueuesApi* | [**showMessagesQueue**](docs/Api/Class5QueuesApi.md#showmessagesqueue) | **GET** /showMessagesQueue | Get outbound messages queue.
*Class6BanApi* | [**banTest**](docs/Api/Class6BanApi.md#bantest) | **POST** /banTest | Test ban settings
*Class6BanApi* | [**getBanSettings**](docs/Api/Class6BanApi.md#getbansettings) | **GET** /banSettings | Get settings
*Class6BanApi* | [**setBanSettings**](docs/Api/Class6BanApi.md#setbansettings) | **POST** /banSettings | Set settings
*Class7TestingApi* | [**instanceStatuses**](docs/Api/Class7TestingApi.md#instancestatuses) | **GET** /instanceStatuses | Returns instance status changes history.
*Class7TestingApi* | [**webhookStatuses**](docs/Api/Class7TestingApi.md#webhookstatuses) | **GET** /webhookStatus | Returns webhook status for message.


## Documentation For Models

 - [Ack](docs/Model/Ack.md)
 - [BanSettings](docs/Model/BanSettings.md)
 - [BanTestAction](docs/Model/BanTestAction.md)
 - [BanTestStatus](docs/Model/BanTestStatus.md)
 - [Chat](docs/Model/Chat.md)
 - [ChatIdProp](docs/Model/ChatIdProp.md)
 - [ChatUpdate](docs/Model/ChatUpdate.md)
 - [Chats](docs/Model/Chats.md)
 - [ClearActionsQueueStatus](docs/Model/ClearActionsQueueStatus.md)
 - [ClearMessagesQueueStatus](docs/Model/ClearMessagesQueueStatus.md)
 - [CreateGroupAction](docs/Model/CreateGroupAction.md)
 - [CreateGroupStatus](docs/Model/CreateGroupStatus.md)
 - [ForwardMessageRequest](docs/Model/ForwardMessageRequest.md)
 - [GroupParticipantAction](docs/Model/GroupParticipantAction.md)
 - [GroupParticipantStatus](docs/Model/GroupParticipantStatus.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse2002](docs/Model/InlineResponse2002.md)
 - [InlineResponse2003](docs/Model/InlineResponse2003.md)
 - [InlineResponse2004](docs/Model/InlineResponse2004.md)
 - [InlineResponse2005](docs/Model/InlineResponse2005.md)
 - [InlineResponse2005Update](docs/Model/InlineResponse2005Update.md)
 - [InlineResponse401](docs/Model/InlineResponse401.md)
 - [InstanceStatus](docs/Model/InstanceStatus.md)
 - [InstanceStatusAction](docs/Model/InstanceStatusAction.md)
 - [InstanceStatusLink](docs/Model/InstanceStatusLink.md)
 - [InstanceStatusStatusData](docs/Model/InstanceStatusStatusData.md)
 - [InstanceStatusStatusDataActions](docs/Model/InstanceStatusStatusDataActions.md)
 - [Message](docs/Model/Message.md)
 - [Messages](docs/Model/Messages.md)
 - [OutboundAction](docs/Model/OutboundAction.md)
 - [OutboundActions](docs/Model/OutboundActions.md)
 - [OutboundMessage](docs/Model/OutboundMessage.md)
 - [OutboundMessages](docs/Model/OutboundMessages.md)
 - [PhoneProp](docs/Model/PhoneProp.md)
 - [ReadChatAction](docs/Model/ReadChatAction.md)
 - [ReadChatStatus](docs/Model/ReadChatStatus.md)
 - [SendContactRequest](docs/Model/SendContactRequest.md)
 - [SendFileRequest](docs/Model/SendFileRequest.md)
 - [SendLinkRequest](docs/Model/SendLinkRequest.md)
 - [SendLocationRequest](docs/Model/SendLocationRequest.md)
 - [SendMessageRequest](docs/Model/SendMessageRequest.md)
 - [SendMessageStatus](docs/Model/SendMessageStatus.md)
 - [SendPTTRequest](docs/Model/SendPTTRequest.md)
 - [SendVCardRequest](docs/Model/SendVCardRequest.md)
 - [SetWebhookStatus](docs/Model/SetWebhookStatus.md)
 - [Settings](docs/Model/Settings.md)
 - [Status](docs/Model/Status.md)
 - [Statuses](docs/Model/Statuses.md)
 - [WebhookStatus](docs/Model/WebhookStatus.md)
 - [WebhookUrl](docs/Model/WebhookUrl.md)


## Documentation For Authorization



## instanceId


- **Type**: API key
- **API key parameter name**: instanceId
- **Location**: URL query string




## token


- **Type**: API key
- **API key parameter name**: token
- **Location**: URL query string



## Author

sale@chat-api.com

