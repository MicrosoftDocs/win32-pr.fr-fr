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
# <a name="statistics-functions"></a>Fonctions statistiques

Le système d’exploitation Windows accumule un ensemble de statistiques d’exploitation pour les stations de travail et les serveurs à partir du moment où le service de station de travail ou de serveur est démarré. Pour récupérer ces statistiques, vous pouvez appeler la fonction de statistiques de gestion de réseau suivante.



| Fonction                                     | Description                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Récupère les statistiques d’exploitation d’un service ; prend en charge les services station de travail et serveur. |



 

La fonction **NetStatisticsGet** retourne une structure de [**station de travail stat \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) lorsque des statistiques de station de travail sont demandées ; la fonction retourne une structure [**Stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) lorsque les statistiques du serveur sont demandées.

 

 



