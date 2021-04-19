---
description: À l’heure actuelle, tout le minutage des appels est laissé aux applications.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Minuterie de l’état d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544702"
---
# <a name="call-state-timer"></a><span data-ttu-id="84e11-103">Minuterie de l’état d’appel</span><span class="sxs-lookup"><span data-stu-id="84e11-103">Call State Timer</span></span>

<span data-ttu-id="84e11-104">À l’heure actuelle, tout le minutage des appels est laissé aux applications.</span><span class="sxs-lookup"><span data-stu-id="84e11-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="84e11-105">Cela peut être fastidieux si l’application surveille un grand nombre d’appels, et si plusieurs applications sont présentes, éventuellement sur plusieurs serveurs, il peut être nécessaire qu’ils maintiennent tous les minuteurs sur les mêmes appels.</span><span class="sxs-lookup"><span data-stu-id="84e11-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="84e11-106">Il est donc plus judicieux de gérer le minutage de l’état des appels par le serveur.</span><span class="sxs-lookup"><span data-stu-id="84e11-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="84e11-107">Le membre **tStateEntryTime** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permet d’indiquer le minutage des appels dans les États.</span><span class="sxs-lookup"><span data-stu-id="84e11-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="84e11-108">Le membre (de type **sysTime**) indique l’heure à laquelle l’état actuel a été entré.</span><span class="sxs-lookup"><span data-stu-id="84e11-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



