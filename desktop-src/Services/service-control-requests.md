---
description: Pour envoyer des demandes de contrôle à un service en cours d’exécution, un programme de contrôle de service utilise la fonction ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Demandes de contrôle de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4320aad28f8a176fbf4aaa6b51539256a376a01b8edea034341cae7831ca4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967568"
---
# <a name="service-control-requests"></a>Demandes de contrôle de service

Pour envoyer des demandes de contrôle à un service en cours d’exécution, un programme de contrôle de service utilise la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Cette fonction spécifie une valeur de contrôle qui est passée à la fonction [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) du service spécifié. Cette valeur de contrôle peut être un code défini par l’utilisateur, ou il peut s’agir de l’un des codes standard qui permettent au programme appelant d’effectuer les actions suivantes :

-   Arrêter un service (arrêt du contrôle de SERVICE \_ \_ ).
-   Suspendre un service ( \_ suspendre le contrôle de service \_ ).
-   Reprendre l’exécution d’un service suspendu ( \_ le contrôle du service \_ continue).
-   Récupérer les informations d’État mises à jour à partir d’un service (interrogation du SERVICE de \_ contrôle \_ ).

Chaque service spécifie les valeurs de contrôle qu’il acceptera et traitera. Pour déterminer les valeurs de contrôle standard acceptées par un service, utilisez la fonction [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ou spécifiez la valeur de \_ \_ contrôle d’interrogation du contrôle de service dans un appel à la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Le membre **dwControlsAccepted** de la structure d' [**\_ État de service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) retourné par ces fonctions indique si le service peut être arrêté, suspendu ou repris. Tous les services acceptent la \_ valeur de contrôle d’interrogation du contrôle des services \_ .

La fonction [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) signale l’état le plus récent pour un service spécifié, mais n’obtient pas d’État mis à jour à partir du service lui-même. L’utilisation de \_ la \_ valeur de contrôle d’interrogation du contrôle de service dans un appel à [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantit que les informations d’état retournées sont actuelles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un service à l’aide de SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



