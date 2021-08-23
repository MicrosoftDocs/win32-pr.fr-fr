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
ms.openlocfilehash: c372101aee2817e08545080048c98a25af7efb152f4873e54366e73571763065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652019"
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

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amextra. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRenderedInputPin, classe**](crenderedinputpin.md)
</dt> </dl>

 

 




