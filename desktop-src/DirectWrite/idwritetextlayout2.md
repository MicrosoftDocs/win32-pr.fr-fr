---
title: Interface IDWriteTextLayout2
description: Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. | Interface IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Écriture directe de l’interface IDWriteTextLayout2
- Écriture directe de l’interface IDWriteTextLayout2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322289"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="d4b70-106">Interface IDWriteTextLayout2</span><span class="sxs-lookup"><span data-stu-id="d4b70-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="d4b70-107">Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme.</span><span class="sxs-lookup"><span data-stu-id="d4b70-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="d4b70-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d4b70-108">Members</span></span>

<span data-ttu-id="d4b70-109">L’interface **IDWriteTextLayout2** hérite de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="d4b70-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="d4b70-110">**IDWriteTextLayout2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d4b70-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="d4b70-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4b70-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4b70-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4b70-112">Methods</span></span>

<span data-ttu-id="d4b70-113">L’interface **IDWriteTextLayout2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d4b70-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="d4b70-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d4b70-114">Method</span></span>                                                                                | <span data-ttu-id="d4b70-115">Description</span><span class="sxs-lookup"><span data-stu-id="d4b70-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b70-116">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="d4b70-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="d4b70-117">Obtient l’objet de police de secours actuel.</span><span class="sxs-lookup"><span data-stu-id="d4b70-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="d4b70-118">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="d4b70-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="d4b70-119">Déterminez si le dernier mot sur la dernière ligne est renvoyé à la ligne.</span><span class="sxs-lookup"><span data-stu-id="d4b70-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="d4b70-120">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="d4b70-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="d4b70-121">Récupère les métriques globales de la chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="d4b70-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="d4b70-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="d4b70-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="d4b70-123">Obtient la manière dont les glyphes s’alignent sur les bords de la marge.</span><span class="sxs-lookup"><span data-stu-id="d4b70-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="d4b70-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="d4b70-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="d4b70-125">Obtenir l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.</span><span class="sxs-lookup"><span data-stu-id="d4b70-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="d4b70-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="d4b70-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="d4b70-127">Appliquez une police de secours personnalisée à la disposition.</span><span class="sxs-lookup"><span data-stu-id="d4b70-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="d4b70-128">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="d4b70-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="d4b70-129">Définit si le dernier mot sur la dernière ligne est renvoyé à la ligne.</span><span class="sxs-lookup"><span data-stu-id="d4b70-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="d4b70-130">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="d4b70-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="d4b70-131">Définissez la façon dont les glyphes s’alignent sur les bords de la marge.</span><span class="sxs-lookup"><span data-stu-id="d4b70-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="d4b70-132">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="d4b70-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="d4b70-133">Définissez l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.</span><span class="sxs-lookup"><span data-stu-id="d4b70-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d4b70-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4b70-134">Requirements</span></span>



| <span data-ttu-id="d4b70-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4b70-135">Requirement</span></span> | <span data-ttu-id="d4b70-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4b70-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b70-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4b70-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b70-138">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d4b70-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d4b70-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4b70-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b70-140">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d4b70-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d4b70-141">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4b70-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d4b70-142">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="d4b70-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d4b70-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4b70-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4b70-144"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4b70-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d4b70-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b70-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4b70-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b70-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4b70-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4b70-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b70-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="d4b70-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

