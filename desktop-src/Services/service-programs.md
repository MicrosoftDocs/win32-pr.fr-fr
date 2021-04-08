---
description: Un programme de service contient du code exécutable pour un ou plusieurs services.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programmes de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868186"
---
# <a name="service-programs"></a>Programmes de service

Un *programme de service* contient du code exécutable pour un ou plusieurs services. Un programme de service créé avec le processus de type SERVICE Win32 de type SERVICE \_ \_ \_ contient le code pour un seul service. Un programme de service créé avec le \_ \_ processus de partage de type service Win32 \_ contient du code pour plusieurs services, ce qui leur permet de partager du code. Un exemple de programme de service qui effectue cette opération est le processus hôte de service générique, Svchost.exe, qui héberge des services Windows internes. Notez que Svchost.exe est réservée à une utilisation par le système d’exploitation et qu’il ne doit pas être utilisé par des services non-Windows. Au lieu de cela, les développeurs doivent implémenter leurs propres programmes d’hébergement de service.

Un programme de service peut être configuré pour s’exécuter dans le contexte d’un compte d’utilisateur à partir du domaine intégré (local), principal ou approuvé. Il peut également être configuré pour s’exécuter dans un [compte d’utilisateur de service](service-user-accounts.md)spécial.

Les rubriques suivantes décrivent les exigences d’interface du [Gestionnaire de contrôle des services](service-control-manager.md) (SCM) qu’un programme de service doit inclure :

-   [Point d’entrée de service](service-entry-point.md)
-   [Fonction de service ServiceMain](service-servicemain-function.md)
-   [Fonction du gestionnaire de contrôle des services](service-control-handler-function.md)

Ces rubriques ne s’appliquent pas aux services de pilote. Pour connaître les exigences en matière d’interface des services de pilote, consultez le kit de pilotes Windows (WDK).

Un service s’exécute en tant que processus en arrière-plan qui peut affecter les performances du système, la réactivité, l’efficacité énergétique et la sécurité. Pour obtenir des instructions sur l’optimisation des services, consultez [développement de processus d’arrière-plan efficaces pour Windows](/windows-hardware/drivers/kernel/implementing-power-management). Les rubriques suivantes décrivent d’autres considérations relatives à la programmation :

-   [Transitions d’état de service](service-status-transitions.md)
-   [Réception d’événements dans un service](receiving-events-in-a-service.md)
-   [Services multithread](multithreaded-services.md)
-   [Services et Registre](services-and-the-registry.md)
-   [Services et lecteurs redirigés](services-and-redirected-drives.md)
-   [Événements de déclencheur de service](service-trigger-events.md)

Notez que si le programme de service fonctionne comme un serveur RPC, il doit utiliser des points de terminaison dynamiques et une authentification mutuelle.

 

 
