---
description: Méthode constructeur CCritSec. CCritSec.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Constructeur CCritSec. CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fce4cb5edb9765e7f69726188e5ed0ba2017df7d6fa90cae0bfa059b89fc939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688989"
---
# <a name="ccritsecccritsec-constructor"></a>Constructeur CCritSec. CCritSec

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec();
```



## <a name="parameters"></a>Paramètres

Ce constructeur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Cette méthode appelle la fonction [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) pour initialiser la section critique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

