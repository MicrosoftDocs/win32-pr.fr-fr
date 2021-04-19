---
description: La méthode deliver fournit un exemple de support à la broche d’entrée connectée.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: CBaseOutputPin. Deliver, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521707"
---
# <a name="cbaseoutputpindeliver-method"></a>CBaseOutputPin. Deliver, méthode

La `Deliver` méthode remet un échantillon de média à la broche d’entrée connectée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Opération réussie.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée. **Receive** peut être bloqué si la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) retourne S \_ OK.

Libérez l’exemple après avoir appelé cette méthode. La broche d’entrée peut contenir un décompte de références sur l’échantillon, donc ne pas réutiliser l’exemple. Appelez toujours la méthode [**CBaseOutputPin :: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) pour obtenir un nouvel exemple.

Maintenez la section critique du filtre avant d’appeler cette méthode. Dans le cas contraire, le code pin peut être déconnecté pendant l’appel de la méthode. Si le filtre utilise un thread de travail pour fournir des exemples, conservez la section critique lorsque le filtre est prêt à remettre un échantillon. Dans le cas contraire, vous pouvez conserver la section critique dans la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) du filtre, où le filtre traite les exemples.

Les threads de travail peuvent créer un interblocage potentiel. Lorsque le thread contient la section critique, il peut attendre une modification d’État dans le filtre. En même temps, il est possible que le changement d’État attende que le thread se termine. Pour éviter cela, le code de modification d’État doit signaler un événement qui termine le thread, puis attendre que le thread signale la fin de l’opération.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




