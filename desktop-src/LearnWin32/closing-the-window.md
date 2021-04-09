---
title: Fermeture de la fenêtre
description: Lorsque l’utilisateur ferme une fenêtre, cette action déclenche une séquence de messages de fenêtre.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842305"
---
# <a name="closing-the-window"></a><span data-ttu-id="d7dc2-103">Fermeture de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="d7dc2-103">Closing the Window</span></span>

<span data-ttu-id="d7dc2-104">Lorsque l’utilisateur ferme une fenêtre, cette action déclenche une séquence de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="d7dc2-105">L’utilisateur peut fermer une fenêtre d’application en cliquant sur le bouton **Fermer** ou à l’aide d’un raccourci clavier tel que ALT + F4.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="d7dc2-106">L’une de ces actions amène la fenêtre à recevoir un message de [**\_ fermeture WM**](/windows/desktop/winmsg/wm-close) .</span><span class="sxs-lookup"><span data-stu-id="d7dc2-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="d7dc2-107">Le message **WM \_ Close** vous donne la possibilité d’inviter l’utilisateur avant de fermer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="d7dc2-108">Si vous voulez vraiment fermer la fenêtre, appelez la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="d7dc2-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="d7dc2-109">Sinon, il suffit de retourner zéro à partir du message de **\_ fermeture WM** , et le système d’exploitation ignore le message et ne détruit pas la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="d7dc2-110">Voici un exemple de la façon dont un programme peut gérer la [**\_ fermeture de WM**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="d7dc2-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="d7dc2-111">Dans cet exemple, la fonction [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) affiche une boîte de dialogue modale qui contient les boutons **OK** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="d7dc2-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="d7dc2-112">Si l’utilisateur clique sur **OK**, le programme appelle [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span><span class="sxs-lookup"><span data-stu-id="d7dc2-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="d7dc2-113">Sinon, si l’utilisateur clique sur **Annuler**, l’appel à **DestroyWindow** est ignoré et la fenêtre reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="d7dc2-114">Dans les deux cas, retournez zéro pour indiquer que vous avez géré le message.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="d7dc2-115">Si vous souhaitez fermer la fenêtre sans inviter l’utilisateur, vous pouvez simplement appeler [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sans l’appel de [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span><span class="sxs-lookup"><span data-stu-id="d7dc2-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="d7dc2-116">Toutefois, il existe un raccourci dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="d7dc2-117">Rappelez-vous que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) exécute l’action par défaut pour tous les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="d7dc2-118">Dans le cas de [**la \_ fermeture de WM**](/windows/desktop/winmsg/wm-close), **DefWindowProc** appelle automatiquement **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="d7dc2-119">Cela signifie que si vous ignorez le message **WM \_ Close** dans votre instruction **switch** , la fenêtre est détruite par défaut.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="d7dc2-120">Quand une fenêtre est sur le lieu d’être détruite, elle reçoit un message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="d7dc2-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="d7dc2-121">Ce message est envoyé après la suppression de la fenêtre de l’écran, mais avant la destruction (en particulier, avant la destruction des fenêtres enfants).</span><span class="sxs-lookup"><span data-stu-id="d7dc2-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="d7dc2-122">Dans la fenêtre principale de votre application, vous répondez généralement à [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) en appelant [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="d7dc2-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="d7dc2-123">Nous avons vu dans la section des [messages de fenêtre](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) place un message de [**\_ fermeture WM**](/windows/desktop/winmsg/wm-quit) dans la file d’attente de messages, provoquant la fin de la boucle de message.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="d7dc2-124">Voici un organigramme qui montre comment traiter les messages de type [**WM \_**](/windows/desktop/winmsg/wm-close) et de [**\_ destruction**](/windows/desktop/winmsg/wm-destroy) WM :</span><span class="sxs-lookup"><span data-stu-id="d7dc2-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![Organigramme illustrant comment gérer \- les messages de destruction WM et WM \-](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="d7dc2-126">Suivant</span><span class="sxs-lookup"><span data-stu-id="d7dc2-126">Next</span></span>

[<span data-ttu-id="d7dc2-127">Gestion de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="d7dc2-127">Managing Application State</span></span>](managing-application-state-.md)