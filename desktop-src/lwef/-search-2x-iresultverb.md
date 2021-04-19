---
title: Interface IResultVerb (WdsSharedIDL. h)
description: Expose les propriétés de verbe.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultVerb
- Fonctionnalités d’environnement Windows héritées de l’interface IResultVerb, Description
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513615"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="d1202-105">Interface IResultVerb</span><span class="sxs-lookup"><span data-stu-id="d1202-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="d1202-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d1202-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d1202-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d1202-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d1202-108">Expose les propriétés de verbe.</span><span class="sxs-lookup"><span data-stu-id="d1202-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="d1202-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d1202-109">Members</span></span>

<span data-ttu-id="d1202-110">L’interface **IResultVerb** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d1202-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d1202-111">**IResultVerb** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1202-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="d1202-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1202-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1202-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1202-113">Properties</span></span>

<span data-ttu-id="d1202-114">L’interface **IResultVerb** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1202-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="d1202-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1202-115">Property</span></span>                                                             | <span data-ttu-id="d1202-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d1202-116">Access type</span></span>           | <span data-ttu-id="d1202-117">Description</span><span class="sxs-lookup"><span data-stu-id="d1202-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1202-118">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="d1202-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="d1202-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-119">Read-only</span></span><br/>  | <span data-ttu-id="d1202-120">Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="d1202-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="d1202-121">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="d1202-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="d1202-122">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-122">Write-only</span></span><br/> | <span data-ttu-id="d1202-123">Exécute le verbe.</span><span class="sxs-lookup"><span data-stu-id="d1202-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="d1202-124">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="d1202-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="d1202-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-125">Read-only</span></span><br/>  | <span data-ttu-id="d1202-126">Cette propriété retourne la valeur TRUE si le verbe est activé.</span><span class="sxs-lookup"><span data-stu-id="d1202-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="d1202-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="d1202-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="d1202-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-128">Read-only</span></span><br/>  | <span data-ttu-id="d1202-129">Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="d1202-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="d1202-130">**Icône**</span><span class="sxs-lookup"><span data-stu-id="d1202-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="d1202-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-131">Read-only</span></span><br/>  | <span data-ttu-id="d1202-132">Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.</span><span class="sxs-lookup"><span data-stu-id="d1202-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="d1202-133">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d1202-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="d1202-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1202-134">Read-only</span></span><br/>  | <span data-ttu-id="d1202-135">Cette propriété retourne un pointeur vers le nom de cononical pour le verbe, tel que imprimer, ouvrir, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d1202-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1202-136">Notes</span><span class="sxs-lookup"><span data-stu-id="d1202-136">Remarks</span></span>

<span data-ttu-id="d1202-137">Ces méthodes exposent les propriétés et les actions applicables aux verbes.</span><span class="sxs-lookup"><span data-stu-id="d1202-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1202-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1202-138">Requirements</span></span>



| <span data-ttu-id="d1202-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1202-139">Requirement</span></span> | <span data-ttu-id="d1202-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1202-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1202-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1202-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d1202-142">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1202-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1202-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1202-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d1202-144">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1202-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d1202-145">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d1202-145">Redistributable</span></span><br/>          | <span data-ttu-id="d1202-146">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d1202-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="d1202-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1202-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1202-148"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1202-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

