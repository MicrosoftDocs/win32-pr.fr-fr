---
description: Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation d’harmonique sphérique (SH), à l’aide de l’échantillonnage adaptatif.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762374"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="c3036-103">ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive, méthode</span><span class="sxs-lookup"><span data-stu-id="c3036-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="c3036-104">Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation d’harmonique sphérique (SH), à l’aide de l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c3036-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="c3036-105">Cette méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="c3036-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3036-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3036-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="c3036-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3036-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3036-108">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3036-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3036-109">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3036-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3036-110">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="c3036-110">Order of the SH evaluation.</span></span> <span data-ttu-id="c3036-111">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="c3036-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c3036-112">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="c3036-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c3036-113">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="c3036-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c3036-114">*AdaptiveThresh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3036-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3036-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3036-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3036-116">Seuil sur le vecteur PRT à utiliser pour la subdivision des sommets et des visages de maillage.</span><span class="sxs-lookup"><span data-stu-id="c3036-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="c3036-117">Si cette valeur est inférieure à 1e-6F, la valeur par défaut de 1e-6F est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3036-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c3036-118">*MinEdgeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3036-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3036-119">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3036-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3036-120">Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c3036-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="c3036-121">Si la méthode détermine que la valeur est trop petite, une valeur dépendante du modèle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3036-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="c3036-122">Si la valeur est zéro, la valeur par défaut 4 est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3036-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c3036-123">*MaxSubdiv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3036-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3036-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3036-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3036-125">Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c3036-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c3036-126">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c3036-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3036-127">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c3036-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c3036-128">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="c3036-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="c3036-129">Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="c3036-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3036-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3036-130">Return value</span></span>

<span data-ttu-id="c3036-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3036-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3036-132">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3036-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3036-133">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c3036-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3036-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3036-134">Requirements</span></span>



| <span data-ttu-id="c3036-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3036-135">Requirement</span></span> | <span data-ttu-id="c3036-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3036-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3036-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3036-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c3036-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3036-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3036-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3036-139">Library</span></span><br/> | <dl> <span data-ttu-id="c3036-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3036-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3036-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3036-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3036-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c3036-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="c3036-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="c3036-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
