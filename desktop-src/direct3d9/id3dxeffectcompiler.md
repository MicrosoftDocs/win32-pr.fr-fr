---
description: L’interface ID3DXEffectCompiler compile un effet à partir d’une fonction ou d’un nuanceur de sommets.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interface ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322714"
---
# <a name="id3dxeffectcompiler-interface"></a>Interface ID3DXEffectCompiler

L’interface **ID3DXEffectCompiler** compile un effet à partir d’une fonction ou d’un nuanceur de sommets.

## <a name="members"></a>Membres

L’interface **ID3DXEffectCompiler** hérite de [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXEffectCompiler** possède ces méthodes.



| Méthode                                                      | Description                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Compilez un effet.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | Obtient un État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.<br/>      |
| [**SetLiteral**](id3dxeffectcompiler--setliteral.md)       | Active/désactive l’État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.<br/> |



 

## <a name="remarks"></a>Notes

L’interface ID3DXEffectCompiler est obtenue en appelant [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)ou [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).

Le type LPD3DXEFFECTCOMPILER est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces d’effet](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




