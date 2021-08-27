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
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057599"
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

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Introuvable<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Succès<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (inclure Flux. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




