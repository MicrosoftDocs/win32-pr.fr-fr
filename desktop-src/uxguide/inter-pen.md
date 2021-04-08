---
title: Stylet
description: Toutes les applications Microsoft Windows doivent être activées pour le stylet. Et cela est plus facile que vous ne le pensez.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 35994f345306bd3a270f8d8cf9760e7d07183941
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869382"
---
# <a name="pen"></a>Stylet

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Toutes les applications Microsoft Windows doivent être activées pour le stylet. Et cela est plus facile que vous ne le pensez.

L’entrée PEN fait référence à la façon dont Windows vous permet d’interagir directement avec un ordinateur à l’aide d’un stylet. Un stylet peut être utilisé pour le pointage et également pour les gestes, l’entrée de texte simple et la capture de réflexions de forme libre dans l’encre numérique.

Le stylet utilisé pour l’entrée a un Conseil parfait et lisse qui prend en charge le pointage, l’écriture ou le dessin précis de l’encre. Le stylet peut également avoir un bouton de stylet facultatif (utilisé pour effectuer des clics droits) et gomme (utilisé pour effacer l’encre). La plupart des stylets prennent en charge le pointage.

![figure d’un stylet classique ](images/inter-pen-image1.png)

Stylet classique.

Lorsque le stylet est utilisé pour l’écriture manuscrite, les traits de l’utilisateur peuvent être convertis en texte à l’aide de la reconnaissance de l’écriture manuscrite. Les traits peuvent être conservés exactement tels qu’ils ont été écrits, avec la reconnaissance effectuée en arrière-plan pour prendre en charge la recherche et la copie sous forme de texte. Ces traits non convertis sont appelés encre numérique.

![capture d’écran de l’écriture manuscrite sur la page OneNote ](images/inter-pen-image2.png)

Exemple d’entrée d’encre.

La plupart des programmes Windows sont déjà conviviaux dans la mesure où un stylet peut être utilisé à la place d’une souris, le stylet fonctionne sans heurts pour les tâches et interactions importantes, et le programme répond aux gestes. Un programme devient facile à écrire dans le cadre d’une saisie manuscrite de texte. Un programme prend en charge l’écriture manuscrite lorsqu’il peut gérer l’encre directement, au lieu de faire en sorte que les traits de stylet soient traduits en texte ou en mouvements de souris équivalents. Cela permet aux utilisateurs d’écrire, de dessiner et d’ajouter des commentaires dans une encre numérique de haute qualité, à l’ordre gratuit. La collecte d’encre est différente de la collecte d’événements de souris, car l’encre requiert une résolution plus élevée et une fréquence d’échantillonnage supérieure, et elle peut également ajouter des nuances avec pression et inclinaison. Pour plus d’informations sur la création de programmes compatibles avec l’écriture manuscrite et avec écriture manuscrite, consultez intégration de l’entrée [manuscrite](/previous-versions/windows/desktop/ms700674(v=vs.85)) et [texte à l’aide du stylet](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Lors du positionnement d’un stylet, il est moins nécessaire de disposer d’un curseur, car l’info-bulle se représente lui-même. Toutefois, pour le ciblage de l’assistance, Windows fournit un minuscule curseur de stylet qui indique l’emplacement actuel du stylet. Contrairement au pointeur de la souris qu’il remplace, le curseur de stylet n’est pas nécessaire, sauf si le stylet est proche de l’écran, donc il disparaît après quelques secondes d’inactivité pour permettre une vue sans obstruction des informations.

La plupart des programmes compatibles avec le stylet prennent en charge les gestes. Un mouvement est un mouvement rapide du stylet sur un écran que l’ordinateur interprète comme une commande, plutôt que comme un déplacement de la souris, l’écriture ou le dessin. Un raccourci est l’un des gestes les plus rapides et les plus simples à exécuter. Un raccourci est un mouvement simple qui se traduit par une navigation ou une commande d’édition. Les raccourcis de navigation incluent glisser vers le haut, faire glisser vers le bas, déplacer vers l’arrière et avancer, tandis que les raccourcis de modification incluent copier, coller, annuler et supprimer.

Tous les pointeurs, à l’exception du pointeur Busy, ont une zone réactive de pixel unique qui définit l’emplacement exact de l’écran du pointeur. La zone réactive détermine l’objet affecté par l’interaction. Les objets définissent une zone réactive, qui est la zone dans laquelle la zone réactive est considérée sur l’objet. En règle générale, la zone d’échange coïncide avec les bordures d’un objet, mais elle peut être plus grande pour faciliter l’interaction.

**Comme un stylet peut pointer plus précisément qu’un doigt, si votre interface utilisateur fonctionne bien pour la touche tactile, elle fonctionne également bien pour un stylet.** Par conséquent, cet article se concentre principalement sur l’ajout de la prise en charge du stylet aux programmes qui ont déjà été conçus pour la saisie tactile.

**Remarque :** Les instructions relatives à [la souris](inter-mouse.md), l' [accessibilité](inter-accessibility.md)et l' [effleurement](inter-touch.md) sont présentées dans des articles distincts.

## <a name="design-concepts"></a>Principes de conception

L’utilisation d’un stylet pour l’entrée présente les caractéristiques suivantes :

-   **Naturel et intuitif.** Tout le monde sait comment pointer et appuyer avec un stylet. Les interactions entre objets sont conçues pour correspondre à la façon dont les utilisateurs interagissent avec les objets dans le monde réel de manière cohérente.
-   **Expressif.** Les traits d’un stylet sont faciles à contrôler, ce qui facilite l’écriture, le dessin, l’esquisse, la peinture et l’annotation.
-   **Plus personnel.** Tout comme une note manuscrite ou une signature est plus personnelle qu’une note d’écriture, l’utilisation d’une note ou d’une signature manuscrite est également plus personnelle.
-   **Moins intrusif.** L’utilisation d’un stylet est silencieuse et, par conséquent, bien moins gênante que la saisie ou le clic, en particulier dans des situations sociales telles que des réunions.
-   **Portatif.** Un ordinateur avec une fonctionnalité de stylet peut être plus compact, car la plupart des tâches peuvent être effectuées sans clavier, souris ou pavé tactile. Il peut être plus flexible, car il ne nécessite pas de surface de travail. Il permet de nouveaux emplacements et scénarios d’utilisation d’un ordinateur.
-   **Directe et attrayante.** L’utilisation d’un stylet vous donne l’impression d’interagir directement avec les objets à l’écran, tandis que l’utilisation d’une souris ou d’un pavé tactile vous oblige toujours à coordonner les mouvements de main avec des mouvements de pointeur à l’écran distincts, ce qui est indirect par comparaison.

**Tous les programmes Windows doivent avoir une bonne expérience Pen.** Les utilisateurs doivent être en mesure d’effectuer efficacement les tâches les plus importantes de votre programme à l’aide d’un stylet. Certaines tâches, telles que la saisie ou la manipulation de pixels détaillée, ne sont pas appropriées pour un stylet, mais elles doivent être au moins possibles.

Heureusement, si votre programme est déjà bien conçu et qu’il est convivial, la prise en charge d’un bon stylet est facile à faire. À cet effet, il s’agit d’un programme bien conçu :

-   **Offre une bonne prise en charge de la souris.** Les contrôles interactifs ont des intuitivité clairs et visibles, et ont des États de pointage pour les commentaires des pointeurs. Les objets ont des comportements standard pour les interactions de souris standard (simple et double-clic, cliquer avec le bouton droit, faire glisser et pointer). La [forme du pointeur](inter-mouse.md) change en fonction des besoins pour indiquer le type de manipulation directe.
-   **Offre une bonne prise en charge du clavier.** Le programme améliore l’efficacité des utilisateurs en fournissant des affectations de touches de raccourci standard, en particulier pour les commandes de navigation et de modification qui peuvent également être générées par le biais de gestes.
-   **Dispose de contrôles suffisamment grands pour toucher.** Les contrôles ont une taille minimale de 23x23 pixels (unités de boîte de dialogue 13x13 \[ \] ) et les contrôles les plus couramment utilisés sont au moins 40 x 40 pixels (23x22). Pour éviter tout comportement qui ne répond pas, il ne doit y avoir aucun petit intervalle entre les cibles. les éléments de l’interface utilisateur doivent être espacés afin que les cibles adjacentes soient en contact ou qu’elles aient au moins 5 pixels (3 unités de mémoire) de l’espace entre eux.
-   **Est accessible.** Utilise Microsoft Active Accessibility (MSAA) pour fournir un accès par programme à l’interface utilisateur pour les technologies d’assistance. Le programme répond correctement aux modifications des mesures du thème et du système.
-   **Fonctionne correctement et semble correct en 120 ppp (points par pouce),** qui est la résolution d’affichage par défaut recommandée pour les ordinateurs avec stylet.
-   **Utilise des contrôles communs.** La plupart des contrôles courants sont conçus pour prendre en charge une bonne expérience de stylet. Si nécessaire, le programme utilise des contrôles personnalisés correctement implémentés qui sont conçus pour prendre en charge le ciblage facile et la manipulation interactive.
-   **Utilise des contrôles limités.** Lorsqu’il est conçu pour un ciblage facile, les contrôles restreints comme les listes et les curseurs peuvent être mieux que des contrôles non restreints comme des zones de texte, car ils réduisent le besoin d’entrée de texte.
-   **Fournit les valeurs par défaut appropriées.** Le programme sélectionne le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée par défaut. Si la sécurité et la sécurité ne sont pas des facteurs, le programme sélectionne l’option la plus probable ou la plus pratique, ce qui évite toute interaction inutile.
-   **Fournit la saisie semi-automatique du texte.** Fournit une liste des valeurs d’entrée les plus probables ou récentes pour faciliter grandement la saisie de texte.

Malheureusement, l’inverse est également vrai si votre programme n’est pas bien conçu, ses lacunes sont particulièrement évidentes pour les utilisateurs qui utilisent un stylet.

### <a name="model-for-pen-interaction"></a>Modèle d’interaction du stylet

Si vous n’êtes pas familiarisé avec l’utilisation d’un stylet, la meilleure introduction consiste à apprendre. Procurez-vous un ordinateur avec stylet, mettez la souris et le clavier de côté, puis effectuez les tâches que vous utilisez normalement à l’aide d’un simple stylet. Veillez à essayer les deux programmes avec écriture manuscrite, tels que le journal Windows, et les programmes qui ne sont pas compatibles avec l’écriture manuscrite. Si vous avez un Tablet PC, expérimentez-le à des endroits différents, par exemple sur votre genoux, sur un tableau ou dans vos bras pendant que vous êtes debout. Essayez de l’utiliser en orientation portrait et paysage, en maintenant le stylet pour l’écriture et uniquement pour le pointage, à gauche et à droite.

À mesure que vous expérimentez l’utilisation d’un stylet, vous découvrirez ce qui suit :

-   **Les petits contrôles sont difficiles à utiliser.** La taille des contrôles a un impact considérable sur votre capacité à interagir efficacement. Les contrôles qui sont 10x10 pixels fonctionnent raisonnablement pour un stylet, mais les contrôles les plus grands sont encore plus confortables à utiliser. Par exemple, les [contrôles spin](ctrl-spin-controls.md) (15x11 pixels) sont trop petits pour être facilement utilisés avec un stylet.
-   **La main est un facteur.** Votre main présente parfois des choses que vous pouvez souhaiter voir ou manipuler. Par exemple, pour que les menus contextuels des utilisateurs droitiers soient difficiles à utiliser s’ils apparaissent à droite du point de clic, il est préférable qu’ils apparaissent sur la gauche. Windows permet aux utilisateurs d’indiquer leur droitier dans l’élément du panneau de configuration paramètres du Tablet PC.
-   **La localité des tâches aide.** Bien que vous puissiez déplacer le pointeur sur un écran de 14 pouces avec un mouvement de souris de 3 cm, l’utilisation d’un stylet vous oblige à déplacer la main sur la pleine de 14 pouces. Le déplacement répété entre des cibles éloignées peut être fastidieux, c’est pourquoi il est préférable de conserver les interactions entre les tâches dans la plage d’une main à chaque fois que cela est possible. Les menus contextuels sont pratiques, car ils ne nécessitent pas de déplacement à la main.
-   **L’entrée et la sélection de texte sont difficiles.** Une entrée de texte longue est particulièrement difficile à utiliser un stylet, de sorte que la saisie semi-automatique et les valeurs de texte par défaut acceptables peuvent vraiment simplifier les tâches. La sélection de texte peut également être assez difficile. les tâches sont donc plus faciles quand elles n’ont pas besoin d’un positionnement de curseur précis.
-   **Les petites cibles près du bord de l’écran peuvent être très difficiles à appuyer.** Certains panneaux d’affichage sont saillants et certaines technologies de l’écran tactile sont moins sensibles aux bords, ce qui rend les contrôles à proximité de la périphérie plus difficiles à utiliser. Par exemple, les boutons réduire, agrandir/restaurer et fermer de la barre de titre peuvent être plus difficiles à utiliser lorsqu’une fenêtre est agrandie.

### <a name="control-location"></a>Emplacement du contrôle

La localité des tâches réduit les mouvements de l’écran répétés fastidieux. Pour réduire les mouvements de main, localisez les contrôles près de l’endroit où ils vont probablement être utilisés.

**Incorrect :**

![capture d’écran de la palette de couleurs séparée des outils ](images/inter-pen-image3.png)

Dans cet exemple de Windows XP, la palette de couleurs est trop éloignée de l’endroit où elle est susceptible d’être utilisée.

Supposons que l’emplacement actuel de l’utilisateur est le plus proche possible, ce qui le rend facile à acquérir. Ainsi, les menus contextuels tirent pleinement parti de la [Loi de Fitts](inter-mouse.md), tout comme les mini-barres d’outils utilisées par Microsoft Office.

![capture d’écran des pointeurs près des menus ](images/inter-pen-image4.png)

L’emplacement du pointeur actuel est toujours le plus facile à acquérir.

Les petites cibles près du bord d’affichage peuvent être difficiles à cibler. Évitez donc de placer de petits contrôles près des bords de la fenêtre. Pour vous assurer que les contrôles sont faciles à cibler quand une fenêtre est agrandie, faites-en au moins 23x23 pixels (13x13), ou placez-les en dehors du bord de la fenêtre.

### <a name="pen-interactions"></a>Interactions du stylet

**Gestes système**

Les gestes système sont définis et gérés par Windows. Par conséquent, tous les programmes Windows y ont accès. Ces gestes ont des messages de commande équivalents de souris, de clavier et d’application :



| Mouvement système                                                           | Message équivalent synthétisé                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Pointage (en cas de prise en charge)<br/>                          | Pointage de la souris<br/>                        |
| Appuyer (vers le haut et vers le haut)<br/>                               | Cliquer avec le bouton gauche de la souris<br/>                   |
| Double appui (vers le haut et vers le haut)<br/>                  | Double-clic de la souris<br/>            |
| Maintenez la touche enfoncée (enfoncée, pause, haut)<br/>                | Clic droit de la souris<br/>                  |
| Glisser (vers le haut, vers le haut, vers le haut)<br/>                           | Souris-faire glisser vers la gauche<br/>                    |
| Appuyer, maintenir et faire glisser (descendre, suspendre, déplacer, haut)<br/>   | Souris-faire glisser avec la souris<br/>                   |
| Sélectionner (vers le haut, déplacer vers les objets sélectionnables, vers le haut)<br/> | Sélection de la souris<br/>                       |



 

**Développeurs :** Pour plus d’informations, consultez [énumération SystemGesture](/previous-versions/ms552724(v=vs.100)).

**Les raccourcis**

Les raccourcis sont des mouvements simples qui sont à peu près l’équivalent des raccourcis clavier. Les raccourcis de navigation incluent glisser vers le haut, glisser vers le bas, déplacer vers l’arrière et avancer. Les raccourcis de modification sont les suivants : copier, coller, annuler et supprimer. Pour utiliser les raccourcis, votre programme doit uniquement répondre aux commandes de touches associées.

![Diagramme qui affiche des mouvements de raccourcis et leurs assignations par défaut dans Windows 7.](images/inter-pen-image5.png)

Les huit mouvements de raccourcis et leurs affectations par défaut dans Windows 7. Les raccourcis de navigation ont été modifiés pour correspondre à la panoramisation (où l’objet se déplace avec le geste) au lieu de faire défiler (où l’objet se déplace dans la direction opposée du geste).

![Figure des mouvements de raccourci tels que le mouvement de déplacement ](images/inter-pen-image6.png)

Les huit mouvements de raccourcis et leurs affectations par défaut dans Windows Vista.

Les raccourcis de navigation ont un mappage naturel, de sorte qu’ils sont faciles à apprendre et à mémoriser. Les raccourcis de modification sont des diagonales qui requièrent plus de précision et leurs mappages ne sont pas aussi naturels (le raccourci vers la Corbeille pour la suppression, le mouvement de la flèche vers la droite pour annuler), donc ils ne sont pas activés par défaut. Toutes les actions de raccourci peuvent être personnalisées à l’aide de l’élément du panneau de configuration stylet et périphériques d’entrée.



| Raccourci                                     | Message équivalent synthétisé                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Raccourci vers la gauche<br/>                | Commande Forward (commande back pour Windows Vista)<br/> |
| Raccourci vers la droite<br/>               | Commande Back (commande Forward pour Windows Vista)<br/> |
| Raccourci vers le haut<br/>                  | Défilement au clavier vers le dessous<br/>                             |
| Raccourci vers le<br/>                | Défilement du clavier vers le haut<br/>                               |
| Panoramique vers le haut-diagonale gauche<br/>    | Suppression du clavier<br/>                                  |
| Raccourci vers le dessous de la diagonale gauche<br/>  | Annulation du clavier<br/>                                    |
| Panoramique vers le haut-diagonale droite<br/>   | Copie du clavier<br/>                                    |
| Déplacement vers le dessous-Diagonal vers la droite<br/> | Coller par le clavier<br/>                                   |



 

**Mouvements d’application**

Les applications peuvent également définir et gérer d’autres gestes. Le module de reconnaissance de mouvement Microsoft peut reconnaître plus de [40 mouvements](../tablet/application-gestures-and-semantic-behavior.md). Pour utiliser des mouvements d’application, votre programme doit définir les gestes qu’il reconnaît, puis gérer les événements résultants.

**Réactivité et cohérence**

**La réactivité est essentielle pour créer des expériences de stylet qui semblent directes et attrayantes.** Pour faire en sorte que les gestes soient directs, les gestes doivent prendre effet immédiatement et les points de contact d’un objet doivent rester en douceur dans le stylet tout au long du mouvement. Tout décalage, réponse hachée, perte de contact ou résultats inexacts détruit la perception de la manipulation directe et de la qualité.

**La cohérence est essentielle pour créer des expériences de stylet qui semblent naturelles et intuitives.** Une fois que les utilisateurs apprennent un mouvement standard, ils s’attendent à ce que le mouvement ait le même effet sur tous les programmes applicables. Pour éviter toute confusion et frustration, n’assignez jamais de significations non standard aux gestes standard. Utilisez plutôt des mouvements personnalisés pour les interactions propres à votre programme.

**Modification de l’encre et du texte**

La modification de l’encre et du texte se trouve parmi les interactions les plus difficiles lors de l’utilisation d’un stylet. L’utilisation de contrôles limités, de valeurs par défaut appropriées et de la saisie semi-automatique, élimine ou réduit la nécessité d’entrer du texte. Toutefois, si votre programme implique la modification du texte ou de l’encre, **vous pouvez améliorer la productivité des utilisateurs en zoomant automatiquement l’interface utilisateur d’entrée jusqu’à 150% par défaut lorsqu’un stylet est utilisé.**

Par exemple, un programme de messagerie peut afficher l’interface utilisateur à sa taille normale, mais zoomer l’interface utilisateur d’entrée sur 150% pour composer des messages.

![capture d’écran du message Outlook en grande police ](images/inter-pen-image7.png)

Dans cet exemple, l’interface utilisateur d’entrée est zoomée sur 150 pour cent.

**Si vous ne faites que quatre choses...**

1.  1. Faites de vos programmes Windows une bonne expérience PEN ! Les utilisateurs doivent être en mesure d’effectuer efficacement les tâches les plus importantes de votre programme à l’aide d’un stylet (au moins les tâches qui n’impliquent pas un grand nombre de frappes ou une manipulation de pixels détaillée).
2.  2. Pensez à ajouter la prise en charge de l’écriture, du dessin et de l’ajout de commentaires directement à l’aide de l’encre dans les scénarios les plus pertinents.
3.  3. Pour créer une expérience directe et attrayante, les gestes peuvent être appliqués immédiatement, conserver les points de contact avec le stylet de l’utilisateur sans heurts tout au long du mouvement et avoir l’effet de la carte de mouvement directement sur le mouvement de l’utilisateur.
4.  4. Pour créer une expérience naturelle et intuitive, prenez en charge les gestes standard appropriés et affectez-leur les significations standard. Utilisez des mouvements personnalisés pour les interactions propres à votre programme.

## <a name="guidelines"></a>Consignes

### <a name="control-usage"></a>Utilisation du contrôle

-   **Préférer l’utilisation de contrôles communs.** La plupart des contrôles courants sont conçus pour prendre en charge une bonne expérience de stylet.
-   **Préférer les contrôles restreints.** Utilisez des contrôles restreints comme les listes et les curseurs dans la mesure du possible, au lieu de contrôles non restreints comme des zones de texte, afin de réduire le besoin d’entrée de texte.
-   **Fournissez les valeurs par défaut appropriées.** Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée par défaut. Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez l’option la plus probable ou la plus pratique, en éliminant ainsi toute interaction inutile.
-   **Indiquez la saisie semi-automatique du texte.** Fournissez une liste de valeurs d’entrée les plus probables ou récentes pour faciliter grandement la saisie de texte.
-   **Pour les tâches importantes qui utilisent une sélection multiple, si une liste de sélection multiple standard est normalement utilisée, fournissez une option pour utiliser une liste de cases à cocher à la place.**
-   **Respectez les mesures système.** Utilisez des métriques système pour toutes les tailles qui ne sont pas des tailles d’unimères. Si nécessaire, les utilisateurs peuvent modifier les métriques du système ou les PPP en fonction de leurs besoins. Toutefois, considérez ceci comme un dernier recours, car les utilisateurs ne doivent pas normalement ajuster les paramètres système pour rendre l’interface utilisateur utilisable.

![capture d’écran des menus avec un dimensionnement normal et grand ](images/inter-pen-image8.png)

Dans cet exemple, la métrique système pour la hauteur de menu a été modifiée.

### <a name="control-sizing-layout-and-spacing"></a>Contrôler le dimensionnement, la disposition et l’espacement

-   **Pour les contrôles communs, utilisez les tailles de contrôle recommandées.** Celles-ci sont suffisamment grandes pour une bonne expérience de stylet, à l’exception des contrôles spin (qui ne sont pas utilisables avec un stylet mais sont redondants).
-   **Choisissez une disposition qui place les contrôles à proximité de l’endroit où ils vont probablement être utilisés.** Dans la mesure du possible, conservez les interactions entre les tâches dans une petite zone. Évitez les déplacements à distance longue, en particulier pour les tâches courantes et les opérations de glisser-déplacer.
-   **Utilisez l’espacement recommandé.** L’espacement recommandé est convivial.
-   **Les contrôles interactifs doivent être en contact ou avoir de préférence au moins 5 pixels (3 dlu) d’espace entre eux.** Cela évite toute confusion quand les utilisateurs appuient en dehors de la cible prévue.
-   **Envisagez d’ajouter plus que l’espacement vertical recommandé dans des groupes de contrôles,** tels que des liens de commande, des cases à cocher et des cases d’option, ainsi qu’entre les groupes. Cela les rend plus faciles à distinguer.

### <a name="interaction"></a>Interaction

-   **Pour les programmes conçus pour accepter l’écriture manuscrite, activez l’entrée par défaut.** L’encrage par défaut permet aux utilisateurs d’entrer de l’encre en commençant simplement à écrire, sans avoir à appuyer sur, à fournir une commande ou à faire quelque chose de spécial. Cela permet d’obtenir une expérience plus naturelle avec un stylet. Pour les programmes qui ne sont pas conçus pour accepter l’écriture manuscrite, gérez l’entrée de stylet dans les zones de texte comme sélection.
-   **Autoriser les utilisateurs à effectuer un zoom sur l’interface utilisateur du contenu** si votre programme a des tâches qui requièrent la modification de texte. Vous pouvez effectuer un zoom automatique sur 150 pour cent lorsqu’un stylet est utilisé.
-   **Étant donné que les gestes sont mémorisés, attribuez-leur des significations cohérentes entre les programmes.** N’attribuez pas des significations différentes aux gestes avec une sémantique fixe. Utilisez plutôt un geste approprié propre au programme.

### <a name="handedness"></a>Ergonomie

-   **Si une fenêtre est contextuelle, affichez-la toujours près de l’objet à partir duquel elle a été lancée.** Placez-le en dehors de la façon dont l’objet source n’est pas couvert par la fenêtre.
    -   S’il est affiché à l’aide de la souris, lorsque cela est possible, placez le décalage de la fenêtre contextuelle vers le dessous et vers la droite.

        ![figure de la fenêtre contextuelle placée à droite de l’objet ](images/inter-pen-image9.png)

        Afficher les fenêtres contextuelles près de l’objet à partir duquel elle a été lancée.

    -   S’il est affiché à l’aide d’un stylet, lorsque cela est possible, placez la fenêtre contextuelle de sorte qu’elle ne soit pas couverte par la main de l’utilisateur. Pour les utilisateurs droitiers, afficher à gauche ; Sinon, s’affiche à droite.

        ![figure de la fenêtre contextuelle placée à gauche de l’objet ](images/inter-pen-image10.png)

        Lorsque vous utilisez un stylet, affichez également des fenêtres contextuelles afin qu’elles ne soient pas couvertes par la main de l’utilisateur.

-   **Développeurs :** Vous pouvez faire la distinction entre les événements de souris et les événements de stylet à l’aide de l’API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Vous pouvez déterminer la [gauche](/previous-versions/ms819495(v=msdn.10)) de l’utilisateur à l’aide de l’API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Effacement

-   **Fournissez une commande Annuler.** Dans l’idéal, vous devez fournir une annulation pour toutes les commandes, mais votre programme peut comporter des commandes dont l’effet ne peut pas être annulé.
-   **Fournir des commentaires de pointage corrects.** Indiquez clairement quand le stylet est sur une cible cliquable. Ces commentaires sont un excellent moyen d’éviter toute manipulation accidentelle.
-   **Chaque fois que cela est possible, fournissez de bons commentaires sur le stylet, mais ne prenez pas d’actions avant un déplacement ou un stylet.** Cela permet aux utilisateurs de corriger les erreurs avant de les créer.
-   **Chaque fois que cela est possible, autorisez les utilisateurs à corriger facilement les erreurs.** Si une action prend effet au niveau du stylet, autorisez les utilisateurs à corriger les erreurs en faisant glisser le stylet lorsque le stylet est toujours en cours d’exécution.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à l’entrée de stylet :

-   Reportez-vous à un appareil d’entrée de stylet en forme de stylet. Sur la première mention, utilisez le stylet du Tablet PC.
-   Reportez-vous au bouton situé à côté d’un stylet en tant que bouton stylet, pas au bouton en forme de plume.
-   Faites référence au clavier, à la souris, au trackball, au stylet ou au doigt en tant qu’appareil d’entrée de façon générique.
-   Utilisez le TAP (et le double-clic) au lieu de cliquer pour documenter les procédures spécifiques à l’utilisation d’un stylet. TAP signifie que vous appuyez sur l’écran, puis soulevez avant une durée de suspension. Elle peut ou non être utilisée pour générer un clic de souris. Pour les interactions qui n’impliquent pas le stylet, continuez à utiliser le clic.

