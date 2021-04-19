---
description: 'Pour publier une application en fonction de l’installation par utilisateur lorsque l’application requiert des privilèges élevés (c’est-à-dire système) pour l’installation, utilisez les instructions de la liste suivante :'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Publication d’une application Per-User à installer avec des privilèges élevés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517800"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="ff0e1-103">Publication d’une application Per-User à installer avec des privilèges élevés</span><span class="sxs-lookup"><span data-stu-id="ff0e1-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="ff0e1-104">Pour publier une application en fonction de l’installation par utilisateur lorsque l’application requiert des privilèges élevés (c’est-à-dire système) pour l’installation, utilisez les instructions de la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="ff0e1-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="ff0e1-105">Votre processus doit être un service qui s’exécute sous le compte système LocalSystem sur Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff0e1-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="ff0e1-106">Générez un script de publication en appelant [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) ou [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span><span class="sxs-lookup"><span data-stu-id="ff0e1-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="ff0e1-107">Votre processus doit emprunter l’identité de l’utilisateur qui est la cible de la publication.</span><span class="sxs-lookup"><span data-stu-id="ff0e1-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="ff0e1-108">Appelez [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)et utilisez les \_ raccourcis SCRIPTFLAGS CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ appinfo \| SCRIPTFLAGS \_ \_ \| \_ REGDATA CNFGINFO SCRIPTFLAGS.</span><span class="sxs-lookup"><span data-stu-id="ff0e1-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="ff0e1-109">Lorsque vous suivez les instructions, vous publiez une application auprès d’un utilisateur spécifié et, lorsque l’utilisateur choisit d’installer, l’application est installée avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="ff0e1-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff0e1-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff0e1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff0e1-111">Mise à jour corrective des applications gérées par utilisateur</span><span class="sxs-lookup"><span data-stu-id="ff0e1-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



