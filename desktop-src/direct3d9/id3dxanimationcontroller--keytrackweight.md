---
description: Définit une clé d’événement qui modifie le poids d’une piste d’animation. Le poids est utilisé comme multiplicateur lors de la combinaison de plusieurs pistes.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController :: KeyTrackWeight, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916536"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>ID3DXAnimationController :: KeyTrackWeight, méthode

Définit une clé d’événement qui modifie le poids d’une piste d’animation. Le poids est utilisé comme multiplicateur lors de la combinaison de plusieurs pistes.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste à modifier.

</dd> <dt>

*NewWeight* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Nouveau poids de la piste.

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Clé de temps globale. Spécifie l’heure globale à laquelle la modification doit avoir lieu.

</dd> <dt>

*Durée* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Durée de transition, qui spécifie le délai d’exécution de la transition lisse.

</dd> <dt>

*Transition* \[ dans\]
</dt> <dd>

Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

Spécifie le type de transition utilisé pour la transition entre les poids. Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Descripteur d’événement pour l’événement Priority Blend. La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.

## <a name="remarks"></a>Notes

Le poids est utilisé comme un multiplicateur pour déterminer la proportion de cette piste à mélanger avec d’autres pistes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
