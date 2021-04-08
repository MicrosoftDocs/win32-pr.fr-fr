---
title: Durée de vie du contexte de l’opération et Threading
description: La durée de vie du contexte d’opération, représentée par \_ un \_ handle de contexte de l’opération WS, détermine la durée de vie des propriétés qu’il contient.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Durée de vie du contexte de l’opération et services Web de Threading pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734877"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="cef6e-106">Durée de vie du contexte de l’opération et Threading</span><span class="sxs-lookup"><span data-stu-id="cef6e-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="cef6e-107">La durée de vie du contexte d’opération, représentée par un handle de [ \_ \_ contexte de l’opération WS](ws-operation-context.md) , détermine la durée de vie des propriétés qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="cef6e-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="cef6e-108">Par conséquent, un contexte ne doit être utilisé qu’au cours de la durée de vie de l' [opération de service](service-operation.md) ou du rappel auquel son fourni.</span><span class="sxs-lookup"><span data-stu-id="cef6e-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="cef6e-109">La durée de vie d’un appel synchrone est l’exécution de la fonction elle-même.</span><span class="sxs-lookup"><span data-stu-id="cef6e-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="cef6e-110">Pour un appel asynchrone, la durée de vie se termine une fois l’appel asynchrone terminé.</span><span class="sxs-lookup"><span data-stu-id="cef6e-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="cef6e-111">Le modèle de service ne fournit aucune garantie sur le contexte une fois l’appel terminé.</span><span class="sxs-lookup"><span data-stu-id="cef6e-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="cef6e-112">Le comportement de la confiance sur le contexte de l’opération ou sur l’une de ses propriétés au-delà de sa durée de vie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cef6e-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="cef6e-113">Voir aussi la calculatrice basée sur la session exemple, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="cef6e-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="cef6e-114">Modèle de thread</span><span class="sxs-lookup"><span data-stu-id="cef6e-114">Threading Model</span></span>

<span data-ttu-id="cef6e-115">Le contexte d’opération prend en charge le Threading libre, mais cela est vrai pour le contexte d’opération lui-même et ne s’applique à aucune des propriétés qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="cef6e-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="cef6e-116">Lorsque vous inscrivez un rappel d’annulation pour une opération de service à l’aide de la fonction [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , Notez que la première inscription réussira. Toutefois, la définition du rappel d’annulation à plusieurs moments échoue.</span><span class="sxs-lookup"><span data-stu-id="cef6e-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




