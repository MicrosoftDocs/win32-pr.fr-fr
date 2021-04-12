---
title: Définition de l’image de curseur
description: Définition de l’image de curseur
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463034"
---
# <a name="setting-the-cursor-image"></a>Définition de l’image de curseur

Le *curseur* est la petite image qui indique l’emplacement de la souris ou d’un autre dispositif de pointage. De nombreuses applications modifient l’image du curseur pour fournir des commentaires à l’utilisateur. Bien qu’elle ne soit pas obligatoire, elle ajoute un peu de poli à votre application.

Windows fournit un ensemble d’images de curseurs standard, appelées *curseurs système*. Il peut s’agir de la flèche, de la main, du pointeur en I, du sablier (qui est maintenant un cercle tournant) et d’autres. Cette section décrit comment utiliser les curseurs système. Pour des tâches plus avancées, telles que la création de curseurs personnalisés, consultez [curseurs](/windows/desktop/menurc/cursors).

Vous pouvez associer un curseur à une classe de fenêtre en définissant le membre **hCursor** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Dans le cas contraire, le curseur par défaut est la flèche. Lorsque la souris passe au-dessus d’une fenêtre, la fenêtre reçoit un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) (sauf si une autre fenêtre a capturé la souris). À ce stade, l’un des événements suivants se produit :

-   L’application définit le curseur et la procédure de fenêtre retourne la **valeur true**.
-   L’application ne fait rien et transmet [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Pour définir le curseur, un programme effectue les opérations suivantes :

1.  Appelle [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) pour charger le curseur en mémoire. Cette fonction retourne un handle au curseur.
2.  Appelle [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) et passe dans le handle de curseur.

Sinon, si l’application passe [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la fonction **DefWindowProc** utilise l’algorithme suivant pour définir l’image de curseur :

1.  Si la fenêtre a un parent, transférez le message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) au parent pour le gérer.
2.  Sinon, si la fenêtre possède un curseur de classe, définissez le curseur sur la classe Cursor.
3.  S’il n’y a aucun curseur de classe, définissez le curseur sur le curseur en flèche.

La fonction [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) peut charger soit un curseur personnalisé à partir d’une ressource, soit l’un des curseurs système. L’exemple suivant montre comment définir le curseur sur le curseur de la main du système.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Si vous modifiez le curseur, l’image de curseur se réinitialise au prochain déplacement de la souris, sauf si vous interceptez le message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) et redéfinissez le curseur. Le code suivant montre comment gérer **WM \_ SETCURSOR**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Ce code vérifie d’abord les 16 bits inférieurs de *lParam*. Si est `LOWORD(lParam)` égal à **HTCLIENT**, cela signifie que le curseur se trouve sur la zone cliente de la fenêtre. Dans le cas contraire, le curseur se trouve sur la zone non cliente. En règle générale, vous devez uniquement définir le curseur pour la zone cliente et laisser Windows définir le curseur pour la zone non cliente.

## <a name="next"></a>Suivant

[Entrée utilisateur : exemple étendu](user-input--extended-example.md)

 

 