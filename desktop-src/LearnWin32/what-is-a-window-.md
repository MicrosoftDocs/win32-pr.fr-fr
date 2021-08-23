---
title: Qu’est-ce qu’une fenêtre ?
description: Qu’est-ce qu’une fenêtre ?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af5d845d1a7eac6474dec9da08dcfde8df9f9fd67bf16d6f59cad94c5af0fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631415"
---
# <a name="what-is-a-window"></a>Qu’est-ce qu’une fenêtre ?

## <a name="what-is-a-window"></a>Qu’est-ce qu’une fenêtre ?

Évidemment, Windows est central pour Windows. Ils sont tellement importants qu’ils ont nommé le système d’exploitation après. Mais qu’est-ce qu’une fenêtre ? Lorsque vous pensez à une fenêtre, vous pensez probablement à quelque chose comme ceci :

![capture d’écran d’une fenêtre d’application](images/window01.png)

Ce type de fenêtre est appelé fenêtre d' *application* ou *fenêtre principale*. Il a généralement un frame avec une barre de titre, des boutons de **réduction** et d' **agrandissement** , et d’autres éléments d’interface utilisateur standard. Le frame est appelé la *zone non cliente* de la fenêtre, appelée, car le système d’exploitation gère cette partie de la fenêtre. La zone dans le cadre est la *zone cliente*. Il s’agit de la partie de la fenêtre gérée par votre programme.

Voici un autre type de fenêtre :

![capture d’écran d’une fenêtre de contrôle](images/window02.png)

si vous êtes un nouvel utilisateur de la programmation de Windows, il se peut que vous vous étonnez que les contrôles d’interface utilisateur, tels que les boutons et les zones d’édition, soient eux-mêmes Windows. La principale différence entre un contrôle d’interface utilisateur et une fenêtre d’application est qu’un contrôle n’existe pas de lui-même. Au lieu de cela, le contrôle est positionné par rapport à la fenêtre d’application. Lorsque vous faites glisser la fenêtre d’application, le contrôle se déplace avec elle, comme vous le feriez. En outre, le contrôle et la fenêtre d’application peuvent communiquer entre eux. (Par exemple, la fenêtre d’application reçoit des notifications de clic à partir d’un bouton.)

Par conséquent, lorsque vous pensez à la *fenêtre*, ne pensez pas simplement à la *fenêtre d’application*. Au lieu de cela, Imaginez une fenêtre comme une construction de programmation qui :

-   Occupe une certaine partie de l’écran.
-   Peut être visible ou non à un moment donné.
-   Sait comment se dessiner lui-même.
-   Répond aux événements de l’utilisateur ou du système d’exploitation.

## <a name="parent-windows-and-owner-windows"></a>Windows Parent et propriétaire Windows

Dans le cas d’un contrôle d’interface utilisateur, la fenêtre de contrôle est dite *enfant* de la fenêtre d’application. La fenêtre d’application est le *parent* de la fenêtre de contrôle. La fenêtre parente fournit le système de coordonnées utilisé pour positionner une fenêtre enfant. Avoir une fenêtre parente affecte les aspects de l’apparence d’une fenêtre ; par exemple, une fenêtre enfant est découpée afin qu’aucune partie de la fenêtre enfant ne puisse apparaître en dehors des bordures de sa fenêtre parente.

Une autre relation est la relation entre une fenêtre d’application et une fenêtre de boîte de dialogue modale. Quand une application affiche une boîte de dialogue modale, la fenêtre d’application est la fenêtre *propriétaire* et la boîte de dialogue est une fenêtre *détenue* . Une fenêtre détenue apparaît toujours devant sa fenêtre propriétaire. Elle est masquée lorsque le propriétaire est réduit et est détruite en même temps que le propriétaire.

L’illustration suivante montre une application qui affiche une boîte de dialogue avec deux boutons :

![capture d’écran d’une application avec une boîte de dialogue](images/window03.png)

La fenêtre d’application est propriétaire de la fenêtre de boîte de dialogue, et la fenêtre de dialogue est le parent des deux fenêtres de bouton. Le diagramme suivant illustre ces relations :

![Illustration montrant les relations parent/enfant et propriétaire/détenu](images/window04.png)

## <a name="window-handles"></a>Handles de fenêtre

Windows sont des objets : ils ont à la fois du code et des données, mais ce ne sont pas des classes C++. Au lieu de cela, un programme fait référence à une fenêtre à l’aide d’une valeur appelée *descripteur*. Un handle est un type opaque. En gros, il s’agit simplement d’un nombre que le système d’exploitation utilise pour identifier un objet. vous pouvez créer une image Windows comme contenant un grand tableau de toutes les fenêtres qui ont été créées. Elle utilise cette table pour rechercher des fenêtres par leurs handles. (Que c’est exactement la manière dont il fonctionne en interne n’est pas important.) Le type de données pour les handles de fenêtre est **HWND**, qui est généralement prononcé « AITCH ». Les handles de fenêtre sont retournés par les fonctions qui créent des fenêtres : [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) et [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

Pour effectuer une opération sur une fenêtre, vous devez généralement appeler une fonction qui prend une valeur **HWND** comme paramètre. Par exemple, pour repositionner une fenêtre à l’écran, appelez la fonction [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) :


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Le premier paramètre est le handle de la fenêtre que vous souhaitez déplacer. Les autres paramètres spécifient le nouvel emplacement de la fenêtre et si la fenêtre doit être redessinée.

Gardez à l’esprit que les descripteurs ne sont pas des pointeurs. Si *HWND* est une variable qui contient un descripteur, toute tentative de déréférencement du descripteur en écriture `*hwnd` est une erreur.

## <a name="screen-and-window-coordinates"></a>Coordonnées de l’écran et de la fenêtre

Les coordonnées sont mesurées en pixels indépendants du périphérique. Nous aurons plus d’explications sur la partie *indépendante* du périphérique des *pixels indépendants du périphérique* quand nous aborderons les graphiques.

En fonction de votre tâche, vous pouvez mesurer les coordonnées relatives à l’écran, par rapport à une fenêtre (y compris le cadre) ou par rapport à la zone cliente d’une fenêtre. Par exemple, vous pouvez positionner une fenêtre à l’écran à l’aide de coordonnées d’écran, mais vous dessinez dans une fenêtre à l’aide de coordonnées clientes. Dans chaque cas, l’origine (0,0) est toujours l’angle supérieur gauche de la région.

![Illustration montrant les coordonnées de l’écran, de la fenêtre et du client](images/coordinates01.png)

## <a name="next"></a>Suivant

[WinMain : point d’entrée de l’application](winmain--the-application-entry-point.md)

 

 
