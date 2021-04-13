---
description: Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de volume donnée.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: D3DXFillVolumeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322921"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="f94fe-103">D3DXFillVolumeTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="f94fe-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="f94fe-104">Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de volume donnée.</span><span class="sxs-lookup"><span data-stu-id="f94fe-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f94fe-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="f94fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f94fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94fe-107">*pTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f94fe-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f94fe-108">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="f94fe-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="f94fe-109">Pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant la texture remplie.</span><span class="sxs-lookup"><span data-stu-id="f94fe-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="f94fe-110">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f94fe-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94fe-111">Type : **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="f94fe-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="f94fe-112">Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="f94fe-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="f94fe-113">La fonction suit le prototype de [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="f94fe-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94fe-114">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f94fe-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94fe-115">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f94fe-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f94fe-116">Pointeur vers un bloc arbitraire de données définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f94fe-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="f94fe-117">Ce pointeur sera passé à la fonction fournie dans *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="f94fe-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94fe-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f94fe-118">Return value</span></span>

<span data-ttu-id="f94fe-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f94fe-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f94fe-120">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f94fe-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f94fe-121">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f94fe-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94fe-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f94fe-122">Remarks</span></span>

<span data-ttu-id="f94fe-123">Si le volume n’est pas dynamique (car l’utilisation est définie sur 0 lors de sa création) et située dans la mémoire vidéo (le pool de mémoire défini sur D3DPOOL \_ par défaut), **D3DXFillVolumeTexture** échoue car le volume ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="f94fe-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="f94fe-124">Cet exemple crée une fonction appelée ColorVolumeFill, qui s’appuie sur D3DXFillVolumeTexture.</span><span class="sxs-lookup"><span data-stu-id="f94fe-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f94fe-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f94fe-125">Requirements</span></span>



| <span data-ttu-id="f94fe-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f94fe-126">Requirement</span></span> | <span data-ttu-id="f94fe-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f94fe-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f94fe-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f94fe-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f94fe-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94fe-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f94fe-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f94fe-130">Library</span></span><br/> | <dl> <span data-ttu-id="f94fe-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f94fe-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f94fe-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f94fe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94fe-133">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f94fe-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
