---
description: La méthode CheckTime détermine si une heure spécifiée est due.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Méthode CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910429"
---
# <a name="ccmdqueuechecktime-method"></a>Méthode CCmdQueue. CheckTime

La `CheckTime` méthode détermine si une heure spécifiée est due.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*time* 
</dt> <dd>

Durée à vérifier.

</dd> <dt>

*bStream* 
</dt> <dd>

**True** si le paramètre de *temps* est une valeur de flux de temps ; **False** si *Time* est une valeur au moment de la présentation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’heure spécifiée n’est pas encore passée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




