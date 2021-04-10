---
description: Le type de compteur de performance désigne une formule requise pour obtenir des compteurs de performance calculés. Il s’agit des mêmes types de compteurs que ceux utilisés par l’analyse des performances Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Types de compteurs de performance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115031"
---
# <a name="wmi-performance-counter-types"></a>Types de compteurs de performance WMI

Le [type de compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de performance désigne une formule requise pour obtenir des compteurs de performance calculés. Il s’agit des mêmes types de compteurs que ceux utilisés par l' [analyse des performances](/windows/desktop/PerfCtrs/performance-counters-portal)Windows. Dans les classes de performance WMI, les données brutes pour la formule de type de compteur proviennent d’une classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et le résultat calculé est trouvé dans la même propriété de nom d’une classe [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondante.

Les types de compteurs s’affichent en tant **que qualificateur «** pas » pour les propriétés dans les classes [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et comme qualificateur **CookingType** pour les propriétés dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Par exemple, la propriété **AvgDiskBytesPerRead** de la [**classe \_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) est la source de données brute pour la propriété **AvgDiskBytesPerRead** dans la classe [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md), qui contient les mêmes données que celles affichées dans le moniteur système.

La liste suivante organise les descriptions de type de compteur par type fonctionnel :

-   [Types de compteurs de base](base-counter-types.md)
-   [Types de compteurs de l’algorithme de base](basic-algorithm-counter-types.md)
-   [Types de compteurs d’algorithmes de compteur](counter-algorithm-counter-types.md)
-   [Types de compteurs décalculés](noncomputational-counter-types.md)
-   [Types de compteurs de l’algorithme du minuteur de précision](precision-timer-algorithm-counter-types.md)
-   [Types de compteurs d’algorithmes de longueur de file d’attente](queue-length-algorithm-counter-types.md)
-   [Types de compteurs statistiques](statistical-counter-types.md)
-   [Types de compteurs de l’algorithme Timer](timer-algorithm-counter-types.md)

 

 
