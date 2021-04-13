---
description: Structure d’assistance qui contient les informations de structure de membre.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Structure D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322826"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="a8275-103">D3DXSHADER \_ STRUCTMEMBERINFO, structure</span><span class="sxs-lookup"><span data-stu-id="a8275-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="a8275-104">Structure d’assistance qui contient les informations de structure de membre.</span><span class="sxs-lookup"><span data-stu-id="a8275-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8275-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8275-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="a8275-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a8275-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8275-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a8275-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="a8275-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8275-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8275-109">Offset à partir du début de cette structure, en octets, à la chaîne qui contient le nom du membre de structure.</span><span class="sxs-lookup"><span data-stu-id="a8275-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="a8275-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="a8275-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a8275-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8275-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8275-112">Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations de type.</span><span class="sxs-lookup"><span data-stu-id="a8275-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="a8275-113">Consultez [**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a8275-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8275-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8275-114">Requirements</span></span>



| <span data-ttu-id="a8275-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8275-115">Requirement</span></span> | <span data-ttu-id="a8275-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8275-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8275-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8275-117">Header</span></span><br/> | <dl> <span data-ttu-id="a8275-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8275-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8275-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8275-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8275-120">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="a8275-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a8275-121">**D3DXSHADER \_ TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="a8275-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
