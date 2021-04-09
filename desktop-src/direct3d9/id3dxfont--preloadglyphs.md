---
description: Charge une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: ID3DXFont ::P méthode reloadGlyphs (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043180"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="b791e-103">ID3DXFont ::P méthode reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="b791e-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="b791e-104">Charge une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b791e-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b791e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b791e-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="b791e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b791e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b791e-107">*Premier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b791e-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b791e-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b791e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b791e-109">ID du premier glyphe à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="b791e-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b791e-110">*Dernière* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b791e-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b791e-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b791e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b791e-112">ID du dernier glyphe à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="b791e-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b791e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b791e-113">Return value</span></span>

<span data-ttu-id="b791e-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b791e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b791e-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b791e-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b791e-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="b791e-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b791e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b791e-117">Remarks</span></span>

<span data-ttu-id="b791e-118">Cette méthode génère des textures qui contiennent les glyphes d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b791e-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="b791e-119">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="b791e-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="b791e-120">Les glyphes ne seront pas rendus à l’appareil ; [**DrawText**](id3dxfont--drawtext.md) doit encore être appelé pour restituer les glyphes.</span><span class="sxs-lookup"><span data-stu-id="b791e-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="b791e-121">Toutefois, en préchargeant les glyphes dans la mémoire vidéo, **DrawText** utilise beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="b791e-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="b791e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b791e-122">Requirements</span></span>



| <span data-ttu-id="b791e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b791e-123">Requirement</span></span> | <span data-ttu-id="b791e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b791e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b791e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b791e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b791e-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b791e-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b791e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b791e-127">Library</span></span><br/> | <dl> <span data-ttu-id="b791e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b791e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b791e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b791e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b791e-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="b791e-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
