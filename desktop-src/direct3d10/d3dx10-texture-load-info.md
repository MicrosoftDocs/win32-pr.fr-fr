---
description: Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Structure D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522598"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="33eff-103">\_Structure d' \_ \_ informations sur le chargement de la texture d3dx10</span><span class="sxs-lookup"><span data-stu-id="33eff-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="33eff-104">Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.</span><span class="sxs-lookup"><span data-stu-id="33eff-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="33eff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33eff-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="33eff-106">Membres</span><span class="sxs-lookup"><span data-stu-id="33eff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="33eff-107">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="33eff-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-108">Type : **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="33eff-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="33eff-109">Zone texture source (consultez [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="33eff-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="33eff-110">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="33eff-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-111">Type : **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="33eff-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="33eff-112">Zone texture de destination (voir [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="33eff-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="33eff-113">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="33eff-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-115">Niveau de mipmap de la texture source, consultez [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="33eff-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-116">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="33eff-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-118">Niveau de mipmap de texture de destination, consultez [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="33eff-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-119">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="33eff-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-121">Nombre de niveaux de mipmap dans la texture source.</span><span class="sxs-lookup"><span data-stu-id="33eff-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-122">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="33eff-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-124">Premier élément de la texture source.</span><span class="sxs-lookup"><span data-stu-id="33eff-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-125">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="33eff-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-127">Premier élément de la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="33eff-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="33eff-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-130">Nombre d’éléments à charger.</span><span class="sxs-lookup"><span data-stu-id="33eff-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="33eff-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="33eff-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-133">Options de filtrage pendant le rééchantillonnage (voir [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="33eff-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="33eff-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="33eff-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="33eff-135">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33eff-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33eff-136">Options de filtrage lors de la génération de niveaux MIP (voir [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="33eff-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33eff-137">Notes</span><span class="sxs-lookup"><span data-stu-id="33eff-137">Remarks</span></span>

<span data-ttu-id="33eff-138">Cette structure est utilisée dans un appel à [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="33eff-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33eff-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33eff-139">Requirements</span></span>



| <span data-ttu-id="33eff-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33eff-140">Requirement</span></span> | <span data-ttu-id="33eff-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="33eff-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33eff-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="33eff-142">Header</span></span><br/> | <dl> <span data-ttu-id="33eff-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="33eff-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33eff-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33eff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33eff-145">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="33eff-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
