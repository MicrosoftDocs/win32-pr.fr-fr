---
title: Contexte (services Web Windows)
description: Un contexte est utilisé dans les opérations de service de modèle de service et les rappels pour passer les données d’État pertinentes à l’opération de service ou au rappel lorsqu’il est appelé.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Services Web de contexte pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103940583"
---
# <a name="context-windows-web-services"></a><span data-ttu-id="fe582-106">Contexte (services Web Windows)</span><span class="sxs-lookup"><span data-stu-id="fe582-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="fe582-107">Un contexte est utilisé dans les [opérations de service](service-operation.md) de modèle de service et les rappels pour passer les données d’État pertinentes à l’opération de service ou au rappel lorsqu’il est appelé.</span><span class="sxs-lookup"><span data-stu-id="fe582-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="fe582-108">Un contexte est référencé par une structure [de \_ \_ contexte d’opération WS](ws-operation-context.md) .</span><span class="sxs-lookup"><span data-stu-id="fe582-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="fe582-109">Les propriétés d’un contexte peuvent être récupérées avec la fonction [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="fe582-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="fe582-110">Toutes les propriétés de contexte ne sont pas disponibles à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="fe582-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="fe582-111">Consultez la documentation de la propriété de contexte relative à la disponibilité d’une propriété spécifique dans un rappel ou une [opération de service](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fe582-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="fe582-112">Pour plus d’informations sur la gestion de la durée de vie du contexte de l’opération et le Threading, consultez la rubrique relative à la [durée de vie du contexte de l’opération](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="fe582-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="fe582-113">L’énumération suivante fait partie du contexte :</span><span class="sxs-lookup"><span data-stu-id="fe582-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="fe582-114">**\_ID de \_ propriété de contexte \_ \_ de l’opération WS**</span><span class="sxs-lookup"><span data-stu-id="fe582-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="fe582-115">La fonction suivante fait partie du contexte :</span><span class="sxs-lookup"><span data-stu-id="fe582-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="fe582-116">**WsGetOperationContextProperty**</span><span class="sxs-lookup"><span data-stu-id="fe582-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="fe582-117">Le handle suivant fait partie du contexte :</span><span class="sxs-lookup"><span data-stu-id="fe582-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="fe582-118">contexte de l' \_ opération WS \_</span><span class="sxs-lookup"><span data-stu-id="fe582-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




