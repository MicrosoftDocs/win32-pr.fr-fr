---
title: Interface IResultType (WdsSharedIDL. h)
description: Expose les informations sur le type de propriété.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultType
- Fonctionnalités d’environnement Windows héritées de l’interface IResultType, Description
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464915"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="30669-105">Interface IResultType</span><span class="sxs-lookup"><span data-stu-id="30669-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="30669-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="30669-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="30669-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="30669-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="30669-108">Expose les informations sur le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="30669-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="30669-109">Membres</span><span class="sxs-lookup"><span data-stu-id="30669-109">Members</span></span>

<span data-ttu-id="30669-110">L’interface **IResultType** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="30669-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="30669-111">**IResultType** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="30669-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="30669-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30669-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30669-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30669-113">Properties</span></span>

<span data-ttu-id="30669-114">L’interface **IResultType** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="30669-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="30669-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="30669-115">Property</span></span>                                                                 | <span data-ttu-id="30669-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="30669-116">Access type</span></span>           | <span data-ttu-id="30669-117">Description</span><span class="sxs-lookup"><span data-stu-id="30669-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="30669-118">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="30669-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="30669-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30669-119">Read-only</span></span><br/>  | <span data-ttu-id="30669-120">Nom complet localisé du type :</span><span class="sxs-lookup"><span data-stu-id="30669-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="30669-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="30669-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="30669-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="30669-122">Read/write</span></span><br/> | <span data-ttu-id="30669-123">Cette propriété contient les informations de propriété spécifiées.</span><span class="sxs-lookup"><span data-stu-id="30669-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="30669-124">**PreceivedType**</span><span class="sxs-lookup"><span data-stu-id="30669-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="30669-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30669-125">Read-only</span></span><br/>  | <span data-ttu-id="30669-126">Cette propriété contient la chaîne utilisée pour identifier le type dans l’index.</span><span class="sxs-lookup"><span data-stu-id="30669-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="30669-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="30669-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="30669-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30669-128">Read-only</span></span><br/>  | <span data-ttu-id="30669-129">Cette propriété contient le nombre de propriétés exposées par le type.</span><span class="sxs-lookup"><span data-stu-id="30669-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="30669-130">**Identificateur d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="30669-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="30669-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30669-131">Read-only</span></span><br/>  | <span data-ttu-id="30669-132">Cette propriété contient l’identificateur unique pour le type.</span><span class="sxs-lookup"><span data-stu-id="30669-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="30669-133">Notes</span><span class="sxs-lookup"><span data-stu-id="30669-133">Remarks</span></span>

<span data-ttu-id="30669-134">Ces méthodes exposent les types d’informations retournées.</span><span class="sxs-lookup"><span data-stu-id="30669-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="30669-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30669-135">Requirements</span></span>



| <span data-ttu-id="30669-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30669-136">Requirement</span></span> | <span data-ttu-id="30669-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="30669-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30669-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30669-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30669-139">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30669-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="30669-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30669-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30669-141">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30669-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="30669-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="30669-142">Redistributable</span></span><br/>          | <span data-ttu-id="30669-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="30669-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="30669-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="30669-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="30669-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="30669-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

