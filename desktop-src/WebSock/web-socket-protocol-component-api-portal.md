---
title: API du composant de protocole WebSocket
description: API du composant de protocole WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088817"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="b4da1-103">API du composant de protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="b4da1-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="b4da1-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="b4da1-104">Purpose</span></span>

<span data-ttu-id="b4da1-105">L’API du composant de protocole WebSocket active des canaux de communication bidirectionnels asynchrones sur HTTP qui fonctionnent sur les intermédiaires réseau existants.</span><span class="sxs-lookup"><span data-stu-id="b4da1-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="b4da1-106">Avec l’API du composant de protocole WebSocket, un client utilise le protocole HTTP pour communiquer avec un serveur, puis les deux côtés basculent vers à l’aide du protocole sous-jacent sur lequel HTTP a été superposé (par exemple, TCP ou SSL).</span><span class="sxs-lookup"><span data-stu-id="b4da1-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="b4da1-107">L’objectif est d’utiliser tout d’abord le protocole HTTP pour traverser les intermédiaires réseau, puis d’utiliser le canal TCP/SSL sous-jacent de bout en bout pour la communication des applications bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="b4da1-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="b4da1-108">Le protocole WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] est défini au niveau de l’IETF, tandis qu’un W3CAPI d’API JavaScript associé \[ [](https://dev.w3.org/html5/websockets/) \] est défini au W3C.</span><span class="sxs-lookup"><span data-stu-id="b4da1-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4da1-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b4da1-109">In this section</span></span>



| <span data-ttu-id="b4da1-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b4da1-110">Topic</span></span>                                                                                                          | <span data-ttu-id="b4da1-111">Description</span><span class="sxs-lookup"><span data-stu-id="b4da1-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="b4da1-112">**Types de données de l’API du composant de protocole WebSocket**</span><span class="sxs-lookup"><span data-stu-id="b4da1-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="b4da1-113">L’API du composant de protocole WebSocket définit ces types de données.</span><span class="sxs-lookup"><span data-stu-id="b4da1-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="b4da1-114">Énumérations de l’API du composant de protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="b4da1-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="b4da1-115">L’API du composant de protocole WebSocket définit ces énumérations.</span><span class="sxs-lookup"><span data-stu-id="b4da1-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="b4da1-116">Fonctions de l’API du composant de protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="b4da1-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="b4da1-117">L’API du composant de protocole WebSocket définit ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="b4da1-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="b4da1-118">Structures de l’API du composant de protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="b4da1-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="b4da1-119">L’API du composant de protocole WebSocket définit ces structures.</span><span class="sxs-lookup"><span data-stu-id="b4da1-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="b4da1-120">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="b4da1-120">Developer audience</span></span>

<span data-ttu-id="b4da1-121">L’API du composant de protocole WebSocket est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="b4da1-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="b4da1-122">Vous devez être familiarisé avec la mise en réseau HTTP et Windows.</span><span class="sxs-lookup"><span data-stu-id="b4da1-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="b4da1-123">La meilleure façon d’utiliser le protocole WebSocket sur Windows consiste à utiliser l' [API Windows http services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) ou l' [espace de noms Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="b4da1-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="b4da1-124">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="b4da1-124">Run-time requirements</span></span>

<span data-ttu-id="b4da1-125">L’API du composant de protocole WebSocket requiert Windows 8 et les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="b4da1-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="b4da1-126">Les API peuvent être liées de manière dynamique via websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="b4da1-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="b4da1-127">websocket.dll assure la prise en charge des en-têtes HTTP liés aux protocoles client et serveur, vérifie les données de négociation reçues et analyse le flux de données WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b4da1-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="b4da1-128">Elle ne gère pas les opérations HTTP spécifiques (redirection, authentification, prise en charge du proxy) et n’effectue aucune opération d’e/s (envoi ou réception d’octets de flux WebSocket).</span><span class="sxs-lookup"><span data-stu-id="b4da1-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b4da1-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4da1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4da1-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="b4da1-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="b4da1-131">Services HTTP Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="b4da1-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

