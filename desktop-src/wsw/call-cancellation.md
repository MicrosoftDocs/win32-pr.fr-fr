---
title: Annulation d’appel
description: La notification d’annulation d’appel annule l’opération d’opérations de service côté serveur et de rappels de modèle de service.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Appeler des services Web d’annulation pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106511526"
---
# <a name="call-cancellation"></a><span data-ttu-id="d6efc-106">Annulation d’appel</span><span class="sxs-lookup"><span data-stu-id="d6efc-106">Call cancellation</span></span>

<span data-ttu-id="d6efc-107">La notification d’annulation d’appel annule l’opération d' [opérations de service côté serveur](server-side-service-operations.md) et de rappels de modèle de service.</span><span class="sxs-lookup"><span data-stu-id="d6efc-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="d6efc-108">Cette annulation peut être pour l’une des deux raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6efc-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="d6efc-109">L’hôte de service a arrêté les opérations en raison d’un appel à la fonction [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .</span><span class="sxs-lookup"><span data-stu-id="d6efc-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="d6efc-110">Le canal sous-jacent a généré une erreur.</span><span class="sxs-lookup"><span data-stu-id="d6efc-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="d6efc-111">Pour recevoir une notification d’annulation, le rappel de l’opération de service ou du modèle de service doit inscrire un rappel d' [**annulation de \_ \_ \_ rappel de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) en appelant la fonction [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .</span><span class="sxs-lookup"><span data-stu-id="d6efc-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="d6efc-112">Si vous le souhaitez, dans le cadre de la notification d’annulation, le rappel de l’opération de service ou du modèle de service peut également enregistrer les données d’État spécifiques à l’application et le rappel de rappel de l' [**\_ \_ \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .</span><span class="sxs-lookup"><span data-stu-id="d6efc-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="d6efc-113">Les données d’État sont mises à la disposition du rappel de rappel d’annulation de l' [**\_ opération \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) .</span><span class="sxs-lookup"><span data-stu-id="d6efc-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="d6efc-114">À la fin de l’appel, le rappel de rappel de l' [**\_ \_ \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) est appelé pour permettre à l’application de libérer les données d’État.</span><span class="sxs-lookup"><span data-stu-id="d6efc-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="d6efc-115">Pour obtenir un exemple de code, consultez [BlockingServiceExample](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="d6efc-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="d6efc-116">Le rappel d’annulation est appelé une seule fois pendant la durée de vie des [opérations de service côté serveur](server-side-service-operations.md) ou de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d6efc-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="d6efc-117">L’annulation d’appel est disponible dans pour tous les rappels d’hôte de service qui prennent le [ \_ \_ contexte WS Operation](ws-operation-context.md) comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="d6efc-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="d6efc-118">Les éléments d’API suivants sont liés à l’annulation d’appel.</span><span class="sxs-lookup"><span data-stu-id="d6efc-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="d6efc-119">Rappel</span><span class="sxs-lookup"><span data-stu-id="d6efc-119">Callback</span></span>                                                                         | <span data-ttu-id="d6efc-120">Description</span><span class="sxs-lookup"><span data-stu-id="d6efc-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6efc-121">**rappel d’annulation de l' \_ opération WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6efc-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="d6efc-122">Appelée par le modèle de service pour notifier l’annulation d’une opération de service asynchrone à la suite d’un arrêt abandonné de l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="d6efc-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="d6efc-123">**\_rappel de \_ l' \_ état \_ libre de l’opération WS**</span><span class="sxs-lookup"><span data-stu-id="d6efc-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="d6efc-124">Appelée par le modèle de service pour permettre à une application de nettoyer les données d’État qui ont été inscrites avec le rappel d’annulation.</span><span class="sxs-lookup"><span data-stu-id="d6efc-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="d6efc-125">Fonction</span><span class="sxs-lookup"><span data-stu-id="d6efc-125">Function</span></span>                                                             | <span data-ttu-id="d6efc-126">Description</span><span class="sxs-lookup"><span data-stu-id="d6efc-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6efc-127">**WsRegisterOperationForCancel**</span><span class="sxs-lookup"><span data-stu-id="d6efc-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="d6efc-128">Permet à une opération de service ou à un rappel de modèle de service de s’inscrire pour une notification d’annulation.</span><span class="sxs-lookup"><span data-stu-id="d6efc-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




