---
description: Fonction D3DXSphereBoundProbe (D3DX10math. h)-détermine si un rayon croise le volume du cadre englobant d’une sphère.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: D3DXSphereBoundProbe, fonction (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108467"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="b8689-103">D3DXSphereBoundProbe, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="b8689-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="b8689-104">Détermine si un rayon croise le volume du cadre englobant d’une sphère.</span><span class="sxs-lookup"><span data-stu-id="b8689-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8689-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8689-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="b8689-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8689-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8689-107">*pCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8689-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8689-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8689-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8689-109">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la coordonnée centrale de la sphère.</span><span class="sxs-lookup"><span data-stu-id="b8689-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="b8689-110">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8689-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8689-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8689-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8689-112">Rayon de la sphère.</span><span class="sxs-lookup"><span data-stu-id="b8689-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="b8689-113">*pRayPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8689-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8689-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8689-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8689-115">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la coordonnée d’origine du rayon.</span><span class="sxs-lookup"><span data-stu-id="b8689-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="b8689-116">*pRayDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8689-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8689-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8689-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8689-118">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="b8689-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="b8689-119">Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.</span><span class="sxs-lookup"><span data-stu-id="b8689-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8689-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8689-120">Return value</span></span>

<span data-ttu-id="b8689-121">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8689-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8689-122">Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la sphère.</span><span class="sxs-lookup"><span data-stu-id="b8689-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="b8689-123">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b8689-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8689-124">Notes </span><span class="sxs-lookup"><span data-stu-id="b8689-124">Remarks</span></span>

<span data-ttu-id="b8689-125">**D3DXSphereBoundProbe** détermine si le rayon croise le volume du cadre englobant de la sphère, pas seulement la surface de la sphère.</span><span class="sxs-lookup"><span data-stu-id="b8689-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8689-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8689-126">Requirements</span></span>



| <span data-ttu-id="b8689-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8689-127">Requirement</span></span> | <span data-ttu-id="b8689-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8689-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8689-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8689-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b8689-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8689-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="b8689-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8689-131">Library</span></span><br/> | <dl> <span data-ttu-id="b8689-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8689-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8689-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8689-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8689-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b8689-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
