---
description: La \_ méthode placer un diaporama automatique définit l’indicateur d’état d’affichage automatique.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Méthode CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017277"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>CBaseControlWindow. put, \_ méthode d’affichage automatique

La `put_AutoShow` méthode définit l’indicateur d’état d’affichage automatique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Affichage automatique* 
</dt> <dd>

Indicateur booléen Automation (0 est désactivé, 1 est activé).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette propriété simplifie l’accès à la fenêtre pour les applications. Si cette valeur est définie sur 1 (activé), la fenêtre, qui est généralement masquée après la connexion du filtre, s’affiche automatiquement lorsque le filtre s’interrompt ou s’exécute. Toutefois, la fenêtre ne doit pas être masquée quand le filtre s’arrête. Si la valeur est 0 (OFF), la fenêtre est visible uniquement quand l’application appelle [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_**](cbasecontrolwindow-put-windowstate.md) , avec les paramètres appropriés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




