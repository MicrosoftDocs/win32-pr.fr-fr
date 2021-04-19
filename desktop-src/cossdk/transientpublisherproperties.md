---
description: Contient un objet pour chaque propriété de serveur de publication temporaire pour la collection TransientSubscriptions parente. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Collection TransientPublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 707cb974dce632c6eb5f65bc38f1fff8b779e54d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515373"
---
# <a name="transientpublisherproperties-collection"></a><span data-ttu-id="6acae-104">Collection TransientPublisherProperties</span><span class="sxs-lookup"><span data-stu-id="6acae-104">TransientPublisherProperties collection</span></span>

<span data-ttu-id="6acae-105">Contient un objet pour chaque propriété de serveur de publication temporaire pour la collection [**TransientSubscriptions**](transientsubscriptions.md) parente.</span><span class="sxs-lookup"><span data-stu-id="6acae-105">Contains an object for each transient publisher property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="6acae-106">Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.</span><span class="sxs-lookup"><span data-stu-id="6acae-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="6acae-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6acae-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6acae-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6acae-108">Members</span></span>

<span data-ttu-id="6acae-109">La collection **TransientPublisherProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6acae-109">The **TransientPublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6acae-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="6acae-110">Related Collections</span></span>

<span data-ttu-id="6acae-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="6acae-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6acae-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6acae-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6acae-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6acae-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6acae-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="6acae-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="6acae-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="6acae-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6acae-116">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="6acae-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="6acae-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6acae-117">Properties</span></span>

<span data-ttu-id="6acae-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="6acae-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6acae-119">Nom</span><span class="sxs-lookup"><span data-stu-id="6acae-119">Name</span></span>](#name)
-   [<span data-ttu-id="6acae-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acae-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="6acae-121">Nom</span><span class="sxs-lookup"><span data-stu-id="6acae-121">Name</span></span>



| <span data-ttu-id="6acae-122">Entrée</span><span class="sxs-lookup"><span data-stu-id="6acae-122">Entry</span></span> | <span data-ttu-id="6acae-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acae-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acae-124">Description</span><span class="sxs-lookup"><span data-stu-id="6acae-124">Description</span></span>    | <span data-ttu-id="6acae-125">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="6acae-125">The name of the property.</span></span> <span data-ttu-id="6acae-126">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="6acae-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6acae-127">Accès</span><span class="sxs-lookup"><span data-stu-id="6acae-127">Access</span></span>         | <span data-ttu-id="6acae-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="6acae-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6acae-129">Type</span><span class="sxs-lookup"><span data-stu-id="6acae-129">Type</span></span>           | <span data-ttu-id="6acae-130">String</span><span class="sxs-lookup"><span data-stu-id="6acae-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6acae-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="6acae-131">Default</span></span>        | <span data-ttu-id="6acae-132">« Nouvelle propriété »</span><span class="sxs-lookup"><span data-stu-id="6acae-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6acae-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="6acae-133">Minimum system</span></span> | <span data-ttu-id="6acae-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6acae-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="6acae-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acae-135">Value</span></span>



| <span data-ttu-id="6acae-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="6acae-136">Entry</span></span> | <span data-ttu-id="6acae-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acae-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="6acae-138">Description</span><span class="sxs-lookup"><span data-stu-id="6acae-138">Description</span></span>    | <span data-ttu-id="6acae-139">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="6acae-139">A value for the property.</span></span> |
| <span data-ttu-id="6acae-140">Accès</span><span class="sxs-lookup"><span data-stu-id="6acae-140">Access</span></span>         | <span data-ttu-id="6acae-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6acae-141">ReadWrite</span></span>                 |
| <span data-ttu-id="6acae-142">Type</span><span class="sxs-lookup"><span data-stu-id="6acae-142">Type</span></span>           | <span data-ttu-id="6acae-143">Variante</span><span class="sxs-lookup"><span data-stu-id="6acae-143">Variant</span></span>                   |
| <span data-ttu-id="6acae-144">Default</span><span class="sxs-lookup"><span data-stu-id="6acae-144">Default</span></span>        | <span data-ttu-id="6acae-145">N/A</span><span class="sxs-lookup"><span data-stu-id="6acae-145">N/A</span></span>                       |
| <span data-ttu-id="6acae-146">Système minimal</span><span class="sxs-lookup"><span data-stu-id="6acae-146">Minimum system</span></span> | <span data-ttu-id="6acae-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6acae-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="6acae-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6acae-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6acae-149">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="6acae-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
