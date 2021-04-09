---
title: Proxy de service et sessions
description: Le proxy de service a des comportements spéciaux pour les liaisons de canal de session et non basées sur une session.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Services Web proxy de service et sessions pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032111"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="83305-106">Proxy de service et sessions</span><span class="sxs-lookup"><span data-stu-id="83305-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="83305-107">Le [proxy de service](service-proxy.md) a des comportements spéciaux pour les liaisons de canal de session et non basées sur une session.</span><span class="sxs-lookup"><span data-stu-id="83305-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="83305-108">Le proxy de service fournit une sémantique basée sur une session si la liaison de canal sous-jacente est basée sur une session.</span><span class="sxs-lookup"><span data-stu-id="83305-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="83305-109">Dans ce cas, un canal unique est utilisé pour traiter les appels.</span><span class="sxs-lookup"><span data-stu-id="83305-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="83305-110">Toutefois, si la liaison de canal n’est pas basée sur une session, le proxy de service crée un canal distinct pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="83305-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="83305-111">Notez, cependant, que les canaux non basés sur une session sont regroupés et peuvent être réutilisés.</span><span class="sxs-lookup"><span data-stu-id="83305-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="83305-112">Dans la réutilisation d’un canal, le proxy de service maintient le canal ouvert si le canal sous-jacent n’a pas généré d’erreur ou si l’appel sur un canal a entraîné une erreur du proxy de service.</span><span class="sxs-lookup"><span data-stu-id="83305-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="83305-113">Notez que.</span><span class="sxs-lookup"><span data-stu-id="83305-113">Note that.</span></span> <span data-ttu-id="83305-114">sauf en cas d’erreur, une fois qu’un canal est ouvert, il est maintenu ouvert tant que le proxy de service est ouvert et qu’il est fermé uniquement lorsque le proxy de service est fermé.</span><span class="sxs-lookup"><span data-stu-id="83305-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="83305-115">Si la liaison de canal est basée sur une session et si le canal sous-jacent est défaillant, l’ordinateur d’État du proxy de service passera à l’état d’erreur de l' [**\_ État du \_ proxy \_ \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="83305-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="83305-116">Dans le cas d’une liaison de canal non basée sur une session, une erreur dans le canal sous-jacent n’entraîne pas la transition du proxy vers l’état d’erreur de l' **\_ État du \_ proxy \_ \_ WS service** .</span><span class="sxs-lookup"><span data-stu-id="83305-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="83305-117">Pour plus d’informations sur le proxy de service et sa relation avec l’État, consultez la rubrique [service proxy](service-proxy.md) .</span><span class="sxs-lookup"><span data-stu-id="83305-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="83305-118">Pour obtenir des exemples de liaisons de canal différentes, consultez les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="83305-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="83305-119">liaison de canal non-session, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="83305-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="83305-120">liaison de canal basée sur une session, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="83305-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




