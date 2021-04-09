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
# <a name="logging-off"></a><span data-ttu-id="6bc2d-104">Fermeture de session</span><span class="sxs-lookup"><span data-stu-id="6bc2d-104">Logging Off</span></span>

<span data-ttu-id="6bc2d-105">La fonction [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) déconnecte l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="6bc2d-106">Vous pouvez également appeler la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) avec l' \_ indicateur de fermeture de session EXW.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="6bc2d-107">Par défaut, lorsqu’une application utilise [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) pour se déconnecter, le système envoie le message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) à chaque fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="6bc2d-108">Les applications s’engagent à se terminer en renvoyant la **valeur true** lorsqu’elles reçoivent ce message.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="6bc2d-109">Si une application retourne la **valeur false** lors du traitement de ce message, l’opération de fermeture de session est annulée.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="6bc2d-110">Si votre application gère le message **WM \_ QUERYENDSESSION** , vous pouvez autoriser l’utilisateur à annuler l’opération de fermeture de session, même si une autre application ou le système a émis la demande de session de fin.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="6bc2d-111">Pour obtenir un exemple, consultez [comment fermer la session de l’utilisateur actuel](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="6bc2d-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="6bc2d-112">Quand une application retourne la **valeur true** pour [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), elle reçoit le message [**WM \_ ENDSESSION**](wm-endsession.md) et il se termine, quelle que soit la façon dont les autres applications répondent au message **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="6bc2d-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="6bc2d-113">Pour forcer l’arrêt de toutes les applications, utilisez [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)et spécifiez l' \_ indicateur de force EXW.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="6bc2d-114">Cela empêche le système d’envoyer des messages [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc2d-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="6bc2d-115">Le système envoie également le \_ \_ signal de contrôle d’événement Ctrl Logoff à chaque processus au cours d’une opération de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="6bc2d-116">Une application console peut inscrire un [**HandlerRoutine**](/windows/console/handlerroutine) pour traiter ces messages.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="6bc2d-117">Si le processus qui a appelé [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) s’exécute dans la session d’ouverture de session de l’utilisateur interactif, tous les processus de la session d’ouverture de session sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="6bc2d-118">Si le processus appelant **ExitWindowsEx** se trouve dans une autre session de connexion, seules les notifications sont effectuées. aucun processus n’est terminé.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc2d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6bc2d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc2d-120">Comment se déconnecter de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="6bc2d-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
