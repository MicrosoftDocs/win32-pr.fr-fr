---
description: Structure d’assistance pour la gestion d’une table de constantes de nuanceur. Cela peut également être fait à l’aide de ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Structure D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522954"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="87f8e-104">D3DXSHADER \_ CONSTANTTABLE, structure</span><span class="sxs-lookup"><span data-stu-id="87f8e-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="87f8e-105">Structure d’assistance pour la gestion d’une table de constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="87f8e-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="87f8e-106">Cela peut également être fait à l’aide de [**ID3DXConstantTable**](id3dxconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="87f8e-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="87f8e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87f8e-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="87f8e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="87f8e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="87f8e-109">**Taille**</span><span class="sxs-lookup"><span data-stu-id="87f8e-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-110">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-111">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="87f8e-111">Size of the structure.</span></span> <span data-ttu-id="87f8e-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="87f8e-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-113">**Creator**</span><span class="sxs-lookup"><span data-stu-id="87f8e-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-115">Offset à partir du début de cette structure, en octets, à la chaîne qui contient le nom du créateur.</span><span class="sxs-lookup"><span data-stu-id="87f8e-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-116">**Version**</span><span class="sxs-lookup"><span data-stu-id="87f8e-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-118">Version du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="87f8e-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-119">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="87f8e-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-121">Nombre de constantes.</span><span class="sxs-lookup"><span data-stu-id="87f8e-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-122">**ConstantInfo**</span><span class="sxs-lookup"><span data-stu-id="87f8e-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-124">Tableau d’informations constantes, \_ \[ *constantes* CONSTANTINFO D3DXSHADER \] .</span><span class="sxs-lookup"><span data-stu-id="87f8e-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="87f8e-125">Consultez [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="87f8e-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-126">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="87f8e-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-128">Indicateurs [D3DXSHADER Flags](d3dxshader-flags.md) utilisés pour compiler le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="87f8e-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="87f8e-129">**Cible**</span><span class="sxs-lookup"><span data-stu-id="87f8e-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="87f8e-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87f8e-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87f8e-131">Offset dans la chaîne qui contient la cible.</span><span class="sxs-lookup"><span data-stu-id="87f8e-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87f8e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="87f8e-132">Remarks</span></span>

<span data-ttu-id="87f8e-133">Les informations de constante de nuanceur sont incluses dans une table de commentaires délimitée par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="87f8e-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="87f8e-134">Tous les décalages sont mesurés en octets à partir du début de la structure.</span><span class="sxs-lookup"><span data-stu-id="87f8e-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="87f8e-135">Les entrées de la table constante sont triées par créateur dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="87f8e-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="87f8e-136">Une table de constantes de nuanceur peut être gérée avec les interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) .</span><span class="sxs-lookup"><span data-stu-id="87f8e-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="87f8e-137">Vous pouvez également gérer la table constante avec **D3DXSHADER \_ CONSTANTTABLE**.</span><span class="sxs-lookup"><span data-stu-id="87f8e-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="87f8e-138">Ce membre de taille est souvent initialisé à l’aide des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="87f8e-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="87f8e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87f8e-139">Requirements</span></span>



| <span data-ttu-id="87f8e-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87f8e-140">Requirement</span></span> | <span data-ttu-id="87f8e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="87f8e-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f8e-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="87f8e-142">Header</span></span><br/> | <dl> <span data-ttu-id="87f8e-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f8e-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f8e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87f8e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f8e-145">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="87f8e-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="87f8e-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="87f8e-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
