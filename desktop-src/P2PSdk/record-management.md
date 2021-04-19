---
description: Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d’enregistrement d’HOMOLOGUe \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestion des enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544973"
---
# <a name="record-management"></a>Gestion des enregistrements

Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Lorsque des enregistrements sont créés, mis à jour ou supprimés, les modifications apportées à un graphique sont répliquées sur tous les nœuds. Le tableau suivant répertorie les règles de mise à jour et d’actualisation automatique des enregistrements.



| Tâche de gestion     | Règle                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mise à jour d'un enregistrement   | Conservez la même heure d’expiration ou augmentez-la. Vous ne pouvez pas réduire le délai d’expiration.                                                                                                                      |
| Actualisation d’un enregistrement | Utilisez l’indicateur d’actualisation automatique de l' [**\_ indicateur d’enregistrement \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) pour actualiser automatiquement un enregistrement. Utilisez cet indicateur uniquement lorsque le nœud qui publie un enregistrement est en ligne. Dans le cas contraire, n’utilisez pas cet indicateur. |



 

 

 



