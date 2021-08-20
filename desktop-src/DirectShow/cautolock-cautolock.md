---
description: Méthode de constructeur. Le constructeur verrouille l’objet de section critique spécifié.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Constructeur CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11267b444df319e339bcf13b30f200868a0f62d67712ed147513c2f8bc7d000c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017567"
---
# <a name="cautolockcautolock-constructor"></a>Constructeur CAutoLock. CAutoLock

Méthode de constructeur. Le constructeur verrouille l’objet de section critique spécifié.

## <a name="syntax"></a>Syntaxe


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plock* 
</dt> <dd>

Pointeur vers un objet [**CCritSec**](ccritsec.md) , qui contient un objet de section critique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAutoLock, classe**](cautolock.md)
</dt> </dl>

 

 




