---
description: Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont :: GetGlyphData, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524853"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="2763b-103">ID3DXFont :: GetGlyphData, méthode</span><span class="sxs-lookup"><span data-stu-id="2763b-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="2763b-104">Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="2763b-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="2763b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2763b-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="2763b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2763b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2763b-107">*Glyphe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2763b-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2763b-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2763b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2763b-109">Identificateur de glyphe.</span><span class="sxs-lookup"><span data-stu-id="2763b-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2763b-110">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2763b-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2763b-111">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2763b-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="2763b-112">Adresse d’un pointeur vers un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui contient le glyphe.</span><span class="sxs-lookup"><span data-stu-id="2763b-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="2763b-113">*pBlackBox* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2763b-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2763b-114">Type : **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="2763b-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="2763b-115">Pointeur vers le plus petit objet rectangle qui englobe complètement le glyphe.</span><span class="sxs-lookup"><span data-stu-id="2763b-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="2763b-116">*pCellInc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2763b-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2763b-117">Type : **[ **point**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2763b-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2763b-118">Pointeur vers le vecteur à deux dimensions qui connecte l’origine de la cellule de caractère en cours à l’origine de la cellule de caractère suivante.</span><span class="sxs-lookup"><span data-stu-id="2763b-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="2763b-119">Consultez [**point**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="2763b-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2763b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2763b-120">Return value</span></span>

<span data-ttu-id="2763b-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2763b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2763b-122">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2763b-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2763b-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="2763b-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="2763b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2763b-124">Requirements</span></span>



| <span data-ttu-id="2763b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2763b-125">Requirement</span></span> | <span data-ttu-id="2763b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2763b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2763b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2763b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2763b-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2763b-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2763b-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2763b-129">Library</span></span><br/> | <dl> <span data-ttu-id="2763b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2763b-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2763b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2763b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2763b-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="2763b-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
