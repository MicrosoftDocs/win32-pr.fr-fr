---
description: Définit les distances minimale et maximale de l’intersection entre les objets 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine :: SetMinMaxIntersection, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323037"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="fcd32-103">ID3DXPRTEngine :: SetMinMaxIntersection, méthode</span><span class="sxs-lookup"><span data-stu-id="fcd32-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="fcd32-104">Définit les distances minimale et maximale de l’intersection entre les objets 3D.</span><span class="sxs-lookup"><span data-stu-id="fcd32-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="fcd32-105">Ces valeurs de distance peuvent être utilisées pour contrôler la distance minimale ou maximale que les objets peuvent ombrer ou pour refléter la lumière.</span><span class="sxs-lookup"><span data-stu-id="fcd32-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="fcd32-106">Par exemple, la méthode peut être utilisée pour limiter l’occultation des fonctionnalités avoisinantes d’un modèle 3D.</span><span class="sxs-lookup"><span data-stu-id="fcd32-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd32-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcd32-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="fcd32-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcd32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd32-109">*fmin,* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcd32-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd32-110">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcd32-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcd32-111">Distance d’intersection minimale.</span><span class="sxs-lookup"><span data-stu-id="fcd32-111">Minimum intersection distance.</span></span> <span data-ttu-id="fcd32-112">Doit être positif et inférieur à fMax.</span><span class="sxs-lookup"><span data-stu-id="fcd32-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="fcd32-113">*Fmax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcd32-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd32-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcd32-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcd32-115">Distance d’intersection maximale.</span><span class="sxs-lookup"><span data-stu-id="fcd32-115">Maximum intersection distance.</span></span> <span data-ttu-id="fcd32-116">Si 0.0 f, la valeur précédente est utilisée ; Sinon, doit être supérieur à fmin,.</span><span class="sxs-lookup"><span data-stu-id="fcd32-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd32-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcd32-117">Return value</span></span>

<span data-ttu-id="fcd32-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcd32-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcd32-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fcd32-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcd32-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fcd32-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd32-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fcd32-121">Remarks</span></span>

<span data-ttu-id="fcd32-122">Cette méthode ne peut pas être utilisée dans les simulations de transfert luminance (PRT) précalculées qui s’exécutent dans le GPU.</span><span class="sxs-lookup"><span data-stu-id="fcd32-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="fcd32-123">Consultez [**ID3DXPRTEngine :: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="fcd32-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd32-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcd32-124">Requirements</span></span>



| <span data-ttu-id="fcd32-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcd32-125">Requirement</span></span> | <span data-ttu-id="fcd32-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcd32-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd32-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcd32-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fcd32-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd32-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fcd32-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcd32-129">Library</span></span><br/> | <dl> <span data-ttu-id="fcd32-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcd32-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcd32-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcd32-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd32-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fcd32-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
