---
description: Décrit les données contenues par l’énumération.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Énumération D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322638"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="d4d03-103">\_Énumération de type D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4d03-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="d4d03-104">Décrit les données contenues par l’énumération.</span><span class="sxs-lookup"><span data-stu-id="d4d03-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d03-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4d03-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d4d03-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d4d03-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4d03-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="d4d03-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-108">Le paramètre est un pointeur void.</span><span class="sxs-lookup"><span data-stu-id="d4d03-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d4d03-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-110">Le paramètre est une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="d4d03-110">Parameter is a Boolean.</span></span> <span data-ttu-id="d4d03-111">Toute valeur différente de zéro passée dans [**ID3DXConstantTable :: SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable :: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable :: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable :: SetVector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable :: SetVectorArray**](id3dxconstanttable--setvectorarray.md) sera mappée à 1 (true) avant d’être écrite dans la table de constantes ; dans le cas contraire, la valeur sera définie sur 0 dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="d4d03-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**</span><span class="sxs-lookup"><span data-stu-id="d4d03-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-113">Le paramètre est un entier.</span><span class="sxs-lookup"><span data-stu-id="d4d03-113">Parameter is an integer.</span></span> <span data-ttu-id="d4d03-114">Toutes les valeurs à virgule flottante passées dans [**ID3DXConstantTable :: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable :: SetVector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable :: SetVectorArray**](id3dxconstanttable--setvectorarray.md) sont arrondies (à zéro décimal) avant d’être écrites dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="d4d03-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**</span><span class="sxs-lookup"><span data-stu-id="d4d03-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-116">Le paramètre est un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d4d03-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Chaîne D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="d4d03-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-118">Le paramètre est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d4d03-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Texture D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="d4d03-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-120">Le paramètre est une texture.</span><span class="sxs-lookup"><span data-stu-id="d4d03-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-122">Le paramètre est une texture 1D.</span><span class="sxs-lookup"><span data-stu-id="d4d03-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-124">Le paramètre est une texture 2D.</span><span class="sxs-lookup"><span data-stu-id="d4d03-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-126">Le paramètre est une texture 3D.</span><span class="sxs-lookup"><span data-stu-id="d4d03-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**</span><span class="sxs-lookup"><span data-stu-id="d4d03-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-128">Le paramètre est une texture de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d03-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Échantillonneur D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="d4d03-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-130">Le paramètre est un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d4d03-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-132">Le paramètre est un échantillonneur 1J.</span><span class="sxs-lookup"><span data-stu-id="d4d03-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-134">Le paramètre est un échantillonneur 2D.</span><span class="sxs-lookup"><span data-stu-id="d4d03-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="d4d03-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-136">Le paramètre est un échantillonneur 3D.</span><span class="sxs-lookup"><span data-stu-id="d4d03-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**</span><span class="sxs-lookup"><span data-stu-id="d4d03-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-138">Le paramètre est un échantillonneur de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d03-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**</span><span class="sxs-lookup"><span data-stu-id="d4d03-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-140">Le paramètre est un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d03-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="d4d03-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-142">Le paramètre est un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="d4d03-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="d4d03-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-144">Le paramètre est un fragment de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d03-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="d4d03-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-146">Le paramètre est un fragment de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="d4d03-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d4d03-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-148">Le paramètre n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4d03-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4d03-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4d03-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d4d03-150">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="d4d03-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d4d03-151">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d4d03-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d4d03-152">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d4d03-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4d03-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4d03-153">Requirements</span></span>



| <span data-ttu-id="d4d03-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4d03-154">Requirement</span></span> | <span data-ttu-id="d4d03-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d03-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d03-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4d03-156">Header</span></span><br/> | <dl> <span data-ttu-id="d4d03-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d03-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d03-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d03-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d03-159">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="d4d03-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="d4d03-160">**D3DXSHADER \_ TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="d4d03-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d4d03-161">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="d4d03-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




