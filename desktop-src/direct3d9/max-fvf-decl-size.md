---
description: Cette constante est le nombre maximal de déclarateurs de vertex pour une maille.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Énumération MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538055"
---
# <a name="max_fvf_decl_size-enumeration"></a><span data-ttu-id="dcea3-103">\_Énumération Max Commission de la \_ \_ taille decl</span><span class="sxs-lookup"><span data-stu-id="dcea3-103">MAX\_FVF\_DECL\_SIZE enumeration</span></span>

<span data-ttu-id="dcea3-104">Cette constante est le nombre maximal de déclarateurs de vertex pour une maille.</span><span class="sxs-lookup"><span data-stu-id="dcea3-104">This constant is the maximum number of vertex declarators for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcea3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcea3-105">Syntax</span></span>


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a><span data-ttu-id="dcea3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dcea3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dcea3-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**\_taille de \_ décl max. \_**</span><span class="sxs-lookup"><span data-stu-id="dcea3-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX\_FVF\_DECL\_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="dcea3-108">Nombre maximal d’éléments dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="dcea3-108">The maximum number of elements in the vertex declaration.</span></span> <span data-ttu-id="dcea3-109">Le supplémentaire (+ 1) est pour [**la \_ terminaison D3DDECL**](d3ddecl-end.md).</span><span class="sxs-lookup"><span data-stu-id="dcea3-109">The additional (+1) is for [**D3DDECL\_END**](d3ddecl-end.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcea3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dcea3-110">Remarks</span></span>

<span data-ttu-id="dcea3-111">MAXD3DDECLLENGTH est défini comme un maximum de 64 (voir d3d9types. h).</span><span class="sxs-lookup"><span data-stu-id="dcea3-111">MAXD3DDECLLENGTH is defined as a maximum of 64 (see d3d9types.h).</span></span> <span data-ttu-id="dcea3-112">Cela n’inclut pas l’élément de vertex du marqueur « end ».</span><span class="sxs-lookup"><span data-stu-id="dcea3-112">This does not include the "end" marker vertex element.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcea3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcea3-113">Requirements</span></span>



| <span data-ttu-id="dcea3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcea3-114">Requirement</span></span> | <span data-ttu-id="dcea3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcea3-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcea3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcea3-116">Header</span></span><br/> | <dl> <span data-ttu-id="dcea3-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcea3-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcea3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcea3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcea3-119">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="dcea3-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="dcea3-120">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="dcea3-120">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="dcea3-121">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="dcea3-121">**GetDeclaration**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[<span data-ttu-id="dcea3-122">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="dcea3-122">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[<span data-ttu-id="dcea3-123">**ID3DXSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="dcea3-123">**ID3DXSkinInfo**</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
