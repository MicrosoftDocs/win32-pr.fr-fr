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
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322930"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
