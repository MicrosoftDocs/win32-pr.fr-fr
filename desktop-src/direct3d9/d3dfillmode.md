---
description: Définit des constantes décrivant le mode de remplissage.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Énumération D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531584"
---
# <a name="d3dfillmode-enumeration"></a>Énumération D3DFILLMODE

Définit des constantes décrivant le mode de remplissage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**\_Point D3DFILL**
</dt> <dd>

Points de remplissage.

</dd> <dt>

<span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ filaire**
</dt> <dd>

Remplissez des maquettes.

</dd> <dt>

<span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ Solid**
</dt> <dd>

Remplir des solides.

</dd> <dt>

<span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS FillMode.

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

 

 
