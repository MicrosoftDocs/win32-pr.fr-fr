---
description: Créez un jeton de numéro de version de nuanceur de vertex.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537264"
---
# <a name="d3dvs_version-macro"></a>D3DVS la \_ macro de version

Créez un jeton de numéro de version de nuanceur de vertex.

## <a name="syntax"></a>Syntaxe


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*\_Majeure* 
</dt> <dd>

Version principale du nuanceur de vertex. Consultez la section Notes pour connaître les valeurs appropriées.

</dd> <dt>

*\_Secondaire* 
</dt> <dd>

Version mineure du nuanceur de sommets. Consultez la section Notes pour connaître les valeurs appropriées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur DWORD qui est une version du nuanceur de sommets.

## <a name="remarks"></a>Notes

Numéros de versions

Le numéro de version est une combinaison de la version principale et des numéros de version de nuanceur de vertex secondaires. Les nombres valides sont indiqués dans le tableau.



| Majeure | Secondaire | Exemple             |
|-------|-------|---------------------|
| 1     | 1     | \_Version de D3DVS (1, 1) |
| 2     | 0     | \_Version de D3DVS (2, 0) |
| 3     | 0     | \_Version de D3DVS (3, 0) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




