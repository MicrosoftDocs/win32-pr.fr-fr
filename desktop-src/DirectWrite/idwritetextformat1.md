---
title: Interface IDWriteTextFormat1
description: Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. | Interface IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Écriture directe de l’interface IDWriteTextFormat1
- Écriture directe de l’interface IDWriteTextFormat1, décrite
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522526"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="797af-106">Interface IDWriteTextFormat1</span><span class="sxs-lookup"><span data-stu-id="797af-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="797af-107">Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="797af-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="797af-108">Cette interface a les mêmes méthodes que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et ajoute la possibilité d’appliquer une orientation explicite.</span><span class="sxs-lookup"><span data-stu-id="797af-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="797af-109">Membres</span><span class="sxs-lookup"><span data-stu-id="797af-109">Members</span></span>

<span data-ttu-id="797af-110">L’interface **IDWriteTextFormat1** hérite de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="797af-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="797af-111">**IDWriteTextFormat1** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="797af-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="797af-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="797af-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="797af-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="797af-113">Methods</span></span>

<span data-ttu-id="797af-114">L’interface **IDWriteTextFormat1** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="797af-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="797af-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="797af-115">Method</span></span>                                                                                | <span data-ttu-id="797af-116">Description</span><span class="sxs-lookup"><span data-stu-id="797af-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="797af-117">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="797af-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="797af-118">Obtient le de secours actuel.</span><span class="sxs-lookup"><span data-stu-id="797af-118">Gets the current fallback.</span></span> <span data-ttu-id="797af-119">Si aucun n’a été défini depuis la création de la disposition, il sera nullptr.</span><span class="sxs-lookup"><span data-stu-id="797af-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="797af-120">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="797af-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="797af-121">Obtient le mode d’habillage de la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="797af-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="797af-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="797af-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="797af-123">Obtient l’alignement de la marge optique pour le format texte.</span><span class="sxs-lookup"><span data-stu-id="797af-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="797af-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="797af-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="797af-125">Obtenir l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.</span><span class="sxs-lookup"><span data-stu-id="797af-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="797af-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="797af-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="797af-127">Applique la police de secours personnalisée à la disposition.</span><span class="sxs-lookup"><span data-stu-id="797af-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="797af-128">Si aucune valeur n’est définie, elle utilise la liste de secours système par défaut.</span><span class="sxs-lookup"><span data-stu-id="797af-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="797af-129">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="797af-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="797af-130">Définit le mode d’habillage de la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="797af-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="797af-131">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="797af-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="797af-132">Définit l’alignement de la marge optique pour le format texte.</span><span class="sxs-lookup"><span data-stu-id="797af-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="797af-133">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="797af-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="797af-134">Définit l’orientation d’un format de texte.</span><span class="sxs-lookup"><span data-stu-id="797af-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="797af-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="797af-135">Requirements</span></span>



| <span data-ttu-id="797af-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="797af-136">Requirement</span></span> | <span data-ttu-id="797af-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="797af-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="797af-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="797af-138">Minimum supported client</span></span><br/> | <span data-ttu-id="797af-139">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="797af-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="797af-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="797af-140">Minimum supported server</span></span><br/> | <span data-ttu-id="797af-141">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="797af-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="797af-142">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="797af-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="797af-143">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="797af-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="797af-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="797af-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="797af-145"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="797af-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="797af-146">DLL</span><span class="sxs-lookup"><span data-stu-id="797af-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="797af-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="797af-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="797af-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="797af-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797af-149">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="797af-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

