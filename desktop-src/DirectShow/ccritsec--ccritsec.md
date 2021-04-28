---
description: CCritSec. ~ CCritSec, destructeur, méthode de destructeur.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095807"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec. ~ CCritSec, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CCritSec();
```



## <a name="remarks"></a>Notes 

Cette méthode appelle la fonction [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) pour supprimer la section critique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

