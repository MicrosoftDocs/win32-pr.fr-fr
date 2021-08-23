---
description: La sémantique mappe un paramètre aux registres de nuanceur de vertex ou de pixels. Il peut également s’agir de chaînes descriptives facultatives jointes à des paramètres non enregistrés.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: D3DXSEMANTIC, structure (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631019"
---
# <a name="d3dxsemantic-structure"></a>D3DXSEMANTIC, structure

La sémantique mappe un paramètre aux registres de nuanceur de vertex ou de pixels. Il peut également s’agir de chaînes descriptives facultatives jointes à des paramètres non enregistrés.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Options qui identifient la façon dont les ressources sont utilisées. Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Options qui modifient la façon dont l’utilisation est interprétée. L’index utilisation et utilisation constituent une déclaration de vertex. Voir la [déclaration de vertex (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La sémantique est requise pour les registres d’entrée et de sortie de nuanceur de sommets et de pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
