---
description: Type de données pour la gestion d’un ensemble de paramètres d’effet par défaut.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: D3DXEFFECTINSTANCE, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a4384866ed5a2bfc433caeca1ccd13c4b0f33de1ae43844391625e11211e618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096162"
---
# <a name="d3dxeffectinstance-structure"></a>D3DXEFFECTINSTANCE, structure

Type de données pour la gestion d’un ensemble de paramètres d’effet par défaut.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Membres

<dl> <dt>

**pEffectFilename**
</dt> <dd>

Type : **LPSTR**

</dd> <dd>

Nom du fichier d’effet.

</dd> <dt>

**NumDefaults**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de paramètres par défaut.

</dd> <dt>

**pDefaults**
</dt> <dd>

Type : **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

Pointeur vers un tableau d’éléments [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , chacun d’eux contenant un paramètre Effect.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
