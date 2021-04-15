---
title: Fonctions d’extraction
description: Les fonctions d’extraction de gestion de réseau récupèrent les informations relatives à un domaine. Vous pouvez également appeler ces fonctions pour récupérer des informations sur les comptes d’utilisateur locaux, globaux, de station de travail et de serveur.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507291"
---
# <a name="get-functions"></a><span data-ttu-id="b045a-104">Fonctions d’extraction</span><span class="sxs-lookup"><span data-stu-id="b045a-104">Get Functions</span></span>

<span data-ttu-id="b045a-105">Les fonctions d’extraction de gestion de réseau récupèrent les informations relatives à un domaine.</span><span class="sxs-lookup"><span data-stu-id="b045a-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="b045a-106">Vous pouvez également appeler ces fonctions pour récupérer des informations sur les comptes d’utilisateur locaux, globaux, de station de travail et de serveur.</span><span class="sxs-lookup"><span data-stu-id="b045a-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="b045a-107">Les fonctions d’extraction de gestion de réseau sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b045a-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="b045a-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="b045a-108">Function</span></span>                                                               | <span data-ttu-id="b045a-109">Description</span><span class="sxs-lookup"><span data-stu-id="b045a-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b045a-110">**NetGetAnyDCName**</span><span class="sxs-lookup"><span data-stu-id="b045a-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="b045a-111">Retourne le nom d’un contrôleur de domaine pour un domaine qui est directement approuvé par un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b045a-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="b045a-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="b045a-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="b045a-113">Retourne le nom du contrôleur de domaine principal (PDC) pour le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="b045a-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="b045a-114">**NetGetDisplayInformationIndex**</span><span class="sxs-lookup"><span data-stu-id="b045a-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="b045a-115">Retourne l’index de la première entrée d’informations d’affichage dont le nom commence par une chaîne spécifiée ou qui suit la chaîne par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="b045a-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="b045a-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="b045a-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="b045a-117">Retourne des informations sur le compte de l’utilisateur, de l’ordinateur ou du groupe global.</span><span class="sxs-lookup"><span data-stu-id="b045a-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="b045a-118">Les informations retournées par la fonction [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="b045a-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="b045a-119">**\_groupe d’affichage net \_**</span><span class="sxs-lookup"><span data-stu-id="b045a-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="b045a-120">**\_ordinateur net Display \_**</span><span class="sxs-lookup"><span data-stu-id="b045a-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="b045a-121">**\_utilisateur NET Display \_**</span><span class="sxs-lookup"><span data-stu-id="b045a-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




