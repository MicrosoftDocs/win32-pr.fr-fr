---
description: La méthode Receive fournit un exemple de support à la broche d’entrée.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: COutputQueue. Receive, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8fb896429e53c16b30dbc4301f2e54fca5a2087dc1c89635fa33395f68ba0f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871499"
---
# <a name="coutputqueuereceive-method"></a>COutputQueue. Receive, méthode

La `Receive` méthode remet un échantillon de média à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Receive(
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



| Code de retour                                                                             | Description                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Notification de fin de flux reçue avant le traitement de cet exemple.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                                           |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**COutputQueue :: ReceiveMultiple**](coutputqueue-receivemultiple.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




