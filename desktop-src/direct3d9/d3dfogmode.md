---
description: Définit des constantes qui décrivent le mode de brouillard.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Énumération D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b94992d94779932301c271ca46dc7466344b40b68c62855d4c57bfe8b780a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791969"
---
# <a name="d3dfogmode-enumeration"></a>Énumération D3DFOGMODE

Définit des constantes qui décrivent le mode de brouillard.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ aucun**
</dt> <dd>

Aucun effet de brouillard.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**
</dt> <dd>

L’effet de brouillard augmente de façon exponentielle, en fonction de la formule suivante.

![formule d’intensité de l’effet de brouillard](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

L’effet de brouillard augmente de façon exponentielle avec le carré de la distance, en fonction de la formule suivante.

![formule d’intensité d’effet de brouillard basée sur le carré de distance](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linéaire**
</dt> <dd>

L’effet de brouillard s’intensifie de manière linéaire entre les points de départ et de fin, en fonction de la formule suivante.

![formule d’intensité d’effet de brouillard basée sur les points de départ et de fin](images/fogliner.png)

Il s’agit du seul mode de brouillard actuellement pris en charge.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs de ce type énuméré sont utilisées par les États de \_ rendu D3DRS FOGTABLEMODE et D3DRS \_ FOGVERTEXMODE.

Le brouillard peut être considéré comme une mesure de visibilité : plus la valeur de brouillard produite par une équation de brouillard est faible, moins un objet est visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
