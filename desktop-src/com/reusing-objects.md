---
title: Réutilisation d’objets
description: Réutilisation d’objets
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "104507854"
---
# <a name="reusing-objects"></a><span data-ttu-id="ece25-103">Réutilisation d’objets</span><span class="sxs-lookup"><span data-stu-id="ece25-103">Reusing Objects</span></span>

<span data-ttu-id="ece25-104">L’un des objectifs importants d’un modèle objet est de permettre aux auteurs d’objets de réutiliser et d’étendre des objets fournis par d’autres en tant qu’éléments de leurs propres implémentations.</span><span class="sxs-lookup"><span data-stu-id="ece25-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="ece25-105">L’une des façons d’effectuer cette opération dans Microsoft Visual C++ et d’autres langages consiste à utiliser l' *héritage d’implémentation*, qui permet à un objet d’hériter (« sous-classe ») certaines de ses fonctions d’un autre objet tout en remplaçant d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="ece25-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="ece25-106">Le problème de l’interaction des objets du système à l’aide de l’héritage d’implémentation traditionnel est que le contrat (l’interface) entre les objets d’une hiérarchie d’implémentation n’est pas clairement défini.</span><span class="sxs-lookup"><span data-stu-id="ece25-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="ece25-107">En fait, elle est implicite et ambiguë.</span><span class="sxs-lookup"><span data-stu-id="ece25-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="ece25-108">Lorsque l’objet parent ou enfant modifie son implémentation, le comportement des composants associés peut devenir non défini ou INSTABLEMENT implémenté.</span><span class="sxs-lookup"><span data-stu-id="ece25-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="ece25-109">Dans une application unique, où l’implémentation peut être gérée par une équipe d’ingénierie unique qui met à jour tous les composants en même temps, ce n’est pas toujours un problème majeur.</span><span class="sxs-lookup"><span data-stu-id="ece25-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="ece25-110">Dans un environnement où les composants d’une équipe sont créés par le biais de la réutilisation de la boîte noire d’autres composants créés par d’autres équipes, ce type d’instabilité met en péril la réutilisation.</span><span class="sxs-lookup"><span data-stu-id="ece25-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="ece25-111">En outre, l’héritage d’implémentation fonctionne généralement uniquement dans les limites du processus.</span><span class="sxs-lookup"><span data-stu-id="ece25-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="ece25-112">Cela rend l’héritage d’implémentation traditionnel peu pratique pour les grands systèmes en constante évolution, composés de composants logiciels créés par de nombreuses équipes d’ingénierie.</span><span class="sxs-lookup"><span data-stu-id="ece25-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="ece25-113">La clé de la création des composants réutilisables consiste à pouvoir traiter l’objet comme une boîte opaque.</span><span class="sxs-lookup"><span data-stu-id="ece25-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="ece25-114">Cela signifie que la partie du code qui tente de réutiliser un autre objet ne sait rien et ne doit en savoir rien, à propos de la structure interne ou de l’implémentation du composant utilisé.</span><span class="sxs-lookup"><span data-stu-id="ece25-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="ece25-115">En d’autres termes, le code qui tente de réutiliser un composant dépend du comportement de l’objet et non de son implémentation exacte.</span><span class="sxs-lookup"><span data-stu-id="ece25-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="ece25-116">Pour obtenir une réutilisation de la boîte noire, COM adopte d’autres mécanismes de réutilisation établis, tels que la *relation contenant-contenu* , la délégation et l' *agrégation*.</span><span class="sxs-lookup"><span data-stu-id="ece25-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="ece25-117">Pour plus de commodité, l’objet qui est réutilisé est appelé l' *objet interne* et l’objet qui utilise cet objet interne est l' *objet externe*.</span><span class="sxs-lookup"><span data-stu-id="ece25-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="ece25-118">Il est important de se souvenir dans ces deux mécanismes de la façon dont l’objet externe apparaît à ses clients.</span><span class="sxs-lookup"><span data-stu-id="ece25-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="ece25-119">En ce qui concerne les clients, les deux objets implémentent les interfaces auxquelles le client peut obtenir un pointeur.</span><span class="sxs-lookup"><span data-stu-id="ece25-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="ece25-120">Le client traite l’objet externe comme un cadre opaque et n’a donc pas besoin de se soucier de la structure interne du objectâ externe. il ne s’intéresse pas non plus au comportement.</span><span class="sxs-lookup"><span data-stu-id="ece25-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="ece25-121">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ece25-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ece25-122">Imbrication/délégation</span><span class="sxs-lookup"><span data-stu-id="ece25-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="ece25-123">Agrégation</span><span class="sxs-lookup"><span data-stu-id="ece25-123">Aggregation</span></span>](aggregation.md)

 

 




