---
description: le système d’exploitation Windows accumule un ensemble de statistiques d’exploitation pour les stations de travail et les serveurs à partir du moment où le service de station de travail ou de serveur est démarré.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Fonctions statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2261f0c4f8f8249b401e658759827d6471d3ac47b6eb10df769ad5f37d8ce7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063589"
---
# <a name="statistics-functions"></a>Fonctions statistiques

le système d’exploitation Windows accumule un ensemble de statistiques d’exploitation pour les stations de travail et les serveurs à partir du moment où le service de station de travail ou de serveur est démarré. Pour récupérer ces statistiques, vous pouvez appeler la fonction de statistiques de gestion de réseau suivante.



| Fonction                                     | Description                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Récupère les statistiques d’exploitation d’un service ; prend en charge les services station de travail et serveur. |



 

La fonction **NetStatisticsGet** retourne une structure de [**station de travail stat \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) lorsque des statistiques de station de travail sont demandées ; la fonction retourne une structure [**Stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) lorsque les statistiques du serveur sont demandées.

 

 



