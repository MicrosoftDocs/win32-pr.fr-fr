---
description: 'CBaseInputPin. Notify, méthode : la méthode Notify notifie au code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: CBaseInputPin. Notify, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2067c7698c1af7d7295cffed552ab4f58d0402594dd13bfd82224c81652b9aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659162"
---
# <a name="cbaseinputpinnotify-method"></a>CBaseInputPin. Notify, méthode

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

Pointeur vers le filtre qui envoie le message de contrôle qualité.

</dd> <dt>

*question* 
</dt> <dd>

Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

En règle générale, les filtres passent des messages de contrôle qualité à une broche de sortie en amont, et non à une broche d’entrée. Par conséquent, cette méthode retourne S \_ OK sans rien faire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> <dt>

[Gestion du contrôle de la qualité](quality-control-management.md)
</dt> </dl>

 

 




