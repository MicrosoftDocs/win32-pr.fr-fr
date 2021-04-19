---
description: Retourne des informations matérielles enregistrées dans des fichiers Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: D3DXMATERIAL, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524840"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="7f78b-103">D3DXMATERIAL, structure</span><span class="sxs-lookup"><span data-stu-id="7f78b-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="7f78b-104">Retourne des informations matérielles enregistrées dans des fichiers Direct3D (. x).</span><span class="sxs-lookup"><span data-stu-id="7f78b-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f78b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f78b-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="7f78b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7f78b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f78b-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="7f78b-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="7f78b-108">Type : **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="7f78b-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f78b-109">Structure [**D3DMATERIAL9**](d3dmaterial9.md) qui décrit les propriétés du matériau.</span><span class="sxs-lookup"><span data-stu-id="7f78b-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="7f78b-110">**pTextureFilename**</span><span class="sxs-lookup"><span data-stu-id="7f78b-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="7f78b-111">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="7f78b-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7f78b-112">Pointeur vers une chaîne qui spécifie le nom de fichier de la texture.</span><span class="sxs-lookup"><span data-stu-id="7f78b-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f78b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7f78b-113">Remarks</span></span>

<span data-ttu-id="7f78b-114">Les fonctions [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) et [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) retournent un tableau de structures **D3DXMATERIAL** qui spécifient la couleur matérielle et le nom de la texture pour chaque matériau de la maille.</span><span class="sxs-lookup"><span data-stu-id="7f78b-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="7f78b-115">L’application est ensuite requise pour charger la texture.</span><span class="sxs-lookup"><span data-stu-id="7f78b-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="7f78b-116">Le type LPD3DXMATERIAL est défini en tant que pointeur vers la structure **D3DXMATERIAL** .</span><span class="sxs-lookup"><span data-stu-id="7f78b-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="7f78b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f78b-117">Requirements</span></span>



| <span data-ttu-id="7f78b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f78b-118">Requirement</span></span> | <span data-ttu-id="7f78b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f78b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f78b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f78b-120">Header</span></span><br/> | <dl> <span data-ttu-id="7f78b-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f78b-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f78b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f78b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f78b-123">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="7f78b-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7f78b-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="7f78b-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="7f78b-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="7f78b-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




