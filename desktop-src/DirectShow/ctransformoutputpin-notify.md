---
description: 'CTransformOutputPin. Notify, méthode : la méthode Notify notifie au code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: CTransformOutputPin. Notify, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538139"
---
# <a name="ctransformoutputpinnotify-method"></a>CTransformOutputPin. Notify, méthode

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

Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre qui a fourni le message de contrôle de qualité.

</dd> <dt>

*question* 
</dt> <dd>

Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                       | Description                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un objet pour accepter le message.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**CTransformFilter :: AlterQuality**](ctransformfilter-alterquality.md) du filtre. Si le filtre ne gère pas le message de qualité, cette méthode appelle la méthode [**CBaseInputPin ::P assnotify**](cbaseinputpin-passnotify.md) sur la broche d’entrée du filtre. La méthode **PassNotify** transmet le message de qualité en amont (ou à un gestionnaire de qualité personnalisé, le cas échéant).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




