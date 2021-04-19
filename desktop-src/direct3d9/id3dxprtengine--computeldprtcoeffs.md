---
description: Calcule les coefficients de transfert de luminance précalculés (LDPRT) déformables localement par rapport aux vecteurs normaux par échantillon pour réduire l’erreur des moindres carrés en ce qui concerne les données d’entrée ID3DXPRTBuffer.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine :: ComputeLDPRTCoeffs, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537288"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="25483-103">ID3DXPRTEngine :: ComputeLDPRTCoeffs, méthode</span><span class="sxs-lookup"><span data-stu-id="25483-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="25483-104">Calcule les coefficients de transfert de luminance précalculés (LDPRT) déformables localement par rapport aux vecteurs normaux par échantillon pour réduire l’erreur des moindres carrés en ce qui concerne les données d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="25483-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="25483-105">Ces coefficients peuvent être utilisés avec des vecteurs normaux dépouillés ou transformés pour modéliser les effets globaux sur les objets dynamiques.</span><span class="sxs-lookup"><span data-stu-id="25483-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="25483-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25483-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="25483-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25483-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25483-108">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25483-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25483-109">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="25483-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="25483-110">Pointeur vers un objet de données d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) (SH) de transfert d’harmonique sphérique (SH) précalculé (PRT).</span><span class="sxs-lookup"><span data-stu-id="25483-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="25483-111">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25483-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25483-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25483-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25483-113">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="25483-113">Order of the SH evaluation.</span></span> <span data-ttu-id="25483-114">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="25483-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="25483-115">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="25483-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="25483-116">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="25483-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="25483-117">*pNormOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25483-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25483-118">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="25483-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="25483-119">Tableau de vecteurs facultatif à remplir avec les vecteurs normaux optimaux pour lesquels les coefficients LDPRT sont optimisés.</span><span class="sxs-lookup"><span data-stu-id="25483-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="25483-120">Ce tableau doit avoir la même taille que le nombre d’exemples dans pDataIn.</span><span class="sxs-lookup"><span data-stu-id="25483-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="25483-121">Si la **valeur est null**, les vecteurs normaux de surface sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="25483-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="25483-122">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25483-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25483-123">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="25483-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="25483-124">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui contient les coefficients d’harmoniques Zona ordonnés par canal de couleur par échantillon.</span><span class="sxs-lookup"><span data-stu-id="25483-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25483-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25483-125">Return value</span></span>

<span data-ttu-id="25483-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25483-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25483-127">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25483-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25483-128">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="25483-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="25483-129">Notes</span><span class="sxs-lookup"><span data-stu-id="25483-129">Remarks</span></span>

<span data-ttu-id="25483-130">Les solutions pour les vecteurs normaux d’ombrage peuvent éventuellement être obtenues avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="25483-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="25483-131">Ces vecteurs normaux, ainsi que les coefficients LDPRT, peuvent représenter plus précisément le signal PRT.</span><span class="sxs-lookup"><span data-stu-id="25483-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="25483-132">Dans ce cas, les coefficients représentent les harmoniques zonales orientées dans la direction normale.</span><span class="sxs-lookup"><span data-stu-id="25483-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="25483-133">Cette méthode ne peut pas être utilisée avec les résultats de [**ID3DXPRTEngine :: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) ou [**ID3DXPRTEngine :: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span><span class="sxs-lookup"><span data-stu-id="25483-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25483-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25483-134">Requirements</span></span>



| <span data-ttu-id="25483-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25483-135">Requirement</span></span> | <span data-ttu-id="25483-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="25483-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25483-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="25483-137">Header</span></span><br/>  | <dl> <span data-ttu-id="25483-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="25483-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="25483-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25483-139">Library</span></span><br/> | <dl> <span data-ttu-id="25483-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25483-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25483-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25483-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25483-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="25483-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
