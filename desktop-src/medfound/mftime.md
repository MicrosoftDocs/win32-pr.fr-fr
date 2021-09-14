---
description: Définit les unités de nanosecondes de 100.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: MFTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313713"
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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données Media Foundation](media-foundation-datatypes.md)
</dt> </dl>

 

 




