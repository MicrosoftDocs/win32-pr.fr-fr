---
description: Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine :: ComputeDirectLightingSH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539928"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="fb94a-103">ID3DXPRTEngine :: ComputeDirectLightingSH, méthode</span><span class="sxs-lookup"><span data-stu-id="fb94a-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="fb94a-104">Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="fb94a-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb94a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb94a-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="fb94a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb94a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb94a-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb94a-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb94a-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb94a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb94a-109">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="fb94a-109">Order of the SH evaluation.</span></span> <span data-ttu-id="fb94a-110">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="fb94a-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fb94a-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="fb94a-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fb94a-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="fb94a-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fb94a-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb94a-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb94a-114">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="fb94a-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="fb94a-115">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise la contribution de l’éclairage direct avec l’approximation sh.</span><span class="sxs-lookup"><span data-stu-id="fb94a-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="fb94a-116">Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="fb94a-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb94a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb94a-117">Return value</span></span>

<span data-ttu-id="fb94a-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb94a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb94a-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb94a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb94a-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fb94a-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb94a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fb94a-121">Remarks</span></span>

<span data-ttu-id="fb94a-122">La sortie n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="fb94a-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="fb94a-123">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="fb94a-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="fb94a-124">Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur de transfert de luminance (PRT) précalculé par le Albedo.</span><span class="sxs-lookup"><span data-stu-id="fb94a-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb94a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb94a-125">Requirements</span></span>



| <span data-ttu-id="fb94a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb94a-126">Requirement</span></span> | <span data-ttu-id="fb94a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb94a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb94a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb94a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fb94a-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb94a-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fb94a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb94a-130">Library</span></span><br/> | <dl> <span data-ttu-id="fb94a-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb94a-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb94a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb94a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb94a-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fb94a-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
