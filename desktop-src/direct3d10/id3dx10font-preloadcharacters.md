---
description: Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: ID3DX10Font ::P méthode reloadCharacters (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538338"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="6badf-103">ID3DX10Font ::P méthode reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="6badf-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="6badf-104">Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6badf-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6badf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6badf-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="6badf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6badf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6badf-107">*Premier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6badf-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6badf-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6badf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6badf-109">ID du premier caractère à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="6badf-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="6badf-110">*Dernière* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6badf-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6badf-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6badf-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6badf-112">ID du dernier caractère à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="6badf-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6badf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6badf-113">Return value</span></span>

<span data-ttu-id="6badf-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6badf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6badf-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6badf-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6badf-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="6badf-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6badf-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6badf-117">Remarks</span></span>

<span data-ttu-id="6badf-118">Cette méthode génère des textures contenant des glyphes qui représentent les caractères d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6badf-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="6badf-119">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="6badf-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="6badf-120">Les caractères ne sont pas rendus à l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer les caractères.</span><span class="sxs-lookup"><span data-stu-id="6badf-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="6badf-121">Toutefois, en préchargeant les caractères dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="6badf-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="6badf-122">Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6badf-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6badf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6badf-123">Requirements</span></span>



| <span data-ttu-id="6badf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6badf-124">Requirement</span></span> | <span data-ttu-id="6badf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6badf-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6badf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6badf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6badf-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6badf-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6badf-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6badf-128">Library</span></span><br/> | <dl> <span data-ttu-id="6badf-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6badf-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6badf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6badf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6badf-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="6badf-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="6badf-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6badf-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
