---
description: Définit des constantes qui décrivent les modes d’ombrage pris en charge.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Énumération D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322793"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="d9f40-103">Énumération D3DSHADEMODE</span><span class="sxs-lookup"><span data-stu-id="d9f40-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="d9f40-104">Définit des constantes qui décrivent les modes d’ombrage pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d9f40-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9f40-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="d9f40-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d9f40-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d9f40-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ plat**</span><span class="sxs-lookup"><span data-stu-id="d9f40-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="d9f40-108">Mode d’ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="d9f40-108">Flat shading mode.</span></span> <span data-ttu-id="d9f40-109">Le composant couleur et spéculaire du premier vertex du triangle est utilisé pour déterminer la couleur et le composant spéculaire du visage.</span><span class="sxs-lookup"><span data-stu-id="d9f40-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="d9f40-110">Ces couleurs restent constantes dans le triangle. autrement dit, ils ne sont pas interpolés.</span><span class="sxs-lookup"><span data-stu-id="d9f40-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="d9f40-111">L’alpha spéculaire est interpolé.</span><span class="sxs-lookup"><span data-stu-id="d9f40-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="d9f40-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d9f40-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d9f40-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ Gouraud**</span><span class="sxs-lookup"><span data-stu-id="d9f40-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="d9f40-114">Mode d’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="d9f40-114">Gouraud shading mode.</span></span> <span data-ttu-id="d9f40-115">Les composants de couleur et spéculaire de la face sont déterminés par une interpolation linéaire entre les trois sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="d9f40-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d9f40-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**</span><span class="sxs-lookup"><span data-stu-id="d9f40-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="d9f40-117">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d9f40-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d9f40-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d9f40-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d9f40-119">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="d9f40-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d9f40-120">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d9f40-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d9f40-121">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d9f40-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9f40-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d9f40-122">Remarks</span></span>

<span data-ttu-id="d9f40-123">Le premier vertex d’un triangle pour le mode d’ombrage plat est défini de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="d9f40-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="d9f40-124">Pour une liste de triangles, le premier vertex du triangle i est i \* 3.</span><span class="sxs-lookup"><span data-stu-id="d9f40-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="d9f40-125">Pour une bande triangulaire, le premier vertex du triangle i est le sommet i.</span><span class="sxs-lookup"><span data-stu-id="d9f40-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="d9f40-126">Pour un ventilateur triangulaire, le premier vertex du triangle i est le sommet i + 1.</span><span class="sxs-lookup"><span data-stu-id="d9f40-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="d9f40-127">Les membres de ce type énuméré définissent le valeurs pour l' \_ État de rendu D3DRS SHADEMODE.</span><span class="sxs-lookup"><span data-stu-id="d9f40-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f40-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9f40-128">Requirements</span></span>



| <span data-ttu-id="d9f40-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9f40-129">Requirement</span></span> | <span data-ttu-id="d9f40-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9f40-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f40-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9f40-131">Header</span></span><br/> | <dl> <span data-ttu-id="d9f40-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f40-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f40-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9f40-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f40-134">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="d9f40-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d9f40-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d9f40-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
