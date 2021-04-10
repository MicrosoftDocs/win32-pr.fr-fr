---
description: Détermine si un rayon croise le volume du cadre englobant d’une zone.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: D3DXBoxBoundProbe, fonction (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116238"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="49e8b-103">D3DXBoxBoundProbe fonction)</span><span class="sxs-lookup"><span data-stu-id="49e8b-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="49e8b-104">Détermine si un rayon croise le volume du cadre englobant d’une zone.</span><span class="sxs-lookup"><span data-stu-id="49e8b-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e8b-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="49e8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e8b-107">*pMin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e8b-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8b-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="49e8b-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49e8b-109">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle inférieur gauche du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="49e8b-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="49e8b-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="49e8b-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="49e8b-111">*pMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e8b-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8b-112">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="49e8b-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49e8b-113">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle supérieur droit du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="49e8b-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="49e8b-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="49e8b-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="49e8b-115">*pRayPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e8b-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8b-116">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="49e8b-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49e8b-117">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la coordonnée d’origine du rayon.</span><span class="sxs-lookup"><span data-stu-id="49e8b-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="49e8b-118">*pRayDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e8b-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8b-119">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="49e8b-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49e8b-120">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="49e8b-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="49e8b-121">Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.</span><span class="sxs-lookup"><span data-stu-id="49e8b-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e8b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49e8b-122">Return value</span></span>

<span data-ttu-id="49e8b-123">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49e8b-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49e8b-124">Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la zone.</span><span class="sxs-lookup"><span data-stu-id="49e8b-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="49e8b-125">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="49e8b-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e8b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="49e8b-126">Remarks</span></span>

<span data-ttu-id="49e8b-127">**D3DXboxBoundProbe** détermine si le rayon croise le volume du cadre englobant de la zone, pas seulement la surface de la boîte.</span><span class="sxs-lookup"><span data-stu-id="49e8b-127">**D3DXboxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="49e8b-128">Les valeurs passées à **D3DXboxBoundProbe** sont xmin, xmax, ymin, ymax, zmin et Zmax.</span><span class="sxs-lookup"><span data-stu-id="49e8b-128">The values passed to **D3DXboxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="49e8b-129">Ainsi, les éléments suivants définissent les angles du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="49e8b-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="49e8b-130">La profondeur du cadre englobant dans la direction z est zmax-zmin, la direction y est ymax-ymin, et la direction x est Xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="49e8b-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="49e8b-131">Par exemple, avec les vecteurs minimal et maximal suivants, min (-1,-1,-1) et Max (1, 1, 1), le cadre englobant est défini de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="49e8b-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="49e8b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49e8b-132">Requirements</span></span>



| <span data-ttu-id="49e8b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49e8b-133">Requirement</span></span> | <span data-ttu-id="49e8b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="49e8b-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49e8b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="49e8b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="49e8b-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e8b-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49e8b-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49e8b-137">Library</span></span><br/> | <dl> <span data-ttu-id="49e8b-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49e8b-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49e8b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49e8b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e8b-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="49e8b-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="49e8b-141">**D3DXComputeBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="49e8b-141">**D3DXComputeBoundingBox**</span></span>](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
