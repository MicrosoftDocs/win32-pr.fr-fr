---
title: Informations sur la plage de travail
description: La plage de travail d’un processus correspond à la quantité de mémoire physiquement mappée à son contexte de processus. PSAPI vous permet de prendre des instantanés de la plage de travail ou de surveiller la plage de travail.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56e1e4dc0a68a9d4507a94ad1f5356432f8488a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313297"
---
# <a name="working-set-information"></a>Informations sur la plage de travail

La plage de travail d’un processus correspond à la quantité de mémoire physiquement mappée à son contexte de processus. PSAPI vous permet de prendre des instantanés de la plage de travail ou de surveiller la plage de travail.

La fonction [**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) ou [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) remplit une mémoire tampon avec un instantané des informations pour chaque page de la plage de travail actuelle du processus spécifié. La fonction signale uniquement les pages qui sont physiquement présentes à l’heure exacte à laquelle elles sont appelées.

Vous pouvez utiliser la surveillance de la plage de travail pour déterminer la quantité de RAM supplémentaire que prend une opération particulière (par exemple, l’enregistrement d’un fichier). Pour commencer l’analyse de la plage de travail, appelez la fonction [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) . Tous les processus ne vous permettent pas de lire leurs informations de jeu de travail. par conséquent, assurez-vous que la fonction retourne une valeur différente de zéro avant de continuer. Ensuite, appelez la fonction [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) . Cette fonction signale uniquement les pages qui ont été chargées en mémoire depuis que vous avez commencé à surveiller la plage de travail. La fonction retourne des données dans un tableau de structures d’informations de la vue de gestion de données ( [**PSAPI) \_ WSI \_ \_**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) , une structure pour chaque nouvelle page ajoutée à la plage de travail du processus. La structure vous indique quelles pages sont en mémoire, et ce qui a provoqué la pagination du système.

La fonction [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) prend un handle de processus. Elle supprime autant de pages que possible de la plage de travail du processus. Cette opération est principalement utile pour le test et le réglage. Notez que la fonction [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) effectue la même opération si vous la transmettez-1 pour les tailles minimale et maximale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Plage de travail](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 