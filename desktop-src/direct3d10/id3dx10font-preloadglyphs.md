---
description: Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font ::P méthode reloadGlyphs (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532445"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="4f49c-103">ID3DX10Font ::P méthode reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="4f49c-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="4f49c-104">Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f49c-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f49c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f49c-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="4f49c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f49c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f49c-107">*Premier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f49c-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f49c-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f49c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f49c-109">ID du premier glyphe à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="4f49c-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4f49c-110">*Dernière* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f49c-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f49c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f49c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f49c-112">ID du dernier glyphe à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="4f49c-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f49c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f49c-113">Return value</span></span>

<span data-ttu-id="4f49c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f49c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f49c-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f49c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4f49c-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="4f49c-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f49c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4f49c-117">Remarks</span></span>

<span data-ttu-id="4f49c-118">Cette méthode génère des textures qui contiennent les glyphes d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4f49c-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="4f49c-119">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="4f49c-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="4f49c-120">Les glyphes ne seront pas rendus à l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer les glyphes.</span><span class="sxs-lookup"><span data-stu-id="4f49c-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="4f49c-121">Toutefois, en préchargeant les glyphes dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="4f49c-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f49c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f49c-122">Requirements</span></span>



| <span data-ttu-id="4f49c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f49c-123">Requirement</span></span> | <span data-ttu-id="4f49c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f49c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f49c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f49c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f49c-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f49c-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f49c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f49c-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f49c-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f49c-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f49c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f49c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f49c-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="4f49c-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="4f49c-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4f49c-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
