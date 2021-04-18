---
description: L’interface ID3DXFont encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interface ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520352"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="9b0d4-103">Interface ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="9b0d4-103">ID3DXFont interface</span></span>

<span data-ttu-id="9b0d4-104">L’interface ID3DXFont encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="9b0d4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9b0d4-105">Members</span></span>

<span data-ttu-id="9b0d4-106">L’interface **ID3DXFont** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9b0d4-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9b0d4-107">**ID3DXFont** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b0d4-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="9b0d4-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9b0d4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9b0d4-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9b0d4-109">Methods</span></span>

<span data-ttu-id="9b0d4-110">L’interface **ID3DXFont** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="9b0d4-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="9b0d4-111">Method</span></span>                                                    | <span data-ttu-id="9b0d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="9b0d4-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b0d4-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="9b0d4-114">Dessine du texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-114">Draws formatted text.</span></span> <span data-ttu-id="9b0d4-115">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="9b0d4-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="9b0d4-117">Retourne un handle vers un contexte de périphérique (DC) d’affichage dont la police est définie.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="9b0d4-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="9b0d4-119">Obtient une description de l’objet de police en cours.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-119">Gets a description of the current font object.</span></span> <span data-ttu-id="9b0d4-120">GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une structure [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ DESCA** , respectivement.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="9b0d4-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="9b0d4-122">Récupère le périphérique Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="9b0d4-123">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="9b0d4-124">Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="9b0d4-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="9b0d4-126">Récupère les caractéristiques de police qui sont identifiées dans une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="9b0d4-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="9b0d4-127">Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="9b0d4-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="9b0d4-129">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="9b0d4-130">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="9b0d4-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="9b0d4-132">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="9b0d4-133">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="9b0d4-134">Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="9b0d4-135">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="9b0d4-136">Charge une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9b0d4-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="9b0d4-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="9b0d4-138">Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="9b0d4-139">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b0d4-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="9b0d4-140">Notes</span><span class="sxs-lookup"><span data-stu-id="9b0d4-140">Remarks</span></span>

<span data-ttu-id="9b0d4-141">L’interface **ID3DXFont** est obtenue en appelant [**D3DXCreateFont**](d3dxcreatefont.md) ou [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="9b0d4-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="9b0d4-142">Le type LPD3DXFONT est défini comme un pointeur vers l’interface **ID3DXFont** .</span><span class="sxs-lookup"><span data-stu-id="9b0d4-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="9b0d4-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b0d4-143">Requirements</span></span>



| <span data-ttu-id="9b0d4-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b0d4-144">Requirement</span></span> | <span data-ttu-id="9b0d4-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b0d4-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0d4-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b0d4-146">Header</span></span><br/>  | <dl> <span data-ttu-id="9b0d4-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d4-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9b0d4-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9b0d4-148">Library</span></span><br/> | <dl> <span data-ttu-id="9b0d4-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d4-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b0d4-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b0d4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0d4-151">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9b0d4-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
