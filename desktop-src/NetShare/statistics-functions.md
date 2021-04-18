---
description: Le système d’exploitation Windows accumule un ensemble de statistiques d’exploitation pour les stations de travail et les serveurs à partir du moment où le service de station de travail ou de serveur est démarré.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Fonctions statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520069"
---
# <a name="statistics-functions"></a><span data-ttu-id="208eb-103">Fonctions statistiques</span><span class="sxs-lookup"><span data-stu-id="208eb-103">Statistics Functions</span></span>

<span data-ttu-id="208eb-104">Le système d’exploitation Windows accumule un ensemble de statistiques d’exploitation pour les stations de travail et les serveurs à partir du moment où le service de station de travail ou de serveur est démarré.</span><span class="sxs-lookup"><span data-stu-id="208eb-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="208eb-105">Pour récupérer ces statistiques, vous pouvez appeler la fonction de statistiques de gestion de réseau suivante.</span><span class="sxs-lookup"><span data-stu-id="208eb-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="208eb-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="208eb-106">Function</span></span>                                     | <span data-ttu-id="208eb-107">Description</span><span class="sxs-lookup"><span data-stu-id="208eb-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="208eb-108">**NetStatisticsGet**</span><span class="sxs-lookup"><span data-stu-id="208eb-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="208eb-109">Récupère les statistiques d’exploitation d’un service ; prend en charge les services station de travail et serveur.</span><span class="sxs-lookup"><span data-stu-id="208eb-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="208eb-110">La fonction **NetStatisticsGet** retourne une structure de [**station de travail stat \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) lorsque des statistiques de station de travail sont demandées ; la fonction retourne une structure [**Stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) lorsque les statistiques du serveur sont demandées.</span><span class="sxs-lookup"><span data-stu-id="208eb-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



