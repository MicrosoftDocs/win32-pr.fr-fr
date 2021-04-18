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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540693"
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
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




