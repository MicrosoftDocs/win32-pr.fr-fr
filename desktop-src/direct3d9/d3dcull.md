---
description: Définit les modes d’élimination pris en charge.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Énumération D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 062135f1eff43bd568f1b08674985b4744e0835ebf3fa9e78c2756a798f85ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989059"
---
# <a name="d3dcull-enumeration"></a>Énumération D3DCULL

Définit les modes d’élimination pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ aucun**
</dt> <dd>

Ne pas effectuer de réforme des visages.

</dd> <dt>

<span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL en \_ PV**
</dt> <dd>

Élimination des faces arrières avec les sommets dans le sens des aiguilles

</dd> <dt>

<span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**\_CCW D3DCULL**
</dt> <dd>

Élimination des faces arrières avec sommets à gauche.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS CULLMODE. Les modes d’élimination définissent la manière dont les faces arrière sont éliminées lors du rendu d’une géométrie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
