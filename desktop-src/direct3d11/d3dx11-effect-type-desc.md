---
title: Structure D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Décrit un type de variable Effect.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- Structure D3DX11_EFFECT_TYPE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870181"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="266ca-104">D3DX11 \_ , \_ type d’effet DESC, \_ structure</span><span class="sxs-lookup"><span data-stu-id="266ca-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="266ca-105">Décrit un type de variable Effect.</span><span class="sxs-lookup"><span data-stu-id="266ca-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="266ca-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="266ca-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="266ca-107">Membres</span><span class="sxs-lookup"><span data-stu-id="266ca-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="266ca-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="266ca-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-109">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-110">Nom du type, par exemple « float4 » ou « MyStruct ».</span><span class="sxs-lookup"><span data-stu-id="266ca-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="266ca-111">**Classe**</span><span class="sxs-lookup"><span data-stu-id="266ca-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-112">Type : **[ **\_ classe de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="266ca-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-113">La classe variable (voir [**\_ classe de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="266ca-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="266ca-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-115">Type : **[ **\_ type de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="266ca-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-116">Le type de variable ( [**consultez \_ \_ \_ type de variable de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="266ca-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-117">**Éléments**</span><span class="sxs-lookup"><span data-stu-id="266ca-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-119">Nombre d’éléments dans ce type (0 s’il ne s’agit pas d’un tableau).</span><span class="sxs-lookup"><span data-stu-id="266ca-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-120">**Members** (Membres)</span><span class="sxs-lookup"><span data-stu-id="266ca-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-122">Nombre de membres (0 s’il ne s’agit pas d’une structure).</span><span class="sxs-lookup"><span data-stu-id="266ca-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-123">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="266ca-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-124">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-125">Nombre de lignes dans ce type (0 s’il ne s’agit pas d’une primitive numérique).</span><span class="sxs-lookup"><span data-stu-id="266ca-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-126">**Colonnes**</span><span class="sxs-lookup"><span data-stu-id="266ca-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-127">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-128">Nombre de colonnes dans ce type (0 s’il ne s’agit pas d’une primitive numérique).</span><span class="sxs-lookup"><span data-stu-id="266ca-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="266ca-129">**PackedSize**</span><span class="sxs-lookup"><span data-stu-id="266ca-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-130">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-131">Nombre d’octets requis pour représenter ce type de données, quand il est fortement compressé.</span><span class="sxs-lookup"><span data-stu-id="266ca-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="266ca-132">**UnpackedSize**</span><span class="sxs-lookup"><span data-stu-id="266ca-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-133">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-134">Nombre d’octets occupés par ce type de données, lorsqu’ils sont disposés dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="266ca-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="266ca-135">**Progrès**</span><span class="sxs-lookup"><span data-stu-id="266ca-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="266ca-136">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="266ca-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="266ca-137">Nombre d’octets à rechercher entre les éléments, lorsqu’ils sont disposés dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="266ca-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="266ca-138">Notes</span><span class="sxs-lookup"><span data-stu-id="266ca-138">Remarks</span></span>

<span data-ttu-id="266ca-139">Le \_ \_ type d’effet D3DX11 \_ desc est utilisé avec [ **ID3DX11EffectType :: GetDesc**](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="266ca-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="266ca-140">Spécifications</span><span class="sxs-lookup"><span data-stu-id="266ca-140">Requirements</span></span>



| <span data-ttu-id="266ca-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="266ca-141">Requirement</span></span> | <span data-ttu-id="266ca-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="266ca-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="266ca-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="266ca-143">Header</span></span><br/> | <dl> <span data-ttu-id="266ca-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="266ca-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266ca-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="266ca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266ca-146">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="266ca-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

