---
description: La méthode reset réinitialise l’objet afin qu’il puisse recevoir plus de données.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: COutputQueue. Reset, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4129730ae3ce2f3a95db41d8bc65025c3195056cbd4a1afddbfeb83d9bb33ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073653"
---
# <a name="coutputqueuereset-method"></a>COutputQueue. Reset, méthode

La `Reset` méthode réinitialise l’objet afin qu’il puisse recevoir plus de données.

## <a name="syntax"></a>Syntaxe


```C++
void Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode réinitialise la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ OK. L’objet peut recevoir à nouveau des exemples de supports. par exemple, après une opération de vidage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




