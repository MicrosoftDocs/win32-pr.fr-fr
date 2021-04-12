---
description: Obtention et définition des propriétés
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtention et définition des propriétés (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483448"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="af94b-103">Obtention et définition des propriétés (services de composants)</span><span class="sxs-lookup"><span data-stu-id="af94b-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="af94b-104">Avant de pouvoir lire ou écrire des propriétés particulières exposées par un élément dans une collection, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="af94b-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="af94b-105">Récupérez la collection.</span><span class="sxs-lookup"><span data-stu-id="af94b-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="af94b-106">Remplissez la collection pour y lire les données à partir du catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="af94b-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="af94b-107">Récupérez l’élément spécifique dans la collection, en le représentant avec un objet de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="af94b-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="af94b-108">Pour obtenir un exemple qui illustre ces étapes, consultez [navigation dans la hiérarchie des collections com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="af94b-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="af94b-109">Étant donné que les propriétés particulières exposées peuvent varier en fonction de ce que représente l’élément ; autrement dit, un élément représentant un composant a des propriétés différentes de celles qui représentent une application COM+.</span><span class="sxs-lookup"><span data-stu-id="af94b-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="af94b-110">Définissez l’une de ces propriétés à l’aide d’une propriété générique unique, la propriété Value, sur [**COMAdminCatalogObject**](comadmincatalogobject.md).</span><span class="sxs-lookup"><span data-stu-id="af94b-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="af94b-111">La propriété valeur vous permet d’obtenir ou de définir n’importe quelle propriété nommée spécifique exposée par un élément, en retournant une valeur pour une propriété nommée lors de l’obtention et de la prise d’un nom et d’une valeur lors de la définition de.</span><span class="sxs-lookup"><span data-stu-id="af94b-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="af94b-112">Aucune modification n’est réellement enregistrée dans le catalogue COM+ tant que vous n’avez pas enregistré explicitement les modifications à l’aide de la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="af94b-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="af94b-113">Les modifications en attente pour toutes les propriétés de tous les éléments d’une collection donnée sont enregistrées en même temps.</span><span class="sxs-lookup"><span data-stu-id="af94b-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="af94b-114">Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="af94b-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="af94b-115">Toutes les modifications que vous apportez ne seront pas acceptées.</span><span class="sxs-lookup"><span data-stu-id="af94b-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="af94b-116">Le catalogue COM+ applique une certaine logique de cohérence pour s’assurer que vous configurez les éléments de manière raisonnable.</span><span class="sxs-lookup"><span data-stu-id="af94b-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="af94b-117">En outre, lorsque vous modifiez certaines propriétés, d’autres peuvent changer automatiquement à l’aide de la même logique de cohérence.</span><span class="sxs-lookup"><span data-stu-id="af94b-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="af94b-118">Ces effets s’affichent lorsque vous tentez d’enregistrer des modifications.</span><span class="sxs-lookup"><span data-stu-id="af94b-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="af94b-119">Vous pouvez être en conflit avec un autre enregistreur dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="af94b-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="af94b-120">Entre les appels à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour une collection donnée, vous ne disposez d’aucun verrou sur l’une de ces données dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="af94b-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="af94b-121">Plusieurs parties peuvent configurer simultanément des éléments dans une collection donnée et peuvent être en concurrence lorsqu’ils enregistrent des modifications.</span><span class="sxs-lookup"><span data-stu-id="af94b-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="af94b-122">Cela signifie qu’un autre utilisateur peut modifier les paramètres d’un objet avant ou après l’exécution, soit en exécutant un programme à l’aide des objets comadmin ou à l’aide de l’outil d’administration Services de composants, localement ou à distance.</span><span class="sxs-lookup"><span data-stu-id="af94b-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="af94b-123">La règle générale avec l’écriture d’objets sur le catalogue est que toutes les propriétés d’un objet sont écrites en même temps.</span><span class="sxs-lookup"><span data-stu-id="af94b-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="af94b-124">Autrement dit, le dernier enregistreur gagne : l’objet est enregistré de manière précise dans le catalogue, comme le dernier enregistreur l’a configuré.</span><span class="sxs-lookup"><span data-stu-id="af94b-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="af94b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af94b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af94b-126">Interdépendances entre les propriétés</span><span class="sxs-lookup"><span data-stu-id="af94b-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="af94b-127">Interrogation des propriétés disponibles</span><span class="sxs-lookup"><span data-stu-id="af94b-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="af94b-128">Enregistrement ou rejet des modifications</span><span class="sxs-lookup"><span data-stu-id="af94b-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



