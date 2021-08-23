---
description: Obtient l’heure globale de l’animation.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController :: GetTime, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987829"
---
# <a name="id3dxanimationcontrollergettime-method"></a>ID3DXAnimationController :: GetTime, méthode

Obtient l’heure globale de l’animation.

## <a name="syntax"></a>Syntaxe


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **double**](../winprog/windows-data-types.md)**

Retourne l’heure globale de l’animation.

## <a name="remarks"></a>Remarques

Les animations sont conçues à l’aide d’une heure d’animation locale et sont mélangées dans l’heure globale avec [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
