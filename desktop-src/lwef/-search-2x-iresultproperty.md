---
title: Interface IResultProperty (WdsSharedIDL. h)
description: Expose les propriétés de résultat.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultProperty
- Fonctionnalités d’environnement Windows héritées de l’interface IResultProperty, Description
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510763"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="d0649-105">Interface IResultProperty</span><span class="sxs-lookup"><span data-stu-id="d0649-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="d0649-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d0649-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d0649-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d0649-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d0649-108">Expose les propriétés de résultat.</span><span class="sxs-lookup"><span data-stu-id="d0649-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="d0649-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d0649-109">Members</span></span>

<span data-ttu-id="d0649-110">L’interface **IResultProperty** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d0649-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d0649-111">**IResultProperty** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d0649-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="d0649-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0649-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0649-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0649-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0649-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0649-114">Methods</span></span>

<span data-ttu-id="d0649-115">L’interface **IResultProperty** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d0649-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="d0649-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="d0649-116">Method</span></span>                                                    | <span data-ttu-id="d0649-117">Description</span><span class="sxs-lookup"><span data-stu-id="d0649-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="d0649-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="d0649-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="d0649-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d0649-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d0649-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="d0649-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="d0649-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d0649-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d0649-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0649-122">Properties</span></span>

<span data-ttu-id="d0649-123">L’interface **IResultProperty** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0649-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="d0649-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="d0649-124">Property</span></span>                                                                   | <span data-ttu-id="d0649-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d0649-125">Access type</span></span>          | <span data-ttu-id="d0649-126">Description</span><span class="sxs-lookup"><span data-stu-id="d0649-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="d0649-127">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="d0649-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="d0649-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-128">Read-only</span></span><br/> | <span data-ttu-id="d0649-129">Type de données des propriétés.</span><span class="sxs-lookup"><span data-stu-id="d0649-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="d0649-130">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="d0649-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="d0649-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-131">Read-only</span></span><br/> | <span data-ttu-id="d0649-132">Nom complet localisé de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d0649-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="d0649-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="d0649-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="d0649-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-134">Read-only</span></span><br/> | <span data-ttu-id="d0649-135">Visability de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d0649-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="d0649-136">**Évit**</span><span class="sxs-lookup"><span data-stu-id="d0649-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="d0649-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-137">Read-only</span></span><br/> | <span data-ttu-id="d0649-138">Valeur spéciale utilisée pour faciliter la récupération de données.</span><span class="sxs-lookup"><span data-stu-id="d0649-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="d0649-139">**IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="d0649-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="d0649-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-140">Read-only</span></span><br/> | <span data-ttu-id="d0649-141">Nom de la colonne des propriétés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0649-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="d0649-142">**Identificateur d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0649-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="d0649-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0649-143">Read-only</span></span><br/> | <span data-ttu-id="d0649-144">Identificateur unique de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d0649-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="d0649-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d0649-145">Remarks</span></span>

<span data-ttu-id="d0649-146">Il s’agit des propriétés de retour des éléments.</span><span class="sxs-lookup"><span data-stu-id="d0649-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0649-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0649-147">Requirements</span></span>



| <span data-ttu-id="d0649-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0649-148">Requirement</span></span> | <span data-ttu-id="d0649-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0649-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0649-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0649-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d0649-151">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0649-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d0649-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0649-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d0649-153">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0649-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0649-154">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d0649-154">Redistributable</span></span><br/>          | <span data-ttu-id="d0649-155">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d0649-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="d0649-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0649-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0649-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0649-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

