---
description: Détermine si un rayon croise le volume du cadre englobant d’une sphère.
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
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762235"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="acc99-103">D3DXSphereBoundProbe, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="acc99-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="acc99-104">Détermine si un rayon croise le volume du cadre englobant d’une sphère.</span><span class="sxs-lookup"><span data-stu-id="acc99-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc99-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acc99-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="acc99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acc99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc99-107">*pCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acc99-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc99-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="acc99-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="acc99-109">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la coordonnée centrale de la sphère.</span><span class="sxs-lookup"><span data-stu-id="acc99-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="acc99-110">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acc99-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc99-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc99-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="acc99-112">Rayon de la sphère.</span><span class="sxs-lookup"><span data-stu-id="acc99-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="acc99-113">*pRayPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acc99-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc99-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="acc99-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="acc99-115">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la coordonnée d’origine du rayon.</span><span class="sxs-lookup"><span data-stu-id="acc99-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="acc99-116">*pRayDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acc99-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc99-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="acc99-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="acc99-118">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="acc99-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="acc99-119">Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.</span><span class="sxs-lookup"><span data-stu-id="acc99-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc99-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acc99-120">Return value</span></span>

<span data-ttu-id="acc99-121">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc99-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="acc99-122">Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la sphère.</span><span class="sxs-lookup"><span data-stu-id="acc99-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="acc99-123">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="acc99-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="acc99-124">Notes</span><span class="sxs-lookup"><span data-stu-id="acc99-124">Remarks</span></span>

<span data-ttu-id="acc99-125">**D3DXSphereBoundProbe** détermine si le rayon croise le volume du cadre englobant de la sphère, pas seulement la surface de la sphère.</span><span class="sxs-lookup"><span data-stu-id="acc99-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc99-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acc99-126">Requirements</span></span>



| <span data-ttu-id="acc99-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acc99-127">Requirement</span></span> | <span data-ttu-id="acc99-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="acc99-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acc99-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="acc99-129">Header</span></span><br/>  | <dl> <span data-ttu-id="acc99-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc99-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="acc99-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="acc99-131">Library</span></span><br/> | <dl> <span data-ttu-id="acc99-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acc99-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="acc99-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acc99-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc99-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="acc99-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
