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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="1e9b1-104">Utilisation de la journalisation WinHTTP pour vérifier la récupération du trafic</span><span class="sxs-lookup"><span data-stu-id="1e9b1-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="1e9b1-105">Si l’hôte et le client génériques réussissent, mais que l’hôte et le client réels échouent, il est possible que la demande de métadonnées ne soit pas lancée.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="1e9b1-106">La journalisation [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) peut être utilisée pour vérifier que les messages sortants sont générés et envoyés correctement.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="1e9b1-107">Les applications clientes basées sur WSDAPI utilisent [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) pour se connecter aux appareils.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="1e9b1-108">Les hôtes d’appareils WSDAPI n’utilisent pas WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="1e9b1-109">En outre, certains proxys tiers n’utilisent pas WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="1e9b1-110">Lors du dépannage d’un hôte ou d’un proxy qui n’utilise pas WinHTTP, ignorez cette procédure de diagnostic et poursuivez la résolution des problèmes en suivant les procédures décrites dans [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="1e9b1-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="1e9b1-111">La journalisation [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) n’affiche pas tout le trafic au niveau du protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="1e9b1-112">Passez à l' [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md) si le trafic en dehors du trafic http revêt un intérêt.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="1e9b1-113">**Pour utiliser la journalisation WinHTTP pour vérifier la récupération du trafic**</span><span class="sxs-lookup"><span data-stu-id="1e9b1-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="1e9b1-114">Capturer les journaux WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="1e9b1-115">Lancez le Bloc-notes ou un autre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="1e9b1-116">L’éditeur de texte doit être exécuté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="1e9b1-117">Ouvrez le fichier journal WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="1e9b1-118">Vérifiez que les messages de métadonnées et de requêtes HTTP requis ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="1e9b1-119">Si un message d' [extraction](get--metadata-exchange--http-request-and-message.md) pour l’ordinateur hôte est trouvé dans les journaux WinHTTP, les demandes de métadonnées sont envoyées correctement à WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="1e9b1-120">Poursuivez la résolution des problèmes en suivant les procédures décrites dans [inspection des suivis réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="1e9b1-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="1e9b1-121">Si un message d' [extraction](get--metadata-exchange--http-request-and-message.md) est introuvable pour l’hôte dans les journaux WinHTTP, la demande de métadonnées n’est pas initiée.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="1e9b1-122">Cela peut se produire lorsque l’hôte publie des XAddrs non valides.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="1e9b1-123">Vérifiez que XAddrs sur l’hôte est conforme aux [règles de validation XAddr](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1e9b1-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="1e9b1-124">Vérification de l’envoi des requêtes HTTP et des messages de métadonnées requis</span><span class="sxs-lookup"><span data-stu-id="1e9b1-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="1e9b1-125">Les événements suivants doivent se produire pour réussir l’échange de métadonnées :</span><span class="sxs-lookup"><span data-stu-id="1e9b1-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="1e9b1-126">Le client WSDAPI génère une requête HTTP sortante.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="1e9b1-127">Cette demande est envoyée à l’hôte WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="1e9b1-128">Le client envoie un message d' [extraction](get--metadata-exchange--http-request-and-message.md) à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="1e9b1-129">Ces événements sont capturés dans les journaux WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="1e9b1-130">L’extrait de code de fichier journal WinHTTP suivant montre une demande HTTP sortante générée par un client WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

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

<span data-ttu-id="1e9b1-131">L’extrait de code de fichier journal WinHTTP suivant montre un message d' [extraction](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9b1-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="1e9b1-132">Ce message doit suivre immédiatement la requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-132">This message should immediately follow the HTTP request.</span></span>

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

<span data-ttu-id="1e9b1-133">L’élément **action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifie le message en tant que message d' [extraction](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9b1-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="1e9b1-134">Vérifiez que la valeur de l’élément **à** (par exemple, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) correspond à l’ID d’appareil publié par l’hôte dans les messages d' WS-Discovery UDP d’origine.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="1e9b1-135">L’ID d’appareil publié par l’hôte peut être vérifié à l’aide de l’hôte de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="1e9b1-136">Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="1e9b1-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="1e9b1-137">En outre, la réponse de l’hôte à la demande de métadonnées se trouve dans les journaux WinHTTP du client.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="1e9b1-138">L’hôte génère un message [GetResponse](getresponse--metadata-exchange--message.md) en réponse au message d' [extraction](get--metadata-exchange--http-request-and-message.md) du client.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="1e9b1-139">L’extrait de code de fichier journal WinHTTP suivant montre un message [GetResponse](getresponse--metadata-exchange--message.md) entrant reçu par un client wsdapi.</span><span class="sxs-lookup"><span data-stu-id="1e9b1-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

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

<span data-ttu-id="1e9b1-140">L’élément **action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifie le message en tant que message [GetResponse](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9b1-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="1e9b1-141">Vérifiez que la valeur de l’élément **latesto** du message GetResponse correspond à la valeur de l’élément **MessageID** du message d' [extraction](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9b1-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="1e9b1-142">Dans cet exemple, la valeur de l’élément **latesto** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) correspond à la valeur de l’élément **MessageID** du message d’extraction ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="1e9b1-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e9b1-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e9b1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9b1-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1e9b1-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="1e9b1-145">Capture des journaux WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1e9b1-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="1e9b1-146">Procédures de diagnostic WSDAPI</span><span class="sxs-lookup"><span data-stu-id="1e9b1-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="1e9b1-147">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="1e9b1-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
