---
title: Indicateurs de notification de modification
description: Indicateurs de notification de modification
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifier
- Indicateurs de notification de modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310186"
---
# <a name="change-notification-flags"></a>Indicateurs de notification de modification



| Constante                         | Valeur      | Description                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_types de \_ changement de nombre RTM \_          | 3          | Spécifie le nombre de types de modification actuellement utilisés par le gestionnaire de tables de routage.                                                                            |
| \_type de modification RTM \_ \_ tout           | 0x0001     | Notifie le client de toute modification apportée à une destination.                                                                                                                   |
| \_type de modification RTM \_ \_ optimal          | 0x0002     | Notifie le client des modifications apportées au meilleur itinéraire ou lorsque le meilleur itinéraire change.                                                                                     |
| \_transfert de \_ type de modification RTM \_    | 0x0004     | Notifie le client des modifications de routage les plus adaptées qui affectent le transfert (par exemple, les changements de tronçons suivants).                                                                      |
| les \_ notifications RTM signalent \_ uniquement les \_ \_ dest. | 0x00010000 | Notifie le client des modifications apportées aux destinations marquées par le client. Si cet indicateur n’est pas spécifié, les messages de notification de modification pour toutes les destinations sont envoyés. |



 

 

 




