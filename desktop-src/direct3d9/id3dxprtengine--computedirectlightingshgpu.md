---
description: Utilise le GPU pour calculer la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH). Le calcul de l’éclairage sur le GPU sera généralement beaucoup plus rapide que sur le processeur.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine :: ComputeDirectLightingSHGPU, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537289"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="9ba2c-104">ID3DXPRTEngine :: ComputeDirectLightingSHGPU, méthode</span><span class="sxs-lookup"><span data-stu-id="9ba2c-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="9ba2c-105">Utilise le GPU pour calculer la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="9ba2c-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="9ba2c-106">Le calcul de l’éclairage sur le GPU sera généralement beaucoup plus rapide que sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba2c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ba2c-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="9ba2c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ba2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba2c-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9ba2c-111">Pointeur vers l’objet d’appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour exécuter la simulation sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="9ba2c-112">L’appareil doit prendre en charge les nuanceurs de pixels [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba2c-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="9ba2c-113">Les fonctions de rappel ne doivent pas utiliser l’objet d’appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé par le simulateur GPU.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="9ba2c-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ba2c-116">Paramètre de simulation GPU qui définit la résolution de la mémoire tampon z de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="9ba2c-117">Doit être défini sur l’une des valeurs constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span><span class="sxs-lookup"><span data-stu-id="9ba2c-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="9ba2c-118">Pour spécifier une simulation de précision plus élevée, la \_ valeur highquality D3DXSHGPUSIMOPT peut être combinée avec l’une des \_ valeurs SHADOWRESxxx D3DXSHGPUSIMOPT.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="9ba2c-119">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ba2c-121">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-121">Order of the SH evaluation.</span></span> <span data-ttu-id="9ba2c-122">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9ba2c-123">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="9ba2c-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9ba2c-124">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9ba2c-125">*ZBias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ba2c-127">Décalage dans la direction normale.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="9ba2c-128">*ZAngleBias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ba2c-130">Décalage dans la direction normale, mis à l’échelle d’un moins le cosinus de l’angle avec le rayon de la lumière.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="9ba2c-131">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9ba2c-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba2c-132">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="9ba2c-133">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba2c-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="9ba2c-134">Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba2c-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ba2c-135">Return value</span></span>

<span data-ttu-id="9ba2c-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ba2c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ba2c-137">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9ba2c-138">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba2c-139">Notes</span><span class="sxs-lookup"><span data-stu-id="9ba2c-139">Remarks</span></span>

<span data-ttu-id="9ba2c-140">Dans cette méthode, le Albedo n’est pas multiplié par le signal lumineux, et seule la lumière entrante est intégrée dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="9ba2c-141">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="9ba2c-142">Appelez [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur de transfert luminance (PRT) précalculé par le Albedo.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba2c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ba2c-143">Requirements</span></span>



| <span data-ttu-id="9ba2c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ba2c-144">Requirement</span></span> | <span data-ttu-id="9ba2c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ba2c-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba2c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ba2c-146">Header</span></span><br/>  | <dl> <span data-ttu-id="9ba2c-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba2c-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9ba2c-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ba2c-148">Library</span></span><br/> | <dl> <span data-ttu-id="9ba2c-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ba2c-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ba2c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ba2c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba2c-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9ba2c-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
