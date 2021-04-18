---
title: Interface IDWriteFactory2
description: Interface de fabrique racine pour tous les objets DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Écriture directe de l’interface IDWriteFactory1
- Écriture directe de l’interface IDWriteFactory1, décrite
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511780"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="fe333-105">Interface IDWriteFactory2</span><span class="sxs-lookup"><span data-stu-id="fe333-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="fe333-106">Interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fe333-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="fe333-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fe333-107">Members</span></span>

<span data-ttu-id="fe333-108">L’interface **IDWriteFactory1** hérite de [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="fe333-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="fe333-109">**IDWriteFactory2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fe333-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="fe333-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fe333-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe333-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fe333-111">Methods</span></span>

<span data-ttu-id="fe333-112">L’interface **IDWriteFactory1** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fe333-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="fe333-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="fe333-113">Method</span></span>                                                                             | <span data-ttu-id="fe333-114">Description</span><span class="sxs-lookup"><span data-stu-id="fe333-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe333-115">**CreateCustomRenderingParams**</span><span class="sxs-lookup"><span data-stu-id="fe333-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="fe333-116">Crée un objet de paramètres de rendu avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe333-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="fe333-117">**CreateFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="fe333-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="fe333-118">Crée un objet de générateur de polices de substitution.</span><span class="sxs-lookup"><span data-stu-id="fe333-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="fe333-119">**CreateGlyphRunAnalysis**</span><span class="sxs-lookup"><span data-stu-id="fe333-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="fe333-120">Crée un objet d’analyse de série de glyphes, qui encapsule les informations utilisées pour restituer une exécution de glyphe.</span><span class="sxs-lookup"><span data-stu-id="fe333-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="fe333-121">**GetSystemFontFallback**</span><span class="sxs-lookup"><span data-stu-id="fe333-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="fe333-122">Crée un objet de police de secours à partir de la liste des polices système de secours.</span><span class="sxs-lookup"><span data-stu-id="fe333-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="fe333-123">**TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="fe333-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="fe333-124">Cette méthode est appelée sur une exécution de glyphe pour la traduire en plusieurs exécutions de glyphes de couleurs.</span><span class="sxs-lookup"><span data-stu-id="fe333-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="fe333-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe333-125">Requirements</span></span>



| <span data-ttu-id="fe333-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe333-126">Requirement</span></span> | <span data-ttu-id="fe333-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe333-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe333-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe333-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe333-129">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fe333-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="fe333-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe333-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe333-131">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fe333-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fe333-132">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe333-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="fe333-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="fe333-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="fe333-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe333-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe333-135"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe333-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fe333-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fe333-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe333-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe333-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe333-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe333-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe333-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="fe333-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="fe333-140">**IDWriteFactory**</span><span class="sxs-lookup"><span data-stu-id="fe333-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

