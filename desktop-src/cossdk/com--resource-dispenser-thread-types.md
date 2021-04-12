---
description: Types de threads du distributeur de ressources COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Types de threads du distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393008"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="14b64-103">Types de threads du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="14b64-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="14b64-104">Les appels dans un distributeur de ressources COM+ peuvent provenir de l’un des types de threads suivants :</span><span class="sxs-lookup"><span data-stu-id="14b64-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="14b64-105">Thread cloisonné (STA)</span><span class="sxs-lookup"><span data-stu-id="14b64-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="14b64-106">Thread libre (MTA)</span><span class="sxs-lookup"><span data-stu-id="14b64-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="14b64-107">Thread non-COM (application ou thread de garbage collector du [Gestionnaire de distribution](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="14b64-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="14b64-108">Si un distributeur de ressources n’est pas un objet COM, il doit être en mesure de gérer les appels arrivant à partir de n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="14b64-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="14b64-109">Si un distributeur de ressources est un objet COM, l’objet COM doit être inscrit avec un modèle de thread des **deux**.</span><span class="sxs-lookup"><span data-stu-id="14b64-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="14b64-110">Cela permet aux threads STA ou MTA de créer et d’utiliser le distributeur de ressources sans basculement de thread.</span><span class="sxs-lookup"><span data-stu-id="14b64-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="14b64-111">Si un distributeur de ressources crée et utilise un autre objet COM (par exemple, un gestionnaire de ressources hors processus), le distributeur de ressources peut avoir besoin de gérer plusieurs proxies vers cet autre objet COM et de s’assurer que les appels à l’objet sont effectués à l’aide du proxy approprié pour le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="14b64-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="14b64-112">Lorsque le distributeur de ressources crée cet objet, il marshale et enregistre la référence.</span><span class="sxs-lookup"><span data-stu-id="14b64-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="14b64-113">Avant d’appeler à nouveau l’objet, il doit être démarshalé pour créer un proxy pour le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="14b64-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="14b64-114">Il peut être plus efficace de mettre en cache ces proxys par thread en conservant un mappage de l’ID de thread à un pointeur proxy.</span><span class="sxs-lookup"><span data-stu-id="14b64-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="14b64-115">Ce mappage se développe à mesure que de nouveaux threads sont utilisés dans le processus.</span><span class="sxs-lookup"><span data-stu-id="14b64-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14b64-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14b64-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b64-117">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="14b64-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



