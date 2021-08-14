---
description: la configuration des services permet à l’Windows Installer de personnaliser les services sur un ordinateur.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Utilisation de la configuration des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe1e34cce317ee00c3cc9d6ee4aac449e500499dc2dee4e97df65ba91bca2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012703"
---
# <a name="using-services-configuration"></a>Utilisation de la configuration des services

la configuration des services permet à l’Windows Installer de personnaliser les [services](../services/services.md) sur un ordinateur. les développeurs peuvent créer un package Windows Installer pour installer, arrêter, démarrer et supprimer des services pendant une installation à l’aide des tables [ServiceControl](servicecontrol-table.md) et [ServiceInstall](serviceinstall-table.md) , ainsi que des actions [InstallServices](installservices-action.md), [StopServices](stopservices-action.md) et [DeleteServices](deleteservices-action.md) .

à compter des packages écrits pour Windows Installer 5,0, les développeurs peuvent également utiliser l’action standard [MsiConfigureServices](msiconfigureservices-action.md) et la [table MsiServiceConfig](msiserviceconfig-table.md) pour configurer les options de personnalisation de service étendues disponibles avec Windows 7 et Windows server 2008 R2 et Windows Vista et Windows server 2008. les packages d’installation existants écrits pour les versions du Windows Installer qui n’incluent pas la table MsiServiceConfig peuvent être toujours installés à l’aide de Windows Installer 5,0. la fonctionnalité de configuration des services de la Windows Installer ne peut pas configurer les comptes de service réseau, installer les processus d’hôte de service partagé (svchost) ou redémarrer les services arrêtés dans le cadre de l’installation.

**Windows XP et Windows Server 2003 ou version antérieure :** Non pris en charge. les tables de configuration de service et les actions standard sont disponibles à partir de Windows Installer 5,0 s’exécutant sur Windows 7 et Windows server 2008 R2 et Windows Installer 4,5 s’exécutant sur Windows Vista et Windows server 2008.

Vous devez inclure l’action [MsiConfigureServices](msiconfigureservices-action.md) dans la table [InstallExecuteSequence](installexecutesequence-table.md) pour demander les configurations de service que vous spécifiez dans la [table MsiServiceConfig](msiserviceconfig-table.md). l’Windows Installer utilise les informations de la table MsiServiceConfig uniquement lorsque l’action standard MsiConfigureServices est incluse dans une table de séquences. L’action standard MsiConfigureServices utilise également des informations dans les tables [ServiceControl](servicecontrol-table.md) et [ServiceInstall](serviceinstall-table.md) .

Pour demander que le système accorde uniquement des privilèges requis à un service particulier, spécifiez le service et l’option de configuration **\_ \_ \_ \_ informations sur les privilèges requis** de la configuration du service dans la [table MsiServiceConfig](msiserviceconfig-table.md). Supprimez les privilèges inutiles du jeton de processus du service. Cette option peut être utilisée pour configurer les services exécutés dans le contexte de sécurité des comptes d’utilisateur du [service](../services/service-user-accounts.md)LocalSystem, LocalService ou NetworkService.

Pour demander au système de retarder le démarrage automatique d’un service à un moment donné après le démarrage de tous les autres services de démarrage automatique, spécifiez le service et l’option de **\_ \_ \_ \_ démarrage automatique différé** de la configuration du service dans la [table MsiServiceConfig](msiserviceconfig-table.md). Le service en cours de retardement doit être installé par le package en cours avec le \_ démarrage automatique du service \_ spécifié dans la table [ServiceInstall](serviceinstall-table.md) ou le service doit déjà être installé en tant que service à démarrage automatique.

Pour demander que le système réserve une ressource pour l’utilisation exclusive d’un service particulier, spécifiez le service, le type de SID de service et l’option de configuration service **\_ \_ \_ sid service \_ sid** dans la [table MsiServiceConfig](msiserviceconfig-table.md). Ajoutez le SID du service à la liste de Access Control (ACL) de la ressource pour la ressource.

Pour demander que le [Gestionnaire de contrôle des services](../services/service-control-manager.md) (SCM) attende après l’envoi de la notification de **\_ \_ préfermeture du contrôle de service** à un service, procédez comme suit. Spécifiez le service, la durée d’attente du SCM et l’option de **configuration \_ \_ \_ informations de préarrêt** de la configuration du service dans la [table MsiServiceConfig](msiserviceconfig-table.md).

Pour configurer le moment où le système doit exécuter des actions après la défaillance d’un service, spécifiez l’option de service et l' **\_ \_ \_ \_ indicateur actions d’échec** de la configuration du service dans la [table MsiServiceConfig](msiserviceconfig-table.md). Ajoutez les actions à exécuter dans la [table MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

pour plus d’informations sur les fonctionnalités de personnalisation de service étendues introduites avec les systèmes d’exploitation Windows vista et Windows Server 2008, consultez [modifications de service pour Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
