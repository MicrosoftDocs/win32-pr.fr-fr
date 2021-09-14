---
description: La méthode Unadvise supprime une demande de notification.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: CAMSchedule. Unadvise, méthode (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094970"
---
# <a name="camscheduleunadvise-method"></a>CAMSchedule. Unadvise, méthode

La `Unadvise` méthode supprime une demande de notification.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificateur de la demande de notification, retourné par la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Introuvable<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Succès<br/>   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (inclure Flux. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




