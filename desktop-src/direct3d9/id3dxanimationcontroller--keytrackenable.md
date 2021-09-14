---
description: Définit une clé d’événement qui active ou désactive une piste d’animation.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController :: KeyTrackEnable, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916544"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>ID3DXAnimationController :: KeyTrackEnable, méthode

Définit une clé d’événement qui active ou désactive une piste d’animation.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste d’animation à modifier.

</dd> <dt>

*NewEnable* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Activer l’indicateur. Affectez la valeur **true** pour activer la piste d’animation, ou la **valeur false** pour désactiver la piste.

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Clé de temps globale. Spécifie l’heure globale à laquelle la modification doit avoir lieu.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Descripteur d’événement pour l’événement Priority Blend. La **valeur null** est retournée si Track n’est pas valide.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
