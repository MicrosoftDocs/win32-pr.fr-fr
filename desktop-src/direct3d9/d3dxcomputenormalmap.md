---
description: 'Fonction D3DXComputeNormalMap : convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.'
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: D3DXComputeNormalMap, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105227"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="caf75-104">D3DXComputeNormalMap fonction)</span><span class="sxs-lookup"><span data-stu-id="caf75-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="caf75-105">Convertit une carte de hauteur en une carte normale.</span><span class="sxs-lookup"><span data-stu-id="caf75-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="caf75-106">Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.</span><span class="sxs-lookup"><span data-stu-id="caf75-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf75-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caf75-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="caf75-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caf75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf75-109">*pTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="caf75-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-110">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="caf75-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="caf75-111">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="caf75-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="caf75-112">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caf75-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-113">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="caf75-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="caf75-114">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant la texture de la carte de hauteur source.</span><span class="sxs-lookup"><span data-stu-id="caf75-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="caf75-115">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caf75-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-116">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="caf75-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="caf75-117">Pointeur vers un type [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui contient la palette source de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="caf75-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="caf75-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="caf75-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-119">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="caf75-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="caf75-120">Un ou plusieurs indicateurs [D3DX \_ NORMALMAP](d3dx-normalmap.md) qui contrôlent la génération de mappages normaux.</span><span class="sxs-lookup"><span data-stu-id="caf75-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="caf75-121">*Chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caf75-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="caf75-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="caf75-123">Un indicateur de [ \_ canal D3DX](d3dx-channel.md) spécifiant la source des informations de hauteur.</span><span class="sxs-lookup"><span data-stu-id="caf75-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="caf75-124">*Amplitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="caf75-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf75-125">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="caf75-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="caf75-126">Multiplicateur de valeur constante qui augmente (ou diminue) les valeurs dans la carte normale.</span><span class="sxs-lookup"><span data-stu-id="caf75-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="caf75-127">Les valeurs plus élevées rendent généralement les bosses plus visibles, les valeurs basses rendent généralement les rugosités moins visibles.</span><span class="sxs-lookup"><span data-stu-id="caf75-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf75-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="caf75-128">Return value</span></span>

<span data-ttu-id="caf75-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="caf75-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="caf75-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="caf75-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="caf75-131">Si la fonction échoue, la valeur de retour peut être la valeur suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="caf75-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf75-132">Notes </span><span class="sxs-lookup"><span data-stu-id="caf75-132">Remarks</span></span>

<span data-ttu-id="caf75-133">Cette méthode calcule le normal à l’aide de la différence centrale avec une taille de noyau de 3 x 3.</span><span class="sxs-lookup"><span data-stu-id="caf75-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="caf75-134">Le dénominateur de différenciation central utilisé est 2,0.</span><span class="sxs-lookup"><span data-stu-id="caf75-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="caf75-135">Les canaux RVB dans la destination contiennent des composants (x, y, z) biaisés de la normale.</span><span class="sxs-lookup"><span data-stu-id="caf75-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf75-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caf75-136">Requirements</span></span>



| <span data-ttu-id="caf75-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caf75-137">Requirement</span></span> | <span data-ttu-id="caf75-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="caf75-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="caf75-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="caf75-139">Header</span></span><br/>  | <dl> <span data-ttu-id="caf75-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf75-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="caf75-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="caf75-141">Library</span></span><br/> | <dl> <span data-ttu-id="caf75-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caf75-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="caf75-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caf75-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf75-144">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="caf75-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
