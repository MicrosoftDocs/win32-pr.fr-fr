---
description: Décrit une matrice.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531783"
---
# <a name="d3dmatrix"></a><span data-ttu-id="40fe0-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="40fe0-103">D3DMATRIX</span></span>

<span data-ttu-id="40fe0-104">Décrit une matrice.</span><span class="sxs-lookup"><span data-stu-id="40fe0-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="40fe0-105">Types dérivés : \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="40fe0-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="40fe0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="40fe0-106">Members</span></span>



| <span data-ttu-id="40fe0-107">Élément</span><span class="sxs-lookup"><span data-stu-id="40fe0-107">Item</span></span>                                                        | <span data-ttu-id="40fe0-108">Description</span><span class="sxs-lookup"><span data-stu-id="40fe0-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fe0-109"><span id="_ij"></span><span id="_IJ"></span>\_soudé</span><span class="sxs-lookup"><span data-stu-id="40fe0-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="40fe0-110">Tableau de valeurs float qui représentent une matrice 4x4, où i est le numéro de ligne et j le numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="40fe0-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="40fe0-111">Par exemple, \_ 34 correspond à \[ un ₄ ₃ \] , le composant dans la troisième ligne et la quatrième colonne.</span><span class="sxs-lookup"><span data-stu-id="40fe0-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40fe0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="40fe0-112">Remarks</span></span>

<span data-ttu-id="40fe0-113">Dans Direct3D, l' \_ élément 34 d’une matrice de projection ne peut pas être un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="40fe0-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="40fe0-114">Si votre application doit utiliser une valeur négative à cet emplacement, elle doit mettre à l’échelle la totalité de la matrice de projection par-1 à la place.</span><span class="sxs-lookup"><span data-stu-id="40fe0-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="40fe0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40fe0-115">Requirements</span></span>



| <span data-ttu-id="40fe0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40fe0-116">Requirement</span></span> | <span data-ttu-id="40fe0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="40fe0-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40fe0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="40fe0-118">Header</span></span><br/> | <dl> <span data-ttu-id="40fe0-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="40fe0-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40fe0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40fe0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fe0-121">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="40fe0-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="40fe0-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="40fe0-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="40fe0-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="40fe0-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="40fe0-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="40fe0-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="40fe0-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="40fe0-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="40fe0-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="40fe0-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="40fe0-127">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40fe0-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
