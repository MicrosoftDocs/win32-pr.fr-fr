---
description: La \_ méthode put MessageDrain définit la fenêtre de façon à recevoir les messages de fenêtre envoyés au convertisseur vidéo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Méthode CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b58ac59d83023530ca6da51efc2f84ba42c4bef9ac0d3f25ad9a234a320291f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017257"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow. put \_ MessageDrain, méthode

La `put_MessageDrain` méthode définit la fenêtre pour recevoir les messages de fenêtre envoyés au convertisseur vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Vidage* 
</dt> <dd>

Fenêtre dans laquelle les messages doivent être publiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Les messages envoyés au filtre de convertisseur vidéo peuvent être publiés dans une autre fenêtre. Cette fonction membre inscrit la fenêtre pour recevoir ces messages. Contrairement à la fonction membre [**CBaseControlWindow ::p ut \_ owner**](cbasecontrolwindow-put-owner.md) , cette fonction membre ne rend pas la fenêtre vidéo enfant d’une autre fenêtre. Elle est particulièrement utile pour les convertisseurs vidéo en plein écran, qui ne peuvent pas être des fenêtres enfants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




