---
description: Définit les modes d’élimination pris en charge.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Énumération D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523812"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="e6fab-103">Énumération D3DCULL</span><span class="sxs-lookup"><span data-stu-id="e6fab-103">D3DCULL enumeration</span></span>

<span data-ttu-id="e6fab-104">Définit les modes d’élimination pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6fab-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6fab-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="e6fab-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e6fab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e6fab-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="e6fab-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="e6fab-108">Ne pas effectuer de réforme des visages.</span><span class="sxs-lookup"><span data-stu-id="e6fab-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="e6fab-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL en \_ PV**</span><span class="sxs-lookup"><span data-stu-id="e6fab-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="e6fab-110">Élimination des faces arrières avec les sommets dans le sens des aiguilles</span><span class="sxs-lookup"><span data-stu-id="e6fab-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e6fab-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**\_CCW D3DCULL**</span><span class="sxs-lookup"><span data-stu-id="e6fab-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="e6fab-112">Élimination des faces arrières avec sommets à gauche.</span><span class="sxs-lookup"><span data-stu-id="e6fab-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e6fab-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6fab-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e6fab-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="e6fab-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e6fab-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e6fab-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e6fab-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="e6fab-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6fab-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e6fab-117">Remarks</span></span>

<span data-ttu-id="e6fab-118">Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="e6fab-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="e6fab-119">Les modes d’élimination définissent la manière dont les faces arrière sont éliminées lors du rendu d’une géométrie.</span><span class="sxs-lookup"><span data-stu-id="e6fab-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6fab-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6fab-120">Requirements</span></span>



| <span data-ttu-id="e6fab-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6fab-121">Requirement</span></span> | <span data-ttu-id="e6fab-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6fab-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fab-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6fab-123">Header</span></span><br/> | <dl> <span data-ttu-id="e6fab-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6fab-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6fab-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6fab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fab-126">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="e6fab-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e6fab-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="e6fab-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="e6fab-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e6fab-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
