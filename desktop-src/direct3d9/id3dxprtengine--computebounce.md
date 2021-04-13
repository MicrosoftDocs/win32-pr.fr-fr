---
description: Calcule le luminance source résultant d’un rebond unique de la lumière interreflete. Cette méthode peut être utilisée pour n’importe quelle scène éclairée, y compris un modèle de transfert luminance (PRT) à base d’harmonique sphérique (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine :: ComputeBounce, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323258"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="6ae3e-104">ID3DXPRTEngine :: ComputeBounce, méthode</span><span class="sxs-lookup"><span data-stu-id="6ae3e-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="6ae3e-105">Calcule le luminance source résultant d’un rebond unique de la lumière interreflete.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="6ae3e-106">Cette méthode peut être utilisée pour n’importe quelle scène éclairée, y compris un modèle de transfert luminance (PRT) à base d’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="6ae3e-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae3e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ae3e-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="6ae3e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ae3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae3e-109">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ae3e-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae3e-110">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="6ae3e-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="6ae3e-111">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="6ae3e-112">Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="6ae3e-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6ae3e-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae3e-114">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="6ae3e-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="6ae3e-115">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise un rebond unique de la lumière interreflete.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="6ae3e-116">Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="6ae3e-117">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6ae3e-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae3e-118">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="6ae3e-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="6ae3e-119">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="6ae3e-120">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae3e-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ae3e-121">Return value</span></span>

<span data-ttu-id="6ae3e-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ae3e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ae3e-123">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ae3e-124">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae3e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6ae3e-125">Remarks</span></span>

<span data-ttu-id="6ae3e-126">Utilisez la séquence d’appel suivante pour modéliser plusieurs rebonds de lumière avec éclairage direct.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="6ae3e-127">Utilisez la séquence d’appel suivante pour modéliser plusieurs rebonds de lumière avec la diffusion sous-surface.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="6ae3e-128">La sortie de cette méthode n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="6ae3e-129">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="6ae3e-130">Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur PRT par le Albedo.</span><span class="sxs-lookup"><span data-stu-id="6ae3e-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae3e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ae3e-131">Requirements</span></span>



| <span data-ttu-id="6ae3e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ae3e-132">Requirement</span></span> | <span data-ttu-id="6ae3e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae3e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae3e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ae3e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="6ae3e-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae3e-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ae3e-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ae3e-136">Library</span></span><br/> | <dl> <span data-ttu-id="6ae3e-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ae3e-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ae3e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae3e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae3e-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="6ae3e-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="6ae3e-140">**ID3DXPRTEngine :: en d’autres**</span><span class="sxs-lookup"><span data-stu-id="6ae3e-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




