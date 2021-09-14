---
description: Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet :: GetPeriodicPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921336"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>ID3DXAnimationSet :: GetPeriodicPosition, méthode

Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Position* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Heure locale de l’ensemble d’animations.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **double**](../winprog/windows-data-types.md)**

Position temporelle telle que mesurée dans le laps de temps de l’ensemble d’animations. Cette valeur est limitée par la période de l’ensemble d’animations.

## <a name="remarks"></a>Notes

La position d’heure retournée par cette méthode peut être utilisée en tant que paramètre PeriodicPosition de [**ID3DXAnimationSet :: GetSRT**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
