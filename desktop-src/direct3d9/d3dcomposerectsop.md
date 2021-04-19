---
description: Spécifie comment combiner les données de glyphe des surfaces source et de destination dans un appel à ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Énumération D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529601"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="89fda-103">Énumération D3DCOMPOSERECTSOP</span><span class="sxs-lookup"><span data-stu-id="89fda-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="89fda-104">Spécifie comment combiner les données de glyphe des surfaces source et de destination dans un appel à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span><span class="sxs-lookup"><span data-stu-id="89fda-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="89fda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89fda-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="89fda-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="89fda-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="89fda-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**\_Copie D3DCOMPOSERECTS**</span><span class="sxs-lookup"><span data-stu-id="89fda-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="89fda-108">Copiez la source vers la destination.</span><span class="sxs-lookup"><span data-stu-id="89fda-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="89fda-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ ou**</span><span class="sxs-lookup"><span data-stu-id="89fda-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="89fda-110">Au niveau du bit ou de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="89fda-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="89fda-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ et**</span><span class="sxs-lookup"><span data-stu-id="89fda-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="89fda-112">Au niveau du bit et de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="89fda-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="89fda-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ nég**</span><span class="sxs-lookup"><span data-stu-id="89fda-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="89fda-114">Copiez la source négative vers la destination (DST & ~ SRC).</span><span class="sxs-lookup"><span data-stu-id="89fda-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="89fda-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="89fda-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="89fda-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="89fda-116">Reserved.</span></span> <span data-ttu-id="89fda-117">Utilisé pour forcer l’énumération à une taille de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="89fda-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89fda-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89fda-118">Requirements</span></span>



| <span data-ttu-id="89fda-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89fda-119">Requirement</span></span> | <span data-ttu-id="89fda-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="89fda-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89fda-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="89fda-121">Header</span></span><br/> | <dl> <span data-ttu-id="89fda-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="89fda-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fda-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89fda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fda-124">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="89fda-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




