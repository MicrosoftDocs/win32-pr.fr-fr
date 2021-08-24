---
description: La méthode CheckRequest vérifie s’il existe une demande de thread, sans blocage.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Méthode CSourceStream. CheckRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bb77358ec579415439c2832b00255e7ffeb3c7eba0e387bfa0522a4a5109669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073313"
---
# <a name="csourcestreamcheckrequest-method"></a>Méthode CSourceStream. CheckRequest

La `CheckRequest` méthode vérifie s’il existe une demande de thread, sans blocage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCom* 
</dt> <dd>

Pointeur vers une variable qui reçoit la valeur passée dans le dernier appel à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** s’il y a une demande en attente, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CAMThread :: CheckRequest**](camthread-checkrequest.md) pour effectuer la vérification de type. La classe **CSourceStream** définit le type énuméré suivant pour le paramètre *pCom* :


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

 

 




