---
description: Décrit une surface de rendu.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Structure D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953841"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="f0c3c-103">D3DXRTS \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="f0c3c-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="f0c3c-104">Décrit une surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0c3c-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="f0c3c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f0c3c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0c3c-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="f0c3c-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0c3c-109">Largeur de la surface de rendu, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f0c3c-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="f0c3c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0c3c-112">Hauteur de la surface de rendu, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f0c3c-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="f0c3c-114">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0c3c-115">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f0c3c-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="f0c3c-117">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0c3c-118">Si la **valeur est true**, la surface de rendu prend en charge une surface de stencil de profondeur ; dans le cas contraire, ce membre est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0c3c-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="f0c3c-120">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0c3c-121">Si DepthStencil a la valeur **true**, ce paramètre est un membre du type énuméré [D3DFORMAT](d3dformat.md) , qui décrit le format de stencil de profondeur de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f0c3c-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0c3c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0c3c-122">Requirements</span></span>



| <span data-ttu-id="f0c3c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0c3c-123">Requirement</span></span> | <span data-ttu-id="f0c3c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0c3c-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c3c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0c3c-125">Header</span></span><br/> | <dl> <span data-ttu-id="f0c3c-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c3c-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c3c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0c3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c3c-128">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="f0c3c-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f0c3c-129">**ID3DXRenderToSurface::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="f0c3c-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
