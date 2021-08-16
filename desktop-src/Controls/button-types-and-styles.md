---
title: Types de bouton
description: Il existe plusieurs types de boutons et un ou plusieurs styles de bouton pour faire la distinction entre les boutons du même type.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c3614f90c36d5a81603153ec7c8612d61e73e2e98c7f668cb53a6ad2bb584b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832493"
---
# <a name="button-types"></a>Types de bouton

Il existe plusieurs types de boutons et un ou plusieurs styles de bouton pour faire la distinction entre les boutons du même type.

Ce document traite des rubriques suivantes.

-   [Types et styles de bouton](#button-types-and-styles)
-   [Cases à cocher](#check-boxes)
-   [Zones de groupe](#group-boxes)
-   [Boutons de commande](#push-buttons)
-   [Cases d’option](#radio-buttons)
-   [Rubriques connexes](#related-topics)

## <a name="button-types-and-styles"></a>Types et styles de bouton

Un bouton appartient à un type et peut avoir des styles supplémentaires qui affectent son apparence et son comportement. Pour obtenir un tableau de styles de bouton, consultez [styles de bouton](button-styles.md).

La capture d’écran suivante montre les différents types de boutons.

![capture d’écran d’une boîte de dialogue qui montre des exemples de huit types de boutons](images/buttontypes.png)

la capture d’écran montre comment les boutons peuvent apparaître dans Windows Vista. L’apparence varie selon les versions différentes du système d’exploitation et selon le thème défini par l’utilisateur.

Notez les points suivants sur l’illustration :

-   La case à cocher à trois États est indiquée dans un état indéterminé. Lorsqu’elle est cochée ou décochée, elle ressemble à une case à cocher normale.
-   Le bouton d’envoi (push) de grande taille a été défini par programmation (en envoyant le message [**\_ SETSTATE BM**](bm-setstate.md) ), afin qu’il conserve son apparence même lorsque vous n’avez pas cliqué dessus.
-   Dans le style visuel affiché, l’arrière-plan du bouton de commande par défaut (ou un autre bouton de commande de commande qui a le focus d’entrée) est en mode de basculement entre le bleu et le gris.

## <a name="check-boxes"></a>Cases à cocher

Une case *à cocher* se compose d’une zone carrée et d’une étiquette définie par l’application, d’une icône ou d’une image bitmap qui indique un choix que l’utilisateur peut effectuer en sélectionnant le bouton. Les applications affichent généralement des cases à cocher pour permettre à l’utilisateur de choisir une ou plusieurs options qui ne s’excluent pas mutuellement.

Une case à cocher peut être l’un des quatre styles suivants : standard, automatique, à trois États et automatique automatique, comme défini par la [**\_ case à**](button-styles.md)cocher des constantes BS, la case [**\_ à cocher BS autocase**](button-styles.md), [**BS \_ 3STATE**](button-styles.md)et [**BS \_ AUTO3STATE**](button-styles.md), respectivement. Chaque style peut supposer deux États d’activation : activé (une coche dans la zone) ou désactivé (aucune coche). En outre, une case à cocher à trois États peut supposer un état indéterminé (zone ombrée à l’intérieur de la case à cocher), ce qui peut signifier que l’utilisateur n’a pas effectué de choix. Si vous cliquez à plusieurs reprises sur une case à cocher standard ou automatique, la case à cocher est activée ou désactivée. Si vous cliquez à plusieurs reprises sur une case à cocher à trois États, la case à cocher cochée est désactivée, puis le cycle est répété.

Quand l’utilisateur clique sur une case à cocher (de n’importe quel style), la case à cocher reçoit le focus clavier. Le système envoie la fenêtre parente de la case à cocher un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) contenant le code de notification sur lequel l' [utilisateur a \_ cliqué](bn-clicked.md) . La fenêtre parente n’a pas à gérer ce message s’il provient d’une case à cocher automatique ou automatique à trois États, car le système définit automatiquement l’état d’activation de ces styles. Toutefois, la fenêtre parente doit gérer le message s’il provient d’une case à cocher non automatique ou de la case à cocher à trois États, car la fenêtre parente est chargée de définir l’état d’activation de ces styles. Quel que soit le style de case à cocher, le système redessine automatiquement la case à cocher une fois son état modifié.

L’application peut déterminer l’état d’une case à cocher à l’aide de la fonction [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="group-boxes"></a>Zones de groupe

Une *zone de groupe* est un rectangle qui entoure un ensemble de contrôles, tels que des cases à cocher ou des cases d’option, avec une étiquette de texte définie par l’application dans son coin supérieur gauche. Le seul but d’une zone de groupe est d’organiser les contrôles liés par un objectif commun (généralement indiqué par l’étiquette). La zone groupe n’a qu’un seul style, défini par la zone de groupe constante [**BS \_**](button-styles.md). Comme une zone de groupe ne peut pas être sélectionnée, elle n’a pas d’état d’activation, de focus ou d’état de transmission.

## <a name="push-buttons"></a>Boutons de commande

Un *bouton de commande* est un rectangle contenant une étiquette de texte définie par l’application, une icône ou une image bitmap qui indique ce que fait le bouton quand l’utilisateur le sélectionne.

Un bouton de commande peut être l’un des deux styles standard ou default, comme défini par les constantes [**BS- \_ PUSHBUTTON**](button-styles.md) et [**BS \_ DEFPUSHBUTTON**](button-styles.md). Un bouton de commande standard est généralement utilisé pour démarrer une opération. Elle reçoit le focus clavier lorsque l’utilisateur clique dessus. Un bouton de commande par défaut est généralement utilisé pour indiquer le choix le plus courant ou par défaut, tel que la fermeture de la boîte de dialogue. Il s’agit d’un bouton que l’utilisateur peut sélectionner en appuyant simplement sur entrée lorsqu’aucun autre bouton de commande de la boîte de dialogue n’a le focus d’entrée.

Quand l’utilisateur clique sur un bouton de commande, il reçoit le focus clavier. Le système envoie à la fenêtre parente du bouton un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) qui contient le code de notification sur lequel l' [utilisateur a \_ cliqué](bn-clicked.md) .

le *bouton partagé* est un type spécial de bouton de commande introduit dans Windows Vista et la [Version 6,00](common-control-versions.md). Un bouton partagé est divisé en deux parties. La partie principale fonctionne comme un bouton de commande standard ou par défaut. La deuxième partie a une flèche pointant vers le bas. En général, un menu s’affiche lorsque l’utilisateur clique sur la flèche.

Un bouton partagé a le style [**BS \_ SPLITBUTTON**](button-styles.md) ou le style [**BS \_ DEFSPLITBUTTON**](button-styles.md) s’il s’agit du bouton par défaut dans une boîte de dialogue. Vous pouvez modifier l’apparence du bouton en utilisant le message [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) ou la macro [**\_ SETSPLITINFO Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) correspondante.

Quand l’utilisateur clique sur la partie principale du bouton partagé, il envoie une notification de [ \_ clic sur](bn-clicked.md) le bouton de l’utilisateur, comme un bouton de commande normal. Toutefois, lorsque l’utilisateur clique sur la flèche orientée vers le bas, il envoie une notification de [ \_ liste déroulante BCN](bcn-dropdown.md) . Il incombe à l’application d’afficher un menu en réponse à la \_ liste déroulante BCN.

Windows Vista et la [Version 6,00](common-control-versions.md) ont également introduit un autre type de bouton de commande, le *lien de commande*. Visuellement, un lien de commande est très différent d’un bouton de commande normal, mais il possède la même fonctionnalité. Un lien de commande affiche généralement une icône de flèche, une ligne de texte et du texte supplémentaire dans une police plus petite.

## <a name="radio-buttons"></a>Cases d’option

Une *case d’option (également* appelée case d’option) se compose d’un bouton rond et d’une étiquette définie par l’application, d’une icône ou d’une image bitmap qui indique un choix que l’utilisateur peut effectuer en sélectionnant le bouton. Une application utilise généralement des cases d’option dans une zone de groupe pour permettre à l’utilisateur de choisir l’un des ensembles d’options connexes mais s’excluant mutuellement.

Une case d’option peut être l’un des deux styles suivants : standard ou Automatic, comme défini par les constantes style [**BS \_**](button-styles.md) RadioButton et [**BS \_ RadioButton**](button-styles.md). Chaque style peut supposer deux États d’activation : activé (un point dans le bouton) ou désactivé (aucun point dans le bouton).

Lorsque l’utilisateur sélectionne l’un des deux États, la case d’option reçoit le focus clavier. Le système envoie à la fenêtre parente du bouton un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) contenant le code de notification sur lequel l' [utilisateur a \_ cliqué](bn-clicked.md) . La fenêtre parente n’a pas besoin de gérer ce message s’il provient d’une case d’option automatique, car le système définit automatiquement l’état d’activation pour ce style. Toutefois, la fenêtre parente doit gérer le message s’il provient d’une case d’option non automatique, car la fenêtre parente est responsable de la définition de l’état d’activation pour ce style. Quel que soit le style de la case d’option, le système redessine automatiquement le bouton à mesure que son état change.

Les cases d’option sont organisées en groupes, et un seul bouton du groupe peut être vérifié à tout moment. Si l’indicateur [**WS \_ Group**](/windows/desktop/winmsg/window-styles) est défini pour une case d’option, ce bouton est le premier bouton d’un groupe, et tous les boutons qui le suivent immédiatement dans l’ordre de tabulation (mais qui n’ont pas l’indicateur **WS \_ Group** ) font partie de son groupe. Si aucune case d’option n’a l’indicateur **WS \_ Group** , toutes les cases d’option de la boîte de dialogue sont traitées comme un seul groupe.

L’application peut vérifier si une case d’option est activée à l’aide de la fonction [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Utilisation des boutons](using-buttons.md)
</dt> </dl>

 

 