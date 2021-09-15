---
title: Glossaire (concepts de base de la conception)
description: glossaire des termes utilisés dans les instructions d’expérience utilisateur pour les applications de bureau Windows.
ms.assetid: 9f35f9be-6165-4d98-a2e6-26fb4fc91eae
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3009940612d0b42ae8ee225e8db59ebabdbf35fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295986"
---
# <a name="glossary-design-basics"></a>Glossaire (concepts de base de la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

[A](#alink) \| [B](#b) \| [C](#c) \| [D](#d) \| [e](#e) \| [F](#f) \| [G](#g) \| [H](#h) \| [I](#i) \| [J](#j) \| [K](#k) \| [L](#l) \| [M](#m)\|

[N](#n) \| [O](#o) \| [P](#p) \| [Q](#q) \| [R](#r) \| [](#s) \| [T](#t) \| [U](#u) \| [V](#v) \| [W](#w) \| [X](#x) \| [Y](#y) \| [Z](#z)

## <a name=""></a><a name="alink">A</a>

**Boîte à propos**

Boîte de dialogue fournissant des informations générales sur le programme, telles que l’identification de la version, le Copyright, les contrats de licence et les moyens d’accéder au support technique.

**au-dessus du pli**

Métaphore de la disposition d’écran tirée du journal journalisme. Le contenu au-dessus de la pliure du journal doit être particulièrement attrayant pour les ventes. De même, dans la disposition de l’écran, le contenu le plus important doit être visible sans défilement. Les utilisateurs doivent être motivés à prendre le temps de faire défiler le contenu qu’ils rencontrent initialement « au-dessus du pli ».

**clé d’accès**

Touche alphanumérique qui, lorsqu’elle est combinée avec la touche Alt, active un contrôle. Les touches d’accès sont indiquées par un soulignement de l’un des caractères de l’étiquette du contrôle. Par exemple, en appuyant sur Alt + O, vous activez un contrôle dont l’étiquette est « Open » et dont la clé d’accès est « O ». Les clés d’accès ne respectent pas la casse. L’effet de l’activation d’un contrôle dépend du type de contrôle.

Contrairement aux touches de raccourci, qui sont principalement destinées aux utilisateurs expérimentés, les clés d’accès sont conçues pour améliorer l’accessibilité. Étant donné qu’elles sont documentées directement dans l’interface utilisateur proprement dite, elles ne peuvent pas toujours être affectées de manière cohérente et ne sont pas destinées à être mémorisées.

**moniteur actif**

Analyse où le programme actif est en cours d’exécution.

**barre d’adresses**

Élément de navigation, généralement apparaissant en haut d’une fenêtre, qui affiche et permet aux utilisateurs de modifier leur emplacement actuel. Voir aussi : [barre de navigation](#b).

**offre**

Propriétés visuelles d’un objet qui indiquent comment il peut être utilisé ou traité. Par exemple, les boutons de commande ont l’apparence visuelle des boutons réels, suggérant un push ou un clic.

**application**

Programme utilisé pour effectuer un ensemble connexe de tâches utilisateur ; souvent relativement complexes et sophistiqués. Voir aussi : [programme](#p).

**clé d’application**

Touche du clavier avec un menu contextuel. Cette clé est utilisée pour afficher le menu contextuel de l’élément sélectionné.

**menu de l’application**

Contrôle qui présente un menu de commandes qui impliquent d’effectuer des opérations dans ou avec un document ou un espace de travail, tel que des commandes associées aux fichiers.

Affiche le menu contextuel de la sélection actuelle (identique à la combinaison de touches MAJ + F10).

**application de thèmes**

À l’aide de techniques visuelles associées, telles que des contrôles personnalisés, pour créer une apparence ou une personnalisation unique pour une application.

**proportions**

Expression de la relation entre la largeur d’un objet et sa hauteur. Par exemple, la télévision haute définition utilise un proportions de 16:9.

**saisie semi-automatique**

Type de liste utilisé dans les zones de texte et liste déroulante modifiable dans laquelle l’entrée probable peut être extrapolée et remplie automatiquement à partir de l’entrée précédente. Les utilisateurs tapent une quantité minimale de texte pour remplir la liste de saisie semi-automatique.

**fermeture automatique**

Zone de texte dans laquelle le focus d’entrée passe automatiquement à la zone de texte associée suivante dès qu’un utilisateur tape le dernier caractère.

## <a name="b"></a>B

**forfaitaire**

contrôle de Windows commun qui informe les utilisateurs d’un problème non critique ou d’une condition spéciale.

**barre de navigation**

Élément de navigation, généralement apparaissant en haut d’une fenêtre, qui affiche et permet aux utilisateurs de modifier leur emplacement actuel. « Breadcrumb » fait référence à la Division de l’emplacement actuel en une série de liens séparés par des flèches que les utilisateurs peuvent manipuler directement. Utilisez la barre d’adresses à la place. Voir aussi : [barre d’adresses](#alink).

## <a name="c"></a>C

**case à cocher**

contrôle de Windows commun qui permet aux utilisateurs de choisir entre des choix manifestement différents, tels que l’activation ou la désactivation d’une option.

**ouvrant**

Un petit contrôle ou bouton qui indique qu’il y a plus d’éléments qu’il n’est possible d’afficher dans l’espace alloué. Les utilisateurs cliquent sur le Chevron pour afficher les éléments supplémentaires.

**fenêtre enfant**

Une fenêtre, telle qu’un contrôle ou un volet, contenue entièrement dans une autre fenêtre, appelée fenêtre parente. Voir aussi : [fenêtre parente](#p), [fenêtre propriétaire](#o).

**désactivé**

Dans une case à cocher, indique que l’option n’est pas définie. Voir aussi : [État mixte](#m) [sélectionné](#s).

**zone de liste déroulante**

contrôle de Windows commun qui combine les caractéristiques d’une liste déroulante ou d’une zone de liste standard, et une zone de texte modifiable. Voir aussi : [zone de liste](#l), [liste déroulante](#d).

**zone de commande**

Zone dans une fenêtre où se trouvent les boutons de validation. En règle générale, les boîtes de dialogue et les assistants ont une zone de commande. Voir aussi : bouton valider.

**bouton de commande**

contrôle de Windows commun qui permet aux utilisateurs de lancer immédiatement une action.

**lien de commande**

Contrôle utilisé pour faire un choix parmi un ensemble de choix associés s’excluant mutuellement. Dans leur état normal, les liens de commande ont une apparence légère similaire à celle des liens hypertexte, mais leur comportement est plus semblable aux boutons de commande.

**bouton valider**

Bouton de commande utilisé pour valider une tâche, passer à l’étape suivante d’une tâche à plusieurs étapes ou annuler une tâche. Voir aussi : zone de commande.

**page de validation**

Type de page d’assistant dans laquelle les utilisateurs s’engagent à effectuer la tâche. Après cela, la tâche ne peut pas être annulée en cliquant sur les boutons précédent ou annuler.

**page dernière étape**

Page d’Assistant utilisée pour indiquer la fin d’un Assistant. Parfois utilisé à la place des pages de félicitations. Voir aussi : page félicitations.

**page félicitations**

Page d’Assistant utilisée pour indiquer la fin d’un Assistant. Ces pages ne sont plus recommandées. Les assistants se terminent plus efficacement avec une page de validation ou, si nécessaire, une page de suivi ou de fin. Voir aussi : page validation, page dernière étape, [page de suivi](#f).

**Interface utilisateur de consentement**

Boîte de dialogue utilisée par le contrôle de compte d’utilisateur (UAC) qui permet aux administrateurs protégés d’élever temporairement leurs privilèges.

**contrainte**

Dans les contrôles qui impliquent une entrée d’utilisateur, tels que des zones de texte, les contraintes d’entrée sont un moyen utile d’éviter les erreurs. Par exemple, si la seule entrée valide pour un contrôle particulier est numérique, le contrôle peut utiliser les contraintes de valeur appropriées pour appliquer cette exigence.

**zone de contenu**

La partie des surfaces de l’interface utilisateur, telles que les boîtes de dialogue, les éléments du panneau de configuration et les assistants, consacrée à la présentation des options, à la fourniture d’informations et à la description des contrôles. Distingué de la zone de commande, du volet de tâches et de la zone de navigation.

**onglet contextuel**

Onglet contenant une collection de commandes qui sont pertinentes uniquement lorsque l’utilisateur a sélectionné un type d’objet particulier. Voir aussi : [ruban](#r).

**Panneau de configuration**

Windows programme qui collecte et affiche pour les utilisateurs les fonctionnalités au niveau du système de l’ordinateur, y compris l’installation et la configuration du matériel et des logiciels. Dans le panneau de configuration, les utilisateurs peuvent cliquer sur des éléments individuels pour configurer des fonctionnalités au niveau du système et effectuer des tâches associées. Voir aussi : élément du panneau de configuration.

**élément du panneau de configuration**

Une fonctionnalité individuelle disponible dans le panneau de configuration. Par exemple, les programmes et la facilité d’accès sont deux éléments du panneau de configuration.

**Interface utilisateur des informations d’identification**

Boîte de dialogue utilisée par le contrôle de compte d’utilisateur (UAC) qui permet aux utilisateurs standard de demander une élévation temporaire de leurs privilèges.

**critique**

Degré de gravité le plus élevé. Par exemple, dans les messages d’erreur et d’avertissement, les circonstances critiques peuvent impliquer la perte de données, la perte de confidentialité ou la perte de l’intégrité du système.

**icône personnalisée**

représentation graphique propre à un programme (par opposition à une icône de système Windows).

**visuels personnalisés**

Les graphiques, les animations, les icônes et d’autres éléments visuels spécialement développés pour un programme.

## <a name="d"></a>D

**lien ou bouton de commande par défaut**

Le bouton de commande ou le lien qui est appelé quand les utilisateurs appuient sur la touche entrée. Le bouton ou le lien de commande par défaut est assigné par le développeur, mais un bouton de commande ou un lien devient la valeur par défaut lorsque l’utilisateur clique sur l’onglet utilisateurs.

**moniteur par défaut**

analyse avec la menu Démarrer, la barre des tâches et la zone de notification.

**modèle de validation différée**

Modèle de validation utilisé par les pages spoke de l’élément du panneau de configuration, où les modifications ne sont pas apportées jusqu’à ce que les utilisateurs cliquent explicitement sur un bouton de validation. Ainsi, les utilisateurs peuvent abandonner une tâche, naviguer à l’aide du bouton précédent, fermer ou la barre d’adresses. Voir aussi : [modèle de validation immédiate](#i).

**écran**

la zone de travail à l’écran fournie par Windows, analogue à un bureau physique. Voir aussi : [zone de travail](#w).

**commande destructrice**

Action qui a un effet étendu et qui ne peut pas être annulée facilement, ou qui n’est pas immédiatement perceptible.

**volet d’informations**

volet en bas d’une fenêtre de l’explorateur de Windows qui affiche des détails (le cas échéant) sur les éléments sélectionnés ; dans le cas contraire, il affiche des détails sur le dossier. par exemple, Windows galerie de photos affiche le nom de l’image, le type de fichier, la date de prise, les balises, l’évaluation, les dimensions et la taille du fichier. Voir aussi : [volet de visualisation](#p).

**boîte de dialogue**

Une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question ou fournit aux utilisateurs des informations ou des commentaires sur la progression.

**lanceur de boîte de dialogue**

Dans un ruban, bouton en bas de certains groupes qui ouvre une boîte de dialogue avec les fonctionnalités associées au groupe. Voir aussi : [ruban](#r).

**unité de boîte de dialogue**

Une unité de boîte de dialogue (DLU) est la mesure indépendante du périphérique à utiliser pour la disposition basée sur la police système actuelle.

**manipulation directe**

Interaction directe entre l’utilisateur et les objets de l’interface utilisateur (tels que les icônes, les contrôles et les éléments de navigation). La souris et l’effleurement sont des méthodes courantes de manipulation directe.

**fenêtre ancrée**

Fenêtre qui apparaît à un emplacement fixe sur le bord de sa fenêtre propriétaire. Voir aussi : [fenêtre flottante](#f).

**flèche déroulante**

Flèche associée à des listes déroulantes, des zones de liste modifiable, des boutons partagés et des boutons de menu, indiquant que les utilisateurs peuvent afficher la liste associée en cliquant sur la flèche.

**liste déroulante**

contrôle de Windows commun qui permet aux utilisateurs de sélectionner parmi une liste de valeurs s’excluant mutuellement. Contrairement à une zone de liste, cette liste de choix disponibles est normalement masquée.

## <a name="e"></a>E

**résolution efficace**

Résolution physique d’une analyse normalisée par le paramètre ppp (points par pouce) actuel. À 96 ppp, la résolution effective est la même que la résolution physique, mais dans d’autres DPI, la résolution effective doit être mise à l’échelle proportionnellement. En règle générale, la résolution effective peut être calculée à l’aide de l’équation suivante :

Résolution effective = résolution physique x (96/paramètre PPP actuel)

Voir aussi : [pixels relatifs](#r), [résolution physique](#p).

**administrateur avec élévation de privilèges**

Dans le contrôle de compte d’utilisateur, les administrateurs élevés disposent de leurs privilèges d’administrateur. Sans élévation, les administrateurs s’exécutent dans leur état le moins privilégié. La boîte de dialogue de consentement de l’interface utilisateur est utilisée pour élever l’état des administrateurs uniquement lorsque cela est nécessaire. Voir aussi : [administrateur protégé](#p), [utilisateur standard](#s).

**info-bulle améliorée**

Fenêtre contextuelle qui décrit de façon concise la commande désignée. Comme les info-bulles classiques, les info-bulles améliorées peuvent fournir la touche de raccourci de la commande. Mais contrairement aux info-bulles classiques, elles peuvent également fournir des informations supplémentaires, des graphiques et un indicateur permettant d’obtenir de l’aide. Ils peuvent également utiliser du texte enrichi et des séparateurs. Voir aussi : [info-bulle](#t).

**error**

État dans lequel un problème s’est produit. Voir aussi : [Avertissement](#w).

**en-têtes extensibles**

Modèle de Chevron de divulgation progressive dans lequel un en-tête peut être développé ou réduit pour afficher ou masquer un groupe d’éléments. Voir aussi : [Divulgation progressive](#p).

**sélection étendue**

Dans les affichages de liste et les zones de liste, un mode de sélection multiple dans lequel vous pouvez étendre la sélection d’un seul élément en faisant glisser ou en appuyant sur Maj + clic ou Ctrl + clic pour sélectionner respectivement des groupes de valeurs contiguës ou non adjacentes. Voir aussi : [sélection multiple](#m).

## <a name="f"></a>F

**raccourci**

Trait rapide et droit d’un doigt ou d’un stylet sur un écran. Un raccourci est reconnu comme un geste et interprété comme une navigation ou une commande de modification.

**fenêtre flottante**

Fenêtre qui peut apparaître n’importe où sur l’écran souhaité par l’utilisateur. Voir aussi : [fenêtre ancrée](#d).

**volant**

Fenêtre contextuelle qui affiche temporairement plus d’informations. sur le bureau Windows, les lanceurs s’affichent en cliquant sur un gadget et sont ignorés en cliquant n’importe où en dehors du lanceur. Vous pouvez utiliser des lanceurs à la fois dans les États ancré et flottant.

**page de suivi**

Page de l’Assistant utilisée pour présenter les tâches associées que les utilisateurs sont susceptibles de faire comme suivi. Parfois utilisé à la place des pages de félicitations.

**son**

Ensemble d’attributs pour les caractères de texte.

**plein écran**

Fenêtre agrandie qui n’a pas de cadre.

## <a name="g"></a>G

**Gadget**

Mini-application simple hébergée sur le Bureau de l’utilisateur. Voir aussi : [encadré](#s).

**Office**

Liste des commandes ou options présentées graphiquement. Une galerie basée sur les résultats illustre l’effet des commandes ou des options à la place des commandes elles-mêmes. Peut être étiqueté ou groupé. Par exemple, les options de mise en forme peuvent être présentées dans une galerie de miniatures.

**mouvement**

Mouvement rapide d’un doigt ou d’un stylet sur un écran que l’ordinateur interprète comme une commande, plutôt qu’en tant que déplacement de la souris, écriture ou dessin.

**page mise en route**

Une page d’Assistant facultative qui décrit la configuration requise pour l’exécution de l’Assistant ou explique l’objectif de l’Assistant.

**reflet**

Option de cadre de fenêtre caractérisée par translucence, qui aide les utilisateurs à se concentrer sur le contenu et les fonctionnalités plutôt que sur l’interface qui les entoure.

**variante**

Terme générique utilisé pour faire référence à n’importe quel graphique ou image symbolique. Les flèches, les chevrons et les puces sont des glyphes couramment utilisés dans Windows.

**zone de groupe**

contrôle de Windows commun qui affiche des relations entre un ensemble de contrôles connexes.

## <a name="h"></a>H

**reconnaissance de l’écriture manuscrite**

Logiciel qui convertit l’entrée manuscrite en texte.

**Aide**

Assistance utilisateur d’une nature plus détaillée que celle disponible dans l’interface utilisateur principale. Généralement accessible à partir d’un menu ou en cliquant sur un lien ou une icône d’aide, ce contenu peut prendre plusieurs formes, y compris des procédures pas à pas, du texte conceptuel ou d’autres didacticiels guidés basés sur visuel.

**mode de contraste élevé**

Paramètre d’affichage spécial qui fournit un contraste extrême pour les éléments visuels de premier plan et d’arrière-plan (noir blanc ou blanc sur noir). Particulièrement utile pour l’accessibilité.

**page Hub**

Dans les éléments du panneau de configuration, une page de concentrateur présente des choix de haut niveau, tels que les tâches les plus couramment utilisées (comme les pages de concentrateur basées sur les tâches) ou les objets disponibles (comme avec les pages de concentrateur basés sur des objets). Les utilisateurs peuvent accéder aux pages spoke pour effectuer des tâches spécifiques. Voir aussi : [page spoke](#s).

**page concentrateur hybride**

Dans les éléments du panneau de configuration, une page de concentrateur hybride est une page Hub qui contient également des propriétés ou des commandes directement. Les pages de concentrateur hybride sont vivement recommandées lorsque les utilisateurs sont plus susceptibles d’utiliser l’élément du panneau de configuration pour accéder à ces propriétés et commandes.

## <a name="i"></a>I

**modèle de validation immédiate**

Modèle de validation utilisé par les pages de concentrateur hybride où les modifications prennent effet dès que les utilisateurs les effectuent. Les boutons de validation ne sont pas utilisés dans ce modèle. Voir aussi : [modèle de validation retardé](#d).

**message sur place**

Message qui s’affiche dans le contexte de la surface de l’interface utilisateur actuelle, au lieu d’une fenêtre distincte. Contrairement aux fenêtres distinctes, les messages sur place nécessitent un espace d’écran disponible ou une disposition dynamique.

**boîte de dialogue indirecte**

Une boîte de dialogue s’affiche en dehors du contexte, soit en tant que résultat indirect d’une tâche, soit en raison d’un problème avec un processus système ou d’arrière-plan.

**interface utilisateur inductive**

Une interface utilisateur qui divise une tâche complexe en une tâche simple et facile à décrire, avec un objectif clair.

**info-bulle**

petite fenêtre contextuelle qui décrit de façon concise l’objet désigné, par exemple les descriptions des contrôles toolbar, les icônes, les graphiques, les liens, les objets Windows Explorer, les éléments menu Démarrer et les boutons de la barre des tâches. Les info-bulles sont une forme de divulgation progressive, ce qui évite d’avoir à utiliser du texte descriptif à l’écran à tout moment.

**trait**

Sortie brute d’un stylet. Cette encre numérique peut être conservée comme écrite, ou elle peut être convertie en texte à l’aide du logiciel de reconnaissance de l’écriture manuscrite.

**Inline**

Emplacement des liens ou des messages directement dans le contexte de l’interface utilisateur associée. Par exemple, un lien Inline apparaît dans un autre texte et non séparément.

**Focus d’entrée**

Emplacement dans lequel l’utilisateur dirige actuellement l’entrée. Notez que, juste parce qu’un emplacement de l’interface utilisateur est mis en surbrillance, cela ne signifie pas nécessairement que cet emplacement a le focus d’entrée.

**instancié**

Session de programme. par exemple, Windows Internet Explorer permet aux utilisateurs d’exécuter plusieurs instances du programme, car plusieurs sessions indépendantes peuvent s’exécuter à la fois. les Paramètres peuvent être enregistrées entre les sessions de programme. Voir aussi : [persistance](#p).

## <a name="j"></a>J

## <a name="k"></a>K

**KeyTip**

Dans un ruban, mécanisme utilisé pour afficher les clés d’accès. Les touches d’accès s’affichent sous la forme d’un petit Conseil sur chaque commande ou groupe, par opposition aux lettres soulignées généralement utilisées pour afficher les clés d’accès. Voir aussi : [clé d’accès](#alink).

## <a name="l"></a>L

**mode paysage**

Option de présentation qui oriente un objet pour qu’il soit plus grand que haut. Voir aussi : [mode portrait](#p).

**compte d’utilisateur doté de privilèges minimum**

Un compte d’utilisateur qui s’exécute normalement avec des privilèges minimaux. Voir aussi : [contrôle de compte d’utilisateur](#u).

**zone de liste**

contrôle de Windows commun qui permet aux utilisateurs de sélectionner un ensemble de valeurs présentées dans une liste, qui, à la différence d’une liste déroulante, est toujours visible. Prend en charge les sélections uniques ou multiples.

**mode liste**

contrôle de Windows commun qui permet aux utilisateurs d’afficher et d’interagir avec une collection d’objets de données, à l’aide d’une sélection unique ou d’une sélection multiple.

**aperçu instantané**

Technique de préversion qui affiche l’effet d’une commande immédiatement sur la sélection ou le pointage sans que l’utilisateur n’ait à valider l’action. Par exemple, les options de mise en forme, telles que les thèmes, les polices et les couleurs, tirent parti des aperçus instantanés en indiquant aux utilisateurs l’effet avec un minimum d’effort.

**localisation**

Processus d’adaptation des logiciels pour différents pays, langues, cultures ou marchés.

**fichier journal**

Référentiel basé sur des fichiers pour obtenir des informations sur les différents types d’activité sur un système informatique. Les administrateurs consultent souvent les fichiers journaux. en général, les utilisateurs ordinaires ne le font pas.

## <a name="m"></a>M

**instruction principale**

Texte affiché en évidence qui explique comment faire dans la fenêtre ou la page. L’instruction doit être une instruction spécifique, une direction impérative ou une question. Les bonnes instructions principales communiquent l’objectif de l’utilisateur au lieu de se concentrer uniquement sur la manipulation de l’interface utilisateur.

**environnement géré**

Un environnement informatique en réseau géré par un service informatique ou un fournisseur tiers, plutôt que par des utilisateurs individuels. Les administrateurs peuvent optimiser les performances et appliquer les mises à jour du système d’exploitation et des applications, entre autres tâches.

**manoeuvr**

Type d’interaction tactile dans laquelle l’entrée correspond directement à la façon dont l’objet touchées réagira naturellement à l’action dans le monde réel.

**valoris**

Pour afficher une fenêtre à sa plus grande taille. Voir aussi : réduire, [fenêtre restaurée](#r).

**menus**

Liste des commandes ou options disponibles pour les utilisateurs dans le contexte actuel.

**boîte de message**

Fenêtre secondaire qui s’affiche pour informer l’utilisateur d’une condition particulière.

**Mini-barre d’outils**

Barre d’outils contextuelle affichée au pointage.

**icône**

Pour masquer une fenêtre. Voir aussi : agrandir, [fenêtre restaurée](#r).

**État mixte**

Pour les cases à cocher qui s’appliquent à un groupe d’éléments, un État mixte indique que certains éléments sont sélectionnés et que d’autres sont désactivés.

**exigeant**

Interaction restrictive ou limitée en raison de l’utilisation d’un mode. Modale décrit souvent une fenêtre secondaire qui restreint l’interaction d’un utilisateur avec la fenêtre propriétaire. Voir aussi : non modal.

**non modales**

Interaction non restrictive ou non limitée. Non modal décrit souvent une fenêtre secondaire qui ne restreint pas l’interaction d’un utilisateur avec la fenêtre propriétaire. Voir aussi : modal.

**sélection multiple**

Possibilité pour les utilisateurs de choisir plusieurs objets dans une liste ou une arborescence.

## <a name="n"></a>N

**événement système non critique**

Type d’événement système qui ne nécessite pas une attention immédiate, souvent lié à l’état du système. Voir aussi : [critique](#c).

**notification**

Informations sur une nature non critique qui s’affiche brièvement pour l’utilisateur ; une notification prend la forme d’une info-bulle à partir d’une icône dans la zone de notification de la barre des tâches.

## <a name="o"></a>O

**accepter**

La possibilité pour les utilisateurs de sélectionner explicitement des fonctionnalités facultatives. Moins intrusif pour les utilisateurs que pour la désactivation, en particulier pour les fonctionnalités liées à la confidentialité et au marketing, en raison de l’absence de présomption des souhaits des utilisateurs. Voir aussi : refuser, options.

**refuser**

La possibilité pour les utilisateurs de supprimer les fonctionnalités qu’ils ne souhaitent pas en effaçant leur sélection. Plus intrusive pour les utilisateurs que pour les abonnements, en particulier pour les fonctionnalités liées à la confidentialité et au marketing, en raison des souhaits des utilisateurs. Voir aussi : opt in, options.

**options**

Choix à la disposition des utilisateurs pour la personnalisation d’un programme. Par exemple, une boîte de dialogue Options permet aux utilisateurs d’afficher et de modifier les options du programme. Voir aussi : [Propriétés](#p).

**interface utilisateur hors contexte**

Toute interface utilisateur affichée dans une fenêtre indépendante qui n’est pas directement liée à l’activité actuelle de l’utilisateur. Par exemple, les notifications et l’interface utilisateur de consentement pour l’utilisateur Access Control sont des interfaces utilisateur hors contexte.

**fenêtre propriétaire**

Fenêtre secondaire utilisée pour effectuer une tâche auxiliaire. Il ne s’agit pas d’une fenêtre de niveau supérieur (elle n’est donc pas affichée sur la barre des tâches). au lieu de cela, il est « détenu » par sa fenêtre propriétaire. Par exemple, la plupart des boîtes de dialogue sont des fenêtres détenues. Voir aussi : [fenêtre enfant](#c), fenêtre propriétaire.

**contrôle propriétaire**

Source d’une info-bulle, d’une bulle ou d’un menu volant. Par exemple, une zone de texte qui a des contraintes d’entrée peut afficher une bulle pour informer l’utilisateur de ces limitations. Dans ce cas, la zone de texte est considérée comme le contrôle propriétaire.

**fenêtre propriétaire**

Fenêtre à partir de laquelle provient une fenêtre détenue. S’affiche sous la fenêtre appartenant dans l’ordre de plan. Voir aussi : fenêtre propriétaire, [fenêtre parente](#p), [ordre de plan](#z).

## <a name="p"></a>P

**page**

Unité de navigation de base pour l’interface utilisateur basée sur les tâches, comme les assistants, les feuilles de propriétés, les éléments du panneau de configuration et les sites Web. Les utilisateurs effectuent des tâches en naviguant d’une page à l’autres au sein d’une même fenêtre hôte. Voir aussi : Flow page, [Window](#w).

**Flow page**

Collection de pages dans laquelle les utilisateurs effectuent une tâche. Voir aussi : page, [tâche](#t), [Assistant](#w), [panneau de configuration](#c).

**contrôle de l’espace de page**

Permet aux utilisateurs d’afficher et d’interagir avec une collection hiérarchique d’objets organisée. Les contrôles d’espace de page sont semblables aux contrôles d’arborescence, mais ils ont une apparence visuelle légèrement différente. ils sont principalement utilisés par Windows Explorer.

**fenêtre de palette**

Fenêtre secondaire non modale qui affiche une barre d’outils ou d’autres choix, tels que des couleurs, des modèles, des polices ou des attributs de police.

**fonctions**

Pour déplacer une scène, telle qu’une carte ou une photo, dans deux dimensions, faites-la glisser directement. Cela diffère de la défiler de deux manières : le contenu défilé a généralement une dimension dominante et fait souvent défiler uniquement le long de cette dimension ; et le contenu de défilement apparaît conventionnellement avec des barres de défilement que l’utilisateur fait glisser dans la direction opposée du mouvement de défilement.

**propane**

Zone rectangulaire dans une fenêtre que les utilisateurs peuvent être en mesure de déplacer, redimensionner, masquer ou fermer. Les volets sont toujours ancrés sur le côté de leur fenêtre parente. Ils peuvent être adjacents à d’autres volets, mais ils ne se chevauchent jamais. La désancrage d’un volet le convertit en fenêtre enfant. Voir aussi : [fenêtre](#w).

**fenêtre parente**

Conteneur de fenêtres enfants (tels que les contrôles ou les volets). Voir aussi : [fenêtre propriétaire](#o).

**pénétration**

Stylet utilisé pour le pointage, les gestes, l’entrée de texte simple et l’écriture manuscrite de forme libre. Les plumes ont une astuce fine qui prend en charge le pointage, l’écriture ou le dessin précis de l’encre. Ils peuvent également avoir un bouton de stylet facultatif (utilisé pour effectuer un clic droit) et un gomme (utilisé pour effacer l’encre).

**persistance**

Principe selon lequel l’État ou les propriétés d’un objet sont conservés automatiquement.

**réalisée**

Personnalisation d’une expérience de base cruciale pour l’identification personnelle de l’utilisateur avec un programme. En revanche, les options et les propriétés ordinaires ne sont pas essentielles à l’identification personnelle de l’utilisateur avec un programme.

**personnes**

Description détaillée des personnes imaginaires. Les personnages sont construits à partir de données bien comprises et fortement spécifiées sur les véritables gens.

**résolution physique**

Pixels horizontaux et verticaux qui peuvent être affichés par le matériel d’un moniteur d’ordinateur.

**bouton de groupe contextuel**

Dans un ruban, bouton de menu qui consolide toutes les commandes et options au sein d’un groupe. Utilisé pour afficher des rubans dans de petits espaces.

**mode portrait**

Option de présentation qui oriente un objet pour qu’il soit plus haut que grand. Voir aussi : [mode paysage](#l).

**préférences**

Ne pas utiliser. Utilisez des [options](#o) ou des propriétés à la place.

**préversion**

Représentation de ce que les utilisateurs verront lorsqu’ils sélectionneront une option. Les aperçus peuvent être affichés de manière statique dans le cadre de l’option, ou à la demande avec un bouton d’aperçu ou d’application.

**volet de visualisation**

Volet de fenêtre utilisé pour afficher des aperçus et d’autres données sur les objets sélectionnés.

**commande principale**

Action centrale qui respecte l’objectif principal d’une fenêtre. Par exemple, l’option imprimer est une commande principale pour une boîte de dialogue Imprimer. Voir aussi : [commande secondaire](#s).

**barre d’outils principale**

Collection de commandes conçues pour être suffisamment complètes pour empêcher l’utilisation d’une barre de menus. Voir aussi : [barre d’outils supplémentaires](#s).

**fenêtre principale**

Une fenêtre principale n’a pas de fenêtre propriétaire et est affichée dans la barre des tâches. Les fenêtres principales du programme sont toujours les fenêtres principales. Voir aussi : [fenêtre secondaire](#s).

**table**

Séquence d’instructions qui peuvent être exécutées par un ordinateur. Les types de programmes courants sont les applications de productivité, les applications grand public, les jeux, les bornes et les utilitaires.

**barre de progression**

contrôle de Windows commun qui affiche la progression d’une opération particulière sous la forme d’une barre graphique.

**Divulgation progressive**

Technique permettant aux utilisateurs d’afficher des informations moins couramment utilisées (en général, des données, des options ou des commandes) en fonction des besoins. Par exemple, si d’autres options sont parfois nécessaires, les utilisateurs peuvent les exposer en contexte en cliquant sur un bouton de Chevron.

**escalade progressive**

Séquence dans laquelle l’interface utilisateur utilisée pour informer les utilisateurs devient progressivement plus discrète lorsque l’événement devient plus critique. Par exemple, une notification peut être utilisée pour un événement que les utilisateurs peuvent ignorer au préalable en toute sécurité. À mesure que la situation devient critique, une interface utilisateur plus discrète comme une boîte de dialogue modale doit être utilisée.

**prompt**

Étiquette ou brève instruction placée à l’intérieur d’une zone de texte ou d’une liste déroulante modifiable comme valeur par défaut. Contrairement au texte statique, les invites disparaissent une fois que les utilisateurs ont tapé un texte dans le contrôle ou qu’il obtient le focus d’entrée.

**properties**

Paramètres d’un objet que les utilisateurs peuvent modifier, telles que le nom d’un fichier et l’état en lecture seule, ainsi que les attributs d’un objet que les utilisateurs ne peuvent pas modifier directement, tels que la date de création et la taille d’un fichier. En général, les propriétés définissent l’État, la valeur ou l’apparence d’un objet.

**administrateur protégé**

Dans le contrôle de compte d’utilisateur, administrateur s’exécutant dans l’état le moins privilégié. Voir aussi : [administrateur avec élévation de privilèges](#e), [utilisateur standard](#s).

## <a name="q"></a>Q

**Barre d’outils accès rapide**

Une petite barre d’outils personnalisable qui affiche les commandes fréquemment utilisées.

**Barre lancement rapide**

point d’accès direct sur le bureau Windows, situé en regard du bouton démarrer, renseigné avec des icônes pour les programmes choisis par l’utilisateur. supprimé dans Windows 7.

## <a name="r"></a>R

**case d’option**

contrôle de Windows commun qui permet aux utilisateurs de choisir parmi un ensemble de choix s’excluant mutuellement.

**pixels relatifs**

Métrique indépendante du périphérique qui est identique à un pixel physique à 96 ppp (points par pouce), mais mis à l’échelle proportionnellement dans d’autres DPI. Voir aussi : [résolution efficace](#e).

**fenêtre restaurée**

Fenêtre d’écran partielle visible, ni agrandie, ni réduite. Voir aussi : [agrandir](#m), réduire.

**dernier**

Conteneur avec onglets de commandes et d’options, situé en haut d’une fenêtre ou d’une zone de travail et ayant un emplacement fixe et une hauteur. Les rubans comportent généralement un menu d’application et une barre d’outils accès rapide. Voir aussi : [menu](#m), [barre d’outils](#t).

**action risquée**

Une qualité d’action de l’utilisateur qui peut avoir des conséquences négatives et ne peut pas être facilement annulée. Les actions risquées incluent des actions qui peuvent nuire à la sécurité d’un ordinateur, affecter l’accès à un ordinateur ou entraîner une perte de données involontaire.

## <a name="s"></a>S

**chemin d’analyse**

Les utilisateurs de la route sont susceptibles d’effectuer une analyse pour localiser des éléments dans une fenêtre. Particulièrement important si les utilisateurs ne sont pas engagés dans la lecture immersive du texte.

**lecteur d’écran**

Une technologie d’assistance qui permet aux utilisateurs ayant des handicaps d’interpréter et de naviguer dans une interface utilisateur en transformant les éléments visuels en données audio. Ainsi, le texte, les contrôles, les menus, les barres d’outils, les graphiques et les autres éléments d’écran sont parlés par la voix informatisée du lecteur d’écran.

**barre de défilement**

Contrôle qui permet aux utilisateurs de faire défiler le contenu d’une fenêtre, verticalement ou horizontalement.

**commande secondaire**

Une action périphérique qui, bien qu’utile, n’est pas essentielle à l’objectif de la fenêtre. Par exemple, Rechercher l’imprimante ou installer l’imprimante sont des commandes secondaires pour une boîte de dialogue Imprimer. Voir aussi : [commande principale](#p).

**fenêtre secondaire**

Fenêtre qui a une fenêtre propriétaire et qui, par conséquent, n’est pas affichée dans la barre des tâches. Voir aussi : [fenêtre principale](#p).

**Bureau sécurisé**

Environnement protégé qui est isolé des programmes en cours d’exécution sur le système, utilisé pour augmenter la sécurité des tâches hautement sécurisées telles que l’ouverture de session, les modifications de mot de passe et l’interface utilisateur d’élévation UAC. Voir aussi : [contrôle de compte d’utilisateur](#u).

**Bouclier de sécurité**

Icône de blindage utilisée pour la personnalisation de la sécurité.

**sélectionné**

Choisi par l’utilisateur pour effectuer une opération ; mise.

**majuscules de style de phrase**

Pour les majuscules de style phrase :

-   Mettez toujours en majuscule le premier mot d’une nouvelle phrase.
-   Ne mettez pas en majuscule le mot qui suit un signe deux-points, sauf si le mot est un nom propre ou si le texte qui suit le signe deux-points est une phrase complète.
-   N’mettez pas en majuscule le mot suivant un tiret cadratin, sauf s’il s’agit d’un nom propre, même si le texte qui suit le tiret est une phrase complète.
-   Mettez toujours en majuscule le premier mot d’une nouvelle phrase à la suite de la ponctuation finale. Réécrivez les phrases qui commencent par un mot en minuscules respectant la casse.

**settings**

Valeurs spécifiques qui ont été choisies (par l’utilisateur ou par défaut) pour configurer un programme ou un objet.

**touche de raccourci**

Clés ou combinaisons de touches que les utilisateurs peuvent appuyer pour accéder rapidement aux actions qu’ils effectuent fréquemment. Les combinaisons CTRL + lettre et touches (F1 à F12) sont généralement les meilleures options pour les touches de raccourci. Par définition, une touche de raccourci est l’équivalent du clavier des fonctionnalités prises en charge de manière adéquate ailleurs dans l’interface. Par conséquent, évitez d’utiliser une touche de raccourci comme seule façon d’accéder à une opération particulière.

Contrairement aux clés d’accès, qui sont conçues pour améliorer l’accessibilité, les touches de raccourci sont conçues principalement pour les utilisateurs expérimentés. Étant donné qu’ils ne sont pas documentés directement dans l’interface utilisateur proprement dite (même s’ils peuvent être documentés dans les menus et les info-bulles de barre d’outils), ils sont destinés à être mémorisés et doivent donc être attribués de manière cohérente dans les applications et dans les différentes applications.

**Encadré**

une région sur le côté du bureau de l’utilisateur, utilisée pour afficher les gadgets dans Windows Vista. Voir aussi : [gadget](#g).

**erreur de point unique**

Erreur d’entrée utilisateur liée à un contrôle unique. Par exemple, l’entrée d’un numéro de carte de crédit incorrect est une erreur à point unique, alors qu’une ouverture de session incorrecte est une erreur de double point, car le nom d’utilisateur ou le mot de passe peut être le problème.

**curseur**

contrôle de Windows commun qui affiche et définit une valeur à partir d’une plage continue de valeurs possibles, telles que la luminosité ou le volume.

**expérience spéciale**

Dans les programmes, les expériences spéciales sont liées à la fonction principale du programme, à un point unique sur le programme, ou à une connexion émotionnelle aux utilisateurs. Par exemple, la lecture d’un fichier audio ou vidéo est une expérience spéciale pour un lecteur multimédia.

**zone de sélection numérique**

Combinaison d’une zone de texte et de son contrôle spin associé. Les utilisateurs cliquent sur la flèche vers le haut ou vers le bas d’une zone de sélection numérique pour augmenter ou diminuer une valeur numérique. Contrairement aux contrôles Slider, qui sont utilisés pour les quantités relatives, les zones de sélection numérique sont utilisées uniquement pour les valeurs numériques exactes et connues.

**contrôle spin**

Contrôle sur lequel les utilisateurs cliquent pour modifier les valeurs. Les contrôles spin utilisent des flèches vers le haut et vers le bas pour augmenter ou diminuer la valeur.

**écran de démarrage**

L’image de transition d’écran qui apparaît en tant que programme est en cours de lancement.

**bouton partagé**

Un bouton de commande bipartite qui comprend un petit bouton avec un triangle pointant vers le bas sur la partie la plus à droite du bouton principal. Les utilisateurs cliquent sur le triangle pour afficher les variations d’une commande dans un menu déroulant. Voir aussi : [bouton de commande](#c).

**page spoke**

Dans les éléments du panneau de configuration, les pages spoke sont l’endroit où les utilisateurs effectuent des tâches. Deux types de pages spoke sont des pages de tâches et des pages de formulaire : les pages de tâches présentent une tâche ou une étape dans une tâche avec une instruction principale spécifique basée sur des tâches. les pages de formulaire présentent une collection de propriétés et de tâches associées basées sur une instruction principale générale. Voir aussi : [page Hub](#h).

**utilisateur standard**

Dans le contrôle de compte d’utilisateur, les utilisateurs standard disposent des privilèges minimum sur l’ordinateur et doivent demander l’autorisation à un administrateur sur l’ordinateur pour effectuer des tâches d’administration. Contrairement aux administrateurs protégés, les utilisateurs standard ne peuvent pas s’élever eux-mêmes. Voir aussi : [administrateur avec élévation de privilèges](#e), [administrateur protégé](#p).

**texte statique**

Texte de l’interface utilisateur qui ne fait pas partie d’un contrôle interactif. Comprend des étiquettes, des instructions principales, des instructions supplémentaires et des explications supplémentaires.

**instructions supplémentaires**

Forme facultative de texte d’interface utilisateur qui ajoute des informations, des détails ou un contexte à l’instruction principale. Voir aussi : [instruction principale](#m).

**barre d’outils supplémentaire**

Collection de commandes conçue pour fonctionner conjointement avec une barre de menus. Voir aussi : [barre d’outils principale](#p).

**couleur système**

couleur définie par Windows à un usage spécifique, accessible à l’aide de l’interface de programmation d’applications (API) GetSysColor. Par exemple, \_ la fenêtre couleur définit la couleur et la couleur d’arrière-plan de la fenêtre \_ WINDOWTEXT définit la couleur du texte de la fenêtre. Les couleurs système ne sont pas aussi riches que les couleurs de thème. Voir aussi : [couleur de thème](#t).

**menu système**

Collection de commandes de fenêtre de base, telles que déplacer, dimensionner, agrandir, réduire et fermer, disponibles à partir de l’icône de programme dans la barre de titre, ou en cliquant avec le bouton droit sur un bouton de la barre des tâches.

## <a name="t"></a>T

**boîte de dialogue à onglets**

Boîte de dialogue qui contient des informations connexes sur des pages étiquetées distinctes (onglets). Contrairement aux feuilles de propriétés, qui contiennent également souvent des tabulations, les boîtes de dialogue à onglets ne sont pas utilisées pour afficher les propriétés d’un objet. Voir aussi : [Propriétés](#p).

**tâche**

Unité d’activité utilisateur, souvent représentée par une seule surface d’interface utilisateur (par exemple, une boîte de dialogue) ou une séquence de pages (par exemple, un Assistant).

**boîte de dialogue de tâches**

Boîte de dialogue implémentée à l’aide de l’API de la boîte de dialogue de tâche. requiert Windows Vista ou version ultérieure.

**déroulement des tâches**

Séquence de pages qui aide les utilisateurs à effectuer une tâche, qu’il s’agisse d’un Assistant, d’un explorateur ou d’un navigateur.

**lien de tâche**

Un lien utilisé pour lancer une tâche, contrairement aux liens qui naviguent vers d’autres pages ou fenêtres, choisissez Options ou affichez l’aide.

**volet des tâches**

Type d’interface utilisateur semblable à une boîte de dialogue, à la différence qu’elle est présentée dans un volet de fenêtre plutôt que dans une fenêtre distincte. Par conséquent, les volets des tâches ont une apparence plus directe et contextuelle que les boîtes de dialogue. Un volet de tâches peut contenir un menu pour fournir à l’utilisateur un petit ensemble de commandes liées à l’objet sélectionné ou au mode de programme.

**tâches**

Point d’accès pour exécuter des programmes qui ont une présence sur le bureau. Les utilisateurs interagissent avec les contrôles appelés boutons de la barre des tâches pour afficher, masquer et réduire les fenêtres de programme.

**zone de texte**

Contrôle spécifiquement conçu pour l’entrée textuelle ; permet aux utilisateurs d’afficher, d’entrer ou de modifier du texte ou des nombres.

**couleur du thème**

couleur définie par Windows à un usage spécifique, accessible à l’aide de l’API GetThemeColor avec des parties, des états et des couleurs. Par exemple, la partie Windows définit un FillColor et un TextColor. Les couleurs de thème sont plus riches que les couleurs système, mais nécessitent l’exécution du service de thème. Voir aussi : [couleur système](#s).

**titre-style de casse**

Pour la mise en majuscules du titre :

-   Mettre en majuscules tous les noms, verbes (y compris les autres formes de), les adverbes (y compris et le cas), les adjectifs (y compris celui-ci) et les pronoms (y compris son).
-   Mettez en majuscule le premier et le dernier mot, indépendamment de leurs parties vocales (par exemple, le texte à rechercher).
-   Mettre en majuscule les prépositions qui font partie d’une expression verbale (par exemple, la sauvegarde de votre disque).
-   Ne mettez pas en majuscule les articles (a, a, le), sauf si l’article est le premier mot du titre.
-   Ne pas mettre en majuscules les conjonctions de coordonnées (et, mais, pour, ou), sauf si la conjonction est le premier mot du titre.
-   Ne pas mettre en majuscules les prépositions de quatre lettres ou moins, sauf si la préposition est le premier mot du titre.
-   Ne vous contentez pas d’une expression infinitive (par exemple, le formatage de votre disque dur), à moins que l’expression ne soit le premier mot du titre.
-   Mettez en majuscule le deuxième mot dans les mots composés s’il s’agit d’un nom ou d’un adjectif approprié, un « e-Word » ou les mots ont le même poids (par exemple, le commerce électronique, les références croisées, les logiciels antérieurs à Microsoft, l’accès en lecture/écriture, l’exécution). Ne mettez pas en majuscule le deuxième mot s’il s’agit d’une autre partie de la parole, telle qu’une préposition ou un autre mot secondaire (par exemple, complément, procédure, prise de vue).
-   Mettez en majuscule l’interface utilisateur et les termes de l’interface de programmation d’applications que vous ne devriez généralement pas mettre en majuscules, à moins qu’ils respectent la casse (par exemple, la commande FDISK). Suivez la casse traditionnelle des mots clés et d’autres termes spéciaux dans les langages de programmation (par exemple, la fonction printf, à l’aide des directives pair et ALIGN).
-   Mettre en majuscules uniquement le premier mot de chaque en-tête de colonne.

**barre**

Présentation graphique des commandes optimisées pour un accès efficace.

**bulle**

Petite fenêtre contextuelle qui étiquette le contrôle sans étiquette désigné, par exemple les contrôles de barre d’outils sans étiquette ou les boutons de commande.

**interface**

Interaction directe avec un écran d’ordinateur à l’aide d’un doigt.

## <a name="u"></a>U

**étude de la convivialité**

Technique de recherche qui vous aide à améliorer votre expérience utilisateur en testant la conception de votre interface utilisateur et en recueillant des commentaires à partir d’utilisateurs cibles réels. Les études de convivialité peuvent aller des techniques formelles dans des paramètres tels que les laboratoires de convivialité aux techniques informelles dans des paramètres tels que le Bureau de l’utilisateur. Toutefois, les constantes de ces études sont les suivantes : capture d’informations auprès des participants ; l’évaluation de ces informations pour des tendances et des modèles significatifs ; Enfin, implémenter des modifications logiques qui résolvent les problèmes identifiés dans l’étude.

**Contrôle de compte d'utilisateur**

Avec le contrôle de compte d’utilisateur (ou le contrôle de compte d’utilisateur, anciennement « compte d’utilisateur avec privilèges minimum » ou LUA) activé, les administrateurs interactifs s’exécutent normalement avec le moins de privilèges utilisateur, mais ils peuvent s’élever automatiquement pour effectuer des tâches d’administration en donnant un consentement explicite avec l’interface utilisateur de consentement. Ces tâches d’administration incluent l’installation de logiciels et de pilotes, la modification des paramètres au niveau du système, l’affichage ou la modification d’autres comptes d’utilisateur et l’exécution d’outils d’administration.

**Blindage du contrôle de compte d’utilisateur**

Icône de bouclier utilisée pour indiquer qu’une commande ou une option requiert une élévation pour le contrôle de compte d’utilisateur.

**problème d’entrée d’utilisateur**

Erreur résultant d’une entrée de l’utilisateur. Les problèmes d’entrée d’utilisateur ne sont généralement pas critiques, car ils doivent être corrigés avant de continuer.

**scénario utilisateur**

Description d’un objectif d’utilisateur, d’un problème ou d’une tâche dans un ensemble spécifique de circonstances.

## <a name="v"></a>V

## <a name="w"></a>W

**warning**

Message qui décrit une condition susceptible de provoquer un problème à l’avenir. Les avertissements ne sont pas des erreurs ou des questions. dans Windows Vista et versions ultérieures, les messages d’avertissement s’affichent généralement dans les boîtes de dialogue de tâches, incluent une instruction principale claire et concise, et incluent généralement une icône d’avertissement standard pour le renforcement visuel du texte.

**Page d’accueil**

Première page d’un Assistant, utilisée pour expliquer l’objectif de l’Assistant. Les pages d’accueil ne sont plus recommandées. Les utilisateurs bénéficient d’une expérience plus efficace sans ces pages.

**fenetre**

Zone rectangulaire sur un écran d’ordinateur dans laquelle les programmes et le contenu s’affichent. Une fenêtre peut être déplacée, redimensionnée, réduite ou fermée ; Il peut chevaucher d’autres fenêtres. L’ancrage d’une fenêtre enfant la convertit en un volet. Voir aussi : [volet](#p).

**Touche Windows**

touche de modification avec le logo de Windows. cette clé est utilisée pour un certain nombre de Windows de raccourcis et est réservée à une utilisation Windows. par exemple, si vous appuyez sur la touche Windows logo, vous affichez ou masquez le menu Démarrer Windows.

**des maquettes**

Maquette d’interface utilisateur qui affiche les fonctionnalités et la mise en page d’une fenêtre, mais pas son apparence terminée. Un filaire utilise uniquement des segments de ligne, des contrôles et du texte, sans couleurs, graphiques complexes, ou l’utilisation de thèmes.

**création**

Séquence de pages qui guide les utilisateurs dans une tâche à plusieurs étapes, rarement exécutée. Les assistants efficaces réduisent les connaissances requises pour effectuer la tâche par rapport aux autres interfaces utilisateur.

**Zone de travail**

Zone à l’écran où les utilisateurs peuvent effectuer leur travail, ainsi que pour stocker des programmes, des documents et leurs raccourcis. Voir aussi : [Bureau](#d).

## <a name="x"></a>X

## <a name="y"></a>O

## <a name="z"></a>Z

**Ordre de plan**

Relation en couches des fenêtres sur l’affichage.

 

 
