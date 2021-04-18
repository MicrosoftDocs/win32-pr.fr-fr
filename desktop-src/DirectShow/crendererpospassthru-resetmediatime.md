---
description: La méthode ResetMediaTime réinitialise les horodatages mis en cache à zéro.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Méthode CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540421"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Méthode CRendererPosPassThru. ResetMediaTime

La `ResetMediaTime` méthode réinitialise les horodatages mis en cache à zéro.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Le filtre doit appeler cette méthode chaque fois que les horodatages mis en cache par la méthode [**CRendererPosPassThru :: RegisterMediaTime**](crendererpospassthru-registermediatime.md) deviennent non valides. En particulier, il doit appeler cette méthode en réponse aux méthodes [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) et [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

Une fois cette méthode appelée, la méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) retourne zéro pour les heures de début et de fin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




