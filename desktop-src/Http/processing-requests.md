---
title: Traitement des requêtes
description: Le traitement des demandes comprend quatre étapes.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869346"
---
# <a name="processing-requests"></a><span data-ttu-id="2320f-103">Traitement des requêtes</span><span class="sxs-lookup"><span data-stu-id="2320f-103">Processing Requests</span></span>

<span data-ttu-id="2320f-104">Le traitement des demandes comprend quatre étapes :</span><span class="sxs-lookup"><span data-stu-id="2320f-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="2320f-105">Réception d’une demande</span><span class="sxs-lookup"><span data-stu-id="2320f-105">Receiving a request</span></span>
-   <span data-ttu-id="2320f-106">Gestion de la demande</span><span class="sxs-lookup"><span data-stu-id="2320f-106">Handling the request</span></span>
-   <span data-ttu-id="2320f-107">Envoi de la réponse</span><span class="sxs-lookup"><span data-stu-id="2320f-107">Sending the response</span></span>
-   <span data-ttu-id="2320f-108">Annulation des demandes qui ne peuvent pas être traitées</span><span class="sxs-lookup"><span data-stu-id="2320f-108">Canceling requests that cannot be processed</span></span>

![Diagramme qui affiche la boucle de demande de processus.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="2320f-110">Réception d’une demande</span><span class="sxs-lookup"><span data-stu-id="2320f-110">Receiving a Request</span></span>

<span data-ttu-id="2320f-111">L’API du serveur HTTP fournit une structure de demande pour stocker la demande entrante analysée.</span><span class="sxs-lookup"><span data-stu-id="2320f-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="2320f-112">Cette structure est allouée par l’application et initialisée lors de la réception d’une demande entrante.</span><span class="sxs-lookup"><span data-stu-id="2320f-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="2320f-113">L’application appelle la fonction [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) pour recevoir la demande.</span><span class="sxs-lookup"><span data-stu-id="2320f-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="2320f-114">Si le tampon de demande est trop petit pour recevoir la demande, l’application peut augmenter la taille de la mémoire tampon et appeler à nouveau **HttpReceiveHttpRequest** pour recevoir la demande entière.</span><span class="sxs-lookup"><span data-stu-id="2320f-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="2320f-115">Si la demande comprend des données de corps d’entité à recevoir, les applications appellent [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) avec l’ID de demande retourné dans le paramètre *pRequestBuffer* pendant l’appel à [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span><span class="sxs-lookup"><span data-stu-id="2320f-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="2320f-116">Gestion de la demande</span><span class="sxs-lookup"><span data-stu-id="2320f-116">Handling the Request</span></span>

<span data-ttu-id="2320f-117">L’application effectue le traitement propre à l’application de la demande et formule une réponse.</span><span class="sxs-lookup"><span data-stu-id="2320f-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="2320f-118">L’API du serveur HTTP n’impose aucun délai d’attente sur ce processus.</span><span class="sxs-lookup"><span data-stu-id="2320f-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="2320f-119">Envoi de la réponse</span><span class="sxs-lookup"><span data-stu-id="2320f-119">Sending the Response</span></span>

<span data-ttu-id="2320f-120">Lorsque l’application a terminé la gestion de la demande et en élaborant la réponse, elle appelle la fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) pour envoyer la réponse.</span><span class="sxs-lookup"><span data-stu-id="2320f-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="2320f-121">Si la réponse comprend des données de corps d’entité à envoyer, l’application appelle également [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span><span class="sxs-lookup"><span data-stu-id="2320f-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="2320f-122">Annulation des demandes</span><span class="sxs-lookup"><span data-stu-id="2320f-122">Canceling Requests</span></span>

<span data-ttu-id="2320f-123">Une fois que l’application a reçu un ID de demande de son appel à [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), elle peut annuler la demande à tout moment en appelant [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span><span class="sxs-lookup"><span data-stu-id="2320f-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




