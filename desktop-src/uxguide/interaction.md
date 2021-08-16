---
title: Interaction
description: L’interaction est la variété des manières dont les utilisateurs interagissent avec votre application, y compris le toucher, le clavier, la souris, et ainsi de suite. Utilisez ces instructions pour créer des expériences intuitives et distinctives optimisées pour le toucher, mais qui fonctionnent de manière cohérente sur les périphériques d’entrée.
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 09991d9b1c16c0605c89a695beb14c1117cb54fe8a5de1e2a805f6717070b1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853278"
---
# <a name="interaction"></a>Interaction

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

L’interaction est la variété des manières dont les utilisateurs interagissent avec votre application, y compris le toucher, le clavier, la souris, et ainsi de suite. Utilisez ces instructions pour créer des expériences intuitives et distinctives optimisées pour le toucher, mais qui fonctionnent de manière cohérente sur les périphériques d’entrée.

## <a name="design-for-a-touch-first-experience"></a>Conception pour une expérience tactile

Avant tout, concevez votre application en ayant comme objectif que l’entrée tactile sera la principale méthode d’entrée de vos utilisateurs. si vous utilisez les contrôles de plateforme, la prise en charge du pavé tactile, de la souris et du stylet/stylet ne nécessite aucune programmation supplémentaire, car Windows le fournit gratuitement.

Sachez cependant qu’une interface utilisateur optimisée pour les entrées tactiles ne se révèle pas toujours supérieure à une interface utilisateur classique. Les deux présentent des avantages et des inconvénients propres à la technologie et à l’application. Lors du passage à une interface utilisateur tactile, il est important de comprendre les principales différences entre les touches tactiles (pavé tactile, stylet, souris et clavier). ne vous servez pas des propriétés et comportements de périphérique d’entrée familiers pour l’octroi, car la saisie tactile dans Windows 8 fait plus que simplement émuler cette fonctionnalité.

Comme vous le découvrirez bientôt, les entrées tactiles nécessitent une approche différente de la conception de l’interface utilisateur.

**Comparer les critères de l’interaction tactile**

ce tableau présente quelques-unes des différences entre les périphériques d’entrée que vous devez prendre en compte lorsque vous concevez des applications Windows Store optimisées pour la technologie tactile.



| Facteur          | Interactions tactiles   | Interactions à l’aide de la souris, du clavier, du stylo/stylet | Pavé tactile  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Précision**<br/>        | La zone de contact au bout du doigt est plus importante qu’une simple coordonnées x-y, ce qui augmente le risque d’activations involontaires de commandes.<br/>                                                               | La souris et le stylo/stylet répondent à une coordonnée x-y précise.<br/>                                                                                                                                                                                                                                            | Comme la souris.<br/>                           |
|                                 | La forme de la zone de contact change tout au long du mouvement. <br/>                                                                                                                                       | Les mouvements de la souris et les traits du stylo/stylet répondent à des coordonnées x-y précises. Le focus du clavier est explicite.<br/>                                                                                                                                                                                                   | Comme la souris.<br/>                           |
|                                 | Il n’y a pas de curseur de souris pour aider au ciblage.<br/>                                                                                                                                                    | Le curseur de la souris, le curseur du stylo/stylet et le focus du clavier constituent tous une aide au ciblage.<br/>                                                                                                                                                                                                                   | Comme la souris.<br/>                           |
| **Anatomie humaine**<br/>    | Les mouvements effectués avec le bout du doigt sont imprécis, car le traçage d’une ligne droite avec un ou plusieurs doigts est difficile à réaliser. Cela s’explique par la courbure des articulations de la main et le nombre d’articulations impliquées dans le mouvement.<br/> | Il est plus facile de tracer un mouvement de ligne droite avec la souris ou le stylo/stylet, car la main qui les contrôle parcourt une distance plus courte que le curseur sur l’écran.<br/>                                                                                                                    | Comme la souris.<br/>                           |
|                                 | Certaines zones situées sur la surface tactile d’un périphérique d’affichage peuvent être difficiles à atteindre en raison de la posture des doigts et de la prise en main du périphérique par l’utilisateur.<br/>                                                                | La souris et le stylo/stylet peuvent accéder à toutes les parties de l’écran, et n’importe quel contrôle est accessible par le clavier via l’ordre des onglets. <br/>                                                                                                                                                                 | La posture des doigts et la prise en main peuvent poser problème.<br/> |
|                                 | Le bout des doigts ou la main de l’utilisateur peuvent masquer des objets. C’est ce que l’on appelle l’« occlusion ».<br/>                                                                                                   | Les périphériques d’entrée indirects ne provoquent pas d’occlusion.<br/>                                                                                                                                                                                                                                                       | Comme la souris.<br/>                           |
| **État de l’objet**<br/>     | L’interaction tactile utilise un modèle à deux états : la surface tactile du périphérique d’affichage est touchée (activée) ou non touchée (désactivée) par l’utilisateur. Il n’existe pas d’état de pointage susceptible de déclencher un retour visuel supplémentaire.<br/>                         | Une souris, un stylo/stylet et un clavier exposent tous un modèle à trois états : soulevé (activé), appuyé (activé) et pointé (focus).<br/> Le pointage permet à l’utilisateur d’explorer et de découvrir les éléments à l’aide d’info-bulles associées aux éléments de l’interface utilisateur. Les effets de pointage et de focus peuvent transmettre les objets qui sont interactifs et aident également au ciblage. <br/> | Comme la souris.<br/>                           |
| **Interaction évoluée**<br/> | Prend en charge l’interaction tactile multipoint : plusieurs points d’entrée (bout des doigts) sur une surface tactile.<br/>                                                                                                                          | Prend en charge un point d’entrée unique.<br/>                                                                                                                                                                                                                                                                       | Comme l’entrée tactile.<br/>                           |
|                                 | Prend en charge la manipulation directe des objets par le biais de gestes tels que l’appui, le glissement, le pincement et la rotation.<br/>                                                                                  | Ne prend pas en charge la manipulation directe, car la souris, le stylo/stylet et le clavier sont des périphériques d’entrée indirects.<br/>                                                                                                                                                                                                    | Comme la souris.<br/>                           |



 

**Remarque**

L’entrée indirecte a bénéficié de plus de 25 ans d’amélioration. Les fonctions comme les info-bulles déclenchées par le pointage ont été conçues pour résoudre les problèmes d’exploration de l’interface utilisateur spécifiques aux entrées à l’aide du pavé tactile, de la souris, du stylo/stylet et du clavier. Les fonctionnalités d’interface utilisateur de ce genre ont été repensées pour enrichir l’expérience de la saisie tactile, sans compromettre l’expérience utilisateur sur les autres appareils.

Nous fournissons ici des instructions d’interaction utilisateur générales et couvrent des instructions spécifiques à l’appareil dans ces rubriques.

-   [Interface tactile](/windows/desktop/uxguide/inter-touch)
-   [Souris](/windows/desktop/uxguide/inter-mouse)
-   [Stylet](/windows/desktop/uxguide/inter-pen)
-   [Clavier](/windows/desktop/uxguide/inter-keyboard)
-   [Accessibilité](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Éléments visuels pour les commentaires

les commentaires visuels appropriés au cours des interactions avec votre application aident les utilisateurs à reconnaître, apprendre et s’adapter à la façon dont leurs interactions sont interprétées par l’application et Windows les commentaires visuels peuvent indiquer les interactions réussies, l’état du système de relais, le sens du contrôle, la réduction des erreurs, les utilisateurs à comprendre le système et l’appareil d’entrée, et encourager l’interaction.

Le retour visuel est essentiel quand l’utilisateur doit réaliser, avec la fonction tactile, des activités qui demandent de l’exactitude et de la précision selon l’endroit concerné. Affichez le retour, quels que soient l’emplacement et le moment de la détection de l’entrée tactile, pour aider l’utilisateur à comprendre toutes les méthodes de ciblage personnalisé qui sont définies par votre application et ses contrôles.

## <a name="optimize-for-accuracy"></a>Optimiser pour la précision

La saisie tactile implique l’intégralité de la zone de contact du doigt. Cette géométrie de contact est utilisée pour déterminer l’objet cible le plus probable. Dimensionnez vos contrôles pour garantir une interface utilisateur confortable avec des objets et des contrôles qui sont faciles et sécurisés à cibler.

La taille, l’espace et la position de vos contrôles pour vous aider à éliminer l’occlusion au doigt et à la main, où l’interface utilisateur est masquée par l’interaction de l’utilisateur lui-même.

Placez les menus, les fenêtres contextuelles et les info-bulles au-dessus de la zone de contact chaque fois que cela est possible.

## <a name="constrain-for-confidence"></a>Contraindre en toute confiance

Évitez ou réduisez les interactions mal écrit à l’aide de contraintes d’interface utilisateur.

-   Les points d’alignement peuvent faciliter l’arrêt aux emplacements souhaités. Les points d’ancrage spécifient des arrêts logiques dans le contenu de votre application. Cognitivement, les points d’ancrage jouent le rôle de mécanisme de pagination pour l’utilisateur et réduisent la fatigue en cas de glissement, de balayage ou de rotation excessif. Avec eux, vous pouvez gérer une entrée utilisateur imprécise et vous assurer qu’un sous-ensemble spécifique de contenu ou d’informations de clé est affiché.
-   « Rails » directionnels qui mettent en évidence l’axe du mouvement (vertical ou horizontal).

## <a name="avoid-timed-interactions"></a>Éviter les interactions chronométrées

Ne classez pas les interactions en fonction du temps. Une même interaction doit avoir le même résultat, quel que soit le temps pris pour l’effectuer. Les activations temporelles impliquent des délais obligatoires à respecter par l’utilisateur. Par ailleurs, elles portent atteinte non seulement à la nature immersive des manipulations directes, mais également à la perception de la réactivité du système.

Généralement, les interactions chronométrées dépendent de seuils invisibles, tels que le temps, la distance ou la vitesse, pour déterminer la commande à effectuer. Les interactions chronométrées n’ont aucun Feedback visuel tant que le système n’effectue pas l’action et que les utilisateurs doivent atteindre des seuils arbitraires et invisibles pour obtenir un résultat. Le retour visuel instantané au cours de l’interaction permet à l’utilisateur de se sentir davantage impliqué, confiant et en contrôle.

Les interactions qui affectent directement les objets et qui imitent les gestes réels sont plus intuitives, plus visibles et plus faciles à retenir. Elles ne dépendent pas d’interactions obscures ou abstraites.

**Remarque :** Une exception à cette question est l’endroit où vous utilisez des interactions chronométrées spécifiques pour faciliter l’apprentissage et l’exploration (par exemple, appuyez et maintenez). L’utilisation des descriptions et des indications visuelles appropriées a un effet important sur l’utilisation des interactions avancées.

