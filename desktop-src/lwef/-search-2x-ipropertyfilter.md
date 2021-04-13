---
title: Interface IPropertyFilter (WdsSharedIDL. h)
description: Expose les propriétés utilisées pour filtrer la requête.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter, Description
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508930"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="efb75-105">Interface IPropertyFilter</span><span class="sxs-lookup"><span data-stu-id="efb75-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="efb75-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="efb75-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="efb75-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="efb75-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="efb75-108">Expose les propriétés utilisées pour filtrer la requête.</span><span class="sxs-lookup"><span data-stu-id="efb75-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="efb75-109">Membres</span><span class="sxs-lookup"><span data-stu-id="efb75-109">Members</span></span>

<span data-ttu-id="efb75-110">L’interface **IPropertyFilter** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="efb75-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="efb75-111">**IPropertyFilter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="efb75-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="efb75-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="efb75-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efb75-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="efb75-113">Properties</span></span>

<span data-ttu-id="efb75-114">L’interface **IPropertyFilter** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="efb75-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="efb75-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="efb75-115">Property</span></span>                                                                                      | <span data-ttu-id="efb75-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="efb75-116">Access type</span></span>           | <span data-ttu-id="efb75-117">Description</span><span class="sxs-lookup"><span data-stu-id="efb75-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="efb75-118">**IPropertyFilter::IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="efb75-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="efb75-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="efb75-119">Read/write</span></span><br/> | <span data-ttu-id="efb75-120">Nom de la colonne indexée de la propriété sur laquelle filtrer.</span><span class="sxs-lookup"><span data-stu-id="efb75-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="efb75-121">**IPropertyFilter::LogicOperator**</span><span class="sxs-lookup"><span data-stu-id="efb75-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="efb75-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="efb75-122">Read/write</span></span><br/> | <span data-ttu-id="efb75-123">Opérateur logique à utiliser lors de l’application d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="efb75-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="efb75-124">**IPropertyFilter::NestingDepth**</span><span class="sxs-lookup"><span data-stu-id="efb75-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="efb75-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="efb75-125">Read/write</span></span><br/> | <span data-ttu-id="efb75-126">Filtre la profondeur dans un ensemble imbriqué de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="efb75-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="efb75-127">**IPropertyFilter :: Text**</span><span class="sxs-lookup"><span data-stu-id="efb75-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="efb75-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="efb75-128">Read/write</span></span><br/> | <span data-ttu-id="efb75-129">Texte du filtre.</span><span class="sxs-lookup"><span data-stu-id="efb75-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="efb75-130">**IPropertyFilter :: UID**</span><span class="sxs-lookup"><span data-stu-id="efb75-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="efb75-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="efb75-131">Read/write</span></span><br/> | <span data-ttu-id="efb75-132">UID de la propriété sur laquelle filtrer.</span><span class="sxs-lookup"><span data-stu-id="efb75-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="efb75-133">Notes</span><span class="sxs-lookup"><span data-stu-id="efb75-133">Remarks</span></span>

<span data-ttu-id="efb75-134">Ces propriétés sont utilisées pour filtrer la requête.</span><span class="sxs-lookup"><span data-stu-id="efb75-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb75-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efb75-135">Requirements</span></span>



| <span data-ttu-id="efb75-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efb75-136">Requirement</span></span> | <span data-ttu-id="efb75-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="efb75-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb75-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb75-138">Minimum supported client</span></span><br/> | <span data-ttu-id="efb75-139">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb75-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="efb75-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb75-140">Minimum supported server</span></span><br/> | <span data-ttu-id="efb75-141">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb75-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="efb75-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="efb75-142">Redistributable</span></span><br/>          | <span data-ttu-id="efb75-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="efb75-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="efb75-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="efb75-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb75-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="efb75-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

