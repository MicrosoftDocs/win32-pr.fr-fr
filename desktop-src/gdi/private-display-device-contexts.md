---
description: Un contexte de périphérique privé permet à une application d’éviter de récupérer et d’initialiser un contexte de périphérique d’affichage chaque fois que l’application doit dessiner dans une fenêtre.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contextes de périphérique d’affichage privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528287"
---
# <a name="private-display-device-contexts"></a>Contextes de périphérique d’affichage privé

Un *contexte de périphérique privé* permet à une application d’éviter de récupérer et d’initialiser un contexte de périphérique d’affichage chaque fois que l’application doit dessiner dans une fenêtre. Les contextes de périphérique privé sont utiles pour Windows qui nécessitent de nombreuses modifications des valeurs des attributs du contexte de périphérique pour le préparer au dessin. Les contextes de périphérique privé réduisent le temps nécessaire pour préparer le contexte de périphérique et, par conséquent, le temps nécessaire pour effectuer le dessin dans la fenêtre.

Une application indique au système de créer un contexte de périphérique privé pour une fenêtre en spécifiant le \_ style cs OWNDC dans la classe de fenêtre. Le système crée un contexte de périphérique privé unique chaque fois qu’il crée une nouvelle fenêtre appartenant à la classe. Initialement, le contexte de périphérique privé a les mêmes valeurs par défaut pour les attributs qu’un contexte de périphérique courant, mais l’application peut les modifier à tout moment. Le système conserve les modifications apportées au contexte de périphérique pendant toute la durée de vie de la fenêtre ou jusqu’à ce que l’application apporte des modifications supplémentaires.

Une application peut récupérer un handle vers le contexte de périphérique privé à l’aide de la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) à tout moment après la création de la fenêtre. L’application ne doit récupérer le handle qu’une seule fois. Ensuite, il peut conserver et utiliser le handle autant de fois que possible. Étant donné qu’un contexte de périphérique privé ne fait pas partie du cache du contexte de périphérique d’affichage, une application n’a pas besoin de libérer le contexte de périphérique à l’aide de la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Le système ajuste automatiquement le contexte de périphérique pour refléter les modifications apportées à la fenêtre, telles que le déplacement ou le redimensionnement. Cela garantit que toutes les fenêtres qui se chevauchent sont toujours correctement découpées. autrement dit, aucune action n’est requise par l’application pour garantir le découpage. Toutefois, le système ne révise pas le contexte de périphérique pour inclure la région de mise à jour. Par conséquent, lors du traitement d’un message [**WM \_ Paint**](wm-paint.md) , l’application doit incorporer la région de mise à jour en appelant [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ou en extrayant la région de mise à jour et en l’coupant avec la région de découpage actuelle. Si l’application n’appelle pas **BeginPaint**, elle doit valider explicitement la région de mise à jour à l’aide de la fonction [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) ou [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) . Si l’application ne valide pas la région de mise à jour, la fenêtre reçoit une série infinie de messages de **\_ peinture WM** .

Étant donné que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) masque le signe insertion si une fenêtre l’affiche, une application qui appelle **BeginPaint** doit également appeler la fonction [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) pour restaurer le signe insertion. **EndPaint** n’a aucun autre effet sur un contexte de périphérique privé.

Bien qu’un contexte de périphérique privé soit pratique à utiliser, il utilise beaucoup de mémoire en termes de ressources système, ce qui nécessite 800 ou plus d’octets à stocker. Les contextes de périphérique privé sont recommandés lorsque les considérations relatives aux performances dépassent les coûts de stockage.

Le système comprend le contexte de périphérique privé lors de l’envoi du message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à l’application. Les sélections actuelles du contexte de périphérique privé, y compris le mode de mappage, sont appliquées lorsque l’application ou le système traite ces messages. Pour éviter les effets indésirables, le système utilise des coordonnées logiques lors de l’effacement de l’arrière-plan. par exemple, elle utilise la fonction [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) pour récupérer les coordonnées logiques de la zone à effacer et transmet ces coordonnées à la fonction [**fillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect) . Les applications qui traitent ces messages peuvent utiliser des techniques similaires.

Une application peut utiliser la fonction [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) pour forcer le système à retourner un contexte de périphérique courant pour la fenêtre qui possède un contexte de périphérique privé. Cela est utile pour effectuer des touches rapides dans une fenêtre sans modifier les valeurs actuelles des attributs du contexte de périphérique privé.

 

 
