---
description: Encapsule un frame de transformation dans une hiérarchie d’frame de transformation.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: D3DXFRAME, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211762"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="f70ca-103">D3DXFRAME, structure</span><span class="sxs-lookup"><span data-stu-id="f70ca-103">D3DXFRAME structure</span></span>

<span data-ttu-id="f70ca-104">Encapsule un frame de transformation dans une hiérarchie d’frame de transformation.</span><span class="sxs-lookup"><span data-stu-id="f70ca-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f70ca-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="f70ca-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f70ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f70ca-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f70ca-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f70ca-108">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="f70ca-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f70ca-109">Nom du frame.</span><span class="sxs-lookup"><span data-stu-id="f70ca-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f70ca-110">**TransformationMatrix**</span><span class="sxs-lookup"><span data-stu-id="f70ca-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="f70ca-111">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="f70ca-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f70ca-112">Matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="f70ca-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f70ca-113">**pMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="f70ca-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="f70ca-114">Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="f70ca-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f70ca-115">Pointeur vers le conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="f70ca-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="f70ca-116">**pFrameSibling**</span><span class="sxs-lookup"><span data-stu-id="f70ca-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="f70ca-117">Type : \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="f70ca-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="f70ca-118">Pointeur vers un frame frère.</span><span class="sxs-lookup"><span data-stu-id="f70ca-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="f70ca-119">**pFrameFirstChild**</span><span class="sxs-lookup"><span data-stu-id="f70ca-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="f70ca-120">Type : \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="f70ca-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="f70ca-121">Pointeur vers un Frame enfant.</span><span class="sxs-lookup"><span data-stu-id="f70ca-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f70ca-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f70ca-122">Remarks</span></span>

<span data-ttu-id="f70ca-123">Une application peut dériver de cette structure pour ajouter d’autres données.</span><span class="sxs-lookup"><span data-stu-id="f70ca-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70ca-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f70ca-124">Requirements</span></span>



| <span data-ttu-id="f70ca-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f70ca-125">Requirement</span></span> | <span data-ttu-id="f70ca-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f70ca-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f70ca-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f70ca-127">Header</span></span><br/> | <dl> <span data-ttu-id="f70ca-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70ca-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70ca-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f70ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70ca-130">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="f70ca-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




