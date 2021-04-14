---
description: Spécifie le rectangle utilisé pour encadrer les glyphes sur une surface monochrome.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: D3DCOMPOSERECTDESC, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394079"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="d1cf9-103">D3DCOMPOSERECTDESC, structure</span><span class="sxs-lookup"><span data-stu-id="d1cf9-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="d1cf9-104">Spécifie le rectangle utilisé pour encadrer les glyphes sur une surface monochrome.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cf9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1cf9-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="d1cf9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d1cf9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1cf9-107">**X**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="d1cf9-108">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1cf9-109">Coordonnée gauche à laquelle commencer la copie.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="d1cf9-110">**O**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="d1cf9-111">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1cf9-112">Coordonnée supérieure à laquelle commencer la copie.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="d1cf9-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d1cf9-114">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1cf9-115">Nombre de texels de la coordonnée gauche.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d1cf9-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d1cf9-117">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1cf9-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1cf9-118">Nombre de texels de la coordonnée supérieure.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1cf9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d1cf9-119">Remarks</span></span>

<span data-ttu-id="d1cf9-120">Cette structure est utilisée dans les appels à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) pour encadrer les glyphes sur la surface source.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="d1cf9-121">Une mémoire tampon de vertex (voir [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) remplie avec ces structures est créée pour contenir les emplacements de glyphe.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="d1cf9-122">Les membres USHORT sont utilisés pour réduire autant que possible l’encombrement mémoire.</span><span class="sxs-lookup"><span data-stu-id="d1cf9-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cf9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1cf9-123">Requirements</span></span>



| <span data-ttu-id="d1cf9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1cf9-124">Requirement</span></span> | <span data-ttu-id="d1cf9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1cf9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cf9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1cf9-126">Header</span></span><br/> | <dl> <span data-ttu-id="d1cf9-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1cf9-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cf9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1cf9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cf9-129">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="d1cf9-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
