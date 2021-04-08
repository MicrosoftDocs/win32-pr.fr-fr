---
title: Réponse aux clics de souris
description: Réponse aux clics de souris
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101620"
---
# <a name="responding-to-mouse-clicks"></a>Réponse aux clics de souris

Si l’utilisateur clique sur un bouton de la souris alors que le curseur se trouve sur la zone cliente d’une fenêtre, la fenêtre reçoit l’un des messages suivants.



| Message                                        | Signification                   |
|------------------------------------------------|---------------------------|
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Bouton gauche enfoncé          |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)     | Bouton gauche vers le haut            |
| [**\_MBUTTONDOWN WM**](/windows/desktop/inputdev/wm-mbuttondown) | Bouton central enfoncé        |
| [**\_MBUTTONUP WM**](/windows/desktop/inputdev/wm-mbuttonup)     | Bouton central vers le haut          |
| [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown) | Bouton droit enfoncé         |
| [**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)     | Bouton droit vers le haut           |
| [**\_XBUTTONDOWN WM**](/windows/desktop/inputdev/wm-xbuttondown) | LE bouton XButton1 ou XBUTTON2 |
| [**\_XBUTTONUP WM**](/windows/desktop/inputdev/wm-xbuttonup)     | LE bouton XButton1 ou XBUTTON2   |



 

Souvenez-vous que la zone cliente est la partie de la fenêtre qui exclut le frame. Pour plus d’informations sur les zones clientes, consultez [qu’est-ce qu’une fenêtre ?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordonnées de la souris

Dans tous ces messages, le paramètre *lParam* contient les coordonnées x et y du pointeur de la souris. Les 16 bits les plus bas de *lParam* contiennent la coordonnée x, et les 16 bits suivants contiennent la coordonnée y. Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour décompresser les coordonnées de *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Ces macros sont définies dans le fichier d’en-tête WindowsX. h.

Sur Windows 64 bits, *lParam* est une valeur de 64 bits. Les 32 bits supérieurs de *lParam* ne sont pas utilisés. La documentation MSDN mentionne le « mot de poids faible » et le « mot de poids fort » de *lParam*. Dans le cas 64 bits, cela signifie que les mots de poids fort et de poids fort des 32 bits inférieurs. Les macros extraient les valeurs correctes. par conséquent, si vous les utilisez, vous en êtes sûr.

Les coordonnées de la souris sont exprimées en pixels, et non en pixels indépendants du périphérique (DIP). elles sont mesurées par rapport à la zone cliente de la fenêtre. Les coordonnées sont des valeurs signées. Les positions au-dessus et à gauche de la zone cliente ont des coordonnées négatives, ce qui est important si vous effectuez le suivi de la position de la souris en dehors de la fenêtre. Nous verrons comment le faire dans une rubrique ultérieure, en [capturant le mouvement de la souris en dehors de la fenêtre](mouse-movement.md).

### <a name="additional-flags"></a>Indicateurs supplémentaires

Le paramètre *wParam* contient une opération or au niveau du bit, indiquant l’état des autres **boutons de la** souris plus les touches Maj et Ctrl.



| Indicateur             | Signification                          |
|------------------|----------------------------------|
| **\_contrôle MK**  | La touche CTRL est enfoncée.            |
| **\_LBUTTON MK**  | Le bouton gauche de la souris est enfoncé.   |
| **\_MBUTTON MK**  | Le bouton central de la souris est enfoncé. |
| **\_RBUTTON MK**  | Le bouton droit de la souris est enfoncé.  |
| **\_MAJ MK**    | La touche Maj est enfoncée.           |
| **\_Le bouton XButton1 MK** | Le bouton le bouton XButton1 est enfoncé.     |
| **\_XButton2 MK** | Le bouton XBUTTON2 est enfoncé.     |



 

L’absence d’un indicateur signifie que le bouton ou la touche correspondant n’a pas été enfoncé. Par exemple, pour tester si la touche CTRL est enfoncée :


```C++
if (wParam & MK_CONTROL) { ...
```



Si vous devez Rechercher l’état d’autres clés en plus de CTRL et Maj, utilisez la fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , qui est décrite dans [entrée au clavier](keyboard-input.md).

Les messages de fenêtre [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) et [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) s’appliquent à le bouton XButton1 et XButton2. Le paramètre *wParam* indique le bouton sur lequel l’utilisateur a cliqué.


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>Double-clic

Une fenêtre ne reçoit pas de notifications de double-clic par défaut. Pour recevoir des doubles clics, définissez l’indicateur **cs \_ DBLCLKS** dans la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) lorsque vous inscrivez la classe de fenêtre.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Si vous définissez l’indicateur **cs \_ DBLCLKS** comme indiqué, la fenêtre recevra des notifications de double-clic. Un double-clic est indiqué par un message de fenêtre avec « DBLCLK » dans le nom. Par exemple, un double-clic sur le bouton gauche de la souris produit la séquence de messages suivante :

<dl>

[**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)  
[**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)  
[**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

En effet, le deuxième message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) qui devrait normalement être généré devient un message [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) . Des messages équivalents sont définis pour les boutons droit, moyen et XBUTTON.

Tant que vous n’avez pas obtenu le message de double-clic, il n’existe aucun moyen de savoir que le premier clic de souris est le début d’un double-clic. Par conséquent, une action de double-clic doit continuer une action qui commence par le premier clic de souris. Par exemple, dans le shell Windows, un seul clic sélectionne un dossier, tandis qu’un double-clic ouvre le dossier.

## <a name="non-client-mouse-messages"></a>Messages de souris non-client

Un ensemble distinct de messages est défini pour les événements de souris qui se produisent dans la zone non cliente de la fenêtre. Ces messages contiennent les lettres « NC » dans le nom. Par exemple, le [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) est l’équivalent non-client de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Une application classique n’intercepte pas ces messages, car la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gère ces messages correctement. Toutefois, elles peuvent être utiles pour certaines fonctions avancées. Par exemple, vous pouvez utiliser ces messages pour implémenter un comportement personnalisé dans la barre de titre. Si vous gérez ces messages, vous devez généralement les transmettre à **DefWindowProc** par la suite. Dans le cas contraire, votre application interrompt les fonctionnalités standard telles que le glisser-déplacer ou la minimisation de la fenêtre.

## <a name="next"></a>Suivant

[Mouvement de la souris](mouse-movement.md)

 

 