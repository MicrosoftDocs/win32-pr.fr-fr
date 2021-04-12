---
description: Décrit une case verrouillée (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Structure D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211816"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="255fb-103">\_Structure de la boîte de D3DLOCKED</span><span class="sxs-lookup"><span data-stu-id="255fb-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="255fb-104">Décrit une case verrouillée (volume).</span><span class="sxs-lookup"><span data-stu-id="255fb-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="255fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="255fb-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="255fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="255fb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="255fb-107">**RowPitch**</span><span class="sxs-lookup"><span data-stu-id="255fb-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="255fb-108">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="255fb-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="255fb-109">Offset d’octet à partir du bord gauche d’une ligne jusqu’au bord gauche de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="255fb-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="255fb-110">**SlicePitch**</span><span class="sxs-lookup"><span data-stu-id="255fb-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="255fb-111">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="255fb-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="255fb-112">Décalage d’octet par rapport à l’angle supérieur gauche d’un secteur à l’angle supérieur gauche du secteur le plus profond suivant.</span><span class="sxs-lookup"><span data-stu-id="255fb-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="255fb-113">**pBits**</span><span class="sxs-lookup"><span data-stu-id="255fb-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="255fb-114">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="255fb-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="255fb-115">Pointeur vers le début de la zone de volume.</span><span class="sxs-lookup"><span data-stu-id="255fb-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="255fb-116">Si un [**D3DBOX**](d3dbox.md) a été fourni à l’appel de la boîte postale scellée, pBits sera correctement décalé à partir du début du volume.</span><span class="sxs-lookup"><span data-stu-id="255fb-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="255fb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="255fb-117">Remarks</span></span>

<span data-ttu-id="255fb-118">Les volumes peuvent être visualisés comme étant organisés en secteurs de surfaces 2D de largeur x hauteur empilées pour créer un volume de profondeur x hauteur x profondeur.</span><span class="sxs-lookup"><span data-stu-id="255fb-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="255fb-119">Pour plus d’informations, consultez [ressources de texture de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="255fb-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="255fb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="255fb-120">Requirements</span></span>



| <span data-ttu-id="255fb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="255fb-121">Requirement</span></span> | <span data-ttu-id="255fb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="255fb-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="255fb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="255fb-123">Header</span></span><br/> | <dl> <span data-ttu-id="255fb-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="255fb-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="255fb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="255fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="255fb-126">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="255fb-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="255fb-127">**IDirect3DVolume9 :: LockBox**</span><span class="sxs-lookup"><span data-stu-id="255fb-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="255fb-128">**IDirect3DVolumeTexture9 :: LockBox**</span><span class="sxs-lookup"><span data-stu-id="255fb-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
