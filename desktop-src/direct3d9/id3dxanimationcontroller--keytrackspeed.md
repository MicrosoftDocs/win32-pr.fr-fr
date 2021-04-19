---
description: Définit une clé d’événement qui modifie le taux de lecture d’une piste d’animation.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController :: KeyTrackSpeed, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543572"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>ID3DXAnimationController :: KeyTrackSpeed, méthode

Définit une clé d’événement qui modifie le taux de lecture d’une piste d’animation.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*NewSpeed* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Nouvelle vitesse de la piste d’animation.

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

Spécifie le type de transition utilisé pour la transition entre les vitesses. Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Descripteur d’événement pour l’événement Priority Blend. La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
