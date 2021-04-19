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
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528514"
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
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAutoLock, classe**](cautolock.md)
</dt> </dl>

 

 




