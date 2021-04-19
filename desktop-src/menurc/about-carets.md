---
title: À propos des signes
description: Cette rubrique traite des signes d’insertion.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- ressources, signes
- signes insertion, suppression
- lignes clignotantes
- blocs clignotants
- bitmaps clignotantes
- signes insertion, visibilité
- signes d’insertion et de clignotement
- temps de clignotement
- signes, positions
- suppression des signes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509653"
---
# <a name="about-carets"></a>À propos des signes

Le système fournit un signe insertion par file d’attente de messages. Une fenêtre doit créer un signe insertion uniquement lorsqu’elle a le focus clavier ou est active. La fenêtre doit détruire le signe insertion avant de perdre le focus clavier ou de devenir inactive. Pour plus d’informations sur l’entrée au clavier, consultez [entrée au clavier](/windows/desktop/inputdev/keyboard-input).

Utilisez la fonction [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) pour spécifier les paramètres d’un signe insertion. Le système forme un signe insertion en inversant la couleur de pixel dans le rectangle spécifié par la position, la largeur et la hauteur du signe insertion. La largeur et la hauteur sont spécifiées en unités logiques ; par conséquent, l’apparence d’un signe insertion est soumise au mode de mappage de la fenêtre.

Les rubriques suivantes sont présentées dans cette section.

-   [Visibilité du signe insertion](#caret-visibility)
-   [Temps de clignotement du signe insertion](#caret-blink-time)
-   [Position du signe insertion](#caret-position)
-   [Suppression d’un signe insertion](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilité du signe insertion

Une fois le signe insertion défini, utilisez la fonction [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) pour afficher le signe insertion. Quand le signe insertion apparaît, il commence automatiquement à clignoter. Pour afficher un signe insertion unie, le système inverse chaque pixel dans le rectangle ; pour afficher un signe d’insertion gris, le système inverse tous les autres pixels ; pour afficher un signe insertion bitmap, le système inverse uniquement les bits blancs de l’image bitmap.

## <a name="caret-blink-time"></a>Temps de clignotement du signe insertion

Le temps écoulé, en millisecondes, requis pour inverser le signe insertion est appelé « *heure de clignotement*». Le signe insertion clignote tant que le thread qui possède la file d’attente de messages a une pompe de messages qui traite les messages.

L’utilisateur peut définir l’heure de clignotement du signe insertion à l’aide du panneau de configuration et les applications doivent respecter les paramètres choisis par l’utilisateur. Une application peut déterminer la durée de clignotement du signe insertion à l’aide de la fonction [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) . Si vous écrivez une application qui permet à l’utilisateur d’ajuster la durée de clignotement, par exemple une applet du panneau de configuration, utilisez la fonction [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) pour définir le taux de temps de clignotement sur un nombre spécifié de millisecondes.

Le *temps de clignotement* est le temps écoulé, en millisecondes, nécessaire pour afficher, inverser et restaurer l’affichage du signe insertion. Le temps de clignotement d’un signe insertion est deux fois plus grand que la durée de clignotement.

## <a name="caret-position"></a>Position du signe insertion

Vous pouvez déterminer la position du signe insertion à l’aide de la fonction [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) . La position, dans les coordonnées clientes, est copiée dans une structure spécifiée par un paramètre dans **GetCaretPos**. Une application peut déplacer un signe insertion dans une fenêtre à l’aide de la fonction [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) . Une fenêtre ne peut déplacer un signe insertion que si elle possède déjà le signe insertion. **SetCaretPos** peut déplacer le signe insertion s’il est visible ou non.

## <a name="removing-a-caret"></a>Suppression d’un signe insertion

Vous pouvez supprimer temporairement un signe insertion en le masquant, ou vous pouvez supprimer définitivement le signe insertion en le détruisant. Pour masquer le signe insertion, utilisez la fonction [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Cela s’avère utile lorsque votre application doit redessiner l’écran lors du traitement d’un message, mais que le signe insertion doit être conservé. Lorsque l’application termine le dessin, elle peut Réafficher le signe insertion à l’aide de la fonction [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Le masquage du signe insertion ne détruit pas sa forme ou n’invalide pas le point d’insertion. Le masquage du signe insertion est cumulatif ; autrement dit, si l’application appelle **HideCaret** cinq fois, elle doit également appeler **ShowCaret** cinq fois avant que le signe insertion ne réapparaisse.

Pour supprimer le signe insertion de l’écran et détruire sa forme, utilisez la fonction [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . **DestroyCaret** détruit le signe insertion uniquement si la fenêtre impliquée dans la tâche actuelle est propriétaire du signe insertion.

 

 