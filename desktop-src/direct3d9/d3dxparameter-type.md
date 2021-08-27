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
ms.openlocfilehash: 2d342e664aac81cf337cde2de7669c94a4ac6c94ce85c564a29da1f38dd93bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096189"
---
# <a name="d3dxparameter_type-enumeration"></a>\_Énumération de type D3DXPARAMETER

Décrit les données contenues par l’énumération.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**
</dt> <dd>

Le paramètre est un pointeur void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ bool**
</dt> <dd>

Le paramètre est une valeur booléenne. Toute valeur différente de zéro passée dans [**ID3DXConstantTable :: SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable :: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable :: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable :: SetVector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable :: SetVectorArray**](id3dxconstanttable--setvectorarray.md) sera mappée à 1 (true) avant d’être écrite dans la table de constantes ; dans le cas contraire, la valeur sera définie sur 0 dans la table constante.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**
</dt> <dd>

Le paramètre est un entier. Toutes les valeurs à virgule flottante passées dans [**ID3DXConstantTable :: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable :: SetVector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable :: SetVectorArray**](id3dxconstanttable--setvectorarray.md) sont arrondies (à zéro décimal) avant d’être écrites dans la table constante.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**
</dt> <dd>

Le paramètre est un nombre à virgule flottante.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Chaîne D3DXPT**
</dt> <dd>

Le paramètre est une chaîne.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Texture D3DXPT**
</dt> <dd>

Le paramètre est une texture.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

Le paramètre est une texture 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

Le paramètre est une texture 2D.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

Le paramètre est une texture 3D.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

Le paramètre est une texture de cube.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Échantillonneur D3DXPT**
</dt> <dd>

Le paramètre est un échantillonneur.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

Le paramètre est un échantillonneur 1J.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

Le paramètre est un échantillonneur 2D.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

Le paramètre est un échantillonneur 3D.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

Le paramètre est un échantillonneur de cube.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**
</dt> <dd>

Le paramètre est un nuanceur de pixels.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

Le paramètre est un nuanceur de sommets.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

Le paramètre est un fragment de nuanceur de pixels.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

Le paramètre est un fragment de nuanceur de sommets.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ non pris en charge**
</dt> <dd>

Le paramètre n’est pas pris en charge.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)
</dt> </dl>

 

 




