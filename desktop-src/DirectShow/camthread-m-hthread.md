---
description: Handle du thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membre CAMThread :: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094921"
---
# <a name="camthreadm_hthread-member"></a>CAMThread :: m \_ hThread, membre

Handle du thread.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Notes

Cette variable est initialisée avec la **valeur null**. La méthode [**CAMThread :: Create**](camthread-create.md) définit cette variable sur le handle de thread. Pour déterminer si le thread existe, appelez la méthode [**CAMThread :: ThreadExists**](camthread-threadexists.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




