---
description: Calcule une projection d’éclairage distant dans des vecteurs d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine :: ComputeVolumeSamplesDirectSH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529631"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="63cb7-103">ID3DXPRTEngine :: ComputeVolumeSamplesDirectSH, méthode</span><span class="sxs-lookup"><span data-stu-id="63cb7-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="63cb7-104">Calcule une projection d’éclairage distant dans des vecteurs d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="63cb7-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="63cb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63cb7-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="63cb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63cb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63cb7-107">*Ordre de tri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63cb7-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63cb7-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63cb7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63cb7-109">Ordre de la représentation SH de l’éclairage distant.</span><span class="sxs-lookup"><span data-stu-id="63cb7-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="63cb7-110">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="63cb7-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="63cb7-111">Le degré de l’évaluation est Order in-1.</span><span class="sxs-lookup"><span data-stu-id="63cb7-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="63cb7-112">*OrderOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63cb7-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63cb7-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63cb7-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63cb7-114">Ordre de la représentation SH de l’éclairage local.</span><span class="sxs-lookup"><span data-stu-id="63cb7-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="63cb7-115">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="63cb7-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="63cb7-116">Le degré de l’évaluation est OrderOut-1.</span><span class="sxs-lookup"><span data-stu-id="63cb7-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="63cb7-117">*NumVolSamples.xml* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63cb7-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63cb7-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63cb7-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63cb7-119">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="63cb7-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="63cb7-120">*pSampleLocs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63cb7-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63cb7-121">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="63cb7-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63cb7-122">Position pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="63cb7-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="63cb7-123">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="63cb7-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63cb7-124">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="63cb7-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="63cb7-125">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui projette l’éclairage distant dans les vecteurs de base sh.</span><span class="sxs-lookup"><span data-stu-id="63cb7-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="63cb7-126">Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="63cb7-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="63cb7-127">Cette méthode génère l’ordre des \* OrderOut ² «² scalaires par canal à chaque emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="63cb7-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63cb7-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63cb7-128">Return value</span></span>

<span data-ttu-id="63cb7-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63cb7-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63cb7-130">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63cb7-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63cb7-131">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="63cb7-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="63cb7-132">Notes</span><span class="sxs-lookup"><span data-stu-id="63cb7-132">Remarks</span></span>

<span data-ttu-id="63cb7-133">Cette méthode calcule la lumière d’une source distante arrivant à chaque point dans l’espace spécifié par pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="63cb7-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="63cb7-134">Les coefficients SH représentent le mappage, à chaque point de pSampleLocs, du luminance source au luminance de l’incident transféré.</span><span class="sxs-lookup"><span data-stu-id="63cb7-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="63cb7-135">Pour utiliser cette méthode avec succès, vous devez définir l’échantillonnage sur une sphère avec UseSphere = **true** et UseCosine = **false** dans [**ID3DXPRTEngine :: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); Sinon, cette méthode retourne une erreur avec D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="63cb7-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="63cb7-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63cb7-136">Requirements</span></span>



| <span data-ttu-id="63cb7-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63cb7-137">Requirement</span></span> | <span data-ttu-id="63cb7-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="63cb7-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63cb7-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="63cb7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="63cb7-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="63cb7-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="63cb7-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63cb7-141">Library</span></span><br/> | <dl> <span data-ttu-id="63cb7-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63cb7-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63cb7-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63cb7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63cb7-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="63cb7-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="63cb7-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span><span class="sxs-lookup"><span data-stu-id="63cb7-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
