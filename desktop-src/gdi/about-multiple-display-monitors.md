---
description: Lorsque plusieurs analyses font partie du bureau, les objets peuvent circuler de façon transparente entre les moniteurs.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: À propos de plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972467"
---
# <a name="about-multiple-display-monitors"></a>À propos de plusieurs moniteurs d’affichage

Lorsque plusieurs analyses font partie du bureau, les objets peuvent circuler de façon transparente entre les moniteurs. Autrement dit, vous pouvez faire glisser des fenêtres ou des raccourcis d’une analyse vers une autre, et vous pouvez redimensionner les fenêtres pour couvrir plusieurs moniteurs. En outre, si une analyse est installée au-dessus d’un autre, un curseur qui laisse le bas de l’écran supérieur s’affiche en haut de l’écran inférieur.

En règle générale, un utilisateur organise les moniteurs dans le système pour refléter la disposition des unités d’affichage physique ; par exemple, côte à côte ou un-sur-un-en-tête. L’utilisateur procède ainsi avec l’onglet analyses, qui remplace l’onglet Paramètres de la boîte de dialogue **propriétés d’affichage** via le panneau de **configuration** . Les moniteurs doivent former une région contiguë, autrement dit, chaque moniteur touche une autre analyse sur au moins une partie d’un bord.

Quand une fenêtre est déplacée ou redimensionnée, une partie de la légende est toujours visible, de sorte que l’utilisateur peut déplacer et redimensionner la fenêtre à l’aide de la souris. Le déplacement du curseur étant limité à la zone des moniteurs, il est toujours visible. Les [icônes de l'](multiple-monitor-considerations-for-older-programs.md)interpréteur de commandes sont positionnées sur le même moniteur que la barre des tâches, et la barre des tâches peut se trouver sur n’importe quelle analyse.

Un système à plusieurs écrans affecte certaines combinaisons de touches. La combinaison de touches ALT + IMPR. Maj prend une capture instantanée de la fenêtre de premier plan, comme toujours. Toutefois, la touche Impr. écran prend un instantané du moniteur qui a la souris. La combinaison de touches CTRL + Impr... prend une capture instantanée de l’intégralité de l’écran virtuel, consultez [l’écran virtuel](the-virtual-screen.md).

La prise en charge de plusieurs analyses n’affecte pas les performances des applications lorsqu’elles s’exécutent dans un environnement d’affichage unique. Autrement dit, lorsqu’il s’exécute sur un système d’affichage unique, aucune surcharge supplémentaire n’est présente dans le code des opérations graphiques à hautes performances. Toutefois, dans un système à plusieurs écrans, les performances sont légèrement affectées si une application s’exécute uniquement sur l’un des périphériques graphiques. En outre, les performances peuvent être largement affectées si une application s’étend sur plusieurs affichages, en particulier pour les opérations nécessitant de nombreuses ressources graphiques.

Le *mode plein écran* est une fonctionnalité fournie par le système d’exploitation qui permet à un utilisateur de basculer une application dans un état spécial dans lequel l’application peut accéder directement au matériel graphique VGA. Il s’agit d’une fonctionnalité clé pour les jeux et d’autres applications graphiques qui requièrent des performances élevées. En outre, elle est souvent utilisée par les développeurs pour la modification de texte, car elle permet un défilement de texte très rapide.

Dans un environnement à plusieurs moniteurs, un seul périphérique graphique peut être compatible VGA. Il s’agit d’une limitation du matériel informatique qui requiert qu’un seul appareil réponde à une adresse matérielle. Étant donné que la norme de compatibilité matérielle VGA requiert des adresses matérielles spécifiques, un seul périphérique graphique VGA peut être présent sur une machine et seul cet appareil peut répondre physiquement aux adresses VGA. Par conséquent, les applications qui nécessitent un plein écran s’exécutent uniquement sur l’appareil spécifique qui prend en charge la compatibilité matérielle VGA.

Cette vue d’ensemble fournit des informations sur les rubriques suivantes.

-   [Écran virtuel](the-virtual-screen.md)
-   [HMONITOR et le contexte de périphérique](hmonitor-and-the-device-context.md)
-   [Énumération et contrôle d’affichage](enumeration-and-display-control.md)
-   [Métriques système à plusieurs moniteurs](multiple-monitor-system-metrics.md)
-   [Utilisation de plusieurs moniteurs comme affichages indépendants](using-multiple-monitors-as-independent-displays.md)
-   [Couleurs sur plusieurs moniteurs d’affichage](colors-on-multiple-display-monitors.md)
-   [Positionnement des objets sur plusieurs moniteurs d’affichage](positioning-objects-on-multiple-display-monitors.md)
-   [Plusieurs applications de surveillance sur différents systèmes](multiple-monitor-applications-on-different-systems.md)
-   [Considérations relatives à la surveillance multiple pour les anciens programmes](multiple-monitor-considerations-for-older-programs.md)

 

 



