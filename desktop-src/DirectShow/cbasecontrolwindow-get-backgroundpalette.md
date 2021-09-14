---
description: La \_ méthode obtenir BackgroundPalette récupère la palette réalisée dans l’indicateur d’arrière-plan.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Méthode CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923964"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Méthode CBaseControlWindow. obten \_ BackgroundPalette

La `get_BackgroundPalette` méthode récupère la palette réalisée dans l’indicateur d’arrière-plan.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IVideoWindow :: obten \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Si une vidéo est lue dans une autre application ou un autre document, l’application peut utiliser sa propre palette. Elle peut demander à ce que la vidéo utilise la palette de premier plan actuelle plutôt que sa propre, en affectant la valeur 1 à cet indicateur. Si cette valeur est définie sur 0, la fenêtre installe et réalise sa propre palette par défaut. Notez que le fait de demander à la fenêtre d’utiliser une palette différente entraîne des pénalités de performances graves.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




