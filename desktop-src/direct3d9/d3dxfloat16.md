---
description: Décrit un vecteur à virgule flottante 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520323"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="79282-103">D3DXFLOAT16, structure (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="79282-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="79282-104">Décrit un vecteur à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="79282-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="79282-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79282-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="79282-106">Membres</span><span class="sxs-lookup"><span data-stu-id="79282-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="79282-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="79282-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="79282-108">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79282-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79282-109">Données 16 bits.</span><span class="sxs-lookup"><span data-stu-id="79282-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79282-110">Notes</span><span class="sxs-lookup"><span data-stu-id="79282-110">Remarks</span></span>

<span data-ttu-id="79282-111">Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXFLOAT16**](d3dxfloat16-extensions.md), qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).</span><span class="sxs-lookup"><span data-stu-id="79282-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="79282-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79282-112">Requirements</span></span>



| <span data-ttu-id="79282-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79282-113">Requirement</span></span> | <span data-ttu-id="79282-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="79282-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79282-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="79282-115">Header</span></span><br/> | <dl> <span data-ttu-id="79282-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="79282-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79282-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79282-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79282-118">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="79282-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
