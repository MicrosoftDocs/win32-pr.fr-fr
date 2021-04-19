---
description: La \_ méthode obtenir un affichage automatique récupère l’indicateur d’état d’affichage automatique actuel.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Méthode CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525380"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow. obtient la \_ méthode d’affichage automatique

La `get_AutoShow` méthode récupère l’indicateur d’état d’affichage automatique actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Affichage automatique* 
</dt> <dd>

Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode d' [**\_ affichage automatique IVideoWindow :: obtient**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) . Cette propriété simplifie l’accès à la fenêtre pour les applications. Si cette valeur est définie sur 1 (activé), la fenêtre, qui est généralement masquée après la connexion du filtre, s’affiche automatiquement lorsque le filtre s’interrompt ou s’exécute. Toutefois, la fenêtre ne doit pas être masquée quand le filtre s’arrête. Si ce paramètre a la valeur 0 (OFF), la fenêtre est rendue visible uniquement lorsque l’application appelle [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_**](cbasecontrolwindow-put-windowstate.md) , avec les paramètres appropriés.

Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé. Appelez la fonction membre [**CBaseControlWindow :: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




