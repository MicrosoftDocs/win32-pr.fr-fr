---
description: En règle générale, une application dessine dans une fenêtre en réponse à un \_ message de peinture WM.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: Message WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965179"
---
# <a name="the-wm_paint-message"></a>Message de \_ peinture WM

En règle générale, une application dessine dans une fenêtre en réponse à un message de [**\_ peinture WM**](wm-paint.md) . Le système envoie ce message à une procédure de fenêtre lorsque les modifications apportées à la fenêtre ont modifié le contenu de la zone cliente. Le système envoie le message uniquement s’il n’y a pas d’autres messages dans la file d’attente des messages d’application.

Lors de la réception d’un message [**WM \_ Paint**](wm-paint.md) , une application peut appeler [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) pour récupérer le contexte de périphérique d’affichage pour la zone cliente et l’utiliser dans les appels aux fonctions GDI pour effectuer toutes les opérations de dessin nécessaires pour mettre à jour la zone cliente. Une fois les opérations de dessin terminées, l’application appelle la fonction [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) pour libérer le contexte de périphérique d’affichage.

Avant que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retourne le contexte de périphérique d’affichage, le système prépare le contexte de périphérique pour la fenêtre spécifiée. Il définit d’abord la zone de découpage pour que le contexte de périphérique soit égal à l’intersection de la partie de la fenêtre qui doit être mise à jour et de la partie qui est visible pour l’utilisateur. Seules les parties de la fenêtre qui ont changé sont redessinées. Les tentatives de dessin en dehors de cette région sont découpées et n’apparaissent pas à l’écran.

Le système peut également envoyer des messages [**WM \_ NCPAINT**](wm-ncpaint.md) et [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à la procédure de fenêtre avant que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retourne. Ces messages indiquent à l’application de dessiner la zone non cliente et l’arrière-plan de la fenêtre. La *zone non cliente* est la partie d’une fenêtre qui est en dehors de la zone cliente. La zone comprend des fonctionnalités telles que la barre de titre, le menu fenêtre (également connu sous le nom de menu **système** ) et les barres de défilement. La plupart des applications s’appuient sur la fonction de fenêtre par défaut, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), pour dessiner cette zone et transmettre donc le message **WM \_ NCPAINT** à cette fonction. L' *arrière-plan* de la fenêtre est la couleur ou le motif avec lequel une fenêtre est remplie avant le début des autres opérations de dessin. L’arrière-plan couvre les images précédemment dans la fenêtre ou sur l’écran sous la fenêtre. Si une fenêtre appartient à une classe de fenêtre ayant un pinceau d’arrière-plan de classe, la fonction **DefWindowProc** dessine automatiquement l’arrière-plan de la fenêtre.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) remplit une structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) avec des informations telles que les dimensions de la partie de la fenêtre à mettre à jour et un indicateur qui spécifie si l’arrière-plan de la fenêtre a été dessiné. L’application peut utiliser ces informations pour optimiser le dessin. Par exemple, il peut utiliser les dimensions de la région de mise à jour, spécifiées par le membre **rcPaint** , pour limiter le dessin uniquement aux parties de la fenêtre qui nécessitent une mise à jour. Si une application a une sortie très simple, elle peut ignorer la région de mise à jour et dessiner dans la fenêtre entière, en se basant sur le système pour ignorer (détourer) toute sortie inutile. Étant donné que le dessin de clips s’étend hors de la zone de découpage, seul le dessin qui se trouve dans la région de mise à jour est visible.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) affecte la **valeur null** à la zone de mise à jour d’une fenêtre. Cela efface la région, ce qui l’empêche de générer les messages de [**\_ peinture WM**](wm-paint.md) suivants. Si une application traite un message de **\_ peinture WM** mais n’appelle pas **BeginPaint** ou efface la zone de mise à jour, l’application continue à recevoir des messages de **\_ peinture WM** tant que la région n’est pas vide. Dans tous les cas, une application doit effacer la zone de mise à jour avant de retourner le message de **\_ peinture WM** .

Une fois que l’application a terminé le dessin, elle doit appeler [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Pour la plupart des fenêtres, **EndPaint** libère le contexte de périphérique d’affichage, ce qui le rend disponible pour d’autres fenêtres. **EndPaint** affiche également le signe insertion, s’il a été précédemment masqué par [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). **BeginPaint** masque le signe insertion pour empêcher les opérations de dessin de l’endommager.

-   [La région de mise à jour](the-update-region.md)
-   [Invalidation et validation de la région de mise à jour](invalidating-and-validating-the-update-region.md)
-   [Récupération de la région de mise à jour](retrieving-the-update-region.md)
-   [Exclusion de la région de mise à jour](excluding-the-update-region.md)
-   [Dessin synchrone et asynchrone](synchronous-and-asynchronous-drawing.md)

 

 
