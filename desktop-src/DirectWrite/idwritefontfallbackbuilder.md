---
title: Interface IDWriteFontFallbackBuilder
description: Vous permet de créer des mappages de substitution de police Unicode et de créer une police qui revient à l’objet de ces mappages.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Écriture directe de l’interface IDWriteFontFallbackBuilder
- Écriture directe de l’interface IDWriteFontFallbackBuilder, décrite
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942364"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="893ad-105">Interface IDWriteFontFallbackBuilder</span><span class="sxs-lookup"><span data-stu-id="893ad-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="893ad-106">Vous permet de créer des mappages de substitution de police Unicode et de créer une police qui revient à l’objet de ces mappages.</span><span class="sxs-lookup"><span data-stu-id="893ad-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="893ad-107">Membres</span><span class="sxs-lookup"><span data-stu-id="893ad-107">Members</span></span>

<span data-ttu-id="893ad-108">L’interface **IDWriteFontFallbackBuilder** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="893ad-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="893ad-109">**IDWriteFontFallbackBuilder** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="893ad-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="893ad-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="893ad-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="893ad-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="893ad-111">Methods</span></span>

<span data-ttu-id="893ad-112">L’interface **IDWriteFontFallbackBuilder** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="893ad-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="893ad-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="893ad-113">Method</span></span>                                                                      | <span data-ttu-id="893ad-114">Description</span><span class="sxs-lookup"><span data-stu-id="893ad-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="893ad-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="893ad-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="893ad-116">Ajoute un mappage unique à la liste.</span><span class="sxs-lookup"><span data-stu-id="893ad-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="893ad-117">Appelez cette fois pour chaque mappage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="893ad-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="893ad-118">**AddMappings**</span><span class="sxs-lookup"><span data-stu-id="893ad-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="893ad-119">Ajoutez tous les mappages à partir d’un objet de police de secours existant.</span><span class="sxs-lookup"><span data-stu-id="893ad-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="893ad-120">**CreateFontFallback**</span><span class="sxs-lookup"><span data-stu-id="893ad-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="893ad-121">Crée l’objet de secours finalisé à partir des mappages ajoutés.</span><span class="sxs-lookup"><span data-stu-id="893ad-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="893ad-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="893ad-122">Requirements</span></span>



| <span data-ttu-id="893ad-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="893ad-123">Requirement</span></span> | <span data-ttu-id="893ad-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="893ad-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="893ad-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="893ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="893ad-126">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="893ad-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="893ad-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="893ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="893ad-128">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="893ad-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="893ad-129">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="893ad-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="893ad-130">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="893ad-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="893ad-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="893ad-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="893ad-132"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="893ad-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="893ad-133">DLL</span><span class="sxs-lookup"><span data-stu-id="893ad-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="893ad-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="893ad-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

