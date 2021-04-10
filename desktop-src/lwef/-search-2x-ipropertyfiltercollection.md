---
title: Interface IPropertyFilterCollection (WdsSharedIDL. h)
description: Expose les propriétés de la collection retournée en fonction de la requête envoyée.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, Description
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317318"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="73f00-105">Interface IPropertyFilterCollection</span><span class="sxs-lookup"><span data-stu-id="73f00-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="73f00-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73f00-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="73f00-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="73f00-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="73f00-108">Expose les propriétés de la collection retournée en fonction de la requête envoyée.</span><span class="sxs-lookup"><span data-stu-id="73f00-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="73f00-109">Membres</span><span class="sxs-lookup"><span data-stu-id="73f00-109">Members</span></span>

<span data-ttu-id="73f00-110">L’interface **IPropertyFilterCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="73f00-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73f00-111">**IPropertyFilterCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73f00-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="73f00-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73f00-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73f00-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73f00-113">Properties</span></span>

<span data-ttu-id="73f00-114">L’interface **IPropertyFilterCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="73f00-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="73f00-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="73f00-115">Property</span></span>                                                                         | <span data-ttu-id="73f00-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="73f00-116">Access type</span></span>           | <span data-ttu-id="73f00-117">Description</span><span class="sxs-lookup"><span data-stu-id="73f00-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="73f00-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="73f00-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="73f00-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73f00-119">Read-only</span></span><br/>  | <span data-ttu-id="73f00-120">Ajoute un nouveau filtre à la collection.</span><span class="sxs-lookup"><span data-stu-id="73f00-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="73f00-121">**effacé**</span><span class="sxs-lookup"><span data-stu-id="73f00-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="73f00-122">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="73f00-122">Write-only</span></span><br/> | <span data-ttu-id="73f00-123">Efface la collection.</span><span class="sxs-lookup"><span data-stu-id="73f00-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="73f00-124">**Saut**</span><span class="sxs-lookup"><span data-stu-id="73f00-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="73f00-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73f00-125">Read-only</span></span><br/>  | <span data-ttu-id="73f00-126">Nombre de filtres dans la collection.</span><span class="sxs-lookup"><span data-stu-id="73f00-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="73f00-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="73f00-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="73f00-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="73f00-128">Read/write</span></span><br/> | <span data-ttu-id="73f00-129">Retourne un filtre spécifique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="73f00-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="73f00-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="73f00-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="73f00-131">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="73f00-131">Write-only</span></span><br/> | <span data-ttu-id="73f00-132">Supprime un filtre spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="73f00-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="73f00-133">Notes</span><span class="sxs-lookup"><span data-stu-id="73f00-133">Remarks</span></span>

<span data-ttu-id="73f00-134">Ces propriétés sont utilisées pour filtrer les collections retournées par la requête.</span><span class="sxs-lookup"><span data-stu-id="73f00-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f00-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73f00-135">Requirements</span></span>



| <span data-ttu-id="73f00-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73f00-136">Requirement</span></span> | <span data-ttu-id="73f00-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="73f00-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f00-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73f00-138">Minimum supported client</span></span><br/> | <span data-ttu-id="73f00-139">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73f00-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73f00-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73f00-140">Minimum supported server</span></span><br/> | <span data-ttu-id="73f00-141">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73f00-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="73f00-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="73f00-142">Redistributable</span></span><br/>          | <span data-ttu-id="73f00-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="73f00-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="73f00-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="73f00-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f00-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f00-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

