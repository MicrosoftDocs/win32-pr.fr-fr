---
title: Windows Vue d’ensemble de l’animation
description: cette vue d’ensemble fournit une introduction au gestionnaire d’animations Windows et se concentre sur les composants et les concepts clés.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows animation Windows animation, vue d’ensemble
- objets du gestionnaire d’animations Windows animation, description
- variables d’animation Windows animation, description
- objets de minuteur d’animation Windows animation, description
- Animation système de minutage Windows
- durée contextuelle Windows Animation
- Animation de correspondance de vélocité Windows
- Animation gestion de la contention Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc0892cffa3e79428e19cbe5b1a3c27d7abda62365c4ceb15731101aa857f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348001"
---
# <a name="windows-animation-overview"></a>Windows Vue d’ensemble de l’animation

cette vue d’ensemble fournit une introduction au gestionnaire d’animations Windows et se concentre sur les composants et les concepts clés. Pour plus d’informations sur les storyboards et les transitions, consultez [vue d’ensemble de la table de montage séquentiel](storyboard-construction.md).

Cette rubrique contient les sections suivantes :

-   [Concepts de base](#basic-concepts)
-   [composants de Windows Animation](#components-of-windows-animation)
-   [API d’Animation Windows](#the-windows-animation-api)
-   [Configurations](#configurations)
    -   [Animation pilotée par les applications](#application-driven-animation)
    -   [Animation pilotée par minuterie](#timer-driven-animation)
-   [Fonctionnalités avancées](#advanced-features)
    -   [Gestion des conflits](#contention-management)
-   [Rubriques connexes](#related-topics)

## <a name="basic-concepts"></a>Concepts de base

L' *animation* est une séquence d’images continues consécutives qui produisent une illusion de mouvement lors de la lecture. L’utilisation de l’animation interactive dans son interface utilisateur peut offrir à une application une personnalité unique et améliorer l’expérience utilisateur. L’animation peut faciliter la communication des modifications d’État majeures dans l’interface utilisateur et aider à gérer la complexité de l’interface utilisateur. L’animation peut également être ajoutée à la perception de l’utilisateur de la qualité d’une application.

en guise d’exemples, Windows Animation est utilisée dans la barre des tâches pour vous aider à gérer et à accéder aux fichiers et aux programmes, et à la loupe pour agrandir différentes parties de l’écran afin de faciliter la tâche des utilisateurs.

Les unités fondamentales d’une animation sont la caractéristique d’un élément visuel à animer et la description de la façon dont cette caractéristique change dans le temps. Une application peut animer un large éventail de caractéristiques telles que la position, la couleur, la taille, la rotation, le contraste et l’opacité.

dans Windows animation, une *variable d’animation* représente la caractéristique à animer. Une *transition* décrit comment la valeur de cette variable d’animation change au fur et à mesure que l’animation se produit. Par exemple, un élément visuel peut avoir une variable d’animation qui spécifie son opacité, et une action de l’utilisateur peut générer une transition qui accepte cette opacité d’une valeur de 50 à 100, représentant une animation de semi-transparente à entièrement opaque.

Une *table de montage séquentiel* est un ensemble de transitions appliquées à une ou plusieurs variables d’animation dans le temps. Une application affiche les animations en construisant et en lisant des storyboards, puis en dessinant des séquences d’images discrètes à mesure que les valeurs des variables d’animation changent au fil du temps.

## <a name="components-of-windows-animation"></a>composants de Windows Animation

Windows L’animation est constituée des composants suivants :

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>gestionnaire d’animations
</dt> <dd>

Les applications utilisent un objet du gestionnaire d’animations pour créer des variables d’animation et des storyboards, planifier et contrôler des animations et mettre à jour les informations d’État avant que l’application ne dessine chaque frame. Un seul objet de gestionnaire d’animations gère généralement toutes les animations au sein d’une application et dispose donc d’un contrôle global sur toutes les storyboards planifiées.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variables d’animation
</dt> <dd>

Avant de démarrer des animations, une application doit créer des objets de variable d’animation. Une variable d’animation représente un aspect d’un élément visuel à animer. La variable est une valeur à virgule flottante scalaire, bien que la valeur puisse être arrondie à une valeur entière.

Une variable d’animation a généralement la même durée de vie que l’élément visuel qu’elle doit animer. La valeur initiale d’une variable d’animation est spécifiée lors de la création de la variable. Par la suite, sa valeur ne peut pas être modifiée directement ; elle doit être mise à jour par le biais du gestionnaire d’animations.

Une variable d’animation peut être identifiée par une *balise*, qui est le jumelage d’un identificateur entier avec un pointeur vers un objet com. Une balise n’a pas besoin d’être unique, sauf si l’application l’utilise pour rechercher une variable. Par défaut, une variable d’animation n’a pas de balise et toute tentative de lecture de sa balise échouera jusqu’à ce que l’une d’elles ait été définie.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>système de minutage
</dt> <dd>

Windows L’animation comprend un système de minutage qui permet de s’assurer que les animations sont rendues à une fréquence d’images lisse et cohérente, tout en réduisant l’utilisation des ressources système pour le rendu lorsque le système est occupé. Un *minuteur* permet de gérer le rendu d’animation en indiquant automatiquement le passage d’une petite unité de temps, appelée *graduation*. Le système de minutage surveille les performances globales du rendu du système et *limite* les animations en renforçant ou en diminuant de manière dynamique la fréquence des graduations. Les applications peuvent permettre à un minuteur de piloter le gestionnaire d’animations et d’inscrire un gestionnaire pour être notifié avant et après la mise à jour du gestionnaire pour chaque cycle. Les applications peuvent spécifier la fréquence d’images d’animation minimale acceptable pour un minuteur et être notifiées si la fréquence d’images réelle d’une animation tombe en dessous de cette fréquence.

Pour économiser les ressources système, un minuteur peut être configuré pour s’arrêter lorsqu’aucune animation n’est en cours.

</dd> </dl>

## <a name="the-windows-animation-api"></a>API d’Animation Windows

l’api d’Animation Windows est une api COM à thread unique qui fournit les fonctionnalités suivantes aux développeurs :

-   Objet gestionnaire d’animations, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), pour la création d’objets d’animation et le contrôle d’animations
-   Variables d’animation et storyboards
-   Bibliothèque fondamentale, [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), de transitions prêtes à l’emploi
-   Un objet Timer, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), pour déterminer l’heure actuelle et, éventuellement, pour la conduite de l’animation
-   Hooks d’événement pour surveiller l’État et la progression de l’animation

pour obtenir des informations de référence sur l’API, consultez Windows informations de référence sur les [animations](windows-animation-reference.md). pour obtenir un exemple de code, consultez [Windows des tâches d’animation](using-windows-animation.md) et des exemples d' [animation Windows](windows-animation-samples.md).

## <a name="configurations"></a>Configurations

Les applications doivent obtenir l’heure actuelle avant de planifier une nouvelle animation. les mécanismes de synchronisation pris en charge par Windows Animation sont les suivants :

-   [Animation pilotée par les applications](#application-driven-animation)
-   [Animation pilotée par minuterie](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animation Application-Driven

Les applications qui utilisent une API Graphics à accélération matérielle peuvent se synchroniser avec la fréquence d’actualisation du moniteur pour afficher des animations lisses. Une application peut également utiliser un mécanisme de minutage propre pour déterminer quand dessiner chaque image d’une animation. Dans les deux cas, l’application indique au gestionnaire d’animations le moment où il doit mettre à jour son état. Une minuterie d’animation peut encore être utilisée pour déterminer l’heure actuelle avec une précision élevée, dans les unités requises par le gestionnaire d’animations.

le diagramme suivant montre les interactions entre une application et les composants d’animation Windows lorsque l’application pilote directement les mises à jour d’animation.

![diagramme qui montre les interactions entre une application et les composants d’animation Windows lorsque l’application pilote directement les mises à jour d’animation.](images/animationupdates.png)

Dans la configuration la plus simple, une application redessine tout chaque fois que l’écran est actualisé, même si aucune animation n’est lue. Pour éviter toute perte de travail, une application peut inscrire un gestionnaire d’événements de gestionnaire pour être averti lorsque des animations sont planifiées, et peut détecter lorsque la planification est vide afin de pouvoir arrêter le rafraîchissement.

### <a name="timer-driven-animation"></a>Animation Timer-Driven

Plutôt que de mettre directement à jour le gestionnaire d’animations, les applications peuvent laisser le minuteur faire savoir au gestionnaire d’animations le moment où il doit mettre à jour son état, et être averti quand chaque mise à jour a eu lieu. Cette approche est recommandée pour les API Graphics plus anciennes. En général, s’il est possible de synchroniser avec la fréquence d’actualisation du moniteur, il est préférable de le faire et d’utiliser une animation pilotée par l’application.

le diagramme suivant montre les interactions entre une application et les composants d’animation Windows lorsque le minuteur d’animation pilote des mises à jour d’animation.

![diagramme qui montre les interactions entre une application et les composants d’animation Windows lorsque le minuteur d’animation pilote des mises à jour d’animation.](images/animationtimerupdates.png)

La minuterie peut être configurée pour s’exécuter uniquement lorsque les animations sont planifiées ; pour ce faire, il suffit de passer un paramètre particulier lorsque la minuterie et le gestionnaire d’animations sont connectés.

## <a name="advanced-features"></a>Fonctionnalités avancées

au-delà d’une base pour prendre en charge l’animation, Windows animation inclut la prise en charge de plusieurs techniques d’animation avancées, notamment :

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*durée contextuelle*
</dt> <dd>

La durée d’une transition n’a pas besoin d’être fixe ; Il peut être déterminé en fonction de la valeur et de la vélocité de la variable animée au début de la transition.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*correspondance de vélocité*
</dt> <dd>

Le mouvement est généralement plus agréable à l’œil si la position et la vélocité d’un objet en mouvement ne sautent pas instantanément entre les valeurs. Lorsqu’une nouvelle table de montage séquentiel interrompt une nouvelle chronologie en cours de diffusion, la correspondance de vélocité permet à la nouvelle table de montage séquentiel de récupérer sans heurts là où la précédente s’est terminée.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*gestion des conflits*
</dt> <dd>

Si deux storyboards doivent mettre à jour la même variable d’animation simultanément, un conflit de planification se produit. plutôt que d’exiger une priorité numérique spécifique pour chaque storyboard, Windows Animation permet à l’application de déterminer les priorités relatives de deux storyboards.

</dd> </dl>

### <a name="contention-management"></a>Gestion des conflits

Les développeurs peuvent implémenter un rappel de *Comparaison de priorité* pour comparer la priorité de la table de montage séquentiel planifiée et la table de montage séquentiel qui figure déjà dans la planification. Une application qui implémente une comparaison de priorité peut utiliser n’importe quelle logique préférée pour déterminer quand une table de montage séquentiel en passe une autre. pour résoudre le conflit de planification, Windows Animation demande à l’application laquelle de ces actions peuvent être prises, dans l’ordre suivant :

-   **Annulez le Storyboard planifié.** Si la lecture de la table de montage séquentiel planifiée n’a pas encore commencé, elle peut être annulée et immédiatement supprimée de la planification.
-   **Supprimez le Storyboard planifié.** Lorsqu’une nouvelle table de montage séquentiel supprime une table de montage séquentiel planifiée, le Storyboard planifié cesse d’affecter la variable dès que le nouveau Storyboard commence à l’animer. Les vitesses sont mises en correspondance, ce qui permet à la nouvelle table de montage séquentiel de se retrouver sans heurts là où le précédent s’est arrêté.
-   **Terminez le Storyboard planifié.** Une table de montage séquentiel peut être conclue uniquement si elle contient une boucle qui se répète indéfiniment. Si la table de montage séquentiel est dans une telle boucle lorsqu’elle est terminée, la répétition en cours se termine, et le reste de la table de montage séquentiel est alors lu. Si la boucle n’a pas encore commencé lorsqu’une table de montage séquentiel est terminée, la boucle est entièrement ignorée.
-   **Compresser le Storyboard planifié.** Si la suppression ou l’annulation de la table de montage séquentiel planifiée n’est pas une option, le Storyboard est autorisé à se terminer. Windows L’animation introduit la possibilité de compresser le temps disponible pour le Storyboard planifié (et les storyboards planifiés avant celui-ci), de sorte que les variables atteignent leur état final plus rapidement. Lorsque la compression est appliquée, le temps est temporairement accéléré pour les storyboards affectés, de sorte qu’ils s’exécutent plus rapidement.

Si aucune des actions ci-dessus n’est autorisée par les objets de comparaison de priorité enregistrés, la tentative de planification de la nouvelle table de montage séquentiel échoue. Par défaut, tous les storyboards peuvent être supprimés, terminés ou compressés pour éviter les défaillances, mais aucun ne peut être annulé.

Le diagramme suivant illustre le cycle de vie d’une table de montage séquentiel, à l’aide des États définis par l’énumération de l’état de l' [**animation d’animation d’interface utilisateur \_ \_ \_**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) . les Applications utilisent l’API d’Animation Windows pour créer une table de montage séquentiel et l’envoyer pour la planification. Le gestionnaire d’animations planifie le Storyboard et gère l’animation.

![diagramme qui montre comment le gestionnaire d’animations planifie le Storyboard et gère l’animation.](images/statediagram.png)

Pour plus d’informations sur la planification et la gestion des storyboards, consultez [vue d’ensemble des storyboards](storyboard-construction.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Référence d’animation](windows-animation-reference.md)
</dt> <dt>

[Windows Exemples d’animation](windows-animation-samples.md)
</dt> <dt>

[Windows Tâches d’animation](using-windows-animation.md)
</dt> </dl>

 

 