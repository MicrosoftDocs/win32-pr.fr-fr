---
title: Peindre la fenêtre
description: Vous avez créé votre fenêtre. À présent, vous voulez afficher un contenu à l’intérieur de celui-ci. Dans la terminologie Windows, c’est ce que l’on appelle peindre la fenêtre. Pour mélanger des métaphores, une fenêtre est une zone de dessin vide, en attendant que vous la complétiez.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104552403"
---
# <a name="painting-the-window"></a>Peindre la fenêtre

Vous avez créé votre fenêtre. À présent, vous voulez afficher un contenu à l’intérieur de celui-ci. Dans la terminologie Windows, c’est ce que l’on appelle peindre la fenêtre. Pour mélanger des métaphores, une fenêtre est une zone de dessin vide, en attendant que vous la complétiez.

Parfois, votre programme lance la peinture pour mettre à jour l’apparence de la fenêtre. À d’autres moments, le système d’exploitation vous informera que vous devez redessiner une partie de la fenêtre. Dans ce cas, le système d’exploitation envoie un message [**de \_ peinture WM**](/windows/desktop/gdi/wm-paint) à la fenêtre. La partie de la fenêtre qui doit être peinte est appelée *zone de mise à jour*.

La première fois qu’une fenêtre est affichée, la totalité de la zone cliente de la fenêtre doit être peinte. Par conséquent, vous recevrez toujours au moins un message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) lorsque vous affichez une fenêtre.

![Illustration montrant la région de mise à jour d’une fenêtre](images/painting01.png)

Vous êtes uniquement responsable de la peinture de la zone cliente. Le frame environnant, y compris la barre de titre, est automatiquement peint par le système d’exploitation. Une fois que vous avez fini de peindre la zone client, vous désactivez la zone de mise à jour, ce qui indique au système d’exploitation qu’elle n’a pas besoin d’envoyer un autre message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) tant qu’un changement n’est pas effectué.

Supposons à présent que l’utilisateur déplace une autre fenêtre afin qu’elle masque une partie de votre fenêtre. Lorsque la partie masquée redevient visible, cette partie est ajoutée à la région de mise à jour et votre fenêtre reçoit un autre message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .

![Illustration montrant comment la région de mise à jour change lorsque deux fenêtres se chevauchent](images/painting02.png)

La région de mise à jour change également si l’utilisateur étire la fenêtre. Dans le diagramme suivant, l’utilisateur étire la fenêtre à droite. La zone récemment exposée sur le côté droit de la fenêtre est ajoutée à la zone de mise à jour :

![Illustration montrant comment la région de mise à jour change lorsqu’une fenêtre est redimensionnée](images/painting03.png)

Dans notre premier exemple de programme, la routine de peinture est très simple. Elle remplit simplement la zone cliente entière avec une couleur unie. Toutefois, cet exemple suffit pour illustrer certains des concepts importants.

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

Démarrez l’opération de peinture en appelant la fonction [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) . Cette fonction remplit la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) avec des informations sur la demande Repaint. La région de mise à jour actuelle est donnée dans le membre **rcPaint** de **PAINTSTRUCT,**. Cette région de mise à jour est définie par rapport à la zone cliente :

![Illustration montrant l’origine de la zone cliente](images/painting04.png)

Dans votre code de peinture, vous disposez de deux options de base :

- Peignez toute la zone cliente, quelle que soit la taille de la région de mise à jour. Tout ce qui se trouve en dehors de la région de mise à jour est coupé. Autrement dit, le système d’exploitation l’ignore.
- Optimisez en peignant uniquement la partie de la fenêtre à l’intérieur de la région de mise à jour.

Si vous peignez toujours la totalité de la zone cliente, le code sera plus simple. Toutefois, si vous avez une logique de peinture compliquée, il peut être plus efficace d’ignorer les zones en dehors de la région de mise à jour.

La ligne de code suivante remplit la zone de mise à jour avec une couleur unique, à l’aide de la couleur d’arrière-plan de la fenêtre définie par le système (**\_ fenêtre de couleur**). La couleur réelle indiquée par **la \_ fenêtre couleur** dépend du modèle de couleurs actuel de l’utilisateur.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Les détails des [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) ne sont pas importants pour cet exemple, mais le deuxième paramètre donne les coordonnées du rectangle à remplir. Dans ce cas, nous transmettons l’intégralité de la région de mise à jour (le membre **rcPaint** de [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Sur le premier message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , toute la zone cliente doit être peinte, de sorte que **rcPaint** contiendra la totalité de la zone cliente. Pour les messages de **\_ peinture WM** suivants, **rcPaint** peut contenir un rectangle plus petit.

La fonction [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) fait partie du Graphics Device Interface (GDI), qui dispose de graphiques Windows alimentés pendant beaucoup de temps. Dans Windows 7, Microsoft a introduit un nouveau moteur graphique, nommé Direct2D, qui prend en charge les opérations graphiques hautes performances, telles que l’accélération matérielle. Direct2D est également disponible pour Windows Vista via la [mise à jour de plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) et pour windows Server 2008 via la mise à jour de plateforme pour windows Server 2008. (GDI est toujours entièrement pris en charge.)

Une fois que vous avez fini de peindre, appelez la fonction [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) . Cette fonction efface la zone de mise à jour, qui signale à Windows que la fenêtre a fini de se peindre.

## <a name="next"></a>Suivant

[Fermeture de la fenêtre](closing-the-window.md)