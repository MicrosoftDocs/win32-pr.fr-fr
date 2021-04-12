---
description: COM+ fournit un modèle de programmation simple pour l’utilisation de ses services automatiques.
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: Initiation aux services COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317913"
---
# <a name="com-services-primer"></a><span data-ttu-id="e42a1-103">Initiation aux services COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-103">COM+ Services Primer</span></span>

<span data-ttu-id="e42a1-104">COM+ fournit un modèle de programmation simple pour l’utilisation de ses services automatiques.</span><span class="sxs-lookup"><span data-stu-id="e42a1-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="e42a1-105">Vous pouvez simplement définir ces services en tant qu’attributs déclaratifs sur des composants et leurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="e42a1-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="e42a1-106">Lorsque vous définissez ces attributs, COM+ remet automatiquement les services demandés à l’objet en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="e42a1-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="e42a1-107">Ce guide d’initiation montre les services COM+ en action en parcourant l’exemple de code de composant en trois étapes définies.</span><span class="sxs-lookup"><span data-stu-id="e42a1-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="e42a1-108">La complexité des informations est générée au fur et à mesure de la progression des étapes.</span><span class="sxs-lookup"><span data-stu-id="e42a1-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="e42a1-109">Le code se concentre sur le modèle de programmation simplifié, en utilisant le traitement des transactions pour illustrer les principes de base de COM+.</span><span class="sxs-lookup"><span data-stu-id="e42a1-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="e42a1-110">Chacune des étapes suivantes illustre un aspect fondamental des services COM+ :</span><span class="sxs-lookup"><span data-stu-id="e42a1-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="e42a1-111">Étape 1 : création d’un composant transactionnel</span><span class="sxs-lookup"><span data-stu-id="e42a1-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="e42a1-112">Étape 2 : extension d’une transaction à travers plusieurs composants</span><span class="sxs-lookup"><span data-stu-id="e42a1-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="e42a1-113">Étape 3 : réutilisation des composants</span><span class="sxs-lookup"><span data-stu-id="e42a1-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="e42a1-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e42a1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e42a1-115">Vue d’ensemble de la programmation COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="e42a1-116">Vue d’ensemble de l’application COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="e42a1-117">Configuration des applications COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e42a1-118">Contextes COM+ et modèles de thread</span><span class="sxs-lookup"><span data-stu-id="e42a1-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="e42a1-119">Création d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e42a1-120">Conception d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="e42a1-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 



