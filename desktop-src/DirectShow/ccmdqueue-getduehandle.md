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
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016417"
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

## <a name="remarks"></a>Remarques

Retourne le descripteur d’événement chaque fois que des commandes différées sont dues pour l’exécution (quand [**CCmdQueue :: GetDueCommand**](ccmdqueue-getduecommand.md) n’est pas bloqué).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




