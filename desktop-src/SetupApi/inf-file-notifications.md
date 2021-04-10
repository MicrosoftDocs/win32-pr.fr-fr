---
description: Les notifications suivantes sont utilisées avec les fonctions SetupInstallFile, SetupInstallFileEx et SetupInstallFromInfSection. Pour plus d’informations sur le format et l’utilisation des notifications, consultez notifications.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notifications de fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952107"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="3a483-104">Notifications de fichier INF</span><span class="sxs-lookup"><span data-stu-id="3a483-104">INF File Notifications</span></span>

<span data-ttu-id="3a483-105">Les notifications suivantes sont utilisées avec les fonctions [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)et [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) .</span><span class="sxs-lookup"><span data-stu-id="3a483-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="3a483-106">Pour plus d’informations sur le format et l’utilisation des notifications, consultez [notifications](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3a483-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="3a483-107">Notification</span><span class="sxs-lookup"><span data-stu-id="3a483-107">Notification</span></span>                                                      | <span data-ttu-id="3a483-108">Description</span><span class="sxs-lookup"><span data-stu-id="3a483-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a483-109">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="3a483-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="3a483-110">Le fichier est en cours d’utilisation et l’opération en cours est retardée jusqu’au redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="3a483-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="3a483-111">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="3a483-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="3a483-112">La langue du fichier actuel ne correspond pas à la langue du système.</span><span class="sxs-lookup"><span data-stu-id="3a483-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="3a483-113">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="3a483-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="3a483-114">Une copie du fichier spécifié existe déjà sur la cible.</span><span class="sxs-lookup"><span data-stu-id="3a483-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="3a483-115">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="3a483-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="3a483-116">Une version plus récente du fichier spécifié existe sur la cible.</span><span class="sxs-lookup"><span data-stu-id="3a483-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="3a483-117">Étant donné que [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crée et valide une file d’attente de fichiers interne, il utilise également les [notifications de file d’attente de fichiers](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3a483-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



