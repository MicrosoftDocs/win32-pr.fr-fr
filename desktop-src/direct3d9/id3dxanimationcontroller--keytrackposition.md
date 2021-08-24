---
description: Définit une clé d’événement qui modifie l’heure locale d’une piste d’animation.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController :: KeyTrackPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e66bac7b5aaa8da87b0cb88e3bfd12469d8aa8b6ec755eaa47268c70da5eadf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791229"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>ID3DXAnimationController :: KeyTrackPosition, méthode

Définit une clé d’événement qui modifie l’heure locale d’une piste d’animation.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste à modifier.

</dd> <dt>

*NewPosition* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Nouvelle heure locale de la piste d’animation.

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Clé de temps globale. Spécifie l’heure globale à laquelle la modification doit avoir lieu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Descripteur d’événement pour l’événement Priority Blend. La **valeur null** est retournée si Track n’est pas valide ou si aucun événement libre n’est disponible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
