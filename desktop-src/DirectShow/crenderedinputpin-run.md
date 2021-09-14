---
description: 'La méthode Run indique au code confidentiel que le filtre est en cours d’exécution. Cette méthode remplace la méthode CBasePin :: Run.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: CRenderedInputPin. Run, méthode (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094810"
---
# <a name="crenderedinputpinrun-method"></a>CRenderedInputPin. Run, méthode

La `Run` méthode notifie le code confidentiel que le filtre est en cours d’exécution. Cette méthode remplace la méthode [**CBasePin :: Run**](cbasepin-run.md) .

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

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amextra. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRenderedInputPin, classe**](crenderedinputpin.md)
</dt> </dl>

 

 




