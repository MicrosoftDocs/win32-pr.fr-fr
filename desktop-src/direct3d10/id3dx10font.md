---
description: L’interface ID3DX10Font encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interface ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211782"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="0e525-103">Interface ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="0e525-103">ID3DX10Font interface</span></span>

<span data-ttu-id="0e525-104">L’interface ID3DX10Font encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="0e525-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="0e525-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0e525-105">Members</span></span>

<span data-ttu-id="0e525-106">L’interface **ID3DX10Font** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0e525-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0e525-107">**ID3DX10Font** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e525-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="0e525-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e525-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e525-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e525-109">Methods</span></span>

<span data-ttu-id="0e525-110">L’interface **ID3DX10Font** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e525-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="0e525-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e525-111">Method</span></span>                                                     | <span data-ttu-id="0e525-112">Description</span><span class="sxs-lookup"><span data-stu-id="0e525-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e525-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="0e525-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="0e525-114">Dessinez du texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="0e525-114">Draw formatted text.</span></span> <span data-ttu-id="0e525-115">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e525-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="0e525-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="0e525-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="0e525-117">Retourne un handle vers un contexte de périphérique (DC) d’affichage sur lequel la police est définie.</span><span class="sxs-lookup"><span data-stu-id="0e525-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="0e525-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="0e525-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="0e525-119">Obtient une description de l’objet de police en cours.</span><span class="sxs-lookup"><span data-stu-id="0e525-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0e525-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="0e525-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="0e525-121">Récupérez l’appareil Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="0e525-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="0e525-122">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="0e525-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="0e525-123">Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="0e525-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="0e525-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="0e525-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="0e525-125">Récupérez les caractéristiques de police.</span><span class="sxs-lookup"><span data-stu-id="0e525-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="0e525-126">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="0e525-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="0e525-127">Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e525-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="0e525-128">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="0e525-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="0e525-129">Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e525-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="0e525-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="0e525-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="0e525-131">Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e525-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="0e525-132">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e525-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e525-133">Notes</span><span class="sxs-lookup"><span data-stu-id="0e525-133">Remarks</span></span>

<span data-ttu-id="0e525-134">L’interface ID3DX10Font est obtenue en appelant [**D3DX10CreateFont**](d3dx10createfont.md) ou [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="0e525-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="0e525-135">Le type LPD3DX10FONT est défini comme un pointeur vers l’interface ID3DX10Font.</span><span class="sxs-lookup"><span data-stu-id="0e525-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="0e525-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e525-136">Requirements</span></span>



| <span data-ttu-id="0e525-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e525-137">Requirement</span></span> | <span data-ttu-id="0e525-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e525-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e525-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e525-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0e525-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e525-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e525-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e525-141">Library</span></span><br/> | <dl> <span data-ttu-id="0e525-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e525-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e525-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e525-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e525-144">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0e525-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
