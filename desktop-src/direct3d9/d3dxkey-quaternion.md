---
description: Décrit une clé Quaternion à utiliser dans l’animation d’image clé. Une clé Quaternion est une valeur Quaternion à un moment donné.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Structure D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322901"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="f5287-104">D3DXKEY, \_ structure de Quaternion</span><span class="sxs-lookup"><span data-stu-id="f5287-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="f5287-105">Décrit une clé Quaternion à utiliser dans l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="f5287-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="f5287-106">Une clé Quaternion est une valeur Quaternion à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="f5287-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5287-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5287-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="f5287-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f5287-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5287-109">**Time**</span><span class="sxs-lookup"><span data-stu-id="f5287-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="f5287-110">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5287-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5287-111">Valeur de temps.</span><span class="sxs-lookup"><span data-stu-id="f5287-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="f5287-112">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f5287-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="f5287-113">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="f5287-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5287-114">[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion qui fournit des valeurs de rotation.</span><span class="sxs-lookup"><span data-stu-id="f5287-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5287-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5287-115">Requirements</span></span>



| <span data-ttu-id="f5287-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5287-116">Requirement</span></span> | <span data-ttu-id="f5287-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5287-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5287-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5287-118">Header</span></span><br/> | <dl> <span data-ttu-id="f5287-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5287-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5287-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5287-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5287-121">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="f5287-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
