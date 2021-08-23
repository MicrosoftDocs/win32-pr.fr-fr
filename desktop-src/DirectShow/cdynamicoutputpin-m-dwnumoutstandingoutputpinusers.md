---
description: Nombre de threads de streaming utilisant ce code PIN.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Membre CDynamicOutputPin :: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688709"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>CDynamicOutputPin :: m \_ dwNumOutstandingOutputPinUsers, membre

Nombre de threads de streaming utilisant ce code PIN.

## <a name="syntax"></a>Syntaxe


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Notes

La méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrémente cette variable, et la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) la décrémente. Lorsque la valeur est supérieure à zéro, un thread utilise ce code PIN pour diffuser des données en continu ou pour modifier le type de connexion. Le code PIN ne peut pas être bloqué tant que c’est le cas.

Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




