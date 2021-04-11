---
description: Décrit un paramètre utilisé pour un objet Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Structure D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211685"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="32a50-103">D3DXPARAMETER \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="32a50-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="32a50-104">Décrit un paramètre utilisé pour un objet Effect.</span><span class="sxs-lookup"><span data-stu-id="32a50-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a50-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32a50-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="32a50-106">Membres</span><span class="sxs-lookup"><span data-stu-id="32a50-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32a50-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="32a50-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-109">Nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="32a50-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-110">**Équivalent**</span><span class="sxs-lookup"><span data-stu-id="32a50-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-112">La signification sémantique, également appelée utilisation.</span><span class="sxs-lookup"><span data-stu-id="32a50-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-113">**Classe**</span><span class="sxs-lookup"><span data-stu-id="32a50-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-114">Type : **[ **D3DXPARAMETER, \_ classe**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-115">Classe de paramètre.</span><span class="sxs-lookup"><span data-stu-id="32a50-115">Parameter class.</span></span> <span data-ttu-id="32a50-116">Définissez cette valeur sur l’une des valeurs de la [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="32a50-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="32a50-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="32a50-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-118">Type : **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-119">Type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="32a50-119">Parameter type.</span></span> <span data-ttu-id="32a50-120">Définissez cette valeur sur l’une des valeurs [**de \_ type D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="32a50-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="32a50-121">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="32a50-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-123">Nombre de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="32a50-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-124">**Colonnes**</span><span class="sxs-lookup"><span data-stu-id="32a50-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-125">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-126">Nombre de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="32a50-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-127">**Éléments**</span><span class="sxs-lookup"><span data-stu-id="32a50-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-128">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-129">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="32a50-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-130">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="32a50-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-131">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-132">Nombre d’annotations.</span><span class="sxs-lookup"><span data-stu-id="32a50-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-133">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="32a50-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-134">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-135">Nombre de membres de structure.</span><span class="sxs-lookup"><span data-stu-id="32a50-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="32a50-136">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="32a50-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-137">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-138">Attributs du paramètre.</span><span class="sxs-lookup"><span data-stu-id="32a50-138">Parameter attributes.</span></span> <span data-ttu-id="32a50-139">Consultez [effets, constantes](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="32a50-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="32a50-140">**Octets**</span><span class="sxs-lookup"><span data-stu-id="32a50-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="32a50-141">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32a50-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32a50-142">Taille du paramètre, en octets.</span><span class="sxs-lookup"><span data-stu-id="32a50-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32a50-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32a50-143">Requirements</span></span>



| <span data-ttu-id="32a50-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32a50-144">Requirement</span></span> | <span data-ttu-id="32a50-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="32a50-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a50-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="32a50-146">Header</span></span><br/> | <dl> <span data-ttu-id="32a50-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="32a50-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a50-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32a50-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a50-149">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="32a50-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
