---
description: 'Calcule un vecteur de transfert qui mappe les luminance sources pour quitter les luminance résultant de la diffusion sous-surface, à l’aide de l’échantillonnage adaptatif et des propriétés de matériau définies par ID3DXPRTEngine :: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine :: ComputeSSAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542201"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="59cd2-103">ID3DXPRTEngine :: ComputeSSAdaptive, méthode</span><span class="sxs-lookup"><span data-stu-id="59cd2-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="59cd2-104">Calcule un vecteur de transfert qui mappe les luminance sources pour quitter les luminance résultant de la diffusion sous-surface, à l’aide de l’échantillonnage adaptatif et des propriétés de matériau définies par [**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="59cd2-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="59cd2-105">La méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="59cd2-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="59cd2-106">Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.</span><span class="sxs-lookup"><span data-stu-id="59cd2-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cd2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59cd2-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="59cd2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59cd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59cd2-109">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-110">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="59cd2-111">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.</span><span class="sxs-lookup"><span data-stu-id="59cd2-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="59cd2-112">Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="59cd2-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="59cd2-113">*AdaptiveThresh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59cd2-115">Seuil sur le vecteur PRT à utiliser pour la subdivision des sommets et des visages de maillage.</span><span class="sxs-lookup"><span data-stu-id="59cd2-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="59cd2-116">Si cette valeur est inférieure à 1e-6F, la valeur par défaut de 1e-6F est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59cd2-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="59cd2-117">*MinEdgeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59cd2-119">Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="59cd2-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="59cd2-120">Si la méthode détermine que la valeur est trop petite, une valeur dépendante du modèle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59cd2-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="59cd2-121">*MaxSubdiv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59cd2-123">Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="59cd2-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="59cd2-124">Si la valeur est zéro, la valeur par défaut 4 est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59cd2-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="59cd2-125">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-126">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="59cd2-127">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise un rebond unique de la lumière diffusée sous-surface.</span><span class="sxs-lookup"><span data-stu-id="59cd2-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="59cd2-128">Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="59cd2-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="59cd2-129">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59cd2-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd2-130">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="59cd2-131">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes.</span><span class="sxs-lookup"><span data-stu-id="59cd2-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="59cd2-132">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="59cd2-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59cd2-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59cd2-133">Return value</span></span>

<span data-ttu-id="59cd2-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59cd2-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59cd2-135">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59cd2-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="59cd2-136">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="59cd2-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="59cd2-137">Notes</span><span class="sxs-lookup"><span data-stu-id="59cd2-137">Remarks</span></span>

<span data-ttu-id="59cd2-138">Pour modéliser la diffusion sous-surface, appelez cette méthode pour chaque rebond de lumière après l’appel d’une méthode [**ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) .</span><span class="sxs-lookup"><span data-stu-id="59cd2-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="59cd2-139">La sortie de cette méthode n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="59cd2-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="59cd2-140">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="59cd2-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="59cd2-141">Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur PRT par le Albedo.</span><span class="sxs-lookup"><span data-stu-id="59cd2-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cd2-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59cd2-142">Requirements</span></span>



| <span data-ttu-id="59cd2-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59cd2-143">Requirement</span></span> | <span data-ttu-id="59cd2-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="59cd2-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59cd2-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="59cd2-145">Header</span></span><br/>  | <dl> <span data-ttu-id="59cd2-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59cd2-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59cd2-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59cd2-147">Library</span></span><br/> | <dl> <span data-ttu-id="59cd2-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59cd2-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59cd2-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59cd2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cd2-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="59cd2-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="59cd2-151">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="59cd2-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="59cd2-152">**ID3DXPRTEngine :: en d’autres**</span><span class="sxs-lookup"><span data-stu-id="59cd2-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
