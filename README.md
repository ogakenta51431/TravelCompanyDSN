# EchoBot

Bot Framework v4 echo bot sample.

This bot has been created using [Bot Framework](https://dev.botframework.com), it shows how to create a simple bot that accepts input from the user and echoes it back.

## Prerequisites

- [.NET Core SDK](https://dotnet.microsoft.com/download) version 3.1

  ```bash
  # determine dotnet version
  dotnet --version
  ```

# To run this bot locally
- Download the bot code from the Build blade in the Azure Portal (make sure you click "Yes" when asked "Include app settings in the downloaded zip file?").
    - If you clicked "No" you will need to copy all the Application Settings properties from your App Service to your local appsettings.json file.

## Visual Studio
- Open the .sln file with Visual Studio.
- Run the project (press `F5` key)

## .NET Core CLI
- Install the [.NET Core CLI tools](https://docs.microsoft.com/en-us/dotnet/core/tools/?tabs=netcore2x). 
- Using the command line, navigate to your project folder.
- Type `dotnet run`.

## Testing the bot using Bot Framework Emulator

[Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the latest Bot Framework Emulator from [here](https://github.com/Microsoft/BotFramework-Emulator/releases)

### Connect to the bot using Bot Framework Emulator

- Launch Bot Framework Emulator
- File -> Open Bot
- Enter a Bot URL of `http://localhost:3978/api/messages`

## Deploy the bot to Azure

To learn more about deploying a bot to Azure, see [Deploy your bot to Azure](https://aka.ms/azuredeployment) for a complete list of deployment instructions.

## Further reading

- [Bot Framework Documentation](https://docs.botframework.com)
- [Bot Basics](https://docs.microsoft.com/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0)
- [Activity processing](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-activity-processing?view=azure-bot-service-4.0)
- [Azure Bot Service Introduction](https://docs.microsoft.com/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0)
- [Azure Bot Service Documentation](https://docs.microsoft.com/azure/bot-service/?view=azure-bot-service-4.0)
- [.NET Core CLI tools](https://docs.microsoft.com/en-us/dotnet/core/tools/?tabs=netcore2x)
- [Azure CLI](https://docs.microsoft.com/cli/azure/?view=azure-cli-latest)
- [Azure Portal](https://portal.azure.com)
- [Language Understanding using LUIS](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/)
- [Channels and Bot Connector Service](https://docs.microsoft.com/en-us/azure/bot-service/bot-concepts?view=azure-bot-service-4.0)



# Bot Framework Emulator

## 事前準備

### BotFramework Emulator

1. Bot Framework Emulator（以下Emulator）をダウンロード（[https://github.com/Microsoft/BotFramework-Emulator/releases]）
2. ダウンロードしたEmulatorをインストール

### ngrok

1. ngrokをダウンロード（[https://ngrok.com/download]）
2. zipファイルを展開しPC上のどこかに置く
3. ２のパスを環境変数Pathに追加



## Emulatorの設定を変更する

1. Emulatorを起動する
2. Emulatorの画面左下の歯車マークを押下
3. テキストボックス「Path to ngrok」の横の「Browse」ボタンを押下するとファイル選択ダイアログが表示されるので、`事前準備-ngrok-2で用意したngrok.exe`を選択する
4. チェックボックス「Bypass ngrok for local addresses」にチェック
5. チェックボックス「Run ngrok when the Emulator starts up」にチェック
6. テキストボックス「localhost override」に`localhost`と入力
7. テキストボックス「Locale」に`en-US`と入力
8. User settingsのチェックボックス「Use a sign-in verification code for OAuthCards」にチェック
9. 「Save」ボタンを押下する



## Visual StudioでEchoBotを起動する

1. VisualStdioを起動する
2. EchoBot.shを開く
3. ソリューションエクスプローラーから`appsettings.json`を開く
4. `appsettings.json`に記載された`MicrosoftAppId`、`MicrosoftAppPassword`をメモる
5. 画面上部のボタン「▶IIS Express」を押下。ブラウザが立ち上がりタブ名「Core Bot Sample」が表示されるまで待つ。
6. Emulatorを起動する
7. ボタン「Open Bot」を押下する
8. テキストボックス「Bot URL」に`http://localhost:3978/api/messages`と入力
9. テキストボックス「Microsoft App ID」に４でメモした`MicrosoftAppId`を入力
10. テキストボックス「Microsoft App Password」に４でメモした`MicrosoftAppPassword`を入力
11. ボタン「Connect」を押下
12. EmulatorのLiveChatタブに`Hello and welcome`と表示されればOK。

