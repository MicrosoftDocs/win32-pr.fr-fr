---
title: Architecture et composants
description: Cette rubrique décrit les composants qui composent Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922080"
---
# <a name="architecture-and-components"></a>Architecture et composants

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique décrit les composants qui composent Microsoft DirectComposition. Il se compose des sections suivantes.

-   [Composants logiciels](#software-components)
-   [Bibliothèque d’applications](#application-library)
-   [Moteur de composition](#composition-engine)
-   [Rubriques connexes](#related-topics)

## <a name="software-components"></a>Composants logiciels

DirectComposition comprend les principaux composants logiciels suivants.

-   Bibliothèque d’applications en mode utilisateur (dcomp.dll) qui implémente l’API publique basée sur le modèle COM (Component Object Model).
-   Un moteur de composition en mode utilisateur (dwmcore.dll) qui est hébergé dans le processus de Gestionnaire de fenêtrage (DWM) (dwm.exe) et effectue la composition du bureau.
-   Base de données d’objets en mode noyau (partie de win32k.sys) qui marshale les commandes de l’application vers le moteur de composition.

Une seule instance du moteur de composition gère les arborescences de composition DirectComposition pour toutes les applications et l’arborescence de composition DWM, qui représente l’intégralité du bureau. La base de données d’objets en mode noyau et le moteur de composition en mode utilisateur sont instanciés une fois par session, de sorte qu’un ordinateur Terminal Server avec plusieurs utilisateurs a plusieurs instances de ces deux composants.

Le diagramme suivant montre les principaux composants DirectComposition et la façon dont ils sont liés les uns aux autres.

![architecture de niveau supérieur directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Bibliothèque d’applications

La bibliothèque d’applications DirectComposition est une API COM publique avec un point d’entrée unique à deux dimensions qui est exporté à partir de dcomp.dll et retourne un pointeur d’interface vers un objet appareil. L’objet périphérique a, à son tour, des méthodes pour créer tous les autres objets, chacun d’eux étant représenté par un pointeur d’interface. Toutes les interfaces DirectComposition héritent de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) et l’implémentent entièrement. Toutes les méthodes qui acceptent des interfaces DirectComposition vérifient si l’interface est implémentée à l’intérieur de dcomp.dll ou si elle est implémentée par un autre composant. Étant donné que DirectComposition n’est pas extensible, les méthodes qui prennent des interfaces comme paramètres retournent E \_ INVALIDARG si les interfaces ne sont pas implémentées dans dcomp.dll. L’API ne requiert pas de privilèges spéciaux. Il peut être appelé par des processus s’exécutant au niveau d’accès le plus bas. Toutefois, étant donné que l’API ne fonctionne pas dans la session 0, elle ne convient pas aux services. À ces égards, l’API DirectComposition est similaire à d’autres API Microsoft DirectX, notamment Direct2D, Microsoft Direct3D et Microsoft DirectWrite.

Étant donné que le moteur de composition est conçu exclusivement pour une exécution asynchrone, les propriétés d’objet dans l’API DirectComposition sont en écriture seule. Toutes les propriétés ont des méthodes setter, mais pas des méthodes getter. La lecture des propriétés n’est pas seulement gourmande en ressources, mais elle peut également être inexacte, car toute valeur retournée par le moteur de composition peut devenir immédiatement non valide. Cela peut se produire si, par exemple, une animation indépendante est liée à la propriété en cours de lecture.

L’API est thread-safe. Une application peut appeler n’importe quelle méthode à tout moment à partir de n’importe quel thread. Toutefois, étant donné que de nombreuses méthodes d’API doivent être appelées dans une séquence particulière, sans synchronisation, une application peut rencontrer un comportement imprévisible en fonction de la façon dont les threads entrelacent. Par exemple, si deux threads modifient la même propriété du même objet en différentes valeurs en même temps, l’application ne peut pas prédire laquelle des deux valeurs sera la valeur finale de la propriété. De même, si deux threads appellent une [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) sur le même appareil, aucun thread ne reçoit véritablement le comportement transactionnel, car un appel à **Commit** sur un thread envoie le lot de toutes les commandes émises par les deux threads, pas seulement celui qui a appelé **Commit**.

Le système conserve tous les États internes par objet appareil. Si une application crée au moins deux objets d’appareil DirectComposition, l’application peut gérer des lots indépendants et d’autres États entre les deux.

Tous les objets DirectComposition ont une affinité d’objet d’appareil ; les objets créés par un objet appareil particulier ne peuvent être utilisés qu’avec cet objet appareil et ne peuvent être associés qu’à d’autres objets créés par le même objet appareil. En d’autres termes, chaque objet d’appareil est un îlot de fonctionnalités séparé. La seule exception est la classe visuelle, qui permet de générer des arborescences visuelles où un visuel peut appartenir à un objet appareil différent de son parent. Cela permet des scénarios dans lesquels une application et un contrôle peuvent gérer une arborescence de composition unique sans avoir besoin de partager un seul objet d’appareil DirectComposition.

## <a name="composition-engine"></a>Moteur de composition

Le moteur de composition DirectComposition s’exécute sur un processus dédié, distinct de tout processus d’application. Un processus de composition unique, dwm.exe, prend en charge toutes les applications d’une session. Chaque application peut créer deux arborescences d’éléments visuels pour chaque fenêtre qu’elle possède. Toutes les arborescences sont réellement implémentées sous la forme de sous-arborescences d’une arborescence d’éléments visuels plus grande qui englobe également les structures de composition du DWM. Le DWM construit une arborescence d’éléments visuels importante pour chaque bureau dans une session. Voici les principaux avantages de cette architecture :

-   Le moteur de composition a accès à toutes les bitmaps d’application et aux arborescences d’éléments visuels, ce qui permet l’interopérabilité entre les fenêtres et la composition.
-   Le moteur de composition s’exécute dans un processus système approuvé distinct de tout processus d’application, ce qui permet aux applications disposant de droits d’accès insuffisants de composer en toute sécurité du contenu protégé.
-   Le moteur de composition peut détecter si une fenêtre particulière est entièrement bloqués et éviter de gaspiller des ressources de processeur et d’unité de traitement graphique (GPU) pour la fenêtre.
-   Le moteur de composition peut composer directement la mémoire tampon d’arrière-plan de l’écran, ce qui évite d’avoir besoin d’une copie supplémentaire requise pour les moteurs de composition par processus.
-   Toutes les applications partagent un seul appareil Direct3D pour la composition, ce qui permet d’économiser beaucoup de mémoire

L’arborescence d’éléments visuels est une structure conservée. L’API DirectComposition expose des méthodes pour modifier la structure dans des lots de modifications traitées atomiquement. L’objet racine dans l’API DirectComposition est l’objet appareil, qui sert de fabrique pour tous les autres objets DirectComposition et contient une méthode appelée [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Le moteur de composition ne reflète pas les modifications apportées par l’application à l’arborescence d’éléments visuels tant que l’application n’appelle pas la **validation**, auquel cas toutes les modifications apportées depuis la dernière **validation** sont traitées comme une transaction unique.

La nécessité d’appeler la [**validation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) est similaire au concept de « frame », à l’exception du fait que le moteur de composition s’exécute de façon asynchrone, il peut présenter plusieurs frames différents entre les appels à **Commit**. Dans DirectComposition, un *Frame* est une itération unique du moteur de composition, et l’intervalle passé par une application entre deux appels à **Commit** est appelé un *lot*.

DirectComposition regroupe tous les appels d’application à l’API DirectComposition. La base de données d’objets de noyau, qui est implémentée dans le pilote de session win32k.sys, stocke toutes les informations d’état associées aux appels d’API.

Le moteur de composition produit une image pour chaque espace vertical dans l’affichage. Le frame est démarré à un espace vertical et cible le champ vertical suivant. Lorsque le frame démarre, le moteur de composition récupère tous les lots en attente et comprend leurs commandes dans ce frame. Les lots sont placés dans une file d’attente en attente lorsque l’application appelle [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), et la file d’attente en attente est vidée atomiquement au début du frame. Par conséquent, il existe un point unique dans le temps qui marque le début d’une image. Tous les lots soumis avant ce point sont inclus dans le cadre, tandis que tous les lots soumis après doivent attendre que le frame suivant soit traité. La boucle de composition complète se présente comme suit :

1.  Estimer l’heure de la zone verticale suivante.
2.  Récupérer tous les lots en attente.
3.  Traitez les lots récupérés.
4.  Mettez à jour toutes les animations à l’aide du temps estimé à l’étape 1.
5.  Déterminez les régions de l’écran qui doivent être recomposées.
6.  Ré-composez les régions modifiées.
7.  Présentez le frame en retournant les mémoires tampons d’arrière-plan et d’avant pour chaque écran.
8.  Si rien n’a été composé et présenté aux étapes 6 et 7, attendez la validation d’un lot.
9.  Attendez le prochain espace vertical.

Si plusieurs moniteurs sont attachés à une seule carte vidéo, le moteur de composition utilise la zone verticale du moniteur principal pour piloter la boucle de composition et définir les heures d’échantillonnage de l’animation. Chaque moniteur est représenté par une chaîne de retournement plein écran distincte ; le moteur de composition répète les étapes 6 et 7 pour chaque analyse, en mode tourniquet (Round Robin), à l’aide d’un seul appareil Direct3D. S’il existe également plusieurs cartes vidéo, le moteur de composition utilise un appareil Direct3D distinct pour chaque carte vidéo des étapes 6 et 7.

Les frames de composition sont planifiés pour toujours démarrer à un espace vertical, comme le montre l’illustration suivante.

![planification du cadre de la composition](images/composition-frame-scheduling.png)

Si le moteur de composition n’a pas de travail à effectuer parce que l’arborescence de composition n’a pas changé, le thread de composition se met en veille en attendant un nouveau lot. Lors de l’envoi d’un nouveau lot, le thread de composition s’active, mais revient immédiatement en mode veille jusqu’à ce que le champ vertical suivant soit renseigné. Ce comportement garantit des heures de début et de fin de trame prévisibles pour les applications et pour le moteur de composition.

Le moteur de composition publie les durées de présentation du cadre et la fréquence d’images actuelle. La publication de ces informations permet aux applications d’estimer l’heure de présentation de leurs propres lots, ce qui à son tour permet la synchronisation des animations. En particulier, une application peut utiliser une combinaison de statistiques de frame à partir du moteur de composition, et un modèle historique de la durée de son thread de l’interface utilisateur pour produire un lot, afin de déterminer la durée d’échantillonnage pour ses propres animations.

Par exemple, au début du lot d’applications présenté dans l’illustration précédente, l’application peut interroger le moteur de composition pour déterminer l’heure exacte de présentation du cadre suivant. L’application peut ensuite utiliser l’heure actuelle, ainsi que des informations sur les traitements précédents qu’elle a générés, afin de déterminer si l’application peut terminer le traitement en cours avant le prochain espace vertical. Par conséquent, l’application utilise l’heure de présentation du frame comme durée d’échantillonnage pour ses propres animations. Si l’application détermine qu’il est peu probable qu’elle ne termine pas son travail dans le champ vertical actuel, l’application peut utiliser la durée d’image suivante comme durée d’échantillonnage à la place, en utilisant les informations de fréquence d’images retournées par le moteur de composition pour calculer cette durée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 