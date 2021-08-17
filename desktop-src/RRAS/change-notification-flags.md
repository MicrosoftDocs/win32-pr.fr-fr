---
title: Indicateurs de notification de modification
description: Indicateurs de notification de modification
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifier
- Indicateurs de notification de modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f5311e3313bf23c92972395143d288483181e7a69212115082a2f150d7d1bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791833"
---
# <a name="change-notification-flags"></a>Indicateurs de notification de modification



| Constante                         | Valeur      | Description                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_types de \_ changement de nombre RTM \_          | 3          | Spécifie le nombre de types de modification actuellement utilisés par le gestionnaire de tables de routage.                                                                            |
| \_type de modification RTM \_ \_ tout           | 0x0001     | Notifie le client de toute modification apportée à une destination.                                                                                                                   |
| \_type de modification RTM \_ \_ optimal          | 0x0002     | Notifie le client des modifications apportées au meilleur itinéraire ou lorsque le meilleur itinéraire change.                                                                                     |
| \_transfert de \_ type de modification RTM \_    | 0x0004     | Notifie le client des modifications de routage les plus adaptées qui affectent le transfert (par exemple, les changements de tronçons suivants).                                                                      |
| les \_ notifications RTM signalent \_ uniquement les \_ \_ dest. | 0x00010000 | Notifie le client des modifications apportées aux destinations marquées par le client. Si cet indicateur n’est pas spécifié, les messages de notification de modification pour toutes les destinations sont envoyés. |



 

 

 




