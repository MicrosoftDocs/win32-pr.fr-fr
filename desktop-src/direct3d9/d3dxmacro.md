---
description: Décrit les définitions de préprocesseur utilisées par un objet Effect.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: D3DXMACRO, structure (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: fa78c69ffe0c25b66e73da6fd9139c3b1f69661e5237c3c03e4dd2d8a377461d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095946"
---
# <a name="d3dxmacro-structure"></a>D3DXMACRO, structure

Décrit les définitions de préprocesseur utilisées par un objet Effect.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nom du préprocesseur.

</dd> <dt>

**Définition**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nom de la définition.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour utiliser **D3DXMACRO** sur plusieurs lignes, préfixez chaque caractère de nouvelle ligne avec une barre oblique inverse (par exemple, une \# définition dans le langage C). Par exemple :


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Notez les 3 barres obliques inverses à la fin de la ligne. Les deux premières sont requises pour générer un seul « \\ », suivi du caractère de saut de ligne « \\ n ». Si vous le souhaitez, vous pouvez également mettre fin à vos lignes à l’aide de « \\ \\ \\ r \\ n ».

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
