---
description: Mappe les index de la plage 0 à 255 aux États de transformation correspondants.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530874"
---
# <a name="d3dts_worldmatrix-macro"></a>D3DTS \_ macro WORLDMATRIX

Mappe les index de la plage 0 à 255 aux États de transformation correspondants.

## <a name="syntax"></a>Syntaxe


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* 
</dt> <dd>

Valeur d’index comprise entre 0 et 255.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) mappé à l' *index* donné.

## <a name="remarks"></a>Notes

Les États de transformation de la plage 256 à 511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’index 8 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
