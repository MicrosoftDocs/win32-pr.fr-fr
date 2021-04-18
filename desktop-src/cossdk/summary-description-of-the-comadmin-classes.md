---
description: Il existe trois classes fournies par la bibliothèque comadmin (comadmin.dll), chacune implémentant une interface COM double.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Description Résumé des classes comadmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512890"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="e5d0e-103">Description Résumé des classes comadmin</span><span class="sxs-lookup"><span data-stu-id="e5d0e-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="e5d0e-104">Il existe trois classes fournies par la bibliothèque comadmin (comadmin.dll), chacune implémentant une interface COM double.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="e5d0e-105">Vous utilisez des objets créés à partir de ces classes pour accéder au catalogue, pour représenter des collections dans le catalogue et pour représenter les éléments contenus dans des collections.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="e5d0e-106">COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="e5d0e-106">COMAdminCatalog</span></span>

<span data-ttu-id="e5d0e-107">La classe [**COMAdminCatalog**](comadmincatalog.md) représente le catalogue lui-même.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="e5d0e-108">Un objet créé à partir de **COMAdminCatalog** est l’objet fondamental que vous utilisez dans l’administration par programme.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="e5d0e-109">Outre l’établissement de la connexion de base avec le serveur de catalogue quand vous l’instanciez, **COMAdminCatalog** fournit des méthodes qui vous permettent d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5d0e-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="e5d0e-110">Obtient des collections sur le catalogue.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="e5d0e-111">Connectez-vous au serveur de catalogue sur une machine distante.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="e5d0e-112">Installer, exporter, démarrer, arrêter et obtenir des informations sur les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="e5d0e-113">Installer des composants dans des applications COM+ et obtenir des informations sur les composants.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="e5d0e-114">Démarrez, arrêtez ou actualisez les services s’exécutant sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="e5d0e-115">Actualisez, restaurez ou sauvegardez les informations du catalogue.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="e5d0e-116">Dans COM+ 1,0, la classe [**COMAdminCatalog**](comadmincatalog.md) implémente l’interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="e5d0e-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="e5d0e-117">Dans COM+ 1,5, la classe **COMAdminCatalog** implémente [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) en tant qu’interface par défaut.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="e5d0e-118">COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="e5d0e-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="e5d0e-119">La classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) représente n’importe quelle collection dans le catalogue, en fournissant une chaîne nommant la collection particulière au moment de l’instanciation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="e5d0e-120">(Les collections de catalogues disponibles sont nommées dans la table dans les [collections d’administration com+](com--administration-collections.md).) Les objets sont créés à partir de cette classe lors de la récupération d’une collection de niveau supérieur en appelant la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) de l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d0e-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="e5d0e-121">Ces objets sont également créés lors de la récupération d’une collection enfant en appelant la méthode **GetCollection** de son objet de collection parent.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="e5d0e-122">Les objets **COMAdminCatalogCollection** vous permettent d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5d0e-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="e5d0e-123">Énumérer les éléments contenus dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="e5d0e-124">Récupère un élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="e5d0e-125">Ajoutez ou supprimez des éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="e5d0e-126">Enregistrez ou ignorez toutes les modifications en attente apportées à la collection ou aux éléments qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="e5d0e-127">Obtenir une autre collection dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="e5d0e-128">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implémente l’interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .</span><span class="sxs-lookup"><span data-stu-id="e5d0e-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="e5d0e-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="e5d0e-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="e5d0e-130">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) représente tout élément contenu dans une collection.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="e5d0e-131">Les objets sont créés à partir de cette classe lors de l’obtention d’un élément via la propriété [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) d’un objet de collection de catalogues.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="e5d0e-132">Les objets créés à partir de la classe **COMAdminCatalogObject** vous permettent d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5d0e-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="e5d0e-133">Obtient ou définit les propriétés prises en charge par l’élément que l’objet est utilisé pour représenter.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="e5d0e-134">Obtenir des informations sur l’élément et ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="e5d0e-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="e5d0e-135">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implémente l’interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="e5d0e-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d0e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5d0e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d0e-137">Accès au catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="e5d0e-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="e5d0e-138">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="e5d0e-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



