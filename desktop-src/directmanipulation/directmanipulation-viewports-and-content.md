---
description: La manipulation directe utilise des Viewports, du contenu et des contacts pour décrire les éléments interactifs de l’interface utilisateur.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewports et contenu
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787076"
---
# <a name="viewports-and-content"></a>Viewports et contenu

La [manipulation directe](direct-manipulation-portal.md) utilise des *Viewports*, du *contenu* et des *contacts* pour décrire les éléments interactifs de l’interface utilisateur.

- [Configuration d’une fenêtre d’affichage](#configuring-a-viewport)
- [Points d’alignement et limites](#snap-points-and-boundaries)
- [Décalage du point d’alignement et scénarios RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportements](#behaviors)
- [Système de coordonnées](#coordinate-system)
- [Transformations](#transforms)
- [État de la fenêtre d’affichage](#viewport-state)
- [Rubriques connexes](#related-topics)

Une fenêtre d' *affichage* est une région au sein d’une fenêtre qui peut recevoir et traiter l’entrée des interactions de l’utilisateur. La fenêtre d’affichage représente la région du contenu qui peut être consultée par l’utilisateur final à un moment donné (également appelé le clip de contenu). La fenêtre d’affichage comporte plusieurs fonctions :

- Il gère l’état de l’interaction (par exemple, lorsque le contenu est prêt à être manipulé, lorsque le contenu est en cours de manipulation, lorsque le contenu est une animation d’inertie) et mappe l’entrée aux transformations de sortie.
- Elle contient du contenu qui se déplace en réponse à l’interaction de l’utilisateur. il peut s’agir d’un élément HTML div (défilement), d’une liste de panoramique (l’Windows 8 écran de démarrage) ou du menu contextuel d’un contrôle select.

Une fenêtre d’affichage est créée en appelant [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). Vous pouvez créer plusieurs Viewports dans une seule fenêtre pour obtenir une expérience d’interface utilisateur riche.

Le *contenu* représente l’élément qui est transformé en réponse à une interaction. En d’autres termes, il s’agit du contenu déplacé ou mis à l’échelle à mesure que l’utilisateur monte ou pince. Il existe deux types de contenu :

- Le *contenu principal* est le seul élément intrinsèque dans une fenêtre d’affichage qui répond aux manipulations et à l’inertie des entrées. Le contenu principal est créé en même temps que la fenêtre d’affichage et ne peut pas être ajouté ou supprimé d’une fenêtre d’affichage. Vous pouvez personnaliser le comportement du contenu principal à l’aide de points d’alignement (voir plus loin).
- Le *contenu secondaire* se déplace par rapport au mouvement du contenu principal. Le contenu secondaire est créé séparément de la fenêtre d’affichage et peut être ajouté ou supprimé d’une fenêtre d’affichage. Toutes les transformations de contenu secondaires sont calculées en fonction de la transformation du contenu principal. Des règles spécifiques peuvent être appliquées pour modifier la façon dont la transformation est calculée en fonction de l’objectif prévu de l’élément, identifié par son CLSID lors de la création.

Dans ce diagramme montrant avant et après une panoramisation, un seul contact a été utilisé pour faire pivoter le contenu principal. Même si l’utilisateur n’interagit pas directement avec l’indicateur de panoramique (contenu secondaire), le contenu secondaire se déplace en tant que contenu principal panoramique. Cela fournit des indications visuelles sur l’panoramique de l’utilisateur.

![Diagramme montrant avant/après une panoramisation](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configuration d’une fenêtre d’affichage

Une fois que vous avez créé la fenêtre d’affichage. Configurez son comportement à l’aide d’une *configuration d’interaction*. La configuration d’interaction spécifie quelles manipulations, telles que le panoramique, sont prises en charge.

La *panoramisation* change la position du contenu le long de l’axe horizontal ou vertical, ou les deux en tant que panoramiques utilisateur. Quand vous configurez la traduction sur les deux axes, le contenu se déplace librement dans n’importe quelle direction.

Pour contraindre le mouvement du contenu, configurez les *rails*, généralement sur l’axe horizontal et sur l’axe vertical. Si l’interaction d’un utilisateur est principalement le long d’un axe unique (représenté par les régions bleues dans le diagramme suivant), le panoramique est *rail* et le contenu se déplace uniquement le long de l’axe du rail. Si l’utilisateur dispose de panoramique et est actuellement rail et effectue une deuxième panoramisation alors que le contenu est en inertie, le nouveau panoramique continue à être rail.

![Diagramme montrant le contenu dans une fenêtre d’affichage d’un panoramique avec rail](images/dm-art-3.png)

Exemple : une fenêtre d’affichage est configurée pour le panoramique horizontal et vertical. Dans le premier frame, le contact devient inactif. Dans le second, un panoramique vertical est initié et le contact est verrouillé sur le rail vertical. Enfin, une fois que le panoramique est rail, seul le composant vertical d’un panoramique Diagonal est utilisé pour déplacer le contenu.

Si l’utilisateur effectue le panoramique en diagonale de manière à ce qu’il ne se trouve pas dans les régions de détection rails (les régions blanches), le panoramique est non *rail* et le contenu se déplace librement dans les deux axes.

![Diagramme montrant le déplacement du contenu dans un panoramique non ferroviaire](images/dm-art-4.png)

Le *Zoom* modifie le facteur d’échelle du contenu au fur et à mesure qu’un utilisateur les pince ou les étire. Le point autour duquel le contenu est mis à l’échelle (le centre de zoom) se trouve au centre des contacts. Si vous avez défini l’alignement horizontal ou vertical, le centre de zoom change pour conserver l’alignement.

![Diagramme montrant le zoom du contenu avec un alignement spécifié](images/dm-art-5.png)

Vous pouvez remplacer ce comportement en spécifiant Unlock Center, qui définit le centre de zoom au centre des contacts.

![Diagramme montrant le zoom du contenu avec le centre de zoom déverrouillé](images/dm-art-6.png)

L' *inertie* est la décélération progressive d’une manipulation, panoramique et zoom, après la levée de tous les contacts (dans le cas de Touch) ou après l’entrée clavier/souris (par exemple, en cliquant sur une barre de défilement ou en appuyant sur les touches de direction). Quand un utilisateur manipule le contenu, la manipulation ne s’arrête pas immédiatement après la levée du contact. Au lieu de cela, le contenu continue dans la direction et la vélocité actuelles, ce qui ralentit progressivement jusqu’à un arrêt.

## <a name="snap-points-and-boundaries"></a>Points d’alignement et limites

Une animation d’inertie se produit après la fin de la manipulation suite à la levée d’un doigt sur l’écran (dans le cas d’une pression tactile) ou à la suite d’une action clavier/souris (comme les touches de direction, la mise en page vers le haut/bas, le défilement de la roulette de la souris, etc.).

Il existe deux éléments d’information qui définissent l’animation d’inertie :

- Point de début de l’animation : dernière position de fin du composant de transformation particulier.
- Durée, courbe, vélocité de l’animation : elles sont déterminées par le type du point de Rest.

L’animation d’inertie est affectée par les points d’alignement et les limites. Les limites spécifient le nombre maximal et le nombre minimal de points de REST pour le contenu. Si le contenu atteint une limite pendant l’inertie, une animation de limite est appliquée. Les points d’ancrage sont définis sur le contenu principal pour modifier le point REST et modifier la courbe d’animation d’inertie proprement dite.

Vous définissez des points d’ancrage avec [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) lorsque le contenu est régulièrement espacé ou avec [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) lorsque le contenu est espacé uniformément. Voici un exemple de points d’alignement :

![Diagramme montrant comment les points d’ancrage définis dans le contenu affectent le panoramique](images/dm-snappoint-states-3.png)

Dans le diagramme, il existe une partie du contenu avec une série de blocs de sous-contenu : les éléments d’actualité dans une application de type lecteur d’actualités ou des éléments dans un affichage de grille. L’objectif est d’aligner le bord gauche d’un élément sur le bord gauche de la fenêtre d’affichage une fois l’inertie terminée.

Il existe deux groupes de types de points de magnétisme :

- *Facultatif et obligatoire*: un point d’ancrage facultatif n’aligne l’animation d’inertie que si le point de repos d’inertie est proche du point d’ancrage. Un point de magnétisme obligatoire aligne toujours l’animation d’inertie sur un point d’ancrage spécifié.
- *Single et multiple*: un type de point d’ancrage multiple permet au contenu de déplacer un grand nombre de points d’ancrage avant d’atteindre un reste à un point d’alignement près de son point de repos naturel. Un seul type de point de magnétisme choisit le point d’ancrage le plus proche suivant comme point de REST pour l’animation d’inertie.

Le diagramme suivant montre comment les types de point d’alignement modifient la position REST de l’animation d’inertie.

![Diagramme montrant l’interaction entre l’inertie et les points d’alignement](images/dm-snappoint-states-1.png)

Dans ce diagramme, le point de départ de l’inertie est intitulé « Start » et la position de fin d’inertie naturelle en l’absence de points d’ancrage comme « end ». Les lignes verticales marquent les différents points d’alignement. Ce tableau décrit la façon dont chaque type de point de magnétisme affecte la position de fin de l’animation.

| Type de point         | Description                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Unique obligatoire   | Le point d’alignement P1 est choisi, car il s’agit du premier point d’ancrage dans le sens d’inertie     |
| Multiple obligatoire | Le point d’alignement P2 est choisi, car il est le plus proche du point de terminaison dans la direction de l’inertie. |
| Simple facultatif    | Le point d’alignement P1 est choisi, car il s’agit du premier point d’ancrage rencontré pendant l’inertie.      |
| Multiple facultatif  | Le point de magnétisme P2 est choisi, car il est proche du point de terminaison naturel                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Décalage du point d’alignement et scénarios RTL

![Diagramme montrant l’utilisation du point d’ancrage RTL](images/dm-snappoint-states-2.png)

Vous appliquez le décalage du point d’alignement et le système de coordonnées à l’aide de l’API [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) , qui décale tous les points d’alignement ou les intervalles de magnétisme à l’aide du système de décalage/coordonnées spécifié.

Le système de coordonnées est très utile dans les scénarios RTL, où vous souhaitez décrire les points d’alignement à partir du bord gauche du contenu dans le sens inverse. Dans le schéma précédent, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) est utilisé avec l’indicateur de **\_ \_ mise en miroir** de la coordination de **\_ mouvement DIRECTMANIPULATION \_** et de DIRECTMANIPULATION, qui décale automatiquement les points d’ancrage à partir du bord gauche du contenu et les fournit dans l’ordre de droite à gauche : S1 à 0px, S2 à 50px (et ainsi de suite). Tout décalage défini à l’aide de **SetSnapCoordinate** est décalé automatiquement de ce bord gauche du contenu, y compris le facteur d’échelle correct.

Vous allez presque toujours utiliser [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) avec le paramètre *origin* défini pour éviter de définir des points d’alignement en dehors de la zone de contenu.

Par exemple, si la fenêtre d’affichage est 200x200 et que le contenu est 1000x200, et que l’interface est RTL, la fenêtre d’affichage aura son bord gauche à x = 800 lorsque la fenêtre d’affichage est présentée pour la première fois. Appelez [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) avec `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` pour spécifier que les points d’ancrage doivent être calculés de l’ordre de droite à gauche en partant du bord droit du contenu.

## <a name="behaviors"></a>Comportements

Un *comportement* est un objet qui peut être attaché à une fenêtre d’affichage pour modifier la façon dont la [manipulation directe](direct-manipulation-portal.md) gère la transformation de sortie du contenu principal ou secondaire d’une fenêtre d’affichage. Un objet de comportement peut affecter un ou plusieurs aspects d’une manipulation, tels que la façon dont l’entrée est traitée ou la manière dont l’animation d’inertie est appliquée. Par exemple, un comportement de défilement automatique affecte l’animation d’inertie en effectuant une animation de défilement vers une extrémité du contenu principal. Un comportement de configuration de diapositives croisées affecte le traitement d’entrée de manipulation directe qui détecte quand une action de diapositive croisée est effectuée.

Un objet de comportement est créé en appelant [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), ajouté à une fenêtre d’affichage, puis son comportement est configuré de façon asynchrone. La suppression du comportement de la fenêtre d’affichage supprime ses effets.

## <a name="coordinate-system"></a>Système de coordonnées

Trois systèmes de coordonnées principaux sont utilisés par [la manipulation directe](direct-manipulation-portal.md):

- Système de coordonnées client-décrit le rectangle de la fenêtre cliente. Les unités sont en pixels.
- Système de coordonnées de la fenêtre d’affichage-décrit le rectangle d’une région au sein du client qui peut traiter l’entrée. Les unités sont définies par l’application (à l’aide de [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Système de coordonnées du contenu-décrit le rectangle ou la taille du contenu principal. Les unités sont définies par l’application (à l’aide de [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Pour les trois systèmes, les coordonnées sont définies par rapport à l’origine de l’angle supérieur gauche respectif, et sont positives en plus de droite et de baisse. Ces systèmes de coordonnées sont illustrés dans le diagramme suivant. Seule la section du contenu dans le rectangle de la fenêtre d’affichage peut être affichée ou manipulée par l’utilisateur final.

![Diagramme montrant comment le contenu, le client et les coordonnées de la fenêtre d’affichage interagissent](images/dm-art-7.png)

## <a name="transforms"></a>Transformations

La [manipulation directe](direct-manipulation-portal.md) gère plusieurs transformations différentes qui contribuent à la sortie globale affichée.

- *Transformation de contenu* : transformation initiale calculée par [manipulation directe](direct-manipulation-portal.md) en fonction d’une manipulation ou d’une inertie. Il capture les effets des points d’ancrage, de la glissière, de la overpan par défaut (manipulation), du débond par défaut (inertie) et des animations ZoomToRect.
- *Transformation de sortie* : dernière transformation visuelle ou de sortie. Il s’agit de la combinaison du contenu et des transformations de synchronisation.
- *Sync Transform* : calculées lorsque vous appelez [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform). Elle aide la [manipulation directe](direct-manipulation-portal.md) à appliquer une nouvelle transformation de contenu fournie par l’application tout en conservant la transformation de sortie existante.
- *Transformation d’affichage* : appliquée par l’application dans le cadre du traitement du message. Pour plus d’informations, consultez [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) .

Étant donné que la transformation de sortie est destinée à décaler visuellement une surface sur l’écran, la [manipulation directe](direct-manipulation-portal.md) effectue l’arrondi nécessaire sur les composants de transformation de sortie afin que le texte et d’autres contenus soient toujours rendus/composites à une limite de pixels intégrale. Le mécanisme d’arrondi dépend de plusieurs facteurs, notamment la vélocité du mouvement et la présence de Bureau à distance. Le mécanisme d’arrondi pour le contenu secondaire correspond à celui du contenu principal, tout en tenant compte de la différence de mouvement entre les deux. Les clients de [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) ne doivent pas dépendre du mécanisme d’arrondi exact de la transformation de sortie, car différents facteurs l’affectent.

> [!Note]
>
> Cela signifie que les composants d’une transformation de contenu ne peuvent pas être intégraux et peuvent contenir des décalages de sous-pixel. Les clients qui utilisent la [manipulation directe](direct-manipulation-portal.md) sont encouragés à utiliser le [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) pour calculer la transformation visuelle correcte à appliquer au contenu lors de l’utilisation du mode de mise à jour manuelle. Lorsque vous utilisez le mode de mise à jour automatique à l’aide du compositeur intégré, la manipulation directe applique automatiquement cette transformation au nom du client. Cette transformation est générée par une manipulation directe pour garantir des résultats visuellement agréables lors de la composition de la sortie visuelle.

## <a name="viewport-state"></a>État de la fenêtre d’affichage

Lorsque l’entrée est traitée, la fenêtre d’affichage gère l’état d’interaction et le mappage de l’entrée aux transformations de sortie. Vérifiez l’état d’interaction de la fenêtre d’affichage en appelant [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![Diagramme montrant les États d’interaction directmanipulation](images/dm-states-diagram.png)

- Génération : la fenêtre d’affichage est en cours de création et n’est pas encore en mesure de traiter l’entrée. Pour traiter l’entrée, appelez [**IDirectManipulationViewport :: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Si l' **activation** n’est pas appelée, la fenêtre d’affichage passe à l’état désactivé.

    > [!Note]  
    > Il s’agit de l’état initial de l’interaction.

- Activé : la fenêtre d’affichage est prête à traiter l’entrée. Lorsqu’un contact est interrompu ([**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) est appelé) et qu’une manipulation est détectée, la fenêtre d’affichage passe à l’État en cours d’exécution.

- En cours d’exécution : la fenêtre d’affichage traite actuellement l’entrée et la mise à jour du contenu. Lorsque le contact est levé, la fenêtre d’affichage passe à inertie, si elle est configurée.

- Inertie : le contenu se déplace dans une animation d’inertie. Une fois l’inertie terminée, la fenêtre d’affichage passe à prêt. Si la désactivation automatique a été définie sur la fenêtre d’affichage, elle passera de inertie à Ready, puis à Disabled.

- Prêt : la fenêtre d’affichage est prête à traiter l’entrée. Lorsqu’un contact est interrompu ([**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) est appelé) et qu’une manipulation est détectée, la fenêtre d’affichage passe à l’État en cours d’exécution.

- Suspendu : la fenêtre d’affichage peut être interrompue lorsque son entrée a été promue à un parent dans la chaîne [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) . Ce sujet est abordé plus en détail dans [plusieurs Viewports : le test de positionnement et la hiérarchie des fenêtres d’affichage](directmanipulation-multiple-vieports.md).

- Désactivé : la fenêtre d’affichage ne traite pas les entrées ni les rappels. Une fenêtre d’affichage peut être désactivée à partir de différents États en appelant [**IDirectManipulationViewport ::D désactiver**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Si la désactivation automatique a été définie sur la fenêtre d’affichage, elle passera automatiquement à Disabled après le traitement d’une manipulation. Pour réactiver une fenêtre d’affichage désactivée, appelez [**IDirectManipulationViewport :: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Rubriques connexes

[Viewports multiples : test de positionnement et hiérarchie des Viewports](directmanipulation-multiple-vieports.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform), [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
