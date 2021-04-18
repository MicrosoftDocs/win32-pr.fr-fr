---
description: La \_ méthode put BackgroundPalette définit un indicateur pour réaliser la palette en arrière-plan.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Méthode CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533079"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>CBaseControlWindow. put \_ BackgroundPalette, méthode

La `put_BackgroundPalette` méthode définit un indicateur pour réaliser la palette en arrière-plan.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

Indicateur booléen Automation (0 est désactivé, 1 est activé).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Pour lire une vidéo dans une autre application ou un autre document, l’application peut utiliser sa propre palette. Il peut demander à la vidéo d’utiliser la palette de premier plan actuelle plutôt que sa propre palette en affectant la valeur 1 à cet indicateur. Si cette valeur est définie sur 0, la fenêtre installe et réalise sa propre palette par défaut. Si vous demandez à la fenêtre d’utiliser une palette différente, vous risquez de nuire aux performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




