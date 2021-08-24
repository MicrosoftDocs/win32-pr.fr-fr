---
description: Le \_ type de données de temps de référence définit les unités pour les temps de référence dans DirectShow. Chaque unité de temps de référence est de 100 nanosecondes.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f1600e820ac59c53144743933701a61e4a7b753f814dde06c5c663a760938d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747319"
---
# <a name="reference_time"></a>temps de référence \_

Le type de données de **\_ temps de référence** définit les unités pour les temps de référence dans DirectShow. Chaque unité de temps de référence est de 100 nanosecondes.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Remarques

Le type de données de **\_ temps de référence** est un entier 64 bits.

Les temps de référence sont généralement mesurés à partir de l’une des lignes de base suivantes :

-   Heure de l’horloge absolue. Dans ce cas, la base de référence dépend de l’implémentation de l’horloge. Pour plus d’informations, consultez [horloges de référence](reference-clocks.md).
-   Par rapport au début de la lecture.

Pour plus d’informations sur les temps de référence, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Strmif. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Types de données](directshow-data-types.md)
</dt> </dl>

 

 




