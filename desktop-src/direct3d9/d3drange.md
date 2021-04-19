---
description: Définit une plage.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: D3DRANGE, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535820"
---
# <a name="d3drange-structure"></a><span data-ttu-id="d545f-103">D3DRANGE, structure</span><span class="sxs-lookup"><span data-stu-id="d545f-103">D3DRANGE structure</span></span>

<span data-ttu-id="d545f-104">Définit une plage.</span><span class="sxs-lookup"><span data-stu-id="d545f-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="d545f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d545f-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="d545f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d545f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d545f-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d545f-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="d545f-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d545f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d545f-109">Décalage, en octets.</span><span class="sxs-lookup"><span data-stu-id="d545f-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d545f-110">**Taille**</span><span class="sxs-lookup"><span data-stu-id="d545f-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d545f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d545f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d545f-112">Taille, en octets.</span><span class="sxs-lookup"><span data-stu-id="d545f-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d545f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d545f-113">Requirements</span></span>



| <span data-ttu-id="d545f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d545f-114">Requirement</span></span> | <span data-ttu-id="d545f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d545f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d545f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d545f-116">Header</span></span><br/> | <dl> <span data-ttu-id="d545f-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d545f-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d545f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d545f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d545f-119">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="d545f-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
