---
description: La méthode Run indique au code confidentiel que le filtre est en cours d’exécution.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: CBasePin. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528525"
---
# <a name="cbasepinrun-method"></a>CBasePin. Run, méthode

La `Run` méthode notifie le code confidentiel que le filtre est en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Heure de début passée à la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) du filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Lorsque le filtre passe de en pause à en cours d’exécution, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur tous les codes confidentiels du filtre.

Cette méthode n’a aucun effet dans la classe de base. Les classes dérivées peuvent substituer cette méthode. Par exemple, un code confidentiel peut démarrer un thread de travail qui remet des exemples.

L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




