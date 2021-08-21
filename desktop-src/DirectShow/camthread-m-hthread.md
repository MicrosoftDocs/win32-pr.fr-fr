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
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158910"
---
# <a name="camthreadm_hthread-member"></a>CAMThread :: m \_ hThread, membre

Handle du thread.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Notes

Cette variable est initialisée avec la **valeur null**. La méthode [**CAMThread :: Create**](camthread-create.md) définit cette variable sur le handle de thread. Pour déterminer si le thread existe, appelez la méthode [**CAMThread :: ThreadExists**](camthread-threadexists.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




