---
description: Définit le type de base d’une surface corrective de poids fort.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Énumération D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116190"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="66122-103">Énumération D3DBASISTYPE</span><span class="sxs-lookup"><span data-stu-id="66122-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="66122-104">Définit le type de base d’une surface corrective de poids fort.</span><span class="sxs-lookup"><span data-stu-id="66122-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="66122-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66122-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="66122-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="66122-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66122-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bézier**</span><span class="sxs-lookup"><span data-stu-id="66122-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="66122-108">Les vertex d’entrée sont traités comme une série de correctifs de Bézier.</span><span class="sxs-lookup"><span data-stu-id="66122-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="66122-109">Le nombre de vertex spécifié doit être divisible par 4.</span><span class="sxs-lookup"><span data-stu-id="66122-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="66122-110">Les portions de la maille au-delà de ce critère ne seront pas rendues.</span><span class="sxs-lookup"><span data-stu-id="66122-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="66122-111">Une continuité totale est utilisée entre les sous-correctifs à l’intérieur de la surface rendue par chaque appel.</span><span class="sxs-lookup"><span data-stu-id="66122-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="66122-112">Seuls les vertex situés aux angles de chaque sous-correctif sont assurés de se trouver sur la surface résultante.</span><span class="sxs-lookup"><span data-stu-id="66122-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="66122-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**</span><span class="sxs-lookup"><span data-stu-id="66122-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="66122-114">Les vertex d’entrée sont traités comme des points de contrôle d’une surface B-spline.</span><span class="sxs-lookup"><span data-stu-id="66122-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="66122-115">Le nombre d’ouvertures rendues est inférieur à deux fois le nombre d’ouvertures dans cette direction.</span><span class="sxs-lookup"><span data-stu-id="66122-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="66122-116">En général, la surface générée ne contient pas les vertex de contrôle spécifiés.</span><span class="sxs-lookup"><span data-stu-id="66122-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="66122-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="66122-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="66122-118">Une base d’interpolation définit la surface afin que la surface passe par tous les vertex d’entrée spécifiés.</span><span class="sxs-lookup"><span data-stu-id="66122-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="66122-119">Dans DirectX 8, il s’agissait de D3DBASIS \_ interpoliser.</span><span class="sxs-lookup"><span data-stu-id="66122-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="66122-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="66122-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="66122-121">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="66122-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="66122-122">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="66122-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="66122-123">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="66122-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66122-124">Notes</span><span class="sxs-lookup"><span data-stu-id="66122-124">Remarks</span></span>

<span data-ttu-id="66122-125">Les membres de **D3DBASISTYPE** spécifient la formulation à utiliser lors de l’évaluation de la primitive de surface de patch de poids fort pendant le pavage.</span><span class="sxs-lookup"><span data-stu-id="66122-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="66122-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66122-126">Requirements</span></span>



| <span data-ttu-id="66122-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66122-127">Requirement</span></span> | <span data-ttu-id="66122-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="66122-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66122-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="66122-129">Header</span></span><br/> | <dl> <span data-ttu-id="66122-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="66122-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66122-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66122-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66122-132">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="66122-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="66122-133">**\_Informations D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="66122-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="66122-134">**\_Informations D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="66122-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




