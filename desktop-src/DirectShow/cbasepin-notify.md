---
description: 'CBasePin. Notify, méthode : la méthode Notify notifie au code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: CBasePin. Notify, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910439"
---
# <a name="cbasepinnotify-method"></a>CBasePin. Notify, méthode

La `Notify` méthode notifie le code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSelf* 
</dt> <dd>

Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre qui a fourni le message de contrôle qualité.

</dd> <dt>

*question* 
</dt> <dd>

Spécifie une structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La classe de base retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Les broches de sortie doivent remplacer cette méthode pour accepter des messages de contrôle qualité.

Si un gestionnaire de qualité externe a été installé (voir [**CBasePin :: SetSink**](cbasepin-setsink.md)), transmettez le message à ce gestionnaire de qualité. Dans le cas contraire, le filtre doit gérer le message lui-même ou passer le message en amont. Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




