---
description: Calcule les exemples de transfert luminance (PRT) précalculés pour un point arbitraire (et vecteur normal).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine :: ComputeSurfSamplesBounce, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323398"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="06cad-103">ID3DXPRTEngine :: ComputeSurfSamplesBounce, méthode</span><span class="sxs-lookup"><span data-stu-id="06cad-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="06cad-104">Calcule les exemples de transfert luminance (PRT) précalculés pour un point arbitraire (et vecteur normal).</span><span class="sxs-lookup"><span data-stu-id="06cad-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="06cad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06cad-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="06cad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cad-107">*pSurfDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cad-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-108">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="06cad-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="06cad-109">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente le luminance source de l’objet 3D.</span><span class="sxs-lookup"><span data-stu-id="06cad-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="06cad-110">Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="06cad-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="06cad-111">*Échantillons* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cad-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06cad-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06cad-113">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="06cad-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="06cad-114">*pSampleLocs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cad-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-115">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06cad-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="06cad-116">Position pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="06cad-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="06cad-117">*pSampleNorms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cad-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-118">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06cad-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="06cad-119">Vecteur normal pour chaque exemple d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="06cad-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="06cad-120">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06cad-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-121">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="06cad-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="06cad-122">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise la contribution de l’éclairage direct au point, à l’aide de la approximation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="06cad-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="06cad-123">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06cad-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06cad-124">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="06cad-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="06cad-125">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes.</span><span class="sxs-lookup"><span data-stu-id="06cad-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="06cad-126">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="06cad-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cad-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06cad-127">Return value</span></span>

<span data-ttu-id="06cad-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06cad-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06cad-129">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06cad-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06cad-130">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="06cad-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="06cad-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06cad-131">Requirements</span></span>



| <span data-ttu-id="06cad-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06cad-132">Requirement</span></span> | <span data-ttu-id="06cad-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="06cad-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06cad-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="06cad-134">Header</span></span><br/>  | <dl> <span data-ttu-id="06cad-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06cad-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="06cad-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06cad-136">Library</span></span><br/> | <dl> <span data-ttu-id="06cad-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06cad-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06cad-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06cad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cad-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="06cad-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="06cad-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="06cad-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
