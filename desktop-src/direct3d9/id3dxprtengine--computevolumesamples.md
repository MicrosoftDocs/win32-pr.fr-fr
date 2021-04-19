---
description: Calcule une projection de l’éclairage direct de la lumière précédente dans les vecteurs de base d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine :: ComputeVolumeSamples, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528570"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="73179-103">ID3DXPRTEngine :: ComputeVolumeSamples, méthode</span><span class="sxs-lookup"><span data-stu-id="73179-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="73179-104">Calcule une projection de l’éclairage direct de la lumière précédente dans les vecteurs de base d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="73179-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="73179-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73179-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="73179-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73179-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73179-107">*pSurfDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73179-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73179-108">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="73179-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="73179-109">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.</span><span class="sxs-lookup"><span data-stu-id="73179-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="73179-110">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73179-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73179-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73179-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73179-112">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="73179-112">Order of the SH evaluation.</span></span> <span data-ttu-id="73179-113">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="73179-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="73179-114">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="73179-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="73179-115">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="73179-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="73179-116">*NumVolSamples.xml* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73179-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73179-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73179-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73179-118">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="73179-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="73179-119">*pSampleLocs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73179-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73179-120">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="73179-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="73179-121">Position pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="73179-121">Position for each sample.</span></span> <span data-ttu-id="73179-122">Si pSampleLocs a la **valeur null**, ComputeVolumeSamples calcule les matrices de transfert à chaque vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="73179-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="73179-123">Toutefois, si pSampleLocs n’a pas la **valeur null**, vous devez échantillonner une sphère (Set UseSphere = **true** et UseCosine = **false** dans [**ID3DXPRTEngine :: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); Sinon, ComputeVolumeSamples retourne D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="73179-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="73179-124">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73179-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73179-125">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="73179-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="73179-126">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui projette l’éclairage direct de la lumière précédente Bounce dans les vecteurs de base sh.</span><span class="sxs-lookup"><span data-stu-id="73179-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="73179-127">Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="73179-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73179-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73179-128">Return value</span></span>

<span data-ttu-id="73179-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73179-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73179-130">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73179-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="73179-131">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="73179-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="73179-132">Notes</span><span class="sxs-lookup"><span data-stu-id="73179-132">Remarks</span></span>

<span data-ttu-id="73179-133">Cette méthode calcule la façon dont la lumière de la fonction luminance source est réfléchie à partir de la surface qui représente la scène (pSurfDataIn) et arrive à chaque point dans l’espace spécifié par pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="73179-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="73179-134">Les coefficients SH représentent le mappage, à chaque point de pSampleLocs, du luminance source au luminance de l’incident transféré.</span><span class="sxs-lookup"><span data-stu-id="73179-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="73179-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73179-135">Requirements</span></span>



| <span data-ttu-id="73179-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73179-136">Requirement</span></span> | <span data-ttu-id="73179-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="73179-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73179-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="73179-138">Header</span></span><br/>  | <dl> <span data-ttu-id="73179-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="73179-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="73179-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73179-140">Library</span></span><br/> | <dl> <span data-ttu-id="73179-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73179-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73179-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73179-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73179-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="73179-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="73179-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="73179-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
