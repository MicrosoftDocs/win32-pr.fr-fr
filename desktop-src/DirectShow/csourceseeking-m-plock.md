---
description: Pointeur vers un objet de section critique.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membre CSourceSeeking :: m_pLock (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537101"
---
# <a name="csourceseekingm_plock-member"></a>CSourceSeeking :: m \_ pLock, membre

Pointeur vers un objet de section critique. La `CSourceSeeking` classe utilise cette section critique pour synchroniser l’accès aux variables d’heure de début et de fin, de durée et de taux. Cette variable est initialisée dans la méthode du constructeur ; consultez [**CSourceSeeking :: CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Syntaxe


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




