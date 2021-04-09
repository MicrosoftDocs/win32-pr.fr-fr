---
description: La clé de bonne conception est la planification. Si vous n’êtes pas familiarisé avec la conception d’une application à trois niveaux, consultez la section intitulée conception de l’application COM+ à l’aide de UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Conseils de conception générale pour l’utilisation de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110558"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="03e9f-104">Conseils de conception générale pour l’utilisation de COM+</span><span class="sxs-lookup"><span data-stu-id="03e9f-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="03e9f-105">La clé de bonne conception est la planification.</span><span class="sxs-lookup"><span data-stu-id="03e9f-105">The key to good design is planning.</span></span> <span data-ttu-id="03e9f-106">Si vous n’êtes pas familiarisé avec la conception d’une application à trois niveaux, consultez la section intitulée [conception de l’application com+ à l’aide de UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="03e9f-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="03e9f-107">La façon dont vous construisez les composants COM qui composent la couche intermédiaire de votre application COM+ peut avoir un impact considérable sur les performances, l’évolutivité et la facilité de déploiement.</span><span class="sxs-lookup"><span data-stu-id="03e9f-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="03e9f-108">Les rubriques suivantes fournissent des considérations relatives à la conception et des conseils d’implémentation que vous devez connaître lors de la conception des composants COM.</span><span class="sxs-lookup"><span data-stu-id="03e9f-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="03e9f-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="03e9f-109">Topic</span></span>                                                                   | <span data-ttu-id="03e9f-110">Description</span><span class="sxs-lookup"><span data-stu-id="03e9f-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03e9f-111">Conception pour l’évolutivité</span><span class="sxs-lookup"><span data-stu-id="03e9f-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="03e9f-112">Suggère des méthodes pour augmenter l’évolutivité de votre application COM+.</span><span class="sxs-lookup"><span data-stu-id="03e9f-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="03e9f-113">Conception pour la disponibilité</span><span class="sxs-lookup"><span data-stu-id="03e9f-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="03e9f-114">Décrit les services que vous pouvez utiliser pour améliorer la disponibilité de vos fonctionnalités de niveau intermédiaire dans les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="03e9f-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="03e9f-115">Conception pour la sécurité</span><span class="sxs-lookup"><span data-stu-id="03e9f-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="03e9f-116">Décrit les méthodes permettant de configurer de manière plus efficace la sécurité pour une application COM+.</span><span class="sxs-lookup"><span data-stu-id="03e9f-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="03e9f-117">Conception pour le déploiement</span><span class="sxs-lookup"><span data-stu-id="03e9f-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="03e9f-118">Explique comment réduire les problèmes de déploiement lors de la conception d’une application distribuée.</span><span class="sxs-lookup"><span data-stu-id="03e9f-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="03e9f-119">En outre, assurez-vous d' [améliorer les performances avec](improving-performance-with-object-pooling.md) la mise en pool d’objets pour utiliser le plus efficacement possible la mise en pool d’objets.</span><span class="sxs-lookup"><span data-stu-id="03e9f-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03e9f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03e9f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03e9f-121">Hypothèses et principes de conception de COM+</span><span class="sxs-lookup"><span data-stu-id="03e9f-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="03e9f-122">Conception de l’application COM+ à l’aide d’UML</span><span class="sxs-lookup"><span data-stu-id="03e9f-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="03e9f-123">Optimisation des interactions avec le niveau de logique métier COM+</span><span class="sxs-lookup"><span data-stu-id="03e9f-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="03e9f-124">Autres outils Microsoft pour la création d’applications distribuées</span><span class="sxs-lookup"><span data-stu-id="03e9f-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




