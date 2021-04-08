---
title: Instructions pour les applications
description: Les applications qui s’exécutent sur Windows Vista et Windows Server 2008 doivent respecter ces instructions pour s’assurer que le gestionnaire de redémarrage peut arrêter et redémarrer les applications si nécessaire pour installer les mises à jour.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729628"
---
# <a name="guidelines-for-applications"></a>Instructions pour les applications

Les applications qui s’exécutent sur Windows Vista et Windows Server 2008 doivent respecter ces instructions pour s’assurer que le gestionnaire de redémarrage peut arrêter et redémarrer les applications si nécessaire pour installer les mises à jour. Les services peuvent utiliser les instructions décrites dans [instructions pour les services](guidelines-for-services.md).

-   Le gestionnaire de redémarrage interroge les applications GUI en envoyant une notification [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) dont le paramètre *lParam* est défini sur **ENDSESSION \_ CLOSEAPP** (0x1). Les applications ne doivent pas s’arrêter lorsqu’elles reçoivent un message **WM \_ QUERYENDSESSION** , car une autre application n’est peut-être pas prête à être arrêtée. Les applications GUI doivent écouter le message **WM \_ QUERYENDSESSION** et retourner la valeur **true** si l’arrêt et le redémarrage de l’application sont prêts. Si aucune application ne retourne la valeur **false**, le gestionnaire de redémarrage envoie un message [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) avec le paramètre *lParam* défini sur **ENDSESSION \_ CLOSEAPP** (0x1) et le paramètre *wParam* défini sur **true**. Les applications doivent s’arrêter uniquement lorsqu’elles reçoivent le message **WM \_ ENDSESSION** . Le gestionnaire de redémarrage envoie également un message [**WM \_ Close**](../winmsg/wm-close.md) pour les applications GUI qui ne s’arrêtent pas lors de la réception de **WM \_ ENDSESSION**. Si une application GUI répond à un message **WM \_ QUERYENDSESSION** en retournant la valeur **false**, l’arrêt est annulé. Toutefois, si l’arrêt est forcé, l’application est arrêtée, quel que soit le cas.
-   Quand une application GUI reçoit un message [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) , l’application doit se préparer à s’arrêter dans le délai imparti. Au minimum, les applications doivent se préparer en enregistrant les données utilisateur et les informations d’État nécessaires après un redémarrage. Il est recommandé que les applications enregistrent régulièrement les données et l’état utilisateur.
-   Le gestionnaire de redémarrage envoie une notification d' **\_ \_ événement Ctrl C** aux applications console qui doivent être arrêtées et redémarrées. Lorsqu’une application console reçoit une notification d' **\_ \_ événement Ctrl C** , l’application doit prendre les mesures nécessaires pour préparer un arrêt dans le délai imparti. Au minimum, les applications de console doivent définir une fonction [*HandlerRoutine*](/windows/console/handlerroutine) pour gérer la notification d' **\_ \_ événement Ctrl C** et doivent enregistrer toutes les données utilisateur et les informations d’État qui seront nécessaires après un redémarrage. Il est recommandé que les applications enregistrent régulièrement les données et l’état utilisateur.
-   Si des applications ne s’arrêtent pas en réponse aux messages d’arrêt, les programmes d’installation peuvent utiliser l’option **RmForceShutdown** de la fonction [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) pour forcer l’arrêt des applications. Quand le programme d’installation spécifie un arrêt forcé, le gestionnaire de redémarrage tente d’arrêter les applications correctement en envoyant les messages d’arrêt, mais les force à s’arrêter en cas d’échec. Les applications GUI et les applications de console peuvent être forcées à s’arrêter pour permettre l’installation d’une mise à jour de sécurité critique. Étant donné que cela peut entraîner une perte de données, les applications doivent gérer les messages d’arrêt et s’arrêter correctement quand cela est nécessaire.
-   Les applications doivent s’inscrire à un redémarrage à l’aide de la fonction [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) . Le gestionnaire de redémarrage peut redémarrer uniquement les applications qui ont été inscrites pour le redémarrage. Il s’agit de la seule façon dont le gestionnaire de redémarrage peut déterminer la commande de ligne de commande à utiliser lors du redémarrage de l’application. Si l’application doit être rouverte avec un état enregistré ou des données, ces informations doivent être incluses dans la commande de ligne de commande inscrite pour l’application.
    > [!Note]  
    > Si l’application redémarrée doit s’exécuter dans le même répertoire que celui dans lequel elle a été exécutée avant d’être arrêtée, l’application doit enregistrer les informations de répertoire, puis passer au répertoire après le redémarrage.

     

    > [!Note]  
    > La fonction [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) ne redémarre pas les applications qui ne s’exécutent pas en tant qu’utilisateur actuellement connecté. Par exemple, la fonction **RmRestart** ne redémarre pas les applications démarrées avec la commande **exécuter en tant** que qui ne s’exécutent pas en tant qu’utilisateur actuellement connecté. Ces applications doivent être redémarrées manuellement.

     

-   Lorsque le gestionnaire de redémarrage détermine qu’un redémarrage du système est nécessaire pour installer une mise à jour, il n’arrête pas les applications et les services. Au lieu de cela, il permet au programme d’installation de décider quand planifier un redémarrage du système et installer la mise à jour. Les programmes d’installation peuvent réduire l’interruption aux utilisateurs provoqués par des mises à jour nécessitant un redémarrage du système à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) avec l’indicateur **EWX \_ RESTARTAPPS** ou la fonction [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) avec l’indicateur **Shutdown \_ RESTARTAPPS** . L’utilisation de ces indicateurs permet de s’assurer que les applications inscrites pour le redémarrage sont redémarrées après un redémarrage du système, ce qui réduit l’impact sur l’utilisateur.

 

 