---
description: Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de cube donnée.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: D3DXFillCubeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539445"
---
# <a name="d3dxfillcubetexture-function"></a><span data-ttu-id="1e5b5-103">D3DXFillCubeTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="1e5b5-103">D3DXFillCubeTexture function</span></span>

<span data-ttu-id="1e5b5-104">Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de cube donnée.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-104">Uses a user-provided function to fill each texel of each mip level of a given cube texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e5b5-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a><span data-ttu-id="1e5b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e5b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e5b5-107">*pTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e5b5-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5b5-108">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="1e5b5-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="1e5b5-109">Pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) représentant la texture remplie.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="1e5b5-110">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e5b5-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5b5-111">Type : **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="1e5b5-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="1e5b5-112">Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="1e5b5-113">La fonction suit le prototype de [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="1e5b5-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e5b5-114">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e5b5-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5b5-115">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e5b5-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e5b5-116">Pointeur vers un bloc arbitraire de données définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="1e5b5-117">Ce pointeur sera passé à la fonction fournie dans *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e5b5-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e5b5-118">Return value</span></span>

<span data-ttu-id="1e5b5-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e5b5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e5b5-120">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e5b5-121">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e5b5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1e5b5-122">Remarks</span></span>

<span data-ttu-id="1e5b5-123">Voici un exemple qui crée une fonction appelée ColorCubeFill, qui s’appuie sur D3DXFillCubeTexture.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-123">Here is an example that creates a function called ColorCubeFill, which relies on D3DXFillCubeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1e5b5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e5b5-124">Requirements</span></span>



| <span data-ttu-id="1e5b5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e5b5-125">Requirement</span></span> | <span data-ttu-id="1e5b5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e5b5-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5b5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e5b5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1e5b5-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e5b5-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1e5b5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e5b5-129">Library</span></span><br/> | <dl> <span data-ttu-id="1e5b5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e5b5-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1e5b5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e5b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5b5-132">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1e5b5-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
