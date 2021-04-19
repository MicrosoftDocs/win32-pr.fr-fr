---
description: Informations sur les propriétés d’un mode d’affichage.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: D3DDISPLAYMODEEX, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535799"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="be434-103">D3DDISPLAYMODEEX, structure</span><span class="sxs-lookup"><span data-stu-id="be434-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="be434-104">Informations sur les propriétés d’un mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="be434-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="be434-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be434-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="be434-106">Membres</span><span class="sxs-lookup"><span data-stu-id="be434-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be434-107">**Taille**</span><span class="sxs-lookup"><span data-stu-id="be434-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="be434-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-109">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="be434-109">The size of this structure.</span></span> <span data-ttu-id="be434-110">Il doit toujours être défini sur sizeof (D3DDISPLAYMODEEX).</span><span class="sxs-lookup"><span data-stu-id="be434-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="be434-111">**Width**</span><span class="sxs-lookup"><span data-stu-id="be434-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="be434-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-113">Largeur du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="be434-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="be434-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="be434-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="be434-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-116">Hauteur du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="be434-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="be434-117">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="be434-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="be434-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-119">Fréquence d’actualisation du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="be434-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="be434-120">**Format**</span><span class="sxs-lookup"><span data-stu-id="be434-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="be434-121">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-122">Format du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="be434-122">Format of the display mode.</span></span> <span data-ttu-id="be434-123">Consultez [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="be434-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="be434-124">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="be434-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="be434-125">Type : **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="be434-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be434-126">Indique si l’ordre de numérisation est progressif ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="be434-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="be434-127">Consultez [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="be434-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be434-128">Notes</span><span class="sxs-lookup"><span data-stu-id="be434-128">Remarks</span></span>

<span data-ttu-id="be434-129">Cette structure est utilisée dans différentes méthodes pour créer et gérer des appareils Direct3D 9Ex ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) et chaînes d’échange ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span><span class="sxs-lookup"><span data-stu-id="be434-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="be434-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be434-130">Requirements</span></span>



| <span data-ttu-id="be434-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be434-131">Requirement</span></span> | <span data-ttu-id="be434-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="be434-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be434-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="be434-133">Header</span></span><br/> | <dl> <span data-ttu-id="be434-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="be434-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be434-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be434-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be434-136">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="be434-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
