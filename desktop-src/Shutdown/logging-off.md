---
description: La fonction ExitWindows déconnecte l’utilisateur actuel. Vous pouvez également appeler la fonction ExitWindowsEx avec l' \_ indicateur de fermeture de session EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Fermeture de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869233"
---
# <a name="logging-off"></a>Fermeture de session

La fonction [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) déconnecte l’utilisateur actuel. Vous pouvez également appeler la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) avec l' \_ indicateur de fermeture de session EXW.

Par défaut, lorsqu’une application utilise [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) pour se déconnecter, le système envoie le message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) à chaque fenêtre. Les applications s’engagent à se terminer en renvoyant la **valeur true** lorsqu’elles reçoivent ce message. Si une application retourne la **valeur false** lors du traitement de ce message, l’opération de fermeture de session est annulée. Si votre application gère le message **WM \_ QUERYENDSESSION** , vous pouvez autoriser l’utilisateur à annuler l’opération de fermeture de session, même si une autre application ou le système a émis la demande de session de fin. Pour obtenir un exemple, consultez [comment fermer la session de l’utilisateur actuel](how-to-log-off-the-current-user.md).

Quand une application retourne la **valeur true** pour [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), elle reçoit le message [**WM \_ ENDSESSION**](wm-endsession.md) et il se termine, quelle que soit la façon dont les autres applications répondent au message **WM \_ QUERYENDSESSION** .

Pour forcer l’arrêt de toutes les applications, utilisez [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)et spécifiez l' \_ indicateur de force EXW. Cela empêche le système d’envoyer des messages [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .

Le système envoie également le \_ \_ signal de contrôle d’événement Ctrl Logoff à chaque processus au cours d’une opération de fermeture de session. Une application console peut inscrire un [**HandlerRoutine**](/windows/console/handlerroutine) pour traiter ces messages.

Si le processus qui a appelé [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) s’exécute dans la session d’ouverture de session de l’utilisateur interactif, tous les processus de la session d’ouverture de session sont arrêtés. Si le processus appelant **ExitWindowsEx** se trouve dans une autre session de connexion, seules les notifications sont effectuées. aucun processus n’est terminé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment se déconnecter de l’utilisateur actuel](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
