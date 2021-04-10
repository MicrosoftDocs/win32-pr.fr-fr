---
description: Définit un rectangle.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: D3DRECT, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762098"
---
# <a name="d3drect-structure"></a><span data-ttu-id="c9a97-103">D3DRECT, structure</span><span class="sxs-lookup"><span data-stu-id="c9a97-103">D3DRECT structure</span></span>

<span data-ttu-id="c9a97-104">Définit un rectangle.</span><span class="sxs-lookup"><span data-stu-id="c9a97-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9a97-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="c9a97-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c9a97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9a97-107">**x1**</span><span class="sxs-lookup"><span data-stu-id="c9a97-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="c9a97-108">Type : **[ **long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a97-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a97-109">Coordonnée x du coin supérieur gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c9a97-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-110">**y1**</span><span class="sxs-lookup"><span data-stu-id="c9a97-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="c9a97-111">Type : **[ **long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a97-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a97-112">Coordonnée y du coin supérieur gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c9a97-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-113">**x2**</span><span class="sxs-lookup"><span data-stu-id="c9a97-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="c9a97-114">Type : **[ **long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a97-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a97-115">Coordonnée x du coin inférieur droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c9a97-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-116">**Y2**</span><span class="sxs-lookup"><span data-stu-id="c9a97-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="c9a97-117">Type : **[ **long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a97-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a97-118">Coordonnée y du coin inférieur droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c9a97-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9a97-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9a97-119">Requirements</span></span>



| <span data-ttu-id="c9a97-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9a97-120">Requirement</span></span> | <span data-ttu-id="c9a97-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9a97-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a97-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9a97-122">Header</span></span><br/> | <dl> <span data-ttu-id="c9a97-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a97-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a97-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9a97-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a97-125">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="c9a97-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c9a97-126">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="c9a97-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
