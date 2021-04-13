---
description: Encapsule un objet de maillage dans une hiérarchie de frame de transformation.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: D3DXMESHCONTAINER, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322649"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="888cc-103">D3DXMESHCONTAINER, structure</span><span class="sxs-lookup"><span data-stu-id="888cc-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="888cc-104">Encapsule un objet de maillage dans une hiérarchie de frame de transformation.</span><span class="sxs-lookup"><span data-stu-id="888cc-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="888cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="888cc-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="888cc-106">Membres</span><span class="sxs-lookup"><span data-stu-id="888cc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="888cc-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="888cc-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-108">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="888cc-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-109">Nom du maillage.</span><span class="sxs-lookup"><span data-stu-id="888cc-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="888cc-110">**MeshData**</span><span class="sxs-lookup"><span data-stu-id="888cc-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-111">Type : **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="888cc-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-112">Type de données dans la maille.</span><span class="sxs-lookup"><span data-stu-id="888cc-112">Type of data in the mesh.</span></span> <span data-ttu-id="888cc-113">Consultez [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="888cc-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="888cc-114">**pMaterials**</span><span class="sxs-lookup"><span data-stu-id="888cc-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-115">Type : **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="888cc-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-116">Tableau de supports de maillage.</span><span class="sxs-lookup"><span data-stu-id="888cc-116">Array of mesh materials.</span></span> <span data-ttu-id="888cc-117">Consultez [**D3DXMATERIAL**](d3dxmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="888cc-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="888cc-118">**pEffects**</span><span class="sxs-lookup"><span data-stu-id="888cc-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-119">Type : **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="888cc-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-120">Pointeur vers un ensemble de paramètres d’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="888cc-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="888cc-121">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="888cc-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="888cc-122">**NumMaterials**</span><span class="sxs-lookup"><span data-stu-id="888cc-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="888cc-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-124">Nombre de matériaux dans la maille.</span><span class="sxs-lookup"><span data-stu-id="888cc-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="888cc-125">**pAdjacency**</span><span class="sxs-lookup"><span data-stu-id="888cc-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="888cc-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="888cc-127">Pointeur vers un tableau de trois DWORDs par triangle du maillage qui contient les informations d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="888cc-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="888cc-128">**pSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="888cc-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-129">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="888cc-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="888cc-130">Pointeur vers l’interface d’informations d’apparence.</span><span class="sxs-lookup"><span data-stu-id="888cc-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="888cc-131">Consultez [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="888cc-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="888cc-132">**pNextMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="888cc-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="888cc-133">Type : \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="888cc-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="888cc-134">Pointeur vers le conteneur de maillage suivant.</span><span class="sxs-lookup"><span data-stu-id="888cc-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="888cc-135">Notes</span><span class="sxs-lookup"><span data-stu-id="888cc-135">Remarks</span></span>

<span data-ttu-id="888cc-136">Une application peut dériver de cette structure pour ajouter d’autres données.</span><span class="sxs-lookup"><span data-stu-id="888cc-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="888cc-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="888cc-137">Requirements</span></span>



| <span data-ttu-id="888cc-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="888cc-138">Requirement</span></span> | <span data-ttu-id="888cc-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="888cc-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="888cc-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="888cc-140">Header</span></span><br/> | <dl> <span data-ttu-id="888cc-141"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="888cc-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888cc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="888cc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888cc-143">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="888cc-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
