---
description: Définition du bit terminé
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Définition du bit terminé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514543"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="2611d-103">Définition du bit terminé</span><span class="sxs-lookup"><span data-stu-id="2611d-103">Setting the Done Bit</span></span>

<span data-ttu-id="2611d-104">COM+ désactivera un objet activé juste-à-temps en fonction de l’état d’une propriété de contexte, le bit terminé, comme suit :</span><span class="sxs-lookup"><span data-stu-id="2611d-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="2611d-105">Lorsque le bit Done a la valeur true, COM+ désactive l’objet lors du retour de l’appel de la méthode en cours.</span><span class="sxs-lookup"><span data-stu-id="2611d-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="2611d-106">Lorsque le bit Done est défini sur false, l’objet reste actif lorsque l’appel de la méthode en cours est retourné.</span><span class="sxs-lookup"><span data-stu-id="2611d-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="2611d-107">Par défaut, le bit Done a la valeur false lorsqu’un objet est créé et que son contexte est initialisé.</span><span class="sxs-lookup"><span data-stu-id="2611d-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="2611d-108">(Tout objet activé juste-à-temps est créé dans son propre contexte afin qu’il ait son propre bit terminé à définir.) Toutefois, vous pouvez modifier ce paramètre par défaut pour chaque méthode à l’aide de la propriété terminé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2611d-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="2611d-109">Vous pouvez définir le bit Done des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="2611d-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="2611d-110">Utilisation de [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="2611d-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="2611d-111">Utilisation de [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="2611d-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="2611d-112">Utilisation de la propriété Done automatique</span><span class="sxs-lookup"><span data-stu-id="2611d-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="2611d-113">Utilisation de IContextState</span><span class="sxs-lookup"><span data-stu-id="2611d-113">Using IContextState</span></span>

<span data-ttu-id="2611d-114">Vous pouvez utiliser [**IContextState :: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) pour définir le bit Done sur true ou false.</span><span class="sxs-lookup"><span data-stu-id="2611d-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="2611d-115">Vous pouvez utiliser [**IContextState :: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) pour récupérer l’état actuel du bit Done à partir du contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2611d-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="2611d-116">Utilisation de IObjectContext</span><span class="sxs-lookup"><span data-stu-id="2611d-116">Using IObjectContext</span></span>

<span data-ttu-id="2611d-117">Vous pouvez utiliser les méthodes suivantes sur [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) pour définir le bit terminé tout en configurant simultanément le bit cohérent utilisé pour le vote dans les transactions :</span><span class="sxs-lookup"><span data-stu-id="2611d-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="2611d-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signale que vous avez terminé et que vous votez pour valider la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="2611d-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="2611d-119">Il définit à la fois le bit Done et le bit consistent sur true.</span><span class="sxs-lookup"><span data-stu-id="2611d-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="2611d-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signale que vous avez terminé et Dooms la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="2611d-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="2611d-121">Elle définit le bit Done sur true et le bit cohérent sur false.</span><span class="sxs-lookup"><span data-stu-id="2611d-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="2611d-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signale que vous n’avez pas terminé mais que vous votez pour valider la transaction.</span><span class="sxs-lookup"><span data-stu-id="2611d-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="2611d-123">Elle définit le bit Done sur false et le bit cohérent sur true.</span><span class="sxs-lookup"><span data-stu-id="2611d-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="2611d-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signale que vous n’avez pas terminé et que vous votez pour ne pas valider la transaction à ce stade, généralement parce que l’État est incohérent.</span><span class="sxs-lookup"><span data-stu-id="2611d-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="2611d-125">Il définit à la fois le bit Done et le bit consistent sur false.</span><span class="sxs-lookup"><span data-stu-id="2611d-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2611d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2611d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2611d-127">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="2611d-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="2611d-128">Activation de l’activation JIT pour un composant</span><span class="sxs-lookup"><span data-stu-id="2611d-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="2611d-129">Mise en pool d’objets et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="2611d-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="2611d-130">Transactions et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="2611d-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



