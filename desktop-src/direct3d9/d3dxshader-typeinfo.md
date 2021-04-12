---
description: Structure d’assistance qui contient les informations de type de membre.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Structure D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322862"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="66b67-103">D3DXSHADER \_ TypeInfo, structure</span><span class="sxs-lookup"><span data-stu-id="66b67-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="66b67-104">Structure d’assistance qui contient les informations de type de membre.</span><span class="sxs-lookup"><span data-stu-id="66b67-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b67-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66b67-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="66b67-106">Membres</span><span class="sxs-lookup"><span data-stu-id="66b67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="66b67-107">**Classe**</span><span class="sxs-lookup"><span data-stu-id="66b67-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-108">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-109">Type d’objet Shader.</span><span class="sxs-lookup"><span data-stu-id="66b67-109">Shader object type.</span></span> <span data-ttu-id="66b67-110">Consultez [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="66b67-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="66b67-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="66b67-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-112">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-113">Type de données.</span><span class="sxs-lookup"><span data-stu-id="66b67-113">Data type.</span></span> <span data-ttu-id="66b67-114">Consultez [**\_ type D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="66b67-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="66b67-115">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="66b67-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-116">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-117">Nombre de lignes de matrice (matrices).</span><span class="sxs-lookup"><span data-stu-id="66b67-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="66b67-118">**Colonnes**</span><span class="sxs-lookup"><span data-stu-id="66b67-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-119">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-120">Nombre de colonnes (vecteurs et matrices).</span><span class="sxs-lookup"><span data-stu-id="66b67-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="66b67-121">**Éléments**</span><span class="sxs-lookup"><span data-stu-id="66b67-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-122">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-123">Dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="66b67-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="66b67-124">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="66b67-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-125">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-126">Nombre de membres de structure.</span><span class="sxs-lookup"><span data-stu-id="66b67-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="66b67-127">**StructMemberInfo**</span><span class="sxs-lookup"><span data-stu-id="66b67-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="66b67-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66b67-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66b67-129">Tableau d’informations sur les membres de la structure, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] .</span><span class="sxs-lookup"><span data-stu-id="66b67-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="66b67-130">Consultez [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="66b67-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66b67-131">Notes</span><span class="sxs-lookup"><span data-stu-id="66b67-131">Remarks</span></span>

<span data-ttu-id="66b67-132">Les informations de type font partie de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="66b67-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66b67-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66b67-133">Requirements</span></span>



| <span data-ttu-id="66b67-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66b67-134">Requirement</span></span> | <span data-ttu-id="66b67-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="66b67-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b67-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="66b67-136">Header</span></span><br/> | <dl> <span data-ttu-id="66b67-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b67-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b67-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66b67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b67-139">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="66b67-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="66b67-140">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="66b67-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
