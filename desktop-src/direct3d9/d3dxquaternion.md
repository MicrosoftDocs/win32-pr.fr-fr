---
description: Décrit un Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION, structure (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543561"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="66a92-103">D3DXQUATERNION, structure (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="66a92-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="66a92-104">Décrit un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="66a92-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66a92-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="66a92-106">Membres</span><span class="sxs-lookup"><span data-stu-id="66a92-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="66a92-107">**x**</span><span class="sxs-lookup"><span data-stu-id="66a92-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="66a92-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66a92-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66a92-109">Composant x.</span><span class="sxs-lookup"><span data-stu-id="66a92-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="66a92-110">**y**</span><span class="sxs-lookup"><span data-stu-id="66a92-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="66a92-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66a92-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66a92-112">Composant y.</span><span class="sxs-lookup"><span data-stu-id="66a92-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="66a92-113">**z**</span><span class="sxs-lookup"><span data-stu-id="66a92-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="66a92-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66a92-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66a92-115">Composant z.</span><span class="sxs-lookup"><span data-stu-id="66a92-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="66a92-116">**w**</span><span class="sxs-lookup"><span data-stu-id="66a92-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="66a92-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66a92-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66a92-118">Composant w.</span><span class="sxs-lookup"><span data-stu-id="66a92-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66a92-119">Notes</span><span class="sxs-lookup"><span data-stu-id="66a92-119">Remarks</span></span>

<span data-ttu-id="66a92-120">Les quaternions ajoutent un quatrième élément aux \[ valeurs x, y, z \] qui définissent un vecteur, entraînant des vecteurs 4D arbitraires.</span><span class="sxs-lookup"><span data-stu-id="66a92-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="66a92-121">Toutefois, l’exemple suivant illustre la façon dont chaque élément d’un Quaternion d’unité se réfère à une rotation de l’axe d’un axe (où q représente un Quaternion d’unité (x, y, z, w), l’axe est normalisé et Theta la rotation CCW souhaitée sur l’axe) :</span><span class="sxs-lookup"><span data-stu-id="66a92-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="66a92-122">Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXQUATERNION**](d3dxquaternion-extensions.md), qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).</span><span class="sxs-lookup"><span data-stu-id="66a92-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a92-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66a92-123">Requirements</span></span>



| <span data-ttu-id="66a92-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66a92-124">Requirement</span></span> | <span data-ttu-id="66a92-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="66a92-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a92-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="66a92-126">Header</span></span><br/> | <dl> <span data-ttu-id="66a92-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a92-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a92-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66a92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a92-129">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="66a92-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="66a92-130">Vecteurs, vertex et quaternions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="66a92-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
