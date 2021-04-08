---
description: Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Généralement utilisé pour déterminer si un point donné se trouve dans une ombre.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine :: ShadowRayIntersects, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043125"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="11e93-104">ID3DXPRTEngine :: ShadowRayIntersects, méthode</span><span class="sxs-lookup"><span data-stu-id="11e93-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="11e93-105">Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille.</span><span class="sxs-lookup"><span data-stu-id="11e93-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="11e93-106">Généralement utilisé pour déterminer si un point donné se trouve dans une ombre.</span><span class="sxs-lookup"><span data-stu-id="11e93-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11e93-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="11e93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11e93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e93-109">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11e93-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e93-110">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="11e93-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="11e93-111">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="11e93-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="11e93-112">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11e93-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e93-113">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="11e93-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="11e93-114">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction normalisée du rayon.</span><span class="sxs-lookup"><span data-stu-id="11e93-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e93-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11e93-115">Return value</span></span>

<span data-ttu-id="11e93-116">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11e93-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11e93-117">Retourne la **valeur true** si le rayon croise le maillage actuel ; Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="11e93-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11e93-118">Notes</span><span class="sxs-lookup"><span data-stu-id="11e93-118">Remarks</span></span>

<span data-ttu-id="11e93-119">Utilisez [**ID3DXPRTEngine :: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) pour définir les distances minimale et maximale de l’intersection avec le rayon.</span><span class="sxs-lookup"><span data-stu-id="11e93-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="11e93-120">Cette méthode s’exécute plus rapidement que [**ID3DXPRTEngine :: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="11e93-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11e93-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11e93-121">Requirements</span></span>



| <span data-ttu-id="11e93-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11e93-122">Requirement</span></span> | <span data-ttu-id="11e93-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="11e93-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11e93-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="11e93-124">Header</span></span><br/>  | <dl> <span data-ttu-id="11e93-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e93-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="11e93-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11e93-126">Library</span></span><br/> | <dl> <span data-ttu-id="11e93-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e93-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11e93-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11e93-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e93-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="11e93-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="11e93-130">**ID3DXPRTEngine::ClosestRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="11e93-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="11e93-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="11e93-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
