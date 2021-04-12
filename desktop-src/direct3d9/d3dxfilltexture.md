---
description: Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture donnée.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: D3DXFillTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322922"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="b10c1-103">D3DXFillTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="b10c1-103">D3DXFillTexture function</span></span>

<span data-ttu-id="b10c1-104">Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture donnée.</span><span class="sxs-lookup"><span data-stu-id="b10c1-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b10c1-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="b10c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b10c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b10c1-107">*pTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b10c1-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b10c1-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="b10c1-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="b10c1-109">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant la texture remplie.</span><span class="sxs-lookup"><span data-stu-id="b10c1-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="b10c1-110">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b10c1-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10c1-111">Type : **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="b10c1-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="b10c1-112">Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="b10c1-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="b10c1-113">La fonction suit le prototype de [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="b10c1-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="b10c1-114">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b10c1-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10c1-115">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b10c1-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b10c1-116">Pointeur vers un bloc arbitraire de données définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b10c1-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="b10c1-117">Ce pointeur sera passé à la fonction fournie dans *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="b10c1-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b10c1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b10c1-118">Return value</span></span>

<span data-ttu-id="b10c1-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b10c1-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b10c1-120">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b10c1-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b10c1-121">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b10c1-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b10c1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b10c1-122">Remarks</span></span>

<span data-ttu-id="b10c1-123">Voici un exemple qui crée une fonction appelée ColorFill, qui s’appuie sur D3DXFillTexture.</span><span class="sxs-lookup"><span data-stu-id="b10c1-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b10c1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b10c1-124">Requirements</span></span>



| <span data-ttu-id="b10c1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b10c1-125">Requirement</span></span> | <span data-ttu-id="b10c1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b10c1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b10c1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b10c1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b10c1-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b10c1-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b10c1-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b10c1-129">Library</span></span><br/> | <dl> <span data-ttu-id="b10c1-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b10c1-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b10c1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b10c1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10c1-132">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b10c1-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
