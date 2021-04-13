---
description: Décrit un Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION, structure (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323109"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="d7257-103">D3DXQUATERNION, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d7257-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="d7257-104">Décrit un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d7257-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7257-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7257-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="d7257-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d7257-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7257-107">**x**</span><span class="sxs-lookup"><span data-stu-id="d7257-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="d7257-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7257-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7257-109">Composant x.</span><span class="sxs-lookup"><span data-stu-id="d7257-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="d7257-110">**y**</span><span class="sxs-lookup"><span data-stu-id="d7257-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="d7257-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7257-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7257-112">Composant y.</span><span class="sxs-lookup"><span data-stu-id="d7257-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="d7257-113">**z**</span><span class="sxs-lookup"><span data-stu-id="d7257-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="d7257-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7257-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7257-115">Composant z.</span><span class="sxs-lookup"><span data-stu-id="d7257-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="d7257-116">**w**</span><span class="sxs-lookup"><span data-stu-id="d7257-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="d7257-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7257-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7257-118">Composant w.</span><span class="sxs-lookup"><span data-stu-id="d7257-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7257-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d7257-119">Remarks</span></span>

<span data-ttu-id="d7257-120">Les quaternions ajoutent un quatrième élément aux \[ valeurs x, y, z \] qui définissent un vecteur, entraînant des vecteurs 4D arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d7257-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="d7257-121">Toutefois, l’exemple suivant illustre la façon dont chaque élément d’un Quaternion d’unité se réfère à une rotation de l’axe d’un axe (où q représente un Quaternion d’unité (x, y, z, w), l’axe est normalisé et Theta la rotation CCW souhaitée sur l’axe) :</span><span class="sxs-lookup"><span data-stu-id="d7257-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="d7257-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7257-122">Requirements</span></span>



| <span data-ttu-id="d7257-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7257-123">Requirement</span></span> | <span data-ttu-id="d7257-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7257-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7257-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7257-125">Header</span></span><br/> | <dl> <span data-ttu-id="d7257-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7257-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7257-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7257-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7257-128">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="d7257-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
