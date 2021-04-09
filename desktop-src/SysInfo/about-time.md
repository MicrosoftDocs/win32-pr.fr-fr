---
description: Les fonctions relatives à l’heure retournent du temps dans l’un des nombreux formats. Vous pouvez utiliser les fonctions d’heure pour effectuer une conversion entre des formats d’heure pour faciliter la comparaison et l’affichage. Le tableau suivant récapitule les formats d’heure.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: À propos du temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034630"
---
# <a name="about-time"></a>À propos du temps

Les fonctions relatives à l’heure retournent du temps dans l’un des nombreux formats. Vous pouvez utiliser les fonctions d’heure pour effectuer une conversion entre des formats d’heure pour faciliter la comparaison et l’affichage. Le tableau suivant récapitule les formats d’heure.



| Format          | Type                                                                     | Description                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Système          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Année, mois, jour, heure, seconde et milliseconde, pris de l’horloge matérielle interne.                                            |
| Local           | [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) ou [ **fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Heure système ou heure du fichier convertie dans le fuseau horaire local du système.                                                               |
| Fichier            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Mot condensé pour la date, un autre pour le moment.                                                                                   |
| Windows         | **DWORD** ou **ULONGLONG**                                               | Nombre de millisecondes écoulées depuis le dernier démarrage du système. En cas de récupération en tant que valeur DWORD, cycles de temps Windows tous les 49,7 jours. |
| Nombre d’interruptions | **ULONGLONG**                                                            | Nombre d’intervalles de 100 nanosecondes depuis le dernier démarrage du système.                                                           |



 

Pour plus d'informations, voir les rubriques suivantes :

-   [Temps système](system-time.md)
-   [Heure locale](local-time.md)
-   [Heures du fichier](file-times.md)
-   [Date et heure MS-DOS](ms-dos-date-and-time.md)
-   [Horloge Windows](windows-time.md)
-   [Temps d’interruption](interrupt-time.md)

 

 
