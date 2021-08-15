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
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989959"
---
# <a name="d3dx11_effect_type_desc-structure"></a>D3DX11 \_ , \_ type d’effet DESC, \_ structure

Décrit un type de variable Effect.

## <a name="syntax"></a>Syntaxe


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



## <a name="members"></a>Membres

<dl> <dt>

**TypeName**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nom du type, par exemple « float4 » ou « MyStruct ».

</dd> <dt>

**Classe**
</dt> <dd>

Type : **[ **\_ classe de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

La classe variable (voir [**\_ classe de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **\_ type de \_ variable \_ de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Le type de variable ( [**consultez \_ \_ \_ type de variable de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Éléments**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’éléments dans ce type (0 s’il ne s’agit pas d’un tableau).

</dd> <dt>

**Members** (Membres)
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de membres (0 s’il ne s’agit pas d’une structure).

</dd> <dt>

**Lignes**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de lignes dans ce type (0 s’il ne s’agit pas d’une primitive numérique).

</dd> <dt>

**Colonnes**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de colonnes dans ce type (0 s’il ne s’agit pas d’une primitive numérique).

</dd> <dt>

**PackedSize**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’octets requis pour représenter ce type de données, quand il est fortement compressé.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’octets occupés par ce type de données, lorsqu’ils sont disposés dans une mémoire tampon constante.

</dd> <dt>

**Progrès**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’octets à rechercher entre les éléments, lorsqu’ils sont disposés dans une mémoire tampon constante.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le \_ \_ type d’effet D3DX11 \_ desc est utilisé avec [ **ID3DX11EffectType :: GetDesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

