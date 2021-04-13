---
description: Calcule, à un point arbitraire qui ne se trouve pas sur un maillage, un vecteur de transfert qui mappe les luminance sources (représentés par une approximation d’harmoniques sphériques) pour quitter luminance.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'ID3DXPRTEngine :: ComputeSurfSamplesDirectSH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323394"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="b2595-103">ID3DXPRTEngine :: ComputeSurfSamplesDirectSH, méthode</span><span class="sxs-lookup"><span data-stu-id="b2595-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="b2595-104">Calcule, à un point arbitraire qui ne se trouve pas sur un maillage, un vecteur de transfert qui mappe les luminance sources (représentés par une approximation d’harmoniques sphériques) pour quitter luminance.</span><span class="sxs-lookup"><span data-stu-id="b2595-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2595-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2595-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="b2595-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2595-107">*SHOrder* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2595-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2595-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2595-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2595-109">Ordre de l’approximation SH à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b2595-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="b2595-110">*Échantillons* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2595-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2595-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2595-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2595-112">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b2595-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="b2595-113">*pSampleLocs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2595-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2595-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2595-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b2595-115">Position pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="b2595-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="b2595-116">*pSampleNorms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2595-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2595-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2595-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b2595-118">Vecteur normal pour chaque exemple d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="b2595-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="b2595-119">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b2595-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2595-120">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b2595-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b2595-121">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise la contribution de l’éclairage direct au point, à l’aide de l’approximation sh.</span><span class="sxs-lookup"><span data-stu-id="b2595-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2595-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2595-122">Return value</span></span>

<span data-ttu-id="b2595-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2595-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2595-124">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2595-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2595-125">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b2595-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2595-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b2595-126">Remarks</span></span>

<span data-ttu-id="b2595-127">N’utilisez pas de mémoire tampon de texture lors de l’appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b2595-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2595-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2595-128">Requirements</span></span>



| <span data-ttu-id="b2595-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2595-129">Requirement</span></span> | <span data-ttu-id="b2595-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2595-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2595-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2595-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b2595-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2595-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2595-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2595-133">Library</span></span><br/> | <dl> <span data-ttu-id="b2595-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2595-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2595-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2595-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2595-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b2595-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="b2595-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="b2595-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="b2595-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span><span class="sxs-lookup"><span data-stu-id="b2595-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
