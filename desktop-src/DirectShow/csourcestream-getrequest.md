---
description: La méthode GetRequest attend la demande de thread suivante.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Méthode CSourceStream. GetRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e28a8e57535a49903cd2a7b23fb0d0d179bf910b20225042c65b3bdcda620f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073203"
---
# <a name="csourcestreamgetrequest-method"></a>Méthode CSourceStream. GetRequest

La `GetRequest` méthode attend la demande de thread suivante.

## <a name="syntax"></a>Syntaxe


```C++
Command GetRequest();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la requête de thread suivante.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) . La valeur de retour est convertie vers le type énuméré suivant :


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




