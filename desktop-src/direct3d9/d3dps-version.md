---
description: Créez un jeton de version de nuanceur de pixels.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922619"
---
# <a name="d3dps_version-macro"></a>D3DPS la \_ macro de version

Créez un jeton de version de nuanceur de pixels.

## <a name="syntax"></a>Syntaxe


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*\_Majeure* 
</dt> <dd>

Version du nuanceur de pixels principal.

</dd> <dt>

*\_Secondaire* 
</dt> <dd>

Version mineure du nuanceur de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur DWORD qui est une version de nuanceur de pixels.

## <a name="remarks"></a>Notes

Numéros de versions

Le numéro de version est une combinaison de la version principale et des numéros de version de nuanceur de vertex secondaires. Les nombres valides sont indiqués dans le tableau.



| Majeure | Secondaire | Exemple             |
|-------|-------|---------------------|
| 1     | 1     | \_Version de D3DPS (1, 1) |
| 1     | 2     | \_Version de D3DPS (1, 2) |
| 1     | 3     | \_Version de D3DPS (1, 3) |
| 1     | 4     | \_Version de D3DPS (1,4) |
| 2     | 0     | \_Version de D3DPS (2, 0) |
| 3     | 0     | \_Version de D3DPS (3, 0) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




