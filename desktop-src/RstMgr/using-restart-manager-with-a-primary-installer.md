---
title: Utilisation du gestionnaire de redémarrage avec un programme d’installation principal
description: La procédure suivante décrit comment utiliser le gestionnaire de redémarrage pour arrêter et redémarrer des applications et des services. Lorsque vous utilisez le gestionnaire de redémarrage avec un seul programme d’installation, ce programme d’installation est également le programme d’installation principal qui contrôle l’interface utilisateur.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38956ee8d04bc377809e93579080d9b767c3da3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939790"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Utilisation du gestionnaire de redémarrage avec un programme d’installation principal

La procédure suivante décrit comment utiliser le gestionnaire de redémarrage pour arrêter et redémarrer des applications et des services. Lorsque vous utilisez le gestionnaire de redémarrage avec un seul programme d’installation, ce programme d’installation est également le programme d’installation principal qui contrôle l’interface utilisateur.

**Pour utiliser le gestionnaire de redémarrage avec un programme d’installation principal**

1.  Le programme d’installation appelle la fonction [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) pour démarrer la session du gestionnaire de redémarrage et obtenir un handle de session et une clé.
2.  Le programme d’installation appelle la fonction [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) pour inscrire des ressources. Le gestionnaire de redémarrage peut uniquement utiliser des ressources inscrites pour déterminer les applications et les services qui doivent être arrêtés et redémarrés. Toutes les ressources qui peuvent être affectées par l’installation doivent être inscrites dans la session. Les ressources peuvent être identifiées par un nom de fichier, un nom abrégé de service ou une structure de [**\_ \_ processus unique RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .
3.  Le programme d’installation appelle la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) pour obtenir un tableau des structures d' [**\_ \_ informations de processus RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) qui répertorient toutes les applications et tous les services qui doivent être arrêtés et redémarrés.

    Si la valeur du paramètre *lpdwRebootReason* retourné par la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) est différente de zéro, le gestionnaire de redémarrage ne peut pas libérer une ressource inscrite par l’arrêt d’une application ou d’un service. Dans ce cas, un arrêt et un redémarrage du système sont requis pour poursuivre l’installation. Le programme d’installation doit inviter l’utilisateur à entrer une action, arrêter des programmes ou des services, ou planifier un arrêt et un redémarrage du système.

    Si la valeur du paramètre *lpdwRebootReason* retourné par la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) est égale à zéro, le programme d’installation doit appeler la fonction [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) . Cela arrête les services et les applications qui utilisent des ressources inscrites. Le programme d’installation doit ensuite effectuer les modifications système requises pour terminer l’installation. Enfin, le programme d’installation doit appeler la fonction [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) afin que le gestionnaire de redémarrage puisse redémarrer les applications qu’il a arrêtées et qui ont été inscrites pour un redémarrage.

4.  Le programme d’installation peut utiliser la fonction [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) pour empêcher l’arrêt ou le redémarrage des applications et des services spécifiés par les opérations du gestionnaire de redémarrage. La fonction [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) retourne une liste des applications et des services à filtrer de l’arrêt et du redémarrage. La fonction [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) supprime un filtre.
5.  Le programme d’installation appelle la fonction [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) pour fermer la session du gestionnaire de redémarrage.

Pour obtenir un exemple d’extrait de code qui illustre le démarrage et l’utilisation d’une session du gestionnaire de redémarrage à l’aide d’un programme d’installation principal, puis l’Association d’un programme d’installation secondaire à la session existante, consultez [utilisation du gestionnaire de redémarrage avec un programme d’installation secondaire](using-restart-manager-with-a-secondary-installer.md).

 

 




