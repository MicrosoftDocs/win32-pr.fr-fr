---
description: Spécifie les types de modes d’affichage à exclure.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: D3DDISPLAYMODEFILTER, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322762"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="d4967-103">D3DDISPLAYMODEFILTER, structure</span><span class="sxs-lookup"><span data-stu-id="d4967-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="d4967-104">Spécifie les types de modes d’affichage à exclure.</span><span class="sxs-lookup"><span data-stu-id="d4967-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4967-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4967-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="d4967-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d4967-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4967-107">**Taille**</span><span class="sxs-lookup"><span data-stu-id="d4967-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d4967-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4967-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4967-109">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="d4967-109">The size of this structure.</span></span> <span data-ttu-id="d4967-110">Il doit toujours être défini sur sizeof (D3DDISPLAYMODEFILTER).</span><span class="sxs-lookup"><span data-stu-id="d4967-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="d4967-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="d4967-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="d4967-112">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d4967-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4967-113">Format du mode d’affichage à exclure. Consultez [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="d4967-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4967-114">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="d4967-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="d4967-115">Type : **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="d4967-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4967-116">Indique si le classement numérisation est entrelacé ou progressif.</span><span class="sxs-lookup"><span data-stu-id="d4967-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="d4967-117">Consultez [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="d4967-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4967-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4967-118">Requirements</span></span>



| <span data-ttu-id="d4967-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4967-119">Requirement</span></span> | <span data-ttu-id="d4967-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4967-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4967-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4967-121">Header</span></span><br/> | <dl> <span data-ttu-id="d4967-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4967-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4967-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4967-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4967-124">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="d4967-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
