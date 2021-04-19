---
description: Décrit l’état de la trame.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Structure D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527735"
---
# <a name="d3draster_status-structure"></a>\_Structure d’État D3DRASTER

Décrit l’état de la trame.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**InVBlank**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** si le raster est dans la période vide verticale. **False** si le raster n’est pas dans la période vide verticale.

</dd> <dt>

**Numérisation**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Si InVBlank a la valeur **false**, cette valeur est un entier qui correspond approximativement à la ligne de numérisation actuelle peinte par le raster. Les lignes de numérisation sont numérotées de la même façon que les coordonnées de la surface Direct3D : 0 est le haut de la surface primaire, qui s’étend jusqu’à la valeur (hauteur de la surface-1) en bas de l’affichage.

Si InVBlank a la valeur **true**, cette valeur est définie à zéro et peut être ignorée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
