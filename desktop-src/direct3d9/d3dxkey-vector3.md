---
description: Décrit une clé vectorielle à utiliser dans une animation d’image clé. Elle spécifie un vecteur à un moment donné. Il est utilisé pour les clés de mise à l’échelle et de traduction.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Structure D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522353"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="795fc-105">D3DXKEY \_ VECTOR3, structure</span><span class="sxs-lookup"><span data-stu-id="795fc-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="795fc-106">Décrit une clé vectorielle à utiliser dans une animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="795fc-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="795fc-107">Elle spécifie un vecteur à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="795fc-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="795fc-108">Il est utilisé pour les clés de mise à l’échelle et de traduction.</span><span class="sxs-lookup"><span data-stu-id="795fc-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="795fc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="795fc-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="795fc-110">Membres</span><span class="sxs-lookup"><span data-stu-id="795fc-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="795fc-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="795fc-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="795fc-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="795fc-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="795fc-113">Horodatage de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="795fc-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="795fc-114">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="795fc-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="795fc-115">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="795fc-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="795fc-116">Vecteur 3D [**D3DXVECTOR3**](d3dxvector3.md) qui fournit des valeurs d’échelle et/ou de translation.</span><span class="sxs-lookup"><span data-stu-id="795fc-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="795fc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="795fc-117">Requirements</span></span>



| <span data-ttu-id="795fc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="795fc-118">Requirement</span></span> | <span data-ttu-id="795fc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="795fc-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="795fc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="795fc-120">Header</span></span><br/> | <dl> <span data-ttu-id="795fc-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="795fc-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795fc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="795fc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795fc-123">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="795fc-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
