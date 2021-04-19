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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539952"
---
# <a name="csourcestreamonthreadcreate-method"></a>Méthode CSourceStream. OnThreadCreate

La `OnThreadCreate` méthode est appelée lorsque le thread de streaming est initialisé.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La procédure de thread, [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md), appelle cette méthode lorsqu’elle reçoit pour la première fois une demande [**CSourceStream :: init**](csourcestream-init.md) . La méthode n’a aucun effet dans la classe de base. La classe dérivée peut substituer cette méthode pour effectuer des initialisations de thread. Si la classe dérivée retourne un code d’erreur, le thread se termine avec une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




