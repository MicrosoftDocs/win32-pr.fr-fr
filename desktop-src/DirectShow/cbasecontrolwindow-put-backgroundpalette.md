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
ms.openlocfilehash: 295889510b96a085865eeff45ba976278519670adbd596b24e6aea829a29df4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966718"
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

## <a name="remarks"></a>Remarques

Pour lire une vidéo dans une autre application ou un autre document, l’application peut utiliser sa propre palette. Il peut demander à la vidéo d’utiliser la palette de premier plan actuelle plutôt que sa propre palette en affectant la valeur 1 à cet indicateur. Si cette valeur est définie sur 0, la fenêtre installe et réalise sa propre palette par défaut. Si vous demandez à la fenêtre d’utiliser une palette différente, vous risquez de nuire aux performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




