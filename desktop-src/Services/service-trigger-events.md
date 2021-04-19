---
description: Un service peut s’inscrire pour être démarré ou arrêté lorsqu’un événement déclencheur se produit.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Événements de déclencheur de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524442"
---
# <a name="service-trigger-events"></a>Événements de déclencheur de service

Un service peut s’inscrire pour être démarré ou arrêté lorsqu’un événement déclencheur se produit. Cela élimine la nécessité de démarrer les services au démarrage du système, ou pour que les services interinterrogent ou attendent activement un événement. un service peut démarrer quand il est nécessaire, au lieu de démarrer automatiquement, qu’il y ait ou non un travail à effectuer. Les exemples d’événements déclencheurs prédéfinis incluent l’arrivée d’un appareil d’une classe d’interface d’appareil spécifiée ou la disponibilité d’un port de pare-feu particulier. Un service peut également s’inscrire pour un événement de déclencheur personnalisé généré par un fournisseur de [suivi d’v nements pour Windows](../etw/event-tracing-portal.md) (ETW).

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Les événements de déclencheur de service ne sont pas pris en charge avant Windows Server 2008 R2 et Windows 7.

Un déclencheur se compose d’un type d’événement déclencheur, d’un sous-type d’événement déclencheur, de l’action à entreprendre en réponse à l’événement déclencheur et (pour certains types d’événements déclencheurs) d’un ou plusieurs éléments de données spécifiques au déclencheur. Le sous-type et les éléments de données spécifiques aux déclencheurs spécifient ensemble les conditions pour notifier le service de l’événement. Le format d’un élément de données dépend du type d’événement déclencheur ; un élément de données peut être des données binaires, une chaîne ou une chaîne. Les chaînes doivent être au format Unicode ; Les chaînes ANSI ne sont pas prises en charge.

Pour s’inscrire aux événements de déclencheur, le service appelle [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) avec les **\_ \_ \_ informations de déclencheur de configuration de service** et fournit une structure d' [**\_ \_ informations de déclencheur de service**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) . La structure des **\_ \_ informations de déclencheur de service** pointe vers un tableau de structures de [**\_ déclencheur de service**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) , chacune spécifiant un déclencheur.

L’action de déclenchement spécifiée est exécutée si la condition de déclenchement est vraie au démarrage du système, ou si la condition de déclencheur devient vraie alors que le système est en cours d’exécution. Par exemple, si un service s’inscrit pour démarrer lorsqu’un appareil particulier est disponible, le service est démarré lorsque le système démarre si l’appareil est déjà connecté à l’ordinateur ; le service est démarré lorsque l’appareil arrive si l’utilisateur se connecte à l’appareil pendant que le système est en cours d’exécution.

Si un déclencheur possède des éléments de données spécifiques aux déclencheurs, l’action du déclencheur est effectuée uniquement si l’élément de données qui accompagne l’événement déclencheur correspond à l’un des éléments de données que le service a spécifiés avec le déclencheur. La correspondance des données binaires est effectuée par comparaison au niveau du bit. La correspondance de chaîne ne respecte pas la casse. Si l’élément de données est une chaîne multichaîne, toutes les chaînes de la chaîne doivent correspondre.

Lorsqu’un service est démarré en réponse à un événement déclencheur, le service reçoit le **\_ déclencheur service Trigger \_ Started \_** comme *argv* \[ 1 \] dans sa fonction de rappel [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . *Argv* \[ 0 \] est toujours le nom abrégé du service.

Un service qui s’inscrit pour démarrer en réponse à un événement déclencheur peut s’arrêter lui-même après un délai d’inactivité lorsque le service n’a pas de travail à effectuer. Un service qui s’arrête lui-même doit être préparé à gérer le **contrôle de service \_ \_ TRIGGEREVENT** les demandes qui arrivent pendant que le service s’arrête lui-même. Le SCM envoie une demande de contrôle de **\_ \_ TRIGGEREVENT de contrôle de service** chaque fois qu’un nouvel événement de déclencheur se produit alors que le service est à l’État en cours d’exécution. Pour éviter de perdre des événements déclencheurs, le service doit retourner l' **arrêt des erreurs \_ \_ en \_ cours** pour toute demande de contrôle **TRIGGEREVENT de \_ contrôle \_ de service** qui arrive pendant que le service passe de l’État exécution à l’état arrêté. Cela indique au SCM d’effectuer la mise en file d’attente des événements déclencheurs et d’attendre que le service passe à l’état arrêté. Le SCM prend ensuite l’action associée à l’événement de déclencheur mis en file d’attente, tel que le démarrage du service.

Lorsque le service est prêt à gérer à nouveau les événements de déclencheur, il définit le paramètre **\_ Accept \_ TRIGGEREVENT** dans son masque de contrôles-accepté dans un appel à [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Cela est généralement fait lorsque le service appelle **SetServiceStatus** avec **service \_ en cours d’exécution**. Le SCM émet ensuite une demande de **contrôle de service \_ \_ TRIGGEREVENT** pour chaque événement de déclencheur mis en file d’attente jusqu’à ce que la file d’attente soit vide.

Un service qui a des services dépendants en cours d’exécution ne peut pas être arrêté en réponse à un événement déclencheur.

Les demandes de démarrage et de déclenchement-arrêt ne sont pas garanties dans des conditions de mémoire insuffisante.

Utilisez la fonction [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) pour récupérer la configuration d’événement de déclencheur d’un service.

L’outil SC (sc.exe) peut être utilisé pour configurer ou interroger les événements de déclencheur d’un service à partir de l’invite de commandes. Utilisez l’option **triggerinfo** pour configurer le démarrage ou l’arrêt d’un service en réponse à un événement déclencheur. Utilisez l’option **qtriggerinfo** pour interroger la configuration du déclencheur d’un service.

L’exemple suivant interroge la configuration du déclencheur du service W32Time, qui est configuré pour démarrer lorsque l’ordinateur est joint à un domaine et s’arrête lorsque l’ordinateur quitte le domaine.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

L’exemple suivant interroge la configuration du déclencheur du service d’entrée de tablette, qui est configuré pour démarrer lorsqu’un périphérique HID avec le **GUID** {4d1e55b2-F16F-11CF-88cb-001111000030} et l’un des ID d’appareil HID spécifiés arrivent.

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
