---
description: Le développement d’une application COM+ réussie nécessite une conception architecturale d’application initiale.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Conception de l’application COM+ à l’aide d’UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393048"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="b31c6-103">Conception de l’application COM+ à l’aide d’UML</span><span class="sxs-lookup"><span data-stu-id="b31c6-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="b31c6-104">Le développement d’une application COM+ réussie nécessite une conception architecturale d’application initiale.</span><span class="sxs-lookup"><span data-stu-id="b31c6-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="b31c6-105">Le langage UML (UML) est essentiel à ce développement de conception.</span><span class="sxs-lookup"><span data-stu-id="b31c6-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="b31c6-106">Le UML est une notation de modélisation pour les données d’application et les processus qui combine les meilleures pratiques de l’industrie des logiciels.</span><span class="sxs-lookup"><span data-stu-id="b31c6-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="b31c6-107">Étant donné que le langage UML divise l’application en trois vues reflétant l’application, ainsi que son Packaging et sa mise en œuvre, la notation de modélisation s’étend bien à la prise en charge de la modélisation d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b31c6-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="b31c6-108">Le UML traite trois vues de l’application, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b31c6-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="b31c6-109">Vue statique, modélisée par les informations tirées des scénarios utilisateur et des diagrammes de classes.</span><span class="sxs-lookup"><span data-stu-id="b31c6-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="b31c6-110">Vue dynamique, modélisée à l’aide de diagrammes de séquence, de collaboration et de transition d’État.</span><span class="sxs-lookup"><span data-stu-id="b31c6-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="b31c6-111">La vue fonctionnelle, qui est le texte descriptif le plus traditionnel qui utilise le pseudocode et les spécifications.</span><span class="sxs-lookup"><span data-stu-id="b31c6-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="b31c6-112">Les informations de ces vues peuvent être collectées en suivant trois étapes de conception qui fonctionnent bien avec le langage UML.</span><span class="sxs-lookup"><span data-stu-id="b31c6-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="b31c6-113">Avant d’écrire une seule ligne de code, vous devez créer les modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="b31c6-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="b31c6-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modèle conceptuel</span><span class="sxs-lookup"><span data-stu-id="b31c6-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="b31c6-115">Déterminez les composants et services requis.</span><span class="sxs-lookup"><span data-stu-id="b31c6-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="b31c6-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modèle logique</span><span class="sxs-lookup"><span data-stu-id="b31c6-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="b31c6-117">Déterminez le niveau de conception logique auquel ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="b31c6-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="b31c6-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modèle physique</span><span class="sxs-lookup"><span data-stu-id="b31c6-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="b31c6-119">Déterminez où les composants résident physiquement et comment ils doivent être codés.</span><span class="sxs-lookup"><span data-stu-id="b31c6-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="b31c6-120">Ces modèles peuvent ensuite être utilisés avec des outils de cas UML.</span><span class="sxs-lookup"><span data-stu-id="b31c6-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="b31c6-121">Pour plus d’informations sur ces trois modèles de conception, consultez les rubriques suivantes dans cette section :</span><span class="sxs-lookup"><span data-stu-id="b31c6-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="b31c6-122">Modèle conceptuel : exigences de l’application</span><span class="sxs-lookup"><span data-stu-id="b31c6-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="b31c6-123">Modèle logique : définition et planification de l’application</span><span class="sxs-lookup"><span data-stu-id="b31c6-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="b31c6-124">Modèle physique : architecture de l’application</span><span class="sxs-lookup"><span data-stu-id="b31c6-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="b31c6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b31c6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b31c6-126">Hypothèses et principes de conception de COM+</span><span class="sxs-lookup"><span data-stu-id="b31c6-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="b31c6-127">Conseils de conception générale pour l’utilisation de COM+</span><span class="sxs-lookup"><span data-stu-id="b31c6-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="b31c6-128">Optimisation des interactions avec le niveau de logique métier COM+</span><span class="sxs-lookup"><span data-stu-id="b31c6-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="b31c6-129">Autres outils Microsoft pour la création d’applications distribuées</span><span class="sxs-lookup"><span data-stu-id="b31c6-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



