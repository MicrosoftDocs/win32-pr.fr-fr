---
description: Types de correctifs de maillage.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Énumération D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522562"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="766b8-103">Énumération D3DXPATCHMESHTYPE</span><span class="sxs-lookup"><span data-stu-id="766b8-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="766b8-104">Types de correctifs de maillage.</span><span class="sxs-lookup"><span data-stu-id="766b8-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="766b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="766b8-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="766b8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="766b8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="766b8-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="766b8-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="766b8-108">Type de maillage de correctif rectangle.</span><span class="sxs-lookup"><span data-stu-id="766b8-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="766b8-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**</span><span class="sxs-lookup"><span data-stu-id="766b8-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="766b8-110">Type de maillage de la partie triangulaire.</span><span class="sxs-lookup"><span data-stu-id="766b8-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="766b8-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**</span><span class="sxs-lookup"><span data-stu-id="766b8-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="766b8-112">Type de maillage N-patch.</span><span class="sxs-lookup"><span data-stu-id="766b8-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="766b8-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="766b8-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="766b8-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="766b8-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="766b8-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="766b8-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="766b8-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="766b8-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="766b8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="766b8-117">Remarks</span></span>

<span data-ttu-id="766b8-118">Les correctifs triangulaires ont trois côtés et sont décrits dans [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="766b8-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="766b8-119">Les correctifs de rectangle sont à quatre côtés et sont décrits dans [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="766b8-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="766b8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="766b8-120">Requirements</span></span>



| <span data-ttu-id="766b8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="766b8-121">Requirement</span></span> | <span data-ttu-id="766b8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="766b8-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="766b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="766b8-123">Header</span></span><br/> | <dl> <span data-ttu-id="766b8-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="766b8-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="766b8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="766b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766b8-126">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="766b8-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="766b8-127">Utilisation de primitives Higher-Order (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="766b8-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




