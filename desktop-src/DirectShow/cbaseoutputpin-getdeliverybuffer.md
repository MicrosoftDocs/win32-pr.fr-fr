---
description: La méthode GetDeliveryBuffer récupère un exemple de média qui contient une mémoire tampon vide.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Méthode CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526840"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Méthode CBaseOutputPin. GetDeliveryBuffer

La `GetDeliveryBuffer` méthode récupère un exemple de média qui contient une mémoire tampon vide.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSample* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de la mémoire tampon.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Pointeur désignant l’heure de début de l’exemple, ou **null**.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers l’heure de fin de l’exemple, ou **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinaison d’opérations de bits des indicateurs pris en charge par l’interface [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                   | Description                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Aucun allocateur disponible.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode **IMemAllocator :: GetBuffer** sur l’allocateur et passe les paramètres à cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




