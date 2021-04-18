---
description: La fonction D3DXBoxBoundProbe (D3DX10math. h) détermine si un rayon croise le volume du cadre englobant d’une zone.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: D3DXBoxBoundProbe, fonction (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106543196"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="f4400-103">D3DXBoxBoundProbe, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="f4400-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="f4400-104">Détermine si un rayon croise le volume du cadre englobant d’une zone.</span><span class="sxs-lookup"><span data-stu-id="f4400-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4400-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4400-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="f4400-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4400-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4400-107">*pMin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4400-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4400-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4400-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4400-109">Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), décrivant l’angle inférieur gauche du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="f4400-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="f4400-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f4400-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f4400-111">*pMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4400-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4400-112">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4400-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4400-113">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle supérieur droit du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="f4400-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="f4400-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f4400-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f4400-115">*pRayPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4400-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4400-116">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4400-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4400-117">Pointeur vers une structure D3DXVECTOR3, en spécifiant la coordonnée d’origine du rayon.</span><span class="sxs-lookup"><span data-stu-id="f4400-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="f4400-118">*pRayDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4400-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4400-119">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4400-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4400-120">Pointeur vers une structure D3DXVECTOR3, en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="f4400-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="f4400-121">Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.</span><span class="sxs-lookup"><span data-stu-id="f4400-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4400-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4400-122">Return value</span></span>

<span data-ttu-id="f4400-123">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4400-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4400-124">Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la zone.</span><span class="sxs-lookup"><span data-stu-id="f4400-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="f4400-125">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="f4400-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4400-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f4400-126">Remarks</span></span>

<span data-ttu-id="f4400-127">**D3DXBoxBoundProbe** détermine si le rayon croise le volume du cadre englobant de la zone, pas seulement la surface de la boîte.</span><span class="sxs-lookup"><span data-stu-id="f4400-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="f4400-128">Les valeurs passées à **D3DXBoxBoundProbe** sont xmin, xmax, ymin, ymax, zmin et Zmax.</span><span class="sxs-lookup"><span data-stu-id="f4400-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="f4400-129">Ainsi, les éléments suivants définissent les angles du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="f4400-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="f4400-130">La profondeur du cadre englobant dans la direction z est zmax-zmin, la direction y est ymax-ymin, et la direction x est Xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="f4400-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="f4400-131">Par exemple, avec les vecteurs minimal et maximal suivants, min (-1,-1,-1) et Max (1, 1, 1), le cadre englobant est défini de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="f4400-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="f4400-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4400-132">Requirements</span></span>



| <span data-ttu-id="f4400-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4400-133">Requirement</span></span> | <span data-ttu-id="f4400-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4400-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4400-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4400-135">Header</span></span>  | <span data-ttu-id="f4400-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="f4400-136">D3DX10math.h</span></span> |
| <span data-ttu-id="f4400-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4400-137">Library</span></span> | <span data-ttu-id="f4400-138">D3DX10. lib</span><span class="sxs-lookup"><span data-stu-id="f4400-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="f4400-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4400-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4400-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="f4400-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
