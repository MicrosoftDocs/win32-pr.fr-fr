---
description: Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d’enregistrement d’HOMOLOGUe \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestion des enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011517"
---
# <a name="record-management"></a>Gestion des enregistrements

Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Lorsque des enregistrements sont créés, mis à jour ou supprimés, les modifications apportées à un graphique sont répliquées sur tous les nœuds. Le tableau suivant répertorie les règles de mise à jour et d’actualisation automatique des enregistrements.



| Tâche de gestion     | Règle                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mise à jour d'un enregistrement   | Conservez la même heure d’expiration ou augmentez-la. Vous ne pouvez pas réduire le délai d’expiration.                                                                                                                      |
| Actualisation d’un enregistrement | Utilisez l’indicateur d’actualisation automatique de l' [**\_ indicateur d’enregistrement \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) pour actualiser automatiquement un enregistrement. Utilisez cet indicateur uniquement lorsque le nœud qui publie un enregistrement est en ligne. Dans le cas contraire, n’utilisez pas cet indicateur. |



 

 

 



