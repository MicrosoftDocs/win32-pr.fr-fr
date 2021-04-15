---
description: États des ressources regroupées accessibles au distributeur de ressources COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: États des ressources regroupées accessibles au distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483432"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="97cd8-103">États des ressources regroupées accessibles au distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="97cd8-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="97cd8-104">À tout moment, une ressource est en cours d’utilisation ou n’est pas utilisée et est inscrite ou n’est pas inscrite dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="97cd8-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="97cd8-105">Cela donne quatre États de ressources possibles, comme suit :</span><span class="sxs-lookup"><span data-stu-id="97cd8-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="97cd8-106">**Ressources dans un inventaire désinscrit.**</span><span class="sxs-lookup"><span data-stu-id="97cd8-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="97cd8-107">Une ressource qui n’est pas utilisée par un objet et qui n’est pas inscrit dans une transaction est dans un inventaire non inscrit.</span><span class="sxs-lookup"><span data-stu-id="97cd8-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="97cd8-108">Une ressource de l’inventaire général est disponible pour l’attribution.</span><span class="sxs-lookup"><span data-stu-id="97cd8-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="97cd8-109">**Ressources dans l’inventaire inscrit.**</span><span class="sxs-lookup"><span data-stu-id="97cd8-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="97cd8-110">Une ressource qui n’est pas utilisée par un objet mais qui est inscrit dans une transaction est dans un inventaire inscrit.</span><span class="sxs-lookup"><span data-stu-id="97cd8-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="97cd8-111">Une telle ressource est disponible pour une attribution uniquement aux objets s’exécutant dans la même transaction.</span><span class="sxs-lookup"><span data-stu-id="97cd8-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="97cd8-112">Une ressource passe d’un inventaire inscrit à un inventaire non inscrit lorsque COM+ notifie le gestionnaire du distributeur que la transaction est terminée.</span><span class="sxs-lookup"><span data-stu-id="97cd8-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="97cd8-113">**Ressources dans un usage désinscrit.**</span><span class="sxs-lookup"><span data-stu-id="97cd8-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="97cd8-114">Si une ressource est affectée à un objet et que l’instance n’est pas exécutée dans une transaction ou que le distributeur de ressources a identifié la ressource comme non transactionnelle, cette ressource est désinscrite.</span><span class="sxs-lookup"><span data-stu-id="97cd8-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="97cd8-115">**Ressources dans un usage inscrit.**</span><span class="sxs-lookup"><span data-stu-id="97cd8-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="97cd8-116">Si une ressource est assignée à un objet, l’instance s’exécute dans une transaction et le distributeur de ressources a correctement inscrit la ressource dans la transaction, cette ressource est dans un usage inscrit.</span><span class="sxs-lookup"><span data-stu-id="97cd8-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97cd8-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97cd8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97cd8-118">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="97cd8-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="97cd8-119">Inscription d’une ressource dans une transaction</span><span class="sxs-lookup"><span data-stu-id="97cd8-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



