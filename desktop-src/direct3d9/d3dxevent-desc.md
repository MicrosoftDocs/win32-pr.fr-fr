---
description: Décrit un événement d’animation.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Structure D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523827"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="40d8c-103">D3DXEVENT \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="40d8c-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="40d8c-104">Décrit un événement d’animation.</span><span class="sxs-lookup"><span data-stu-id="40d8c-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d8c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40d8c-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="40d8c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="40d8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="40d8c-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="40d8c-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-108">Type : **[ **D3DXEVENT \_**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-109">Type d’événement, tel que défini dans [**D3DXEVENT \_ type**](./d3dxevent-type.md).</span><span class="sxs-lookup"><span data-stu-id="40d8c-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-110">**Assurer**</span><span class="sxs-lookup"><span data-stu-id="40d8c-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-112">Identificateur de suivi d’événement.</span><span class="sxs-lookup"><span data-stu-id="40d8c-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="40d8c-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-114">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-115">Heure de début de l’événement dans l’heure globale.</span><span class="sxs-lookup"><span data-stu-id="40d8c-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-116">**Durée**</span><span class="sxs-lookup"><span data-stu-id="40d8c-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-117">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-118">Durée de l’événement dans l’heure globale.</span><span class="sxs-lookup"><span data-stu-id="40d8c-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-119">**Transition**</span><span class="sxs-lookup"><span data-stu-id="40d8c-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-120">Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-121">Style de transition de l’événement, tel que défini dans [**D3DXTRANSITION \_ type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="40d8c-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-122">**Poids**</span><span class="sxs-lookup"><span data-stu-id="40d8c-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-124">Suivre le poids de l’événement.</span><span class="sxs-lookup"><span data-stu-id="40d8c-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-125">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="40d8c-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-127">Suivre la vitesse de l’événement.</span><span class="sxs-lookup"><span data-stu-id="40d8c-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-128">**Position**</span><span class="sxs-lookup"><span data-stu-id="40d8c-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-129">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-130">Position du suivi pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="40d8c-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="40d8c-131">**Activer**</span><span class="sxs-lookup"><span data-stu-id="40d8c-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="40d8c-132">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40d8c-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40d8c-133">Activer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="40d8c-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40d8c-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40d8c-134">Requirements</span></span>



| <span data-ttu-id="40d8c-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40d8c-135">Requirement</span></span> | <span data-ttu-id="40d8c-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d8c-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d8c-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="40d8c-137">Header</span></span><br/> | <dl> <span data-ttu-id="40d8c-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d8c-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d8c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40d8c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d8c-140">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="40d8c-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
