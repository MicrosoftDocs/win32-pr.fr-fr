---
description: Inscription d’une ressource dans une transaction
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Inscription d’une ressource dans une transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393228"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="eab75-103">Inscription d’une ressource dans une transaction</span><span class="sxs-lookup"><span data-stu-id="eab75-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="eab75-104">Une fois qu’une ressource a été allouée, mais juste avant de retourner la ressource au distributeur de ressources, le gestionnaire de distribution vérifie avec COM+ pour déterminer si l’objet appelant s’exécute dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="eab75-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="eab75-105">Si l’objet appelant s’exécute dans une transaction, le gestionnaire du distributeur rappelle le distributeur de ressources et lui demande d’inscrire la ressource dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="eab75-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="eab75-106">La ressource est ensuite retournée au distributeur de ressources, qui le retourne à l’instance appelante.</span><span class="sxs-lookup"><span data-stu-id="eab75-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="eab75-107">Le distributeur de ressources doit pouvoir s’inscrire dans une transaction OLE avec le Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="eab75-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="eab75-108">L’inscription de la transaction est facultative lorsqu’un distributeur de ressources distribue des ressources non transactionnelles, telles que de la mémoire ou des threads.</span><span class="sxs-lookup"><span data-stu-id="eab75-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="eab75-109">Lorsqu’une transaction est terminée, COM+ notifie le gestionnaire de distribution qu’il a validé ou abandonné.</span><span class="sxs-lookup"><span data-stu-id="eab75-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="eab75-110">Ensuite, le gestionnaire de distribution avertit le détenteur de chaque distributeur de ressources que toutes les ressources inscrites dans cette transaction peuvent maintenant être déplacées vers l’inventaire général.</span><span class="sxs-lookup"><span data-stu-id="eab75-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eab75-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eab75-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eab75-112">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="eab75-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="eab75-113">États des ressources regroupées accessibles au distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="eab75-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="eab75-114">Processus d’allocation des ressources du distributeur de ressources</span><span class="sxs-lookup"><span data-stu-id="eab75-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



