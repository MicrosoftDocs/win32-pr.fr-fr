---
description: Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: D3DXFillCubeTextureTX, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37a831ef95d50f9b0389be0f1c9937e46748f6d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762049"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="c7e7b-103">D3DXFillCubeTextureTX fonction)</span><span class="sxs-lookup"><span data-stu-id="c7e7b-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="c7e7b-104">Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7e7b-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="c7e7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7e7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e7b-107">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7e7b-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e7b-108">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c7e7b-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="c7e7b-109">Pointeur vers un objet [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) représentant la texture à remplir.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="c7e7b-110">*pTextureShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7e7b-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e7b-111">Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="c7e7b-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="c7e7b-112">Pointeur vers un objet de nuanceur de texture [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e7b-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e7b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7e7b-113">Return value</span></span>

<span data-ttu-id="c7e7b-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7e7b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7e7b-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c7e7b-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e7b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c7e7b-117">Remarks</span></span>

<span data-ttu-id="c7e7b-118">La cible de la texture doit être une fonction HLSL qui prend la sémantique suivante :</span><span class="sxs-lookup"><span data-stu-id="c7e7b-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="c7e7b-119">Un paramètre d’entrée doit utiliser une sémantique de POSITION.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="c7e7b-120">Un paramètre d’entrée doit utiliser une sémantique PSIZE.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="c7e7b-121">La fonction doit retourner un paramètre qui utilise la sémantique de couleur.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="c7e7b-122">Les paramètres d’entrée peuvent être dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="c7e7b-122">The input parameters can be in any order.</span></span> <span data-ttu-id="c7e7b-123">Pour obtenir un exemple, consultez [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="c7e7b-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e7b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7e7b-124">Requirements</span></span>



| <span data-ttu-id="c7e7b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7e7b-125">Requirement</span></span> | <span data-ttu-id="c7e7b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7e7b-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e7b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7e7b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c7e7b-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e7b-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c7e7b-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7e7b-129">Library</span></span><br/> | <dl> <span data-ttu-id="c7e7b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7e7b-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7e7b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7e7b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e7b-132">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c7e7b-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="c7e7b-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="c7e7b-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
