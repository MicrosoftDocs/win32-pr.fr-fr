---
description: 'Fonction D3DXFillTextureTX : utilise une fonction de nuanceur de niveau supérieur (HLSL) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.'
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: D3DXFillTextureTX, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107637"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="daf42-103">D3DXFillTextureTX fonction)</span><span class="sxs-lookup"><span data-stu-id="daf42-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="daf42-104">Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.</span><span class="sxs-lookup"><span data-stu-id="daf42-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daf42-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="daf42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf42-107">*pTexture* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="daf42-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="daf42-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="daf42-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="daf42-109">Pointeur vers un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant la texture à remplir.</span><span class="sxs-lookup"><span data-stu-id="daf42-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="daf42-110">*pTextureShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="daf42-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daf42-111">Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="daf42-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="daf42-112">Pointeur vers un objet de nuanceur de texture [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="daf42-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf42-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="daf42-113">Return value</span></span>

<span data-ttu-id="daf42-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="daf42-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="daf42-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="daf42-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="daf42-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="daf42-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf42-117">Notes </span><span class="sxs-lookup"><span data-stu-id="daf42-117">Remarks</span></span>

<span data-ttu-id="daf42-118">La cible de la texture doit être une fonction HLSL qui prend la sémantique suivante :</span><span class="sxs-lookup"><span data-stu-id="daf42-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="daf42-119">Un paramètre d’entrée doit utiliser une sémantique de POSITION.</span><span class="sxs-lookup"><span data-stu-id="daf42-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="daf42-120">Un paramètre d’entrée doit utiliser une sémantique PSIZE.</span><span class="sxs-lookup"><span data-stu-id="daf42-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="daf42-121">La fonction doit retourner un paramètre qui utilise la sémantique de couleur.</span><span class="sxs-lookup"><span data-stu-id="daf42-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="daf42-122">Voici un exemple d’une telle fonction HLSL :</span><span class="sxs-lookup"><span data-stu-id="daf42-122">The following is an example of such an HLSL function:</span></span>


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



<span data-ttu-id="daf42-123">Notez que les paramètres d’entrée peuvent être dans n’importe quel ordre, mais que les deux sémantiques d’entrée doivent être représentées.</span><span class="sxs-lookup"><span data-stu-id="daf42-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf42-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daf42-124">Requirements</span></span>



| <span data-ttu-id="daf42-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daf42-125">Requirement</span></span> | <span data-ttu-id="daf42-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="daf42-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daf42-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="daf42-127">Header</span></span><br/>  | <dl> <span data-ttu-id="daf42-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf42-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="daf42-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="daf42-129">Library</span></span><br/> | <dl> <span data-ttu-id="daf42-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="daf42-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="daf42-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf42-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf42-132">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="daf42-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="daf42-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="daf42-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="daf42-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="daf42-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
