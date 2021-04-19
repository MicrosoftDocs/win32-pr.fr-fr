---
description: Calcule le luminance source résultant d’un rebond unique de la lumière interreflet, à l’aide de l’échantillonnage adaptatif.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine :: ComputeBounceAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528571"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="c014b-103">ID3DXPRTEngine :: ComputeBounceAdaptive, méthode</span><span class="sxs-lookup"><span data-stu-id="c014b-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="c014b-104">Calcule le luminance source résultant d’un rebond unique de la lumière interreflet, à l’aide de l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c014b-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="c014b-105">Cette méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="c014b-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="c014b-106">Cette méthode peut être utilisée pour toute scène éclairée, y compris un modèle PRT basé sur l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="c014b-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="c014b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c014b-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="c014b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c014b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c014b-109">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c014b-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-110">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c014b-111">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.</span><span class="sxs-lookup"><span data-stu-id="c014b-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="c014b-112">Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="c014b-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="c014b-113">*AdaptiveThresh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c014b-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c014b-115">Seuil sur le vecteur PRT à utiliser pour la subdivision des sommets et des visages de maillage.</span><span class="sxs-lookup"><span data-stu-id="c014b-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="c014b-116">Si cette valeur est inférieure à 1e-6F, la valeur par défaut de 1e-6F est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c014b-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c014b-117">*MinEdgeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c014b-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c014b-119">Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c014b-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="c014b-120">Si la méthode détermine que la valeur est trop petite, une valeur dépendante du modèle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c014b-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="c014b-121">Si la valeur est zéro, la valeur par défaut 4 est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c014b-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c014b-122">*MaxSubdiv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c014b-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c014b-124">Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c014b-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c014b-125">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c014b-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-126">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c014b-127">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="c014b-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="c014b-128">Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="c014b-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="c014b-129">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c014b-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c014b-130">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c014b-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c014b-131">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui conserve une somme cumulée de pDataOut avec chaque calcul de retour de lumière.</span><span class="sxs-lookup"><span data-stu-id="c014b-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="c014b-132">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c014b-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c014b-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c014b-133">Return value</span></span>

<span data-ttu-id="c014b-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c014b-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c014b-135">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c014b-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c014b-136">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c014b-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c014b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c014b-137">Requirements</span></span>



| <span data-ttu-id="c014b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c014b-138">Requirement</span></span> | <span data-ttu-id="c014b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c014b-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c014b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c014b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c014b-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c014b-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c014b-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c014b-142">Library</span></span><br/> | <dl> <span data-ttu-id="c014b-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c014b-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c014b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c014b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c014b-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c014b-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="c014b-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="c014b-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
