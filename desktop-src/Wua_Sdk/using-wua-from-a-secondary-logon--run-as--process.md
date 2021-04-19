---
description: Les mises à jour qui nécessitent une intervention de l’utilisateur ne peuvent pas être installées par Windows Update les applications de l’agent (WUA) si les applications WUA s’exécutent dans le contexte du service d’ouverture de session secondaire.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Utilisation de WUA à partir d’un processus d’ouverture de session secondaire (exécuter en tant que)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531666"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="e0eb1-103">Utilisation de WUA à partir d’un processus d’ouverture de session secondaire (exécuter en tant que)</span><span class="sxs-lookup"><span data-stu-id="e0eb1-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="e0eb1-104">Les mises à jour qui nécessitent une intervention de l’utilisateur ne peuvent pas être installées par Windows Update les applications de l’agent (WUA) si les applications WUA s’exécutent dans le contexte du service d’ouverture de session secondaire.</span><span class="sxs-lookup"><span data-stu-id="e0eb1-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="e0eb1-105">Si le processus qui appelle WUA s’exécute dans le contexte du service RunAs ou du service d’ouverture de session secondaire, une tentative d’installation d’une mise à jour nécessitant une interaction avec l’utilisateur échoue et renvoie l’erreur de l' **\_ utilisateur Wu E \_ no \_ interactive \_** .</span><span class="sxs-lookup"><span data-stu-id="e0eb1-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="e0eb1-106">Dans Microsoft Windows, vous pouvez exécuter des programmes en tant qu’utilisateur qui diffère de l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="e0eb1-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="e0eb1-107">Pour ce faire, le service d’ouverture de session secondaire doit être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0eb1-107">To do this the Secondary Logon service must be running.</span></span>

 

 



