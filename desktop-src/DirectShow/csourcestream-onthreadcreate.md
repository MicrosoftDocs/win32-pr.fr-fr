---
description: La méthode OnThreadCreate est appelée lors de l’initialisation du thread de streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Méthode CSourceStream. OnThreadCreate (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296706"
---
# <a name="csourcestreamonthreadcreate-method"></a>Méthode CSourceStream. OnThreadCreate

La `OnThreadCreate` méthode est appelée lorsque le thread de streaming est initialisé.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La procédure de thread, [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md), appelle cette méthode lorsqu’elle reçoit pour la première fois une demande [**CSourceStream :: init**](csourcestream-init.md) . La méthode n’a aucun effet dans la classe de base. La classe dérivée peut substituer cette méthode pour effectuer des initialisations de thread. Si la classe dérivée retourne un code d’erreur, le thread se termine avec une erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




