---
title: Fermeture de la fenêtre
description: Lorsque l’utilisateur ferme une fenêtre, cette action déclenche une séquence de messages de fenêtre.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaf6922f730e63fa9ab38a8f6baa9009dabf77b2ffeddc2117dcd09ffc08a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328783"
---
# <a name="closing-the-window"></a>Fermeture de la fenêtre

Lorsque l’utilisateur ferme une fenêtre, cette action déclenche une séquence de messages de fenêtre.

L’utilisateur peut fermer une fenêtre d’application en cliquant sur le bouton **Fermer** ou à l’aide d’un raccourci clavier tel que ALT + F4. L’une de ces actions amène la fenêtre à recevoir un message de [**\_ fermeture WM**](/windows/desktop/winmsg/wm-close) . Le message **WM \_ Close** vous donne la possibilité d’inviter l’utilisateur avant de fermer la fenêtre. Si vous voulez vraiment fermer la fenêtre, appelez la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Sinon, il suffit de retourner zéro à partir du message de **\_ fermeture WM** , et le système d’exploitation ignore le message et ne détruit pas la fenêtre.

Voici un exemple de la façon dont un programme peut gérer la [**\_ fermeture de WM**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

Dans cet exemple, la fonction [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) affiche une boîte de dialogue modale qui contient les boutons **OK** et **Annuler** . Si l’utilisateur clique sur **OK**, le programme appelle [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow). Sinon, si l’utilisateur clique sur **Annuler**, l’appel à **DestroyWindow** est ignoré et la fenêtre reste ouverte. Dans les deux cas, retournez zéro pour indiquer que vous avez géré le message.

Si vous souhaitez fermer la fenêtre sans inviter l’utilisateur, vous pouvez simplement appeler [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sans l’appel de [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). Toutefois, il existe un raccourci dans ce cas. Rappelez-vous que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) exécute l’action par défaut pour tous les messages de fenêtre. Dans le cas de [**la \_ fermeture de WM**](/windows/desktop/winmsg/wm-close), **DefWindowProc** appelle automatiquement **DestroyWindow**. Cela signifie que si vous ignorez le message **WM \_ Close** dans votre instruction **switch** , la fenêtre est détruite par défaut.

Quand une fenêtre est sur le lieu d’être détruite, elle reçoit un message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . Ce message est envoyé après la suppression de la fenêtre de l’écran, mais avant la destruction (en particulier, avant la destruction des fenêtres enfants).

Dans la fenêtre principale de votre application, vous répondez généralement à [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) en appelant [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Nous avons vu dans la section des [messages de fenêtre](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) place un message de [**\_ fermeture WM**](/windows/desktop/winmsg/wm-quit) dans la file d’attente de messages, provoquant la fin de la boucle de message.

Voici un organigramme qui montre comment traiter les messages de type [**WM \_**](/windows/desktop/winmsg/wm-close) et de [**\_ destruction**](/windows/desktop/winmsg/wm-destroy) WM :

![Organigramme illustrant comment gérer \- les messages de destruction WM et WM \-](images/wmclose01.png)

## <a name="next"></a>Suivant

[Gestion de l’état de l’application](managing-application-state-.md)