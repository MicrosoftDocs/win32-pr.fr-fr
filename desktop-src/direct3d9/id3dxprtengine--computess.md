---
description: 'Calcule le luminance source résultant de la diffusion sous-surface, à l’aide des propriétés de matériau définies par ID3DXPRTEngine :: SetMeshMaterials. Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'ID3DXPRTEngine :: comhonorive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323402"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="216db-104">ID3DXPRTEngine :: comhonorive, méthode</span><span class="sxs-lookup"><span data-stu-id="216db-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="216db-105">Calcule le luminance source résultant de la diffusion sous-surface, à l’aide des propriétés de matériau définies par [**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="216db-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="216db-106">Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.</span><span class="sxs-lookup"><span data-stu-id="216db-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="216db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="216db-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="216db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="216db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216db-109">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="216db-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216db-110">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="216db-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="216db-111">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.</span><span class="sxs-lookup"><span data-stu-id="216db-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="216db-112">Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="216db-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="216db-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="216db-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="216db-114">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="216db-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="216db-115">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise un rebond unique de la lumière diffusée sous-surface.</span><span class="sxs-lookup"><span data-stu-id="216db-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="216db-116">Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="216db-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="216db-117">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="216db-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="216db-118">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="216db-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="216db-119">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes.</span><span class="sxs-lookup"><span data-stu-id="216db-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="216db-120">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="216db-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216db-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="216db-121">Return value</span></span>

<span data-ttu-id="216db-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="216db-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="216db-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="216db-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="216db-124">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="216db-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="216db-125">Notes</span><span class="sxs-lookup"><span data-stu-id="216db-125">Remarks</span></span>

<span data-ttu-id="216db-126">Pour modéliser la diffusion sous-surface, appelez cette méthode pour chaque rebond de lumière après l’appel d’une méthode ID3DXPRTEngine :: ComputeDirectLighting.</span><span class="sxs-lookup"><span data-stu-id="216db-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="216db-127">Utilisez la séquence d’appel suivante pour modéliser la diffusion sous-surface.</span><span class="sxs-lookup"><span data-stu-id="216db-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="216db-128">La sortie de cette méthode n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="216db-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="216db-129">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="216db-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="216db-130">Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur de transfert de luminance (PRT) précalculé par le Albedo.</span><span class="sxs-lookup"><span data-stu-id="216db-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="216db-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="216db-131">Requirements</span></span>



| <span data-ttu-id="216db-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="216db-132">Requirement</span></span> | <span data-ttu-id="216db-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="216db-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="216db-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="216db-134">Header</span></span><br/>  | <dl> <span data-ttu-id="216db-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="216db-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="216db-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="216db-136">Library</span></span><br/> | <dl> <span data-ttu-id="216db-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="216db-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="216db-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="216db-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216db-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="216db-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="216db-140">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="216db-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




