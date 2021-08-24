---
description: Une application qui prend en charge les compteurs de performance doit avoir une clé de performance sous la clé des services. L’exemple suivant montre les valeurs que vous devez inclure pour cette clé.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Création de la clé de performance des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144032"
---
# <a name="creating-the-applications-performance-key"></a>Création de la clé de performance de l’application

Une application qui prend en charge les compteurs de performance doit avoir une clé de **performance** sous la clé des **services** . L’exemple suivant montre les valeurs que vous devez inclure pour cette clé.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

La valeur de la **bibliothèque** fournit le nom de la dll de performance, et les valeurs **ouvrir**, **collecter** et **Fermer** fournissent les noms des fonctions exportées à partir de la dll de performance. Le type de données de ces valeurs est **reg \_ SZ**. Lorsqu’un consommateur demande des données de performances, le système utilise ces valeurs pour déterminer les dll de performance à charger et les fonctions DLL à appeler.

La valeur de la **bibliothèque** peut contenir le nom de la dll ou un chemin d’accès complet à la dll. Si vous utilisez le type de données **reg \_ expand \_ SZ** pour la **bibliothèque**, vous pouvez spécifier des variables d’environnement dans votre chemin d’accès.

La clé de service de l’application doit exister avant que vous puissiez exécuter **lodctr** pour charger les noms de compteur et les chaînes d’aide.

Pour obtenir des valeurs de Registre supplémentaires que vous pouvez créer, telles que la spécification de valeurs de délai d’attente pour les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) et [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consultez [création d’autres entrées de Registre](creating-other-registry-entries.md).

 

 
