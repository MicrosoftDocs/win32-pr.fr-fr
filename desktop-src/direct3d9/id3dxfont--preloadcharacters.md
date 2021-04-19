---
description: Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: ID3DXFont ::P méthode reloadCharacters (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527954"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="10a6a-103">ID3DXFont ::P méthode reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="10a6a-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="10a6a-104">Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10a6a-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10a6a-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="10a6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10a6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a6a-107">*Premier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10a6a-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10a6a-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10a6a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10a6a-109">ID du premier caractère à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="10a6a-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="10a6a-110">*Dernière* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10a6a-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10a6a-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10a6a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10a6a-112">ID du dernier caractère à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="10a6a-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a6a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10a6a-113">Return value</span></span>

<span data-ttu-id="10a6a-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="10a6a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="10a6a-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10a6a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="10a6a-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="10a6a-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="10a6a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="10a6a-117">Remarks</span></span>

<span data-ttu-id="10a6a-118">Cette méthode génère des textures contenant des glyphes qui représentent les caractères d’entrée.</span><span class="sxs-lookup"><span data-stu-id="10a6a-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="10a6a-119">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="10a6a-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="10a6a-120">Les caractères ne sont pas rendus à l’appareil ; [**DrawText**](id3dxfont--drawtext.md) doit toujours être appelé pour restituer les caractères.</span><span class="sxs-lookup"><span data-stu-id="10a6a-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="10a6a-121">Toutefois, en préchargeant les caractères dans la mémoire vidéo, **DrawText** utilise beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="10a6a-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="10a6a-122">Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="10a6a-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="10a6a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10a6a-123">Requirements</span></span>



| <span data-ttu-id="10a6a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10a6a-124">Requirement</span></span> | <span data-ttu-id="10a6a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="10a6a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10a6a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="10a6a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="10a6a-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="10a6a-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="10a6a-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10a6a-128">Library</span></span><br/> | <dl> <span data-ttu-id="10a6a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10a6a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10a6a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a6a-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="10a6a-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
