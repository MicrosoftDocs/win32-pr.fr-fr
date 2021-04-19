---
description: La Windows Installer peut déterminer à quel moment un redémarrage du système est nécessaire et invite automatiquement l’utilisateur à redémarrer à la fin de l’installation.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Redémarrages du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529706"
---
# <a name="system-reboots"></a>Redémarrages du système

La Windows Installer peut déterminer à quel moment un redémarrage du système est nécessaire et invite automatiquement l’utilisateur à redémarrer à la fin de l’installation. Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers en cours d’utilisation pendant l’installation.

Les applications qui utilisent [Windows Installer](windows-installer-portal.md) version 4,0 ou ultérieure pour l’installation et la maintenance utilisent automatiquement le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pour réduire les redémarrages du système. Windows Installer version 4,0 ou ultérieure possède des propriétés et des stratégies qui permettent à l’auteur du package et aux administrateurs de contrôler l’interaction des Windows Installer avec le gestionnaire de redémarrage. Pour plus d’informations, consultez [utilisation de Windows Installer avec le gestionnaire de redémarrage](using-windows-installer-with-restart-manager.md).

Les auteurs du package d’installation peuvent planifier et supprimer les redémarrages à l’aide d’actions standard dans les tables de séquences et en définissant des propriétés. Les actions et les propriétés suivantes sont utilisées pour gérer les redémarrages du système.



| Action, boîte de dialogue ou propriété                                                | Brève description                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Action ForceReboot](forcereboot-action.md)                                   | Invite l’utilisateur à redémarrer pendant l’installation.                                                                                                        |
| [Action ScheduleReboot](schedulereboot-action.md)                             | Invite l’utilisateur à redémarrer à la fin de l’installation.                                                                                                 |
| [**Reboot, propriété**](reboot.md)                                              | Force ou supprime certaines invites automatiques pour un redémarrage du système.                                                                                           |
| [**Propriété REBOOTPROMPT**](rebootprompt.md)                                  | Supprime l’affichage des invites pour les redémarrages de l’utilisateur. Tous les redémarrages nécessaires se produisent automatiquement.                                                           |
| [**Propriété AFTERREBOOT**](afterreboot.md)                                    | Couramment utilisé dans une condition imposée sur l’action ForceReboot.                                                                                               |
| [Action InstallValidate](installvalidate-action.md)                           | Affiche la boîte de dialogue FilesInUse, si nécessaire, donnant aux utilisateurs la possibilité d’arrêter des processus et d’éviter certains redémarrages du système.                              |
| [Boîte de dialogue FilesInUse](filesinuse-dialog.md)                                     | Donne aux utilisateurs la possibilité d’arrêter des processus pour éviter certains redémarrages du système.                                                                              |
| [Boîte de dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Donne aux utilisateurs la possibilité d’utiliser le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pour fermer et redémarrer les applications. Disponible à partir de Windows Installer version 4,0. |
| [**Propriété ReplacedInUseFiles**](replacedinusefiles.md)                      | Défini si le programme d’installation s’installe sur un fichier en cours d’utilisation. Cette propriété est utilisée par les actions personnalisées pour détecter qu’un redémarrage est nécessaire.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Propriété permettant de désactiver l’interaction Windows Installer avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md). Disponible à partir de Windows Installer version 4,0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Spécifie la façon dont le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) se ferme et redémarre les applications. Disponible à partir de Windows Installer version 4,0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Spécifie la façon dont le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) se ferme et redémarre les applications. Disponible à partir de Windows Installer version 4,0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | Le programme d’installation définit cette propriété si le redémarrage du système d’exploitation est en attente. Disponible à partir de Windows Installer version 4,0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Stratégie de désactivation de l’interaction Windows Installer avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md). Disponible à partir de Windows Installer version 4,0.                |



 

ERREUR d' \_ installation \_ suspendre signifie que l’installation ne s’est pas terminée ou n’a pas été restaurée. L’installation doit reprendre avant qu’elle soit terminée. Le système devra peut-être être redémarré pour que l’installation puisse reprendre.

Le Windows Installer retourne le code d’erreur erreur d’installation de l' \_ \_ interruption lors de l’exécution de l' [action ForceReboot](forcereboot-action.md) . Elle retourne \_ l’erreur \_ redémarrage de \_ la réussite obligatoire si un redémarrage est nécessaire avant l’exécution de l’application, et retourne une erreur de redémarrage \_ de la réussite \_ \_ lancée si le programme d’installation a démarré un redémarrage. Notez que dans la mesure où les redémarrages sont asynchrones, le redémarrage peut réellement se produire avant le renvoi du code d’erreur. Pour plus d’informations, consultez [codes d’erreur](error-codes.md).

Les actions personnalisées peuvent forcer une demande de redémarrage à la fin d’une installation en appelant [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). Les actions personnalisées peuvent également rechercher une invite de redémarrage en attente en appelant [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode).

## <a name="filesinuse-dialog"></a>Boîte de dialogue FilesInUse

Le programme d’installation peut déterminer quand un redémarrage du système est nécessaire et demander à l’utilisateur une demande de redémarrage. En règle générale, un redémarrage du système est nécessaire car le programme d’installation tente d’installer un fichier en cours d’utilisation. Si l' [action InstallValidate](installvalidate-action.md) détecte l’installation d’un fichier en cours d’utilisation, elle affiche la [boîte de dialogue FilesInUse](filesinuse-dialog.md).

Si vous vous attendez à ce que le programme d’installation affiche un FilesInUseDialog, mais ce n’est pas le cas, cela peut être dû à l’une des raisons suivantes :

-   Les fichiers en cours d’utilisation ne sont pas des exécutables.
-   Le programme d’installation n’essaie pas d’installer ces fichiers.
-   Le processus qui contient ces fichiers est le processus appelant l’installation.
-   Le processus contenant ces fichiers est un processus qui n’a pas de fenêtre associée à un titre.

Pour plus d’informations, consultez [journalisation des demandes de redémarrage](logging-of-reboot-requests.md).

 

 
