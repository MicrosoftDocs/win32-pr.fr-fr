---
description: Le \_ type de données de temps de référence définit les unités pour les temps de référence dans DirectShow. Chaque unité de temps de référence est de 100 nanosecondes.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239069"
---
# <a name="reference_time"></a>temps de référence \_

Le type de données de **\_ temps de référence** définit les unités pour les temps de référence dans DirectShow. Chaque unité de temps de référence est de 100 nanosecondes.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Notes

Le type de données de **\_ temps de référence** est un entier 64 bits.

Les temps de référence sont généralement mesurés à partir de l’une des lignes de base suivantes :

-   Heure de l’horloge absolue. Dans ce cas, la base de référence dépend de l’implémentation de l’horloge. Pour plus d’informations, consultez [horloges de référence](reference-clocks.md).
-   Par rapport au début de la lecture.

Pour plus d’informations sur les temps de référence, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Strmif. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Types de données](directshow-data-types.md)
</dt> </dl>

 

 




