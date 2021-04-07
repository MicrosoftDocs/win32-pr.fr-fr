---
description: Récupération des regroupements sur le catalogue COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Récupération des regroupements sur le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748029"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="23b39-103">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="23b39-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="23b39-104">Les données du catalogue COM+ sont stockées dans une hiérarchie de regroupements.</span><span class="sxs-lookup"><span data-stu-id="23b39-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="23b39-105">Dans l’outil d’administration Services de composants, un grand nombre de ces regroupements s’affichent sous la forme de dossiers dans l’arborescence de la console.</span><span class="sxs-lookup"><span data-stu-id="23b39-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="23b39-106">Les regroupements qui n’apparaissent pas en tant que dossiers sont accessibles uniquement par programme.</span><span class="sxs-lookup"><span data-stu-id="23b39-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="23b39-107">Les collections servent de conteneurs pour les éléments.</span><span class="sxs-lookup"><span data-stu-id="23b39-107">Collections serve as containers for items.</span></span> <span data-ttu-id="23b39-108">Les éléments d’une collection donnée sont tous d’un type cohérent ; autrement dit, elles représentent toutes le même type d’élément, et il peut y avoir un nombre arbitraire d’éléments dans une collection.</span><span class="sxs-lookup"><span data-stu-id="23b39-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="23b39-109">Par exemple, la collection d' [**applications**](applications.md) contient un élément pour chaque application com+ installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="23b39-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="23b39-110">Ce regroupement s’affiche dans l’outil d’administration en tant que dossier **applications com+** .</span><span class="sxs-lookup"><span data-stu-id="23b39-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="23b39-111">Les collections se produisent dans une structure hiérarchique, car les éléments qu’elles contiennent suivent un ordre d’inclusion inné.</span><span class="sxs-lookup"><span data-stu-id="23b39-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="23b39-112">Par exemple, étant donné que les composants sont installés dans une application COM+, la collection de [**composants**](components.md) est incluse logiquement sous la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="23b39-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="23b39-113">Plus particulièrement, pour conserver les composants installés dans cette application particulière, il existe une collection de **composants** distincts pour chaque élément de la collection d' **applications** .</span><span class="sxs-lookup"><span data-stu-id="23b39-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="23b39-114">Vous devez obtenir une collection sur le catalogue chaque fois que vous souhaitez récupérer un élément et définir ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="23b39-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="23b39-115">Dans le cas général, vous devez effectuer un pas à pas détaillé dans plusieurs collections pour accéder à l’élément de votre choix.</span><span class="sxs-lookup"><span data-stu-id="23b39-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="23b39-116">Pour connaître la procédure à suivre, consultez [navigation dans la hiérarchie des collections com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="23b39-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="23b39-117">Une fois que vous avez récupéré une collection et que vous pouvez travailler directement avec les éléments qu’elle contient, vous devez remplir la collection, qui extrait les données du contenu de la collection à partir du catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="23b39-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="23b39-118">Pour plus d’informations, consultez [remplissage des collections com+](populating-com--collections.md).</span><span class="sxs-lookup"><span data-stu-id="23b39-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="23b39-119">En outre, vous pouvez utiliser une fonctionnalité qui vous permet d’effectuer des requêtes dynamiques pour voir les regroupements connexes disponibles à partir d’un regroupement donné que vous êtes en possession.</span><span class="sxs-lookup"><span data-stu-id="23b39-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="23b39-120">Pour plus d’informations, consultez [interrogation des collections associées disponibles](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="23b39-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23b39-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23b39-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b39-122">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="23b39-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="23b39-123">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="23b39-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="23b39-124">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="23b39-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="23b39-125">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="23b39-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="23b39-126">Définition des propriétés et enregistrement des modifications dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="23b39-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



