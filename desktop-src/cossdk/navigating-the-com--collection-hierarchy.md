---
description: Navigation dans la hiérarchie de regroupement COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navigation dans la hiérarchie de regroupement COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538630"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="a5be8-103">Navigation dans la hiérarchie de regroupement COM+</span><span class="sxs-lookup"><span data-stu-id="a5be8-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="a5be8-104">Quelques collections que vous pouvez récupérer facilement à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="a5be8-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="a5be8-105">Cette méthode récupère une collection « de niveau supérieur »; autrement dit, une collection telle que [**applications**](applications.md), qui est autonome et qui est unique et ne peut pas être incluse logiquement sous une autre collection.</span><span class="sxs-lookup"><span data-stu-id="a5be8-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="a5be8-106">De nombreux regroupements, toutefois, sont logiquement inclus dans une autre collection, car ils contiennent des éléments qui font partie d’une structure plus grande.</span><span class="sxs-lookup"><span data-stu-id="a5be8-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="a5be8-107">Par exemple, la collection de [**composants**](components.md) est incluse, ou associée, à la collection d' [**applications**](applications.md) , car elle contient les composants installés dans une application com+ particulière, qui correspond elle-même à un élément dans la collection d' **applications** .</span><span class="sxs-lookup"><span data-stu-id="a5be8-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="a5be8-108">Les regroupements associés tels que celui-ci ne sont pas uniques. Il existe une collection de **composants** pour chaque application distincte.</span><span class="sxs-lookup"><span data-stu-id="a5be8-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="a5be8-109">Par conséquent, les collections sont organisées dans une structure hiérarchique qui correspond naturellement aux relations logiques entre les éléments qu’elles contiennent.</span><span class="sxs-lookup"><span data-stu-id="a5be8-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="a5be8-110">Vous trouverez un diagramme de la hiérarchie de collection dans les [collections d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a5be8-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="a5be8-111">Pour la plupart des éléments que vous souhaitez configurer à l’aide des objets comadmin, vous devez parcourir certaines parties de la hiérarchie de collection pour récupérer l’élément approprié.</span><span class="sxs-lookup"><span data-stu-id="a5be8-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="a5be8-112">Dans la pratique, cela signifie que si vous souhaitez obtenir un élément dans un regroupement connexe, vous devez d’abord parcourir tous les regroupements inclus dont fait nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a5be8-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="a5be8-113">Et pour récupérer un regroupement connexe, vous devez récupérer l’élément spécifique dans le regroupement parent auquel la collection enfant est associée.</span><span class="sxs-lookup"><span data-stu-id="a5be8-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="a5be8-114">Par exemple, si vous souhaitez configurer un élément correspondant à un composant dans une application COM+ particulière, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5be8-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="a5be8-115">Récupérez la collection d' [**applications**](applications.md) et remplissez-la.</span><span class="sxs-lookup"><span data-stu-id="a5be8-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="a5be8-116">Énumérez le contenu de la collection d' [**applications**](applications.md) jusqu’à ce que vous obteniez l’élément correspondant à l’application com+ appropriée.</span><span class="sxs-lookup"><span data-stu-id="a5be8-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="a5be8-117">Obtenir et remplir la collection de [**composants**](components.md) pour cette application com+ particulière.</span><span class="sxs-lookup"><span data-stu-id="a5be8-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="a5be8-118">Énumérez le contenu de la collection de [**composants**](components.md) jusqu’à ce que vous obteniez l’élément correspondant au composant approprié.</span><span class="sxs-lookup"><span data-stu-id="a5be8-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="a5be8-119">L’exemple de Visual Basic Microsoft suivant montre comment effectuer les étapes précédentes :</span><span class="sxs-lookup"><span data-stu-id="a5be8-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="a5be8-120">Deux méthodes **GetCollection** distinctes sont utilisées dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="a5be8-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="a5be8-121">Le premier est exposé par [**COMAdminCatalog**](comadmincatalog.md) et est utilisé pour obtenir une collection de niveau supérieur, dans le cas présent, « applications ».</span><span class="sxs-lookup"><span data-stu-id="a5be8-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="a5be8-122">Le deuxième est exposé par [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et est utilisé pour obtenir une collection liée à la collection actuelle. vous indiquez précisément la collection que vous souhaitez en passant le nom « Components » et la valeur de propriété de clé de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="a5be8-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="a5be8-123">La valeur de la propriété de clé est souvent un nom ou un GUID qui identifie l’objet de façon unique ; Cette valeur est identifiée dans la documentation de chaque collection.</span><span class="sxs-lookup"><span data-stu-id="a5be8-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="a5be8-124">Dans le cas le plus général, vous devez obtenir les collections associées de manière itérative dans la hiérarchie de collection jusqu’à ce que vous récupériez le regroupement de votre choix.</span><span class="sxs-lookup"><span data-stu-id="a5be8-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="a5be8-125">Les étapes à suivre pour suivre le même modèle général, de façon répétée.</span><span class="sxs-lookup"><span data-stu-id="a5be8-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="a5be8-126">Pour obtenir la liste complète des regroupements, consultez [regroupements d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a5be8-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="a5be8-127">Dans certains cas, vous souhaiterez peut-être utiliser une méthode de raccourci la deuxième fois que vous suivez un chemin d’accès dans la hiérarchie de collection.</span><span class="sxs-lookup"><span data-stu-id="a5be8-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="a5be8-128">Vous pouvez utiliser cette méthode uniquement après avoir déjà mis en cache toutes les valeurs de clé intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="a5be8-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="a5be8-129">Pour plus d’informations, consultez [**ICOMAdminCatalog :: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="a5be8-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5be8-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5be8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5be8-131">Remplissage des collections COM+</span><span class="sxs-lookup"><span data-stu-id="a5be8-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="a5be8-132">Interrogation des collections associées disponibles</span><span class="sxs-lookup"><span data-stu-id="a5be8-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="a5be8-133">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="a5be8-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



