---
title: Interface ISearchResult (WdsSharedIDL. h)
description: Expose des informations et des propriétés concernant le jeu de résultats.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface ISearchResult
- Fonctionnalités d’environnement Windows héritées de l’interface ISearchResult, Description
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742309"
---
# <a name="isearchresult-interface"></a><span data-ttu-id="0b5cd-105">Interface ISearchResult</span><span class="sxs-lookup"><span data-stu-id="0b5cd-105">ISearchResult interface</span></span>

> [!NOTE]
> <span data-ttu-id="0b5cd-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0b5cd-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="0b5cd-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0b5cd-108">Expose des informations et des propriétés concernant le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-108">Exposes information and properties regarding the result set.</span></span>

## <a name="members"></a><span data-ttu-id="0b5cd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0b5cd-109">Members</span></span>

<span data-ttu-id="0b5cd-110">L’interface **ISearchResult** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0b5cd-110">The **ISearchResult** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b5cd-111">**ISearchResult** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0b5cd-111">**ISearchResult** also has these types of members:</span></span>

-   [<span data-ttu-id="0b5cd-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0b5cd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b5cd-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0b5cd-113">Methods</span></span>

<span data-ttu-id="0b5cd-114">L’interface **ISearchResult** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-114">The **ISearchResult** interface has these methods.</span></span>



| <span data-ttu-id="0b5cd-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="0b5cd-115">Method</span></span>                                                            | <span data-ttu-id="0b5cd-116">Description</span><span class="sxs-lookup"><span data-stu-id="0b5cd-116">Description</span></span>                 |
|:------------------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="0b5cd-117">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-117">**Availability**</span></span>](-search-2x-isearchresult-availability.md)     | <span data-ttu-id="0b5cd-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-118">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-119">**Verbe**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-119">**DoVerb**</span></span>](-search-2x-isearchresult-doverb.md)                 | <span data-ttu-id="0b5cd-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-120">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-121">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-121">**GetIcon**</span></span>](-search-2x-isearchresult-geticon.md)               | <span data-ttu-id="0b5cd-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-122">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-123">**GetThumbnail**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-123">**GetThumbnail**</span></span>](-search-2x-isearchresult-getthumbnail.md)     | <span data-ttu-id="0b5cd-124">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-124">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-125">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-125">**GetValue**</span></span>](-search-2x-isearchresult-getvalue.md)             | <span data-ttu-id="0b5cd-126">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-126">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-127">**GetVerb**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-127">**GetVerb**</span></span>](-search-2x-isearchresult-getverb.md)               | <span data-ttu-id="0b5cd-128">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-128">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-129">**IconCount**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-129">**IconCount**</span></span>](-search-2x-isearchresult-iconcount.md)           | <span data-ttu-id="0b5cd-130">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-130">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-131">**Index**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-131">**Index**</span></span>](-search-2x-isearchresult-index.md)                   | <span data-ttu-id="0b5cd-132">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-132">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-133">**LoadState**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-133">**LoadState**</span></span>](-search-2x-isearchresult-loadstate.md)           | <span data-ttu-id="0b5cd-134">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-134">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-135">**Générateur d’aperçu**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-135">**Previewer**</span></span>](-search-2x-isearchresult-previewer.md)           | <span data-ttu-id="0b5cd-136">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-136">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-137">**PutValue**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-137">**PutValue**</span></span>](-search-2x-isearchresult-putvalue.md)             | <span data-ttu-id="0b5cd-138">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-138">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-139">**ThumbnailState**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-139">**ThumbnailState**</span></span>](-search-2x-isearchresult-thumbnailstate.md) | <span data-ttu-id="0b5cd-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-140">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-141">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-141">**Type**</span></span>](-search-2x-isearchresult-type.md)                     | <span data-ttu-id="0b5cd-142">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-142">Not implemented.</span></span><br/> |
| [<span data-ttu-id="0b5cd-143">**VerbCount**</span><span class="sxs-lookup"><span data-stu-id="0b5cd-143">**VerbCount**</span></span>](-search-2x-isearchresult-verbcount.md)           | <span data-ttu-id="0b5cd-144">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-144">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b5cd-145">Notes</span><span class="sxs-lookup"><span data-stu-id="0b5cd-145">Remarks</span></span>

<span data-ttu-id="0b5cd-146">Ces méthodes exposent les propriétés et les actions applicables au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0b5cd-146">These methods expose properties and actions applicable to the result set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b5cd-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b5cd-147">Requirements</span></span>



| <span data-ttu-id="0b5cd-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b5cd-148">Requirement</span></span> | <span data-ttu-id="0b5cd-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b5cd-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5cd-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b5cd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5cd-151">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b5cd-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0b5cd-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b5cd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5cd-153">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b5cd-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b5cd-154">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0b5cd-154">Redistributable</span></span><br/>          | <span data-ttu-id="0b5cd-155">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0b5cd-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="0b5cd-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b5cd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b5cd-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b5cd-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

