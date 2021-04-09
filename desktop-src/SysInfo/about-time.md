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
# <a name="about-time"></a><span data-ttu-id="a1a2f-105">À propos du temps</span><span class="sxs-lookup"><span data-stu-id="a1a2f-105">About Time</span></span>

<span data-ttu-id="a1a2f-106">Les fonctions relatives à l’heure retournent du temps dans l’un des nombreux formats.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="a1a2f-107">Vous pouvez utiliser les fonctions d’heure pour effectuer une conversion entre des formats d’heure pour faciliter la comparaison et l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="a1a2f-108">Le tableau suivant récapitule les formats d’heure.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="a1a2f-109">Format</span><span class="sxs-lookup"><span data-stu-id="a1a2f-109">Format</span></span>          | <span data-ttu-id="a1a2f-110">Type</span><span class="sxs-lookup"><span data-stu-id="a1a2f-110">Type</span></span>                                                                     | <span data-ttu-id="a1a2f-111">Description</span><span class="sxs-lookup"><span data-stu-id="a1a2f-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a2f-112">Système</span><span class="sxs-lookup"><span data-stu-id="a1a2f-112">System</span></span>          | [<span data-ttu-id="a1a2f-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="a1a2f-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="a1a2f-114">Année, mois, jour, heure, seconde et milliseconde, pris de l’horloge matérielle interne.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="a1a2f-115">Local</span><span class="sxs-lookup"><span data-stu-id="a1a2f-115">Local</span></span>           | <span data-ttu-id="a1a2f-116">[**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) ou [ **fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="a1a2f-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="a1a2f-117">Heure système ou heure du fichier convertie dans le fuseau horaire local du système.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="a1a2f-118">Fichier</span><span class="sxs-lookup"><span data-stu-id="a1a2f-118">File</span></span>            | [<span data-ttu-id="a1a2f-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="a1a2f-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="a1a2f-120">Nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="a1a2f-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="a1a2f-121">MS-DOS</span></span>          | <span data-ttu-id="a1a2f-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="a1a2f-122">**WORD**</span></span>                                                                 | <span data-ttu-id="a1a2f-123">Mot condensé pour la date, un autre pour le moment.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="a1a2f-124">Windows</span><span class="sxs-lookup"><span data-stu-id="a1a2f-124">Windows</span></span>         | <span data-ttu-id="a1a2f-125">**DWORD** ou **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="a1a2f-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="a1a2f-126">Nombre de millisecondes écoulées depuis le dernier démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="a1a2f-127">En cas de récupération en tant que valeur DWORD, cycles de temps Windows tous les 49,7 jours.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="a1a2f-128">Nombre d’interruptions</span><span class="sxs-lookup"><span data-stu-id="a1a2f-128">Interrupt Count</span></span> | <span data-ttu-id="a1a2f-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="a1a2f-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="a1a2f-130">Nombre d’intervalles de 100 nanosecondes depuis le dernier démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a1a2f-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="a1a2f-131">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1a2f-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a1a2f-132">Temps système</span><span class="sxs-lookup"><span data-stu-id="a1a2f-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="a1a2f-133">Heure locale</span><span class="sxs-lookup"><span data-stu-id="a1a2f-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="a1a2f-134">Heures du fichier</span><span class="sxs-lookup"><span data-stu-id="a1a2f-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="a1a2f-135">Date et heure MS-DOS</span><span class="sxs-lookup"><span data-stu-id="a1a2f-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="a1a2f-136">Horloge Windows</span><span class="sxs-lookup"><span data-stu-id="a1a2f-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="a1a2f-137">Temps d’interruption</span><span class="sxs-lookup"><span data-stu-id="a1a2f-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
