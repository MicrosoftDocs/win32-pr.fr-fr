---
description: Fonction D3DXSphereBoundProbe (D3DX9Mesh. h)-détermine si un rayon croise le volume du cadre englobant d’une sphère.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: D3DXSphereBoundProbe, fonction (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2d3ea263d7ad8bc50b936fd1010c352c0c01783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093847"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="fcdba-103">D3DXSphereBoundProbe, fonction (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="fcdba-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="fcdba-104">Détermine si un rayon croise le volume du cadre englobant d’une sphère.</span><span class="sxs-lookup"><span data-stu-id="fcdba-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcdba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcdba-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="fcdba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcdba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcdba-107">*pCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcdba-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdba-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcdba-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fcdba-109">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la coordonnée centrale de la sphère.</span><span class="sxs-lookup"><span data-stu-id="fcdba-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="fcdba-110">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcdba-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdba-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcdba-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcdba-112">Rayon de la sphère.</span><span class="sxs-lookup"><span data-stu-id="fcdba-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="fcdba-113">*pRayPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcdba-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdba-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcdba-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fcdba-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la coordonnée d’origine du rayon.</span><span class="sxs-lookup"><span data-stu-id="fcdba-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="fcdba-116">*pRayDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcdba-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdba-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcdba-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fcdba-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="fcdba-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="fcdba-119">Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.</span><span class="sxs-lookup"><span data-stu-id="fcdba-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcdba-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fcdba-120">Return value</span></span>

<span data-ttu-id="fcdba-121">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcdba-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcdba-122">Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la sphère.</span><span class="sxs-lookup"><span data-stu-id="fcdba-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="fcdba-123">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fcdba-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcdba-124">Notes </span><span class="sxs-lookup"><span data-stu-id="fcdba-124">Remarks</span></span>

<span data-ttu-id="fcdba-125">**D3DXSphereBoundProbe** détermine si le rayon croise le volume du cadre englobant de la sphère, pas seulement la surface de la sphère.</span><span class="sxs-lookup"><span data-stu-id="fcdba-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcdba-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcdba-126">Requirements</span></span>



| <span data-ttu-id="fcdba-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcdba-127">Requirement</span></span> | <span data-ttu-id="fcdba-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcdba-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcdba-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcdba-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fcdba-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcdba-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fcdba-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcdba-131">Library</span></span><br/> | <dl> <span data-ttu-id="fcdba-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcdba-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcdba-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcdba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcdba-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="fcdba-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
