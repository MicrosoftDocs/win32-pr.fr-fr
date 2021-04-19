---
description: La méthode GetDueHandle récupère le descripteur d’événement à signaler.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Méthode CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545341"
---
# <a name="ccmdqueuegetduehandle-method"></a>Méthode CCmdQueue. GetDueHandle

La `GetDueHandle` méthode récupère le handle d’événement à signaler.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le handle d’événement.

## <a name="remarks"></a>Notes

Retourne le descripteur d’événement chaque fois que des commandes différées sont dues pour l’exécution (quand [**CCmdQueue :: GetDueCommand**](ccmdqueue-getduecommand.md) n’est pas bloqué).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




