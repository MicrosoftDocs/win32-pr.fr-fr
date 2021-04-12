---
description: Si l’hôte et le client génériques réussissent, mais que l’hôte et le client réels échouent, il est possible que la demande de métadonnées ne soit pas lancée. La journalisation WinHTTP peut être utilisée pour vérifier que les messages sortants sont générés et envoyés correctement.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Utilisation de la journalisation WinHTTP pour vérifier la récupération du trafic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202998"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Utilisation de la journalisation WinHTTP pour vérifier la récupération du trafic

Si l’hôte et le client génériques réussissent, mais que l’hôte et le client réels échouent, il est possible que la demande de métadonnées ne soit pas lancée. La journalisation [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) peut être utilisée pour vérifier que les messages sortants sont générés et envoyés correctement.

Les applications clientes basées sur WSDAPI utilisent [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) pour se connecter aux appareils. Les hôtes d’appareils WSDAPI n’utilisent pas WinHTTP. En outre, certains proxys tiers n’utilisent pas WinHTTP. Lors du dépannage d’un hôte ou d’un proxy qui n’utilise pas WinHTTP, ignorez cette procédure de diagnostic et poursuivez la résolution des problèmes en suivant les procédures décrites dans [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

La journalisation [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) n’affiche pas tout le trafic au niveau du protocole TCP. Passez à l' [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md) si le trafic en dehors du trafic http revêt un intérêt.

**Pour utiliser la journalisation WinHTTP pour vérifier la récupération du trafic**

1.  [Capturer les journaux WinHTTP.](capturing-winhttp-logs.md)
2.  Lancez le Bloc-notes ou un autre éditeur de texte. L’éditeur de texte doit être exécuté en tant qu’administrateur.
3.  Ouvrez le fichier journal WinHTTP.
4.  Vérifiez que les messages de métadonnées et de requêtes HTTP requis ont été envoyés.

Si un message d' [extraction](get--metadata-exchange--http-request-and-message.md) pour l’ordinateur hôte est trouvé dans les journaux WinHTTP, les demandes de métadonnées sont envoyées correctement à WinHTTP. Poursuivez la résolution des problèmes en suivant les procédures décrites dans [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Si un message d' [extraction](get--metadata-exchange--http-request-and-message.md) est introuvable pour l’hôte dans les journaux WinHTTP, la demande de métadonnées n’est pas initiée. Cela peut se produire lorsque l’hôte publie des XAddrs non valides. Vérifiez que XAddrs sur l’hôte est conforme aux [règles de validation XAddr](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Vérification de l’envoi des requêtes HTTP et des messages de métadonnées requis

Les événements suivants doivent se produire pour réussir l’échange de métadonnées :

-   Le client WSDAPI génère une requête HTTP sortante. Cette demande est envoyée à l’hôte WSDAPI.
-   Le client envoie un message d' [extraction](get--metadata-exchange--http-request-and-message.md) à l’hôte.

Ces événements sont capturés dans les journaux WinHTTP.

L’extrait de code de fichier journal WinHTTP suivant montre une demande HTTP sortante générée par un client WSDAPI.

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

L’extrait de code de fichier journal WinHTTP suivant montre un message d' [extraction](get--metadata-exchange--http-request-and-message.md) . Ce message doit suivre immédiatement la requête HTTP.

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

L’élément **action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifie le message en tant que message d' [extraction](get--metadata-exchange--http-request-and-message.md) . Vérifiez que la valeur de l’élément **à** (par exemple, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) correspond à l’ID d’appareil publié par l’hôte dans les messages d' WS-Discovery UDP d’origine. L’ID d’appareil publié par l’hôte peut être vérifié à l’aide de l’hôte de débogage WSD. Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

En outre, la réponse de l’hôte à la demande de métadonnées se trouve dans les journaux WinHTTP du client. L’hôte génère un message [GetResponse](getresponse--metadata-exchange--message.md) en réponse au message d' [extraction](get--metadata-exchange--http-request-and-message.md) du client.

L’extrait de code de fichier journal WinHTTP suivant montre un message [GetResponse](getresponse--metadata-exchange--message.md) entrant reçu par un client wsdapi.

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

L’élément **action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifie le message en tant que message [GetResponse](getresponse--metadata-exchange--message.md) . Vérifiez que la valeur de l’élément **latesto** du message GetResponse correspond à la valeur de l’élément **MessageID** du message d' [extraction](get--metadata-exchange--http-request-and-message.md) . Dans cet exemple, la valeur de l’élément **latesto** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) correspond à la valeur de l’élément **MessageID** du message d’extraction ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Capture des journaux WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
