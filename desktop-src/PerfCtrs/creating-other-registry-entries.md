---
description: La fonction OpenPerformanceData des dll de performances accepte un argument de chaîne comme entrée.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Création d’autres entrées de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952015"
---
# <a name="creating-other-registry-entries"></a>Création d’autres entrées de Registre

La fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) de la dll de performance accepte un argument de chaîne comme entrée. Pour fournir une chaîne d’entrée à votre fonction ouverte, ajoutez une clé de **liaison** sous la clé de vos **services** . La clé de **liaison** contient une valeur d' **exportation** . Définissez les données de valeur pour **Export** sur la chaîne d’entrée que vous souhaitez transmettre à votre fonction Open. Le type de données de l' **exportation** est **reg \_ multi \_ SZ**.

Si l' **exportation** n’est pas définie (l'**exportation** est facultative), le système passe la **valeur null** à votre fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .

En règle générale, si plusieurs applications partagent la même DLL de performance, chaque application comprend une clé de **liaison** et une valeur d' **exportation** pour fournir le contexte de l’application qui appelle la dll.

L’exemple suivant montre les entrées de Registre :

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

Par défaut, les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) et [**COLLECTPERFORMANCEDATA**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) de la dll de performance doivent retourner dans un délai de 10 000 millisecondes. Si ce n’est pas le cas, le système n’utilise pas les données retournées par la DLL. L’application peut augmenter ou diminuer la valeur du délai d’attente en spécifiant **une valeur de registre d’expiration** ou de **collecte** du délai d’expiration sous leur clé de **performance** , comme indiqué dans l’exemple suivant.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Pour obtenir les données de performances de certaines applications (celles qui retournent des compteurs à l’aide de la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), il est nécessaire d’utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir l’appareil associé à l’application. Dans ce cas, le nom spécifié dans **CreateFile** doit également être installé dans le nœud périphériques dos du Registre, comme illustré ici :

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
