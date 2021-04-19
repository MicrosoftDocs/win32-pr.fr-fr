---
description: Obtient le poids de fusion de priorité actuel utilisé par le contrôleur d’animation.
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: 'ID3DXAnimationController :: GetPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c27e4c6d2cc706b30f2be99030e7bb4a5bccf209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543567"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a>ID3DXAnimationController :: GetPriorityBlend, méthode

Obtient le poids de fusion de priorité actuel utilisé par le contrôleur d’animation.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Retourne le poids de fusion de priorité actuel.

## <a name="remarks"></a>Notes

Le poids de la fusion des priorités est utilisé pour fusionner les pistes haute et basse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
