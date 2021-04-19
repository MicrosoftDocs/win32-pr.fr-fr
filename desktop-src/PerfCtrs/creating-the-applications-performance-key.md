---
description: Une application qui prend en charge les compteurs de performance doit avoir une clé de performance sous la clé des services. L’exemple suivant montre les valeurs que vous devez inclure pour cette clé.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Création de la clé de performance des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517708"
---
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="8b5db-104">Création de la clé de performance de l’application</span><span class="sxs-lookup"><span data-stu-id="8b5db-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="8b5db-105">Une application qui prend en charge les compteurs de performance doit avoir une clé de **performance** sous la clé des **services** .</span><span class="sxs-lookup"><span data-stu-id="8b5db-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="8b5db-106">L’exemple suivant montre les valeurs que vous devez inclure pour cette clé.</span><span class="sxs-lookup"><span data-stu-id="8b5db-106">The following example shows the values that you must include for this key.</span></span>

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

<span data-ttu-id="8b5db-107">La valeur de la **bibliothèque** fournit le nom de la dll de performance, et les valeurs **ouvrir**, **collecter** et **Fermer** fournissent les noms des fonctions exportées à partir de la dll de performance.</span><span class="sxs-lookup"><span data-stu-id="8b5db-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="8b5db-108">Le type de données de ces valeurs est **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="8b5db-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="8b5db-109">Lorsqu’un consommateur demande des données de performances, le système utilise ces valeurs pour déterminer les dll de performance à charger et les fonctions DLL à appeler.</span><span class="sxs-lookup"><span data-stu-id="8b5db-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="8b5db-110">La valeur de la **bibliothèque** peut contenir le nom de la dll ou un chemin d’accès complet à la dll.</span><span class="sxs-lookup"><span data-stu-id="8b5db-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="8b5db-111">Si vous utilisez le type de données **reg \_ expand \_ SZ** pour la **bibliothèque**, vous pouvez spécifier des variables d’environnement dans votre chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8b5db-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="8b5db-112">La clé de service de l’application doit exister avant que vous puissiez exécuter **lodctr** pour charger les noms de compteur et les chaînes d’aide.</span><span class="sxs-lookup"><span data-stu-id="8b5db-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="8b5db-113">Pour obtenir des valeurs de Registre supplémentaires que vous pouvez créer, telles que la spécification de valeurs de délai d’attente pour les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) et [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consultez [création d’autres entrées de Registre](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="8b5db-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
