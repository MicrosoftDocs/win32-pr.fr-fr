---
description: Structure qui contient les attributs d’un filet de correction.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: D3DXPATCHINFO, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322634"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="501b9-103">D3DXPATCHINFO, structure</span><span class="sxs-lookup"><span data-stu-id="501b9-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="501b9-104">Structure qui contient les attributs d’un filet de correction.</span><span class="sxs-lookup"><span data-stu-id="501b9-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="501b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="501b9-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="501b9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="501b9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="501b9-107">**PatchType**</span><span class="sxs-lookup"><span data-stu-id="501b9-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="501b9-108">Type : **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="501b9-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="501b9-109">Type de correctif.</span><span class="sxs-lookup"><span data-stu-id="501b9-109">The patch type.</span></span> <span data-ttu-id="501b9-110">Pour plus d’informations sur les types de correctifs, consultez [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="501b9-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="501b9-111">**Degré**</span><span class="sxs-lookup"><span data-stu-id="501b9-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="501b9-112">Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="501b9-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="501b9-113">Degré des courbes utilisées pour construire le correctif.</span><span class="sxs-lookup"><span data-stu-id="501b9-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="501b9-114">Pour plus d’informations sur les degrés pris en charge, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="501b9-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="501b9-115">**basis**</span><span class="sxs-lookup"><span data-stu-id="501b9-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="501b9-116">Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="501b9-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="501b9-117">Type de courbe utilisé pour construire le correctif.</span><span class="sxs-lookup"><span data-stu-id="501b9-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="501b9-118">Pour plus d’informations sur les types de base pris en charge, consultez [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="501b9-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="501b9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="501b9-119">Remarks</span></span>

<span data-ttu-id="501b9-120">Une maille est un ensemble de faces, chacune d’elles étant décrite par un polygone simple.</span><span class="sxs-lookup"><span data-stu-id="501b9-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="501b9-121">Les objets peuvent être créés en connectant plusieurs mailles ensemble.</span><span class="sxs-lookup"><span data-stu-id="501b9-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="501b9-122">Une maille de correctif est construite à partir de patchs.</span><span class="sxs-lookup"><span data-stu-id="501b9-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="501b9-123">Un patch est un élément de géométrie à quatre faces construit à partir de courbes.</span><span class="sxs-lookup"><span data-stu-id="501b9-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="501b9-124">Le type de courbe utilisé et l’ordre de la courbe peuvent être variés afin que la surface de la facette corresponde à presque toutes les formes de surface.</span><span class="sxs-lookup"><span data-stu-id="501b9-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="501b9-125">Les types de combinaisons de correctifs suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="501b9-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="501b9-126">Type de correctif</span><span class="sxs-lookup"><span data-stu-id="501b9-126">Patch Type</span></span> | <span data-ttu-id="501b9-127">basis</span><span class="sxs-lookup"><span data-stu-id="501b9-127">Basis</span></span>       | <span data-ttu-id="501b9-128">Degré</span><span class="sxs-lookup"><span data-stu-id="501b9-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="501b9-129">Rectangle</span><span class="sxs-lookup"><span data-stu-id="501b9-129">Rectangle</span></span>  | <span data-ttu-id="501b9-130">Bézier</span><span class="sxs-lookup"><span data-stu-id="501b9-130">Bezier</span></span>      | <span data-ttu-id="501b9-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="501b9-131">2,3,5</span></span>  |
| <span data-ttu-id="501b9-132">Rectangle</span><span class="sxs-lookup"><span data-stu-id="501b9-132">Rectangle</span></span>  | <span data-ttu-id="501b9-133">B-spline</span><span class="sxs-lookup"><span data-stu-id="501b9-133">B-Spline</span></span>    | <span data-ttu-id="501b9-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="501b9-134">2,3,5</span></span>  |
| <span data-ttu-id="501b9-135">Rectangle</span><span class="sxs-lookup"><span data-stu-id="501b9-135">Rectangle</span></span>  | <span data-ttu-id="501b9-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="501b9-136">Catmull-Rom</span></span> | <span data-ttu-id="501b9-137">3</span><span class="sxs-lookup"><span data-stu-id="501b9-137">3</span></span>      |
| <span data-ttu-id="501b9-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="501b9-138">Triangle</span></span>   | <span data-ttu-id="501b9-139">Bézier</span><span class="sxs-lookup"><span data-stu-id="501b9-139">Bezier</span></span>      | <span data-ttu-id="501b9-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="501b9-140">2,3,5</span></span>  |
| <span data-ttu-id="501b9-141">N-patch</span><span class="sxs-lookup"><span data-stu-id="501b9-141">N-patch</span></span>    | <span data-ttu-id="501b9-142">N/A</span><span class="sxs-lookup"><span data-stu-id="501b9-142">N/A</span></span>         | <span data-ttu-id="501b9-143">3</span><span class="sxs-lookup"><span data-stu-id="501b9-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="501b9-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="501b9-144">Requirements</span></span>



| <span data-ttu-id="501b9-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="501b9-145">Requirement</span></span> | <span data-ttu-id="501b9-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="501b9-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="501b9-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="501b9-147">Header</span></span><br/> | <dl> <span data-ttu-id="501b9-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="501b9-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="501b9-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="501b9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501b9-150">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="501b9-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="501b9-151">**\_Informations D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="501b9-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="501b9-152">**\_Informations D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="501b9-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="501b9-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="501b9-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
