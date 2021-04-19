---
title: Fonctions de planification
description: Les fonctions de service de planification de la gestion du réseau soumettent et gèrent les tâches qui s’exécutent sur un ordinateur spécifié à un moment donné (ou heure) à l’avenir.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509462"
---
# <a name="schedule-functions"></a>Fonctions de planification

Les fonctions de service de planification de la gestion du réseau soumettent et gèrent les tâches qui s’exécutent sur un ordinateur spécifié à un moment donné (ou heure) à l’avenir. Les tâches peuvent inclure des commandes et des programmes. Les fonctions gèrent les travaux sur les ordinateurs distants et locaux, à condition que le service de planification s’exécute sur l’ordinateur.

Les fonctions de service de planification sont répertoriées ci-après.



| Fonction                                                                     | Description                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Soumet un travail à exécuter à une date et une heure futures spécifiées.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Annule une plage de travaux en file d’attente d’exécution sur un ordinateur.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Répertorie les travaux en file d’attente sur un ordinateur spécifié.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Retourne des informations sur un travail particulier mis en file d’attente sur un ordinateur. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Récupère le nom du compte de service AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Définit le nom du compte de service AT et le mot de passe.                   |



 

Pour que les fonctions de planification de la gestion de réseau fonctionnent correctement, un appelant doit avoir le privilège d’administrateur sur l’ordinateur sur lequel le service de planification est en cours d’exécution. Les fonctions de service de planification sont également appelées fonctions « Job » et « AT Command ». Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

La structure [**at \_ info**](/windows/desktop/api/Lmat/ns-lmat-at_info) est utilisée par la fonction [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) pour spécifier des informations lors de l’envoi d’un travail, et par la fonction [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) pour récupérer des informations sur un travail qui a été soumis. La structure d' [**\_ énumération at**](/windows/desktop/api/Lmat/ns-lmat-at_enum) est utilisée par [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) pour énumérer et retourner des informations sur l’intégralité d’une file d’attente de travaux soumis.

 

 