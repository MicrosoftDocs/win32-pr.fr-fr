---
title: Utilisation du gestionnaire de redémarrage
description: Les sections suivantes décrivent l’utilisation de l’API du gestionnaire de redémarrage.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Restart Manager restart Mgr, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ac72edb9f2395bbd67236806c3ab3029372cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842610"
---
# <a name="using-restart-manager"></a>Utilisation du gestionnaire de redémarrage

Les sections suivantes décrivent l’utilisation de l’API du gestionnaire de redémarrage. Vos applications et services doivent également respecter les [instructions pour les applications et les services](guidelines-for-applications-and-services.md).

## <a name="using-the-microsoft-windows-installer"></a>Utilisation de l’Microsoft Windows Installer

Le [Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4,0 est le service d’installation de l’application de Windows Vista ou de windows Server 2008. Les applications qui utilisent la version 4,0 de Windows Installer pour l’installation et la maintenance utilisent automatiquement le gestionnaire de redémarrage pour réduire les redémarrages du système. Les programmes d’installation personnalisés peuvent également être conçus pour appeler l’API du gestionnaire de redémarrage pour arrêter et redémarrer les applications et les services directement afin d’éviter d’exiger un redémarrage du système. Dans les cas où un redémarrage du système est inévitable, les programmes d’installation peuvent utiliser la fonction [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) pour le planifier de manière à minimiser l’interruption de l’utilisateur. Les packages de Windows Installer interactifs doivent implémenter une interface utilisateur qui comprend une boîte de dialogue [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) . Pour plus d’informations, consultez [utilisation de Windows Installer avec le gestionnaire de redémarrage](/windows/desktop/Msi/using-windows-installer-with-restart-manager) dans la documentation du kit de développement logiciel (SDK) Windows Installer.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Utilisation de l’API du gestionnaire de redémarrage avec des programmes d’installation personnalisés

Les programmes d’installation personnalisés, ou un package Windows Installer qui contient des actions personnalisées entraînant un redémarrage du système, peuvent utiliser l’API du gestionnaire de redémarrage pour arrêter et redémarrer les applications et les services.

-   Toutes les opérations effectuées à l’aide de l’API du gestionnaire de redémarrage doivent être associées à une session. Un maximum de 64 sessions du gestionnaire de démarrage par session utilisateur peuvent être ouvertes simultanément sur le système. Le programme d’installation principal démarre et met fin à la session du gestionnaire de redémarrage. Pour plus d’informations sur l’utilisation du gestionnaire de redémarrage avec un seul programme d’installation, consultez [utilisation du gestionnaire de redémarrage avec un programme d’installation principal](using-restart-manager-with-a-primary-installer.md).
-   Si nécessaire pour l’installation, un ou plusieurs programmes d’installation secondaires peuvent être joints à la session du gestionnaire de redémarrage et peuvent être exécutés en mode in-process ou hors processus du programme d’installation principal. Les programmes d’installation secondaires requièrent que la clé de session soit fournie par le programme d’installation principal pour rejoindre une session. Pour plus d’informations et pour obtenir un exemple d’utilisation des programmes d’installation secondaires, consultez [utilisation du gestionnaire de redémarrage avec un programme d’installation secondaire](using-restart-manager-with-a-secondary-installer.md).
-   Les programmes d’installation interactifs doivent implémenter une interface utilisateur qui comprend une boîte de dialogue [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) qui peut demander aux utilisateurs de fermer les applications et les services. Pour plus d’informations, consultez [utilisation de Windows Installer avec le gestionnaire de redémarrage](/windows/desktop/Msi/using-windows-installer-with-restart-manager) dans la documentation du kit de développement logiciel (SDK) Windows Installer.
-   Les programmes d’installation peuvent appeler l’API du gestionnaire de redémarrage pour modifier, annuler et connaître l’état de l’opération du gestionnaire de redémarrage en cours. Pour plus d’informations, consultez les rubriques suivantes : [obtention de l’état d’une opération du gestionnaire de redémarrage](getting-the-status-of-a-restart-manager-operation.md) et [annulation de l’opération du gestionnaire de redémarrage en cours](canceling-the-current-restart-manager-operation.md).
-   Les programmes d’installation ne doivent pas désactiver la redirection du système de fichiers avant d’appeler l’API gestionnaire de redémarrage. Certains programmes d’installation 32 bits s’exécutent sur Windows 64 bits peuvent ne pas pouvoir inscrire un fichier dans le répertoire% windir% \\ system32.

 

 