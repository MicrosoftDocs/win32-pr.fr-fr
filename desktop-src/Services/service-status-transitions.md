---
description: Un service est chargé de signaler les modifications de son état au gestionnaire de contrôle des services (SCM).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transitions d’état de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039caf68ee7d9da93e86e1760e49df87667da8c16eb5ca6693cfdc7db7def2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967310"
---
# <a name="service-state-transitions"></a>Transitions d’état de service

Un service est chargé de signaler les modifications de son état au gestionnaire de contrôle des services (SCM). Les programmes de contrôle de service et le système peuvent déterminer l’état d’un service uniquement à partir du SCM. il est donc important qu’un service signale son état correctement. Un service signale son état en appelant la fonction [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec un pointeur vers une structure d' [**\_ État de service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) entièrement initialisée. Le membre **dwCurrentState** de la structure contient l’état du service à signaler.

L’état initial d’un service est \_ arrêté. Lorsque le SCM démarre le service, il définit l’état du service sur \_ attente du démarrage du service \_ et appelle la fonction [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) du service. Le service termine ensuite son initialisation à l’aide de l’une des techniques décrites dans la [fonction service ServiceMain](service-servicemain-function.md). Une fois que le service a terminé son initialisation et est prêt à commencer à recevoir des demandes de contrôle, le service appelle [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour signaler le service d' \_ exécution et spécifie les demandes de contrôle que le service est prêt à accepter. La transition du démarrage du SERVICE \_ \_ en attente au service \_ en cours d’exécution indique aux outils SCM et de surveillance des services que le service a démarré avec succès. Si le service signale un État autre que SERVICE \_ en cours d’exécution, les outils SCM ou d’analyse de service peuvent signaler que le service n’a pas pu démarrer.

Le SCM envoie uniquement les demandes de contrôle spécifiées au service (à l’exception de la \_ demande d’interrogation de contrôle de service \_ , qui est toujours envoyée). Pour obtenir la liste des demandes de contrôle qu’un service peut accepter, consultez le membre **dwControlsAccepted** de la structure d' [**\_ État du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Pour plus d’informations sur l’inscription pour recevoir des événements d’appareil, consultez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

L’état du service change généralement suite à la gestion d’une demande de contrôle. Les demandes de contrôle qui provoquent le changement de l’état du service incluent l’arrêt du contrôle de SERVICE \_ , la suspension du contrôle du \_ service et la poursuite du contrôle du \_ \_ service \_ \_ . Si le service doit effectuer un traitement de longue durée pour gérer l’une de ces demandes, il doit créer un thread secondaire pour effectuer le traitement long et signaler l’état d’attente correspondant au SCM. (pour des performances optimales sur Windows Vista et les versions ultérieures de Windows, le service doit utiliser un thread de travail à partir d’un [pool de threads](/windows/desktop/ProcThread/thread-pools) à cet effet.) Le service doit ensuite signaler la transition de l’état terminé lorsque le traitement long est terminé. Pour plus d’informations sur la gestion des demandes de contrôle, consultez [fonction du gestionnaire de contrôle des services](service-control-handler-function.md).

Seules certaines transitions d’état de service sont valides. Le diagramme suivant montre les transitions valides.

![transitions d’état de service valides](images/service-status-transitions.png)

L’état du service signalé au SCM détermine la façon dont le SCM interagit avec le service. Par exemple, si un SERVICE des rapports de service s' \_ arrête \_ en attente, le SCM ne transmet pas d’autres demandes de contrôle au service, car cet État indique que le service est en cours d’arrêt. L’état suivant signalé par le service doit être \_ arrêté, car il s’agit du seul État valide après l’arrêt du service \_ \_ en attente. Toutefois, si un service signale une transition qui n’est pas valide, le SCM n’échoue pas à l’appel.

Le diagramme suivant montre les transitions d’état de service plus en détail, y compris les demandes de contrôle initiées par un programme de contrôle de service (le client de service) et les appels [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) qu’un service effectue pour signaler les modifications d’État au SCM. Comme mentionné précédemment, le SCM envoie uniquement les demandes de contrôle que le service a spécifié qu’il acceptera, donc un service risque de ne pas recevoir toutes les demandes présentées dans le diagramme.

![transitions d’état de service en détail ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
