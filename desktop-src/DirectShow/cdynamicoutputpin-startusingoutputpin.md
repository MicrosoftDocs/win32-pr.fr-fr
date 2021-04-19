---
description: La méthode StartUsingOutputPin obtient l’accès au code confidentiel pour une opération de diffusion en continu.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Méthode CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541720"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>Méthode CDynamicOutputPin. StartUsingOutputPin

La `StartUsingOutputPin` méthode obtient l’accès au code confidentiel pour une opération de diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Opération réussie.<br/>                                               |
| <dl> <dt>**E \_ inattendu**</dt> </dl>          | Erreur inattendue.<br/>                                      |
| <dl> <dt>**\_État VFW \_ E \_ modifié**</dt> </dl> | Le filtre a été arrêté ou le code pin a commencé à être vidé.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode avant d’appeler des méthodes qui fournissent des données à la broche d’entrée connectée ou qui modifient le type de média de la connexion. Par exemple, cette règle s’applique aux méthodes suivantes :

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin ::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin ::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin ::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Ensuite, appelez la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) pour libérer l’accès au code PIN.

Si le code PIN est bloqué, `StartUsingOutputPin` attend le déblocage du code PIN. Si le filtre s’arrête pendant que la méthode attend, la méthode retourne immédiatement \_ l' \_ État VFW E \_ modifié. Le code PIN gère le nombre de fois que `StartUsingOutputPin` a été appelé sans appel correspondant à **StopUsingOutputPin**. Si un autre thread tente de bloquer le pin alors que ce nombre est différent de zéro, le code PIN définit son état de blocage sur « en attente ». Le code PIN est bloqué une fois que toutes les opérations de streaming sont terminées, dans le dernier appel à **StopUsingOutputPin**.

Ne conservez pas la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) lorsque vous appelez cette méthode. Dans le cas contraire, si le code PIN est bloqué, il ne peut jamais être débloqué, provoquant ainsi un blocage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




