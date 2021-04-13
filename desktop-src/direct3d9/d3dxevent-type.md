---
description: Décrit le type des événements qui peuvent être indexés par le contrôleur d’animation.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Énumération D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322929"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="7fcef-103">\_Énumération de type D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="7fcef-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="7fcef-104">Décrit le type des événements qui peuvent être indexés par le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="7fcef-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fcef-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="7fcef-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7fcef-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7fcef-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ TRACKSPEED**</span><span class="sxs-lookup"><span data-stu-id="7fcef-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-108">Suivre la vitesse.</span><span class="sxs-lookup"><span data-stu-id="7fcef-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="7fcef-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ TRACKWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="7fcef-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-110">Poids de la piste.</span><span class="sxs-lookup"><span data-stu-id="7fcef-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="7fcef-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="7fcef-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-112">Suivre la position.</span><span class="sxs-lookup"><span data-stu-id="7fcef-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="7fcef-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ TRACKENABLE**</span><span class="sxs-lookup"><span data-stu-id="7fcef-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-114">Activer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="7fcef-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="7fcef-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ PRIORITYBLEND**</span><span class="sxs-lookup"><span data-stu-id="7fcef-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-116">Valeur de fusion de priorité.</span><span class="sxs-lookup"><span data-stu-id="7fcef-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="7fcef-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7fcef-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7fcef-118">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="7fcef-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7fcef-119">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7fcef-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7fcef-120">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fcef-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fcef-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fcef-121">Requirements</span></span>



| <span data-ttu-id="7fcef-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fcef-122">Requirement</span></span> | <span data-ttu-id="7fcef-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fcef-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcef-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fcef-124">Header</span></span><br/> | <dl> <span data-ttu-id="7fcef-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcef-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fcef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcef-127">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="7fcef-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




