---
description: Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font :: GetGlyphData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532464"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="d9c05-103">ID3DX10Font :: GetGlyphData, méthode</span><span class="sxs-lookup"><span data-stu-id="d9c05-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="d9c05-104">Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="d9c05-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9c05-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="d9c05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c05-107">*Glyphe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9c05-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c05-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9c05-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9c05-109">Identificateur de glyphe.</span><span class="sxs-lookup"><span data-stu-id="d9c05-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d9c05-110">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d9c05-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c05-111">Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9c05-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="d9c05-112">Adresse d’un pointeur vers un objet ID3D10Texture qui contient le glyphe.</span><span class="sxs-lookup"><span data-stu-id="d9c05-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="d9c05-113">*pBlackBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9c05-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c05-114">Type : **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="d9c05-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="d9c05-115">Pointeur vers le plus petit objet rectangle qui englobe complètement le glyphe.</span><span class="sxs-lookup"><span data-stu-id="d9c05-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="d9c05-116">Consultez [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9c05-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9c05-117">*pCellInc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9c05-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c05-118">Type : **point \***</span><span class="sxs-lookup"><span data-stu-id="d9c05-118">Type: **POINT\***</span></span>

<span data-ttu-id="d9c05-119">Pointeur vers le vecteur à deux dimensions qui connecte l’origine de la cellule de caractère en cours à l’origine de la cellule de caractère suivante.</span><span class="sxs-lookup"><span data-stu-id="d9c05-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="d9c05-120">Consultez [point](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9c05-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c05-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9c05-121">Return value</span></span>

<span data-ttu-id="d9c05-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9c05-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9c05-123">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9c05-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d9c05-124">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="d9c05-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c05-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9c05-125">Requirements</span></span>



| <span data-ttu-id="d9c05-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9c05-126">Requirement</span></span> | <span data-ttu-id="d9c05-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9c05-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c05-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9c05-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d9c05-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9c05-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9c05-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9c05-130">Library</span></span><br/> | <dl> <span data-ttu-id="d9c05-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9c05-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c05-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9c05-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c05-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="d9c05-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="d9c05-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d9c05-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
