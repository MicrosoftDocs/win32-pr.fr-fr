---
description: La méthode IsAutoShowEnabled récupère des informations indiquant si la fenêtre vidéo s’affiche automatiquement lorsque le filtre de rendu s’interrompt ou s’exécute.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Méthode CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660228"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Méthode CBaseControlWindow. IsAutoShowEnabled

La `IsAutoShowEnabled` méthode récupère des informations indiquant si la fenêtre vidéo s’affiche automatiquement lorsque le filtre de rendu s’interrompt ou s’exécute.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le membre **m \_ bAutoShow** a la valeur 1 ou **false** s’il a la valeur 0.

## <a name="remarks"></a>Remarques

Si le membre **m \_ bAutoShow** a la valeur 1 dans une fenêtre vidéo masquée, la fenêtre devient visible lorsque le filtre s’interrompt ou s’exécute. Si ce membre a la valeur 0, la fenêtre s’affiche uniquement si vous utilisez la fonction membre [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) avec les paramètres appropriés.

Cette fonction membre récupère le paramètre de membre **m \_ bAutoShow** et produit le même résultat que l’utilisation de la méthode [**IVideoWindow :: obtenir \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




