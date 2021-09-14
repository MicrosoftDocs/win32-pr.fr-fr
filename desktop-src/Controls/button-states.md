---
title: États du bouton
description: Cette section explique comment la sélection d’un bouton modifie son état et comment l’application doit répondre.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123953"
---
# <a name="button-states"></a>États du bouton

Cette section explique comment la sélection d’un bouton modifie son état et comment l’application doit répondre.

La section comprend les rubriques suivantes :

-   [Sélection du bouton](#button-selection)
-   [Éléments d’un état de bouton](#elements-of-a-button-state)
    -   [État du focus](#focus-state)
    -   [État de transmission](#push-state)
    -   [Vérifier l’État](#check-state)
-   [Modifications apportées à un état de bouton](#changes-to-a-button-state)

## <a name="button-selection"></a>Sélection du bouton

L’utilisateur peut sélectionner un bouton de trois façons : en cliquant dessus avec la souris, en appuyant sur la touche Tab, puis en appuyant sur la touche entrée, ou (si le bouton fait partie d’un groupe défini par le style [**WS \_ Group**](/windows/desktop/winmsg/window-styles) ) en appuyant sur la tabulation du bouton sélectionné dans le groupe et en utilisant les touches de direction pour vous déplacer dans ce groupe. Les deux méthodes de tabulation font partie de l’interface clavier prédéfinie fournie par le système. Pour obtenir une description complète de cette interface, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes).

La sélection d’un bouton entraîne généralement les événements suivants :

-   Le système donne au bouton le focus clavier.
-   Le bouton envoie à sa fenêtre parente un message pour l’informer de la sélection.
-   La fenêtre parente (ou le système) envoie au bouton un message pour modifier son état.
-   La fenêtre parente (ou le système) redessine le bouton pour refléter son nouvel État.

## <a name="elements-of-a-button-state"></a>Éléments d’un état de bouton

L’état d’un bouton peut être caractérisé par son état de focus, son état de transmission et son état de vérification.

-   [État du focus](#focus-state)
-   [État de transmission](#push-state)
-   [Vérifier l’État](#check-state)

### <a name="focus-state"></a>État du focus

L’état du focus s’applique à une case à cocher, une case d’option, un bouton de commande ou un bouton owner-drawn. Un bouton reçoit le focus clavier lorsque l’utilisateur le sélectionne et perd le focus lorsque l’utilisateur sélectionne un autre contrôle. Un seul contrôle peut avoir le focus clavier à la fois.

Lorsqu’un bouton a le focus clavier, le système met généralement en surbrillance le texte, l’icône ou l’image bitmap d’un bouton en l’entourant d’une ligne en pointillés. En outre, un bouton de commande a une bordure sombre épaisse lorsqu’il a le focus. Le système modifie automatiquement la mise en surbrillance d’un bouton automatique, mais l’application doit modifier la mise en surbrillance d’un bouton non automatique en envoyant des messages.

### <a name="push-state"></a>État de transmission

L’État Push s’applique à un bouton de commande, une case à cocher, une case d’option ou une case à cocher à trois États, mais ne s’applique pas à d’autres boutons. L’état de transmission d’un bouton peut faire l’objet d’un push ou non d’un push. Lorsqu’un bouton de commande (ou un bouton avec le style [**BS \_ PUSHLIKE**](button-styles.md) style) fait l’objet d’un push, le bouton est dessiné sous la forme d’un bouton enfoncé. Lorsqu’il n’est pas poussé, il est dessiné comme un bouton en relief. Quand vous cliquez sur une case à cocher, une case d’option ou une case à cocher à trois États, l’arrière-plan du bouton est grisé. Lorsqu’il n’est pas poussé, l’arrière-plan du bouton n’est pas grisé.

### <a name="check-state"></a>Vérifier l’État

L’état d’activation s’applique à une case à cocher, à une case d’option ou à trois États, mais ne s’applique pas à d’autres boutons. L’État peut être activé, désactivé ou (pour les cases à cocher à trois États) indéterminé. Une case à cocher est activée lorsqu’elle contient une coche et est désactivée dans le cas contraire. Une case d’option est cochée lorsqu’elle contient un point noir ; elle est désactivée dans le cas contraire. Une case à cocher à trois États est activée lorsqu’elle contient une coche, est désactivée lorsqu’elle ne l’est pas et est indéterminée lorsqu’elle contient une zone grisée. Le système modifie automatiquement l’état d’activation d’un bouton automatique, mais l’application doit modifier l’état d’activation d’un bouton non automatique.

## <a name="changes-to-a-button-state"></a>Modifications apportées à un état de bouton

Lorsque l’utilisateur sélectionne un bouton, il est généralement nécessaire de modifier un ou plusieurs des éléments d’État du bouton. Le système modifie automatiquement l’état du focus pour tous les types de bouton, l’état de transmission pour les boutons de commande ou les boutons avec le style [**BS \_ PUSHLIKE**](button-styles.md) et l’état d’activation pour tous les boutons automatiques. L’application doit effectuer toutes les autres modifications d’État, en tenant compte du type, du style et de l’état actuel du bouton. La liste suivante répertorie les éléments d’État qui doivent être modifiés pour chaque type de bouton :

-   Une case à cocher doit changer l’état d’activation.
-   Une case d’option doit changer l’état d’activation. Il peut également être nécessaire de modifier l’état d’activation d’autres cases d’option dans le même groupe pour garantir la nature mutuellement exclusive des cases d’option.
-   Étant donné que l’état d’un bouton owner-drawn dépend de l’application, ce que l’application doit modifier dans le bouton peut varier. Aucun élément d’une zone de groupe ne doit être modifié, car les utilisateurs ne peuvent pas sélectionner de zones de groupe.

Une application peut déterminer l’état d’un bouton en lui envoyant un message [**BM \_ GETCHECK**](bm-getcheck.md) ou [**BM \_ GETSTATE**](bm-getstate.md) ; l’application peut définir l’état d’un bouton en lui envoyant un message [**BM \_ SETCHECK**](bm-setcheck.md) ou [**BM \_ SETSTATE**](bm-setstate.md) .

 

 