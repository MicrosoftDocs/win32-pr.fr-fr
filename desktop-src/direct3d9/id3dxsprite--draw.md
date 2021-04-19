---
description: Ajoute un sprite à la liste des sprites regroupés par lots.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite ::D méthode brute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537284"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="821ad-103">ID3DXSprite ::D méthode brute</span><span class="sxs-lookup"><span data-stu-id="821ad-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="821ad-104">Ajoute un sprite à la liste des sprites regroupés par lots.</span><span class="sxs-lookup"><span data-stu-id="821ad-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="821ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="821ad-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="821ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="821ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="821ad-107">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821ad-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821ad-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="821ad-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="821ad-109">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture du sprite.</span><span class="sxs-lookup"><span data-stu-id="821ad-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="821ad-110">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821ad-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821ad-111">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="821ad-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="821ad-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui indique la partie de la texture source à utiliser pour le sprite.</span><span class="sxs-lookup"><span data-stu-id="821ad-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="821ad-113">Si ce paramètre a la **valeur null**, la totalité de l’image source est utilisée pour le sprite.</span><span class="sxs-lookup"><span data-stu-id="821ad-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="821ad-114">*pCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821ad-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821ad-115">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="821ad-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="821ad-116">Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui identifie le centre du sprite.</span><span class="sxs-lookup"><span data-stu-id="821ad-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="821ad-117">Si cet argument a la **valeur null**, le point (0, 0, 0) est utilisé, qui est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="821ad-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="821ad-118">*pPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821ad-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821ad-119">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="821ad-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="821ad-120">Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui identifie la position du sprite.</span><span class="sxs-lookup"><span data-stu-id="821ad-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="821ad-121">Si cet argument a la **valeur null**, le point (0, 0, 0) est utilisé, qui est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="821ad-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="821ad-122">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821ad-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821ad-123">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="821ad-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="821ad-124">Type de [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="821ad-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="821ad-125">La couleur et les canaux alpha sont modulés par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="821ad-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="821ad-126">La valeur 0xFFFFFFFF conserve la couleur source d’origine et les données alpha.</span><span class="sxs-lookup"><span data-stu-id="821ad-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="821ad-127">Utilisez la macro [**D3DCOLOR \_ RVBA**](d3dcolor-rgba.md) pour aider à générer cette couleur.</span><span class="sxs-lookup"><span data-stu-id="821ad-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="821ad-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="821ad-128">Return value</span></span>

<span data-ttu-id="821ad-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="821ad-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="821ad-130">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="821ad-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="821ad-131">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="821ad-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="821ad-132">Notes</span><span class="sxs-lookup"><span data-stu-id="821ad-132">Remarks</span></span>

<span data-ttu-id="821ad-133">Pour mettre à l’échelle, faire pivoter ou traduire un sprite, appelez [**ID3DXSprite :: setTransform**](id3dxsprite--settransform.md) avec une matrice qui contient les valeurs d’échelle, de rotation et de translation (SRT), avant d’appeler ID3DXSprite ::D RAW.</span><span class="sxs-lookup"><span data-stu-id="821ad-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="821ad-134">Pour plus d’informations sur la définition de valeurs SRT dans une matrice, consultez [transformations de matrice](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="821ad-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="821ad-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="821ad-135">Requirements</span></span>



| <span data-ttu-id="821ad-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="821ad-136">Requirement</span></span> | <span data-ttu-id="821ad-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="821ad-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="821ad-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="821ad-138">Header</span></span><br/>  | <dl> <span data-ttu-id="821ad-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="821ad-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="821ad-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="821ad-140">Library</span></span><br/> | <dl> <span data-ttu-id="821ad-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="821ad-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="821ad-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="821ad-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821ad-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="821ad-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="821ad-144">**ID3DXSprite::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="821ad-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
