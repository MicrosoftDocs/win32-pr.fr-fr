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
# <a name="creating-other-registry-entries"></a><span data-ttu-id="8c5e8-103">Création d’autres entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="8c5e8-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="8c5e8-104">La fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) de la dll de performance accepte un argument de chaîne comme entrée.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="8c5e8-105">Pour fournir une chaîne d’entrée à votre fonction ouverte, ajoutez une clé de **liaison** sous la clé de vos **services** .</span><span class="sxs-lookup"><span data-stu-id="8c5e8-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="8c5e8-106">La clé de **liaison** contient une valeur d' **exportation** .</span><span class="sxs-lookup"><span data-stu-id="8c5e8-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="8c5e8-107">Définissez les données de valeur pour **Export** sur la chaîne d’entrée que vous souhaitez transmettre à votre fonction Open.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="8c5e8-108">Le type de données de l' **exportation** est **reg \_ multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="8c5e8-109">Si l' **exportation** n’est pas définie (l'**exportation** est facultative), le système passe la **valeur null** à votre fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8c5e8-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="8c5e8-110">En règle générale, si plusieurs applications partagent la même DLL de performance, chaque application comprend une clé de **liaison** et une valeur d' **exportation** pour fournir le contexte de l’application qui appelle la dll.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="8c5e8-111">L’exemple suivant montre les entrées de Registre :</span><span class="sxs-lookup"><span data-stu-id="8c5e8-111">The following shows the registry entries:</span></span>

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

<span data-ttu-id="8c5e8-112">Par défaut, les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) et [**COLLECTPERFORMANCEDATA**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) de la dll de performance doivent retourner dans un délai de 10 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="8c5e8-113">Si ce n’est pas le cas, le système n’utilise pas les données retournées par la DLL.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="8c5e8-114">L’application peut augmenter ou diminuer la valeur du délai d’attente en spécifiant **une valeur de registre d’expiration** ou de **collecte** du délai d’expiration sous leur clé de **performance** , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

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

<span data-ttu-id="8c5e8-115">Pour obtenir les données de performances de certaines applications (celles qui retournent des compteurs à l’aide de la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), il est nécessaire d’utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir l’appareil associé à l’application.</span><span class="sxs-lookup"><span data-stu-id="8c5e8-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="8c5e8-116">Dans ce cas, le nom spécifié dans **CreateFile** doit également être installé dans le nœud périphériques dos du Registre, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="8c5e8-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
