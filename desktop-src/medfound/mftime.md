---
description: Définit les unités de nanosecondes de 100.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: MFTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a08ac4e82c5cb97615b47430baa1c3388677ac160487c132dd41b7454ce985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240207"
---
# <a name="mftime"></a>MFTIME

Définit les unités de nanosecondes de 100.


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a>Exemples


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données Media Foundation](media-foundation-datatypes.md)
</dt> </dl>

 

 




