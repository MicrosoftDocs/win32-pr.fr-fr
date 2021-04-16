---
description: Définit le type de priorité auquel une piste d’animation est assignée.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Énumération D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394108"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="6d956-103">\_Énumération de type D3DXPRIORITY</span><span class="sxs-lookup"><span data-stu-id="6d956-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="6d956-104">Définit le type de priorité auquel une piste d’animation est assignée.</span><span class="sxs-lookup"><span data-stu-id="6d956-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d956-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d956-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6d956-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6d956-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6d956-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ bas**</span><span class="sxs-lookup"><span data-stu-id="6d956-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="6d956-108">La piste doit être fusionnée avec toutes les pistes de faible priorité avant que la fusion basse priorité ne soit mélangée avec la fusion haute priorité.</span><span class="sxs-lookup"><span data-stu-id="6d956-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="6d956-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ élevé**</span><span class="sxs-lookup"><span data-stu-id="6d956-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="6d956-110">La piste doit être fusionnée avec toutes les pistes haute priorité avant que la fusion haute priorité ne soit mélangée à la fusion basse priorité.</span><span class="sxs-lookup"><span data-stu-id="6d956-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="6d956-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6d956-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6d956-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="6d956-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6d956-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6d956-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6d956-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6d956-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d956-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6d956-115">Remarks</span></span>

<span data-ttu-id="6d956-116">Les pistes avec la même priorité sont fusionnées ensemble, et les deux valeurs résultantes sont ensuite fusionnées à l’aide du facteur de fusion de priorité.</span><span class="sxs-lookup"><span data-stu-id="6d956-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d956-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d956-117">Requirements</span></span>



| <span data-ttu-id="6d956-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d956-118">Requirement</span></span> | <span data-ttu-id="6d956-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d956-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d956-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d956-120">Header</span></span><br/> | <dl> <span data-ttu-id="6d956-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d956-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d956-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d956-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d956-123">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="6d956-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




