---
title: Obtention de l’heure système
description: Obtention de l’heure système
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- minuteries multimédias, heure système
- minuteries, heure système
- heure système
- timeGetTime fonction)
- timeGetSystemTime fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462995"
---
# <a name="obtaining-the-system-time"></a><span data-ttu-id="11565-108">Obtention de l’heure système</span><span class="sxs-lookup"><span data-stu-id="11565-108">Obtaining the System Time</span></span>

<span data-ttu-id="11565-109">En règle générale, avant qu’une application commence à utiliser les services de minuteur multimédia, elle récupère l' *heure système* actuelle.</span><span class="sxs-lookup"><span data-stu-id="11565-109">Typically, before an application begins using the multimedia timer services, it retrieves the current *system time*.</span></span> <span data-ttu-id="11565-110">L’heure système correspond à la durée, en millisecondes, depuis le démarrage du système d’exploitation Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="11565-110">The system time is the time, in milliseconds, since the Microsoft Windows operating system was started.</span></span> <span data-ttu-id="11565-111">Vous pouvez utiliser la fonction [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) ou [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) pour récupérer l’heure système.</span><span class="sxs-lookup"><span data-stu-id="11565-111">You can use the [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) or [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) function to retrieve the system time.</span></span> <span data-ttu-id="11565-112">Ces deux fonctions sont très similaires : **timeGetTime** retourne l’heure système et **timeGetSystemTime** remplit une structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) avec l’heure système.</span><span class="sxs-lookup"><span data-stu-id="11565-112">These two functions are very similar: **timeGetTime** returns the system time, and **timeGetSystemTime** fills an [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure with the system time.</span></span>

 

 