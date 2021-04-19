---
description: La méthode Close attend que le thread se termine, puis libère ses ressources.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Méthode CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525592"
---
# <a name="camthreadclose-method"></a>CAMThread. Close, méthode

La `Close` méthode attend que le thread se termine, puis libère ses ressources.

## <a name="syntax"></a>Syntaxe


```C++
void Close();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, vous devez fournir un moyen de quitter le thread. Par exemple, dans votre méthode [**CAMThread :: ThreadProc**](camthread-threadproc.md) , définissez une demande qui signale au thread de s’arrêter. Appelez ensuite la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) avec cette valeur.

La méthode du destructeur [**~ CAMThread**](camthread--camthread.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




