---
description: Spécifie le glyphe source et l’emplacement dans une surface monochrome dans laquelle copier les glyphes.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: D3DCOMPOSERECTDESTINATION, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523174"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="2dde6-103">D3DCOMPOSERECTDESTINATION, structure</span><span class="sxs-lookup"><span data-stu-id="2dde6-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="2dde6-104">Spécifie le glyphe source et l’emplacement dans une surface monochrome dans laquelle copier les glyphes.</span><span class="sxs-lookup"><span data-stu-id="2dde6-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dde6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dde6-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="2dde6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2dde6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2dde6-107">**SrcRectIndex**</span><span class="sxs-lookup"><span data-stu-id="2dde6-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2dde6-108">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dde6-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2dde6-109">Indexez un glyphe particulier à partir de la mémoire tampon de vertex contenant les structures [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .</span><span class="sxs-lookup"><span data-stu-id="2dde6-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="2dde6-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2dde6-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2dde6-111">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dde6-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2dde6-112">Réservé à des fins d’alignement.</span><span class="sxs-lookup"><span data-stu-id="2dde6-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="2dde6-113">**X**</span><span class="sxs-lookup"><span data-stu-id="2dde6-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="2dde6-114">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dde6-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2dde6-115">Coordonnée gauche à laquelle commencer la copie.</span><span class="sxs-lookup"><span data-stu-id="2dde6-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="2dde6-116">**O**</span><span class="sxs-lookup"><span data-stu-id="2dde6-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="2dde6-117">Type : **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dde6-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2dde6-118">Coordonnée supérieure à laquelle commencer la copie.</span><span class="sxs-lookup"><span data-stu-id="2dde6-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dde6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2dde6-119">Remarks</span></span>

<span data-ttu-id="2dde6-120">Cette structure est utilisée dans les appels à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) pour indiquer que les glyphes d’emplacement doivent être copiés vers et quel glyphe particulier doit être copié.</span><span class="sxs-lookup"><span data-stu-id="2dde6-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="2dde6-121">Une mémoire tampon de vertex (voir [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) remplie avec ces structures est créée pour contenir les emplacements de glyphe.</span><span class="sxs-lookup"><span data-stu-id="2dde6-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="2dde6-122">Les membres USHORT sont utilisés pour réduire autant que possible l’encombrement mémoire.</span><span class="sxs-lookup"><span data-stu-id="2dde6-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dde6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dde6-123">Requirements</span></span>



| <span data-ttu-id="2dde6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2dde6-124">Requirement</span></span> | <span data-ttu-id="2dde6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dde6-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dde6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2dde6-126">Header</span></span><br/> | <dl> <span data-ttu-id="2dde6-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dde6-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dde6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dde6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dde6-129">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="2dde6-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
