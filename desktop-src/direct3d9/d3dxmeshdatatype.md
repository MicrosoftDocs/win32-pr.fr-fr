---
description: Définit le type de données de maillage présentes dans D3DXMESHDATA.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: Énumération D3DXMESHDATATYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536244"
---
# <a name="d3dxmeshdatatype-enumeration"></a><span data-ttu-id="d7d48-103">Énumération D3DXMESHDATATYPE</span><span class="sxs-lookup"><span data-stu-id="d7d48-103">D3DXMESHDATATYPE enumeration</span></span>

<span data-ttu-id="d7d48-104">Définit le type de données de maillage présentes dans [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="d7d48-104">Defines the type of mesh data present in [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7d48-105">Syntax</span></span>


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a><span data-ttu-id="d7d48-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d7d48-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7d48-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**\_Maille D3DXMESHTYPE**</span><span class="sxs-lookup"><span data-stu-id="d7d48-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="d7d48-108">Le type de données est une maille.</span><span class="sxs-lookup"><span data-stu-id="d7d48-108">The data type is a mesh.</span></span> <span data-ttu-id="d7d48-109">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="d7d48-109">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d48-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ PATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="d7d48-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE\_PATCHMESH**</span></span>
</dt> <dd>

<span data-ttu-id="d7d48-111">Le type de données est un maillage de correctifs.</span><span class="sxs-lookup"><span data-stu-id="d7d48-111">The data type is a patch mesh.</span></span> <span data-ttu-id="d7d48-112">Consultez [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="d7d48-112">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d48-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d7d48-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d7d48-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="d7d48-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d7d48-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d7d48-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d7d48-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d7d48-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7d48-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7d48-117">Requirements</span></span>



| <span data-ttu-id="d7d48-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7d48-118">Requirement</span></span> | <span data-ttu-id="d7d48-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7d48-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d48-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7d48-120">Header</span></span><br/> | <dl> <span data-ttu-id="d7d48-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d48-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d48-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d48-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d48-123">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="d7d48-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="d7d48-124">**D3DXMESHDATA**</span><span class="sxs-lookup"><span data-stu-id="d7d48-124">**D3DXMESHDATA**</span></span>](d3dxmeshdata.md)
</dt> </dl>

 

 




