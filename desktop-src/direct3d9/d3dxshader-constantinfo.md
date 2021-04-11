---
description: D3DXSHADER \_ CONSTANTINFO, structure
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Structure D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211744"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="2c9ae-103">D3DXSHADER \_ CONSTANTINFO, structure</span><span class="sxs-lookup"><span data-stu-id="2c9ae-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9ae-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c9ae-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="2c9ae-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2c9ae-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c9ae-106">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-107">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-108">Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations de constante.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-109">**RegisterSet**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-110">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-111">Ensemble de registres.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-111">Register set.</span></span> <span data-ttu-id="2c9ae-112">Consultez [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="2c9ae-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-113">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-114">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-115">Index du Registre.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-116">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-117">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-118">Nombre de registres.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-120">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-124">Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations [**\_ TypeInfo D3DXSHADER**](d3dxshader-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2c9ae-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ae-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="2c9ae-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c9ae-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c9ae-127">Offset à partir du début de cette structure, en octets, à la chaîne qui contient la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c9ae-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c9ae-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c9ae-128">Requirements</span></span>



| <span data-ttu-id="2c9ae-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c9ae-129">Requirement</span></span> | <span data-ttu-id="2c9ae-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c9ae-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9ae-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c9ae-131">Header</span></span><br/> | <dl> <span data-ttu-id="2c9ae-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9ae-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c9ae-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c9ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9ae-134">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="2c9ae-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
