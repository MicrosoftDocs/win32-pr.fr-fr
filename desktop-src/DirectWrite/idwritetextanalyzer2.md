---
title: Interface IDWriteTextAnalyzer2
description: Analyse diverses propriétés de texte pour le traitement complexe des scripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Écriture directe de l’interface IDWriteTextAnalyzer2
- Écriture directe de l’interface IDWriteTextAnalyzer2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508794"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="c9464-105">Interface IDWriteTextAnalyzer2</span><span class="sxs-lookup"><span data-stu-id="c9464-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="c9464-106">Analyse diverses propriétés de texte pour le traitement complexe des scripts.</span><span class="sxs-lookup"><span data-stu-id="c9464-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="c9464-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c9464-107">Members</span></span>

<span data-ttu-id="c9464-108">L’interface **IDWriteTextAnalyzer2** hérite de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="c9464-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="c9464-109">**IDWriteTextAnalyzer2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9464-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="c9464-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9464-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9464-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9464-111">Methods</span></span>

<span data-ttu-id="c9464-112">L’interface **IDWriteTextAnalyzer2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c9464-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="c9464-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c9464-113">Method</span></span>                                                                                    | <span data-ttu-id="c9464-114">Description</span><span class="sxs-lookup"><span data-stu-id="c9464-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9464-115">**CheckTypographicFeature**</span><span class="sxs-lookup"><span data-stu-id="c9464-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="c9464-116">Vérifie si une fonctionnalité typographique est disponible pour un glyphe ou un ensemble de glyphes.</span><span class="sxs-lookup"><span data-stu-id="c9464-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="c9464-117">**GetGlyphOrientationTransform**</span><span class="sxs-lookup"><span data-stu-id="c9464-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="c9464-118">Retourne la matrice de transformation 2x3 pour l’angle respectif de dessin de l’exécution du glyphe.</span><span class="sxs-lookup"><span data-stu-id="c9464-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="c9464-119">**GetTypographicFeatures**</span><span class="sxs-lookup"><span data-stu-id="c9464-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="c9464-120">Retourne la liste complète des fonctionnalités OpenType disponibles pour un script ou une police.</span><span class="sxs-lookup"><span data-stu-id="c9464-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9464-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9464-121">Requirements</span></span>



| <span data-ttu-id="c9464-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9464-122">Requirement</span></span> | <span data-ttu-id="c9464-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9464-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9464-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9464-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9464-125">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c9464-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c9464-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9464-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9464-127">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c9464-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c9464-128">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9464-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c9464-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c9464-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c9464-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9464-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9464-131"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9464-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c9464-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c9464-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9464-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9464-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9464-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9464-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9464-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="c9464-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

