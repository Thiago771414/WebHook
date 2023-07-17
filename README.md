# WebHook
## Enviar mensagens para o Google Chat com webhooks de entrada
Os webhooks de entrada permitem o envio de mensagens assíncronas para o Google Chat a partir de aplicativos que não são do Chat. Por exemplo, é possível configurar um aplicativo de monitoramento para notificar a equipe de plantão no Google Chat quando um servidor ficar inativo.

```csharp
function webhook() {
  const url = "https://chat.googleapis.com/v1/spaces/AAAAGCYeSRY/messages";
  const options = {
    "method": "post",
    "headers": {
      "Content-Type": "application/json; charset=UTF-8"
    },
    "payload": JSON.stringify({
      "text": "Hello from Apps Script!"
    })
  };
  const response = UrlFetchApp.fetch(url, options);
  Logger.log(response);
}
```
##[Documentação](https://developers.google.com/chat/how-tos/webhooks?hl=pt-br#apps-script)
## WebHook
![Imagem](https://developers.google.com/static/chat/images/arch-pat-notifier.svg?hl=pt-br)

