---
description: Processus d’allocation des ressources du distributeur de ressources
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processus d’allocation des ressources du distributeur de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200978"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="19e5e-103">Processus d’allocation des ressources du distributeur de ressources</span><span class="sxs-lookup"><span data-stu-id="19e5e-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="19e5e-104">Chaque fois qu’un distributeur de ressources alloue une ressource de son détenteur, voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="19e5e-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="19e5e-105">Le distributeur de ressources déclare un identificateur de type de ressource (**RESTYPID**), qui décrit le type de ressource requis.</span><span class="sxs-lookup"><span data-stu-id="19e5e-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="19e5e-106">Le distributeur de ressources appelle la méthode [**IHolder :: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) du détenteur, en passant ce **RESTYPID**.</span><span class="sxs-lookup"><span data-stu-id="19e5e-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="19e5e-107">Le détenteur génère une liste de candidats à partir des ressources disponibles.</span><span class="sxs-lookup"><span data-stu-id="19e5e-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="19e5e-108">Les candidats sont des ressources qui ne sont pas inscrites dans une transaction ou déjà inscrites dans la transaction de l’objet appelant.</span><span class="sxs-lookup"><span data-stu-id="19e5e-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="19e5e-109">Ces candidats sont passés individuellement à la méthode [**IDispenserDriver :: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , où ils sont évalués (sur une échelle de 0 à 100) en fonction de la correspondance entre la ressource candidate et le **RESTYPID** souhaité.</span><span class="sxs-lookup"><span data-stu-id="19e5e-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="19e5e-110">Le détenteur choisit la ressource dont le distributeur de ressources est le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="19e5e-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="19e5e-111">Le distributeur de ressources peut mettre fin à la boucle d’évaluation dès le début en affectant au candidat une évaluation de la ressource 100 (un ajustement parfait).</span><span class="sxs-lookup"><span data-stu-id="19e5e-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="19e5e-112">Une évaluation de 100 serait normalement réservée pour les ressources candidates qui sont déjà inscrites, sauf si le distributeur de ressources conclut que l’inscription est une opération peu coûteuse.</span><span class="sxs-lookup"><span data-stu-id="19e5e-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="19e5e-113">Si toutes les ressources candidates (le cas échéant) sont évaluées à 0 (inutilisables), une nouvelle ressource est créée en appelant [**IDispenserDriver :: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span><span class="sxs-lookup"><span data-stu-id="19e5e-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="19e5e-114">Si la ressource choisie précédemment n’est pas déjà inscrite dans la transaction de l’objet appelant, la méthode [**IDispenserDriver :: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) du distributeur de ressources est appelée.</span><span class="sxs-lookup"><span data-stu-id="19e5e-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="19e5e-115">L’appel de la méthode [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) retourne au distributeur de ressources avec la ressource inscrite.</span><span class="sxs-lookup"><span data-stu-id="19e5e-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19e5e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19e5e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e5e-117">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="19e5e-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="19e5e-118">Inscription d’une ressource dans une transaction</span><span class="sxs-lookup"><span data-stu-id="19e5e-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="19e5e-119">Suivi des ressources non allouées</span><span class="sxs-lookup"><span data-stu-id="19e5e-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



