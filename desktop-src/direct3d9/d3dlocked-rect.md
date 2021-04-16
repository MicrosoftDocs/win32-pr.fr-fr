---
description: Décrit une zone rectangulaire verrouillée.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Structure D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530957"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="d2543-103">D3DLOCKED \_ Rect, structure</span><span class="sxs-lookup"><span data-stu-id="d2543-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="d2543-104">Décrit une zone rectangulaire verrouillée.</span><span class="sxs-lookup"><span data-stu-id="d2543-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2543-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2543-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="d2543-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d2543-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2543-107">**Inclinaison**</span><span class="sxs-lookup"><span data-stu-id="d2543-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="d2543-108">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2543-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2543-109">Nombre d’octets dans une ligne de la surface.</span><span class="sxs-lookup"><span data-stu-id="d2543-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="d2543-110">**pBits**</span><span class="sxs-lookup"><span data-stu-id="d2543-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="d2543-111">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="d2543-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="d2543-112">Pointeur vers les bits verrouillés.</span><span class="sxs-lookup"><span data-stu-id="d2543-112">Pointer to the locked bits.</span></span> <span data-ttu-id="d2543-113">Si un [**Rect**](/previous-versions//dd162897(v=vs.85)) a été fourni à l’appel [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits sera correctement décalé à partir du début de l’aire.</span><span class="sxs-lookup"><span data-stu-id="d2543-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2543-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d2543-114">Remarks</span></span>

<span data-ttu-id="d2543-115">Le pas pour les formats DXTn est différent de ce qui a été retourné dans DirectX 7.</span><span class="sxs-lookup"><span data-stu-id="d2543-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="d2543-116">Il fait maintenant référence au nombre d’octets dans une ligne de blocs.</span><span class="sxs-lookup"><span data-stu-id="d2543-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="d2543-117">Par exemple, si vous avez une largeur de 16, vous obtiendrez un pas de 4 blocs (4 \* 8 pour DXT1, 4 \* pour DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="d2543-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="d2543-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2543-118">Requirements</span></span>



| <span data-ttu-id="d2543-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2543-119">Requirement</span></span> | <span data-ttu-id="d2543-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2543-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2543-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2543-121">Header</span></span><br/> | <dl> <span data-ttu-id="d2543-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2543-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2543-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2543-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2543-124">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="d2543-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d2543-125">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="d2543-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="d2543-126">**IDirect3DSurface9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="d2543-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="d2543-127">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="d2543-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
