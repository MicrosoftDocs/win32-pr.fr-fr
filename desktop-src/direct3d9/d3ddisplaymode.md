---
description: Décrit le mode d’affichage.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: D3DDISPLAYMODE, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116194"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="5b67a-103">D3DDISPLAYMODE, structure</span><span class="sxs-lookup"><span data-stu-id="5b67a-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="5b67a-104">Décrit le mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5b67a-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b67a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b67a-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="5b67a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5b67a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b67a-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="5b67a-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="5b67a-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b67a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b67a-109">Largeur de l’écran, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5b67a-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5b67a-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="5b67a-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="5b67a-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b67a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b67a-112">Hauteur de l’écran, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5b67a-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5b67a-113">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="5b67a-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="5b67a-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b67a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b67a-115">Fréquence d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="5b67a-115">Refresh rate.</span></span> <span data-ttu-id="5b67a-116">La valeur 0 indique une valeur par défaut de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5b67a-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="5b67a-117">**Format**</span><span class="sxs-lookup"><span data-stu-id="5b67a-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="5b67a-118">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5b67a-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b67a-119">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5b67a-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b67a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b67a-120">Requirements</span></span>



| <span data-ttu-id="5b67a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b67a-121">Requirement</span></span> | <span data-ttu-id="5b67a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b67a-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b67a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b67a-123">Header</span></span><br/> | <dl> <span data-ttu-id="5b67a-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b67a-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b67a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b67a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b67a-126">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="5b67a-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="5b67a-127">**EnumAdapterModes**</span><span class="sxs-lookup"><span data-stu-id="5b67a-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="5b67a-128">**GetAdapterDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="5b67a-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="5b67a-129">**GetDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="5b67a-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
