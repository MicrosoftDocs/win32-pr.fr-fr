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
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012234"
---
# <a name="csourcestreamgetrequest-method"></a>Méthode CSourceStream. GetRequest

La `GetRequest` méthode attend la demande de thread suivante.

## <a name="syntax"></a>Syntaxe


```C++
Command GetRequest();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la requête de thread suivante.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) . La valeur de retour est convertie vers le type énuméré suivant :


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




