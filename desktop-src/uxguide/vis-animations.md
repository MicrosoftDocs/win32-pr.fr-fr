---
title: Animations et transitions
description: L’utilisation stratégique des animations et des transitions peut rendre votre programme plus facile à comprendre, se sentir plus lisse, plus naturel et de meilleure qualité, et être plus attrayant.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6d57c696bd78df9c9505bb85453456f10631a00d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104568659"
---
# <a name="animations-and-transitions"></a>Animations et transitions

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

L’utilisation stratégique des animations et des transitions peut rendre votre programme plus facile à comprendre, se sentir plus lisse, plus naturel et de meilleure qualité, et être plus attrayant. Toutefois, l’utilisation gratuite des animations et des transitions peut rendre votre programme plus gênant et même ennuyeux.

Les animations donnent l’apparence d’un mouvement ou d’une modification au fil du temps. Utilisez l’animation pour apporter des commentaires, afficher un aperçu de l’effet d’une action, afficher la relation entre les objets, attirer l’attention sur modifier ou expliquer une tâche visuellement.

![figure du pavé numérique avec une clé mise en surbrillance ](images/vis-animations-image1.png)

Microsoft Windows utilise une animation Flash d’arrière-plan pour fournir des commentaires sur l’objet sur lequel l’utilisateur a cliqué.

Les transitions sont des animations utilisées pour tenir les utilisateurs orientés lors des modifications d’état de l’interface utilisateur et des manipulations d’objets, et rendre ces modifications plus lisses au lieu de transférerez. De bonnes transitions ressemblent naturellement, ce qui donne l’illusion que les utilisateurs interagissent avec les objets réels.

![Capture d’écran montrant trois tailles de gadgets météo.](images/vis-animations-image2.png)

Les gadgets du bureau Windows utilisent des transitions lisses entre leurs États concis et détaillés.

En règle générale, les meilleures animations et transitions sont utilisées pour communiquer aux utilisateurs de manière non verbale et pour rendre les changements d’État plus naturels et moins perceptibles. En revanche, la solution la moins efficace est gratuite en ce sens qu’elle ne communique rien ou n’attire pas une attention inutile. Les animations sont mieux utilisées comme forme secondaire de communication. Ils doivent communiquer des informations qui sont utiles, mais pas critiques, et être accessibles, les utilisateurs doivent être en mesure de déterminer des informations équivalentes par d’autres moyens.

**Remarque :** Les instructions relatives à la [Personnalisation des logiciels](exper-branding.md), aux [sons](vis-sound.md)et à l' [accessibilité](inter-accessibility.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour décider, posez-vous les questions suivantes.

### <a name="animations"></a>Animations

Les conditions suivantes s’appliquent-elles ?

-   L’animation communique visuellement un élément utile, par exemple en fournissant des commentaires, en présentant des relations, des causes et des effets, ou en attire l’attention sur des modifications importantes.
-   L’affichage de l’animation n’est pas essentiel. Vous pouvez obtenir des informations équivalentes d’une autre façon. Les utilisateurs peuvent ne pas tirer parti de l’animation dans les cas suivants :
    -   Ils ont désactivé les animations.
    -   Leur attention est ailleurs.
    -   Ils sont malvoyants.
    -   L’animation est masquée par une autre fenêtre.
    -   L’animation n’est pas jouée en raison de performances insuffisantes du système.
-   L’animation n’affecte pas la productivité de l’utilisateur. Un des deux éléments suivants :
    -   Il se produit rapidement (200 millisecondes ou moins).
    -   Il n’interfère pas avec l’interaction ou peut être interrompu.
    -   L’utilisateur doit attendre quand même.
-   L’animation n’a aucune incidence sur le Flow de l’utilisateur.
    -   Soit il se trouve au centre d’attention de l’utilisateur, soit il attire l’attention sur un élément situé en dehors du centre d’attention qui est important ou utile pour effectuer une tâche.
    -   Il est facile à ignorer, pas gênant ou ennuyeux.
    -   Il ne devient pas pénible. Les utilisateurs le trouvent toujours comme appropriés et agréables, même après un affichage répété.

Si c’est le cas, envisagez d’utiliser une animation.

### <a name="transitions"></a>Transitions

L’état d’un objet ou d’une scène est-il modifié, et toutes les conditions ci-dessus s’appliquent à l’utilisation des animations, ainsi que l’une des conditions suivantes :

-   La modification d’État est conceptuellement désorientée, confuse ou difficile à comprendre.
-   Le changement d’État est visuellement transférerez, manque de continuité ou d’harmonie, ou clignote ; ou apparaît comme une qualité médiocre, inpolie ou de mauvaise qualité, surtout si elle implique une grande zone d’écran.
-   L’utilisation d’une transition rendra le changement d’État plus rapide.
-   Le changement d’État est digne d’attention particulière de l’utilisateur.

Si c’est le cas, envisagez d’utiliser une transition.

## <a name="design-concepts"></a>Principes de conception

Les animations et les transitions sont un moyen efficace de communiquer visuellement des informations qui nécessiteraient normalement un texte à expliquer ou qui peut être manqué par les utilisateurs.

**Incorrect :**

![capture d’écran de la boîte de dialogue avec un message ](images/vis-animations-image3.png)

**Correct :**

![figure de communication de l’animation visuellement ](images/vis-animations-image4.png)

L’utilisation d’une animation communique les mêmes informations, mais de façon naturelle et discrète. Qui vous ferait voir un millier de fois ?

**Les animations et les transitions n’ont pas à faire attention à la réussite.** En fait, ils sont souvent utilisés pour éviter d’attirer l’attention sur les mécanismes de programmation que les utilisateurs n’ont pas besoin de connaître. De nombreuses animations réussies sont tellement naturelles que les utilisateurs ne le sont même pas. les utilisateurs ne remarquent que leur absence. La fréquence des occurrences augmente la nécessité d’une subtilité, donc économisez des effets qui nécessitent une attention particulière pour les événements peu fréquents qui méritent vraiment l’attention.

![capture d’écran de tous les programmes en remplaçant par la flèche de retour ](images/vis-animations-image5.png)

Transition du menu Démarrer qui évite d’attirer l’attention.

En plus de rendre votre programme plus facile à comprendre et à vous sentir plus lisses, les **animations et les transitions bien conçues sont un excellent moyen d’ajouter la personnalité, le caractère et le style à votre programme.** Ils peuvent améliorer l’expérience de l’utilisateur et l’utiliser en lui donnant un sentiment naturel et réaliste.

![Figure illustrant la façon dont le pointage affecte la couleur du bouton ](images/vis-animations-image6.png)

Windows 7 met en surbrillance les boutons de la barre des tâches au pointage selon la position actuelle de la souris et la couleur de l’icône Cette approche est visuellement attrayante, mais subtile, qui transporte une personnalité de la plus proche.

**Toutefois, les animations et les transitions sont plus efficaces et bienvenue quand elles servent un objectif clair.** Ils doivent être utilisés pour améliorer la convivialité, la fluidité et le Flow, ainsi que la perception de la qualité, sans nuire aux performances de manière significative.

Bien que certains types d’animations soient utilisés pour attirer l’attention de l’utilisateur, assurez-vous que l’attention est bien dépensée et digne d’interruption de la formation de l’utilisateur. L’œil humain est sensible à motion, en particulier le mouvement périphérique. Il peut être difficile pour les utilisateurs de se concentrer lorsqu’un bouton de la barre des tâches clignote ou une icône de zone de notification pivotée. **Évitez d’utiliser des animations pour interrompre ou distraire des utilisateurs, ou attirez l’attention sur des choses qui ne justifient pas l’attention de l’utilisateur.**

**Incorrect :**

![figure du bouton de la barre des tâches en surbrillance sans motif ](images/vis-animations-image7.png)

Les programmes ne doivent pas clignoter le bouton de la barre des tâches, sauf si les utilisateurs doivent faire un événement important immédiatement. Dans ce cas, la seule chose que l’utilisateur doit faire est d’activer le programme.

**Utilisez des animations et des transitions, car votre programme en a besoin, et pas simplement parce que vous pouvez.** Et pour l’accessibilité, n’utilisez pas l’animation comme seule façon de transmettre des informations essentielles. Assurez-vous que les utilisateurs peuvent obtenir des informations équivalentes d’une manière différente.

### <a name="attributes-of-good-animations-and-transitions"></a>Attributs de bonnes animations et transitions

Les bonnes animations et les transitions passent le juste équilibre entre ces attributs :

-   **Sont clairement volontaires.** Les bonnes animations sont là, car elles doivent être, s’il faut communiquer des informations, faire d’une interaction une interaction réelle ou attirer l’attention sur un aspect notable. Et les animations volontaires sont exactes ; Si une animation indique qu’une tâche est en cours, c’est parce que la tâche est en cours d’exécution.

**Incorrect :**

![capture d’écran de l’icône de la batterie et de l’étiquette à charge complète ](images/vis-animations-image8.png)

Dans cet exemple, l’animation montre qu’une batterie entièrement chargée est facturée.

-   **Apparence lisse et continue.** Les bonnes animations suppriment facilement les jointures entre les changements d’état des scènes ou des éléments en présentant des relations et en fournissant un sens de la place et du contexte. La continuité aide les utilisateurs à comprendre leur emplacement d’origine et comment revenir à leur origine.

![capture d’écran des trois aperçus de la fenêtre barre des tâches ](images/vis-animations-image9.png)

La fenêtre de la barre des tâches de Windows 7 Aperçu des morphes pour assurer la continuité lorsque l’utilisateur passe d’un programme à un autre.

-   **Sont réalistes.** Les bonnes animations simulent le comportement et les propriétés physiques réelles d’un objet. Cela permet aux utilisateurs de prédire et de comprendre les résultats de leurs interactions. Vous n’avez pas à modéliser exactement le monde réel, mais si vous utilisez des animations réalistes, vous devez les garder cohérentes avec le monde réel. Les résultats ne doivent jamais être surpris ou confondus par les résultats, en particulier avec les animations utilisées pour la manipulation directe.

![figure du bouton de la barre des tâches déplacé vers la nouvelle position ](images/vis-animations-image10.png)

Dans cet exemple, l’animation « déplacer hors de la forme » utilisée par la barre des tâches de Windows 7 est plus réaliste qu’un point d’insertion statique.

-   **Sont authentiques.** Même les objets qui ne se trouvent pas dans le monde réel peuvent sembler naturels en se basant sur le comportement réel d’un objet différent, mais lié. Cette métaphore ne fonctionne que si la relation communique clairement le rôle et le comportement prévus.

![capture d’écran de l’effet déclenché derrière la fenêtre déplacée ](images/vis-animations-image11.png)

Dans cet exemple, l’animation « Squeegee » de la fenêtre utilisée par Windows 7 semble authentique, car elle est cohérente avec la manière dont les fenêtres vitreuses peuvent se comporter dans le monde réel.

-   **Utilisez le mappage naturel.** Les mappages naturels sont physiques ou culturels. Un mappage naturel basé sur la culture peut, par exemple, commencer par le fait que, dans les cultures occidentales, les utilisateurs lisent de gauche à droite. Par conséquent, pour exprimer une séquence horaire d’objets, l’objet central est actuel, les objets à gauche proviennent du passé et les objets à droite sont dans le futur. L’avancement dans le temps est indiqué par un déplacement de gauche à droite.

![capture d’écran de la barre de progression du lecteur multimédia ](images/vis-animations-image12.png)

Dans cet exemple, le contrôle du lecteur Windows Media a un mappage naturel, car la lecture déplace la position de gauche à droite.

-   **Avoir la personnalité.** Les animations bien choisies sont des méthodes intéressantes pour ajouter la personnalité, le caractère et le style à votre programme. Ils peuvent rendre l’expérience utilisateur plus immersive et plus attrayante. Tandis que le type d’animation détermine ce qu’elle communique, le mode spécifique dans lequel l’animation est exécutée montre la personnalité du programme. Les bonnes animations constituent la bonne personnalité pour votre programme, qu’il s’agisse de graves ou de saugrenu, ou entre les deux.

![capture d’écran de l’interface Zune conçue de façon créative ](images/vis-animations-image13.png)

Dans cet exemple, l’utilisation par Zune du texte animé et de la perspective dynamique forme sa personnalité.

-   **Apparence et convivialité.** Les bonnes animations ne nuisent pas à la productivité de l’utilisateur en bloquant les utilisateurs des autres interactions ou en forçant les utilisateurs à les regarder. Quelle que soit la nature de l’animation naturelle et de l’implication des animations de votre programme, personne ne souhaite en attendre exclusivement. Les bonnes animations semblent également réactives sans être transférerezes en ayant un démarrage rapide avec un atterrissage à chaud. Les animations réactives tirent également parti de la communication rapide avec leur objectif. Les utilisateurs ne doivent pas avoir à regarder une animation pendant une longue période juste pour déterminer ce qu’elle fait ou quand elle est terminée. Pour une manipulation directe, les animations réactives sont essentielles pour maintenir un sentiment direct et attrayant. Pour faire en sorte que les points de contact d’un objet soient directs, le pointeur doit rester correctement sous le pointeur tout au long de la manipulation. Tout décalage, réponse hachée ou perte de contact détruit la perception de la manipulation directe.

![figure de doigt touchant un écran tactile ](images/vis-animations-image14.png)

Dans cet exemple, la transition de panoramique tactile semble réactive en gardant le point de contact sous le doigt de l’utilisateur tout au long de la manipulation.

-   **Attirez le niveau d’attention approprié.** Les bonnes animations sont généralement subtiles et attirent uniquement l’attention requise pour atteindre leur objectif. Par conséquent, ils ne sont pas gênants, ennuyeux, trop complexes, trop longs ou répétitifs. Ils ne sont pas pénible après des affichages répétés.

![capture d’écran de la surbrillance des noms de fichiers ](images/vis-animations-image15.png)

Dans cet exemple, la recherche Windows attire temporairement l’attention sur les mots de recherche correspondants, puis diminue.

-   **Recherchez spécial uniquement si authentique.** La fréquence augmente la nécessité d’une subtilité. les interactions courantes nécessitent donc des animations simples qui communiquent une idée simple de manière simple. Réservez des animations spéciales et complexes pour des expériences spéciales et peu fréquentes.

![la capture d’écran des quatre cercles devient le logo Windows ](images/vis-animations-image16.png)

Dans cet exemple, Windows utilise une animation d’attention au démarrage pour rendre l’expérience plus spéciale, mais une telle animation serait inappropriée ailleurs.

Vous savez que vous avez atteint le bon équilibre lorsque l’expérience globale est détériorée si l’un de ces attributs a été supprimé.

### <a name="creating-an-animation-vocabulary"></a>Création d’un vocabulaire d’animation

Les bonnes animations concernent une communication visuelle efficace et la cohérence est essentielle à leur efficacité. Si vous utilisez une transition spécifique, telle que le push d’une scène dans à partir de la droite pour passer à la scène suivante, il doit s’agir de la seule transition utilisée à cette fin et cette transition ne doit pas être utilisée à d’autres fins. L’attribution de significations différentes à la même Animation nuit à sa capacité à communiquer. En assignant des animations et des transitions spécifiques à des significations spécifiques, vous créez un vocabulaire d’animation.

Ce problème s’applique aux animations et aux transitions qui ont une signification, pas à celles qui ne sont pas génériques, auxquelles les utilisateurs ne sont pas susceptibles d’affecter la signification ou ceux dont l’objectif n’est pas perceptible. Par exemple, les animations comme les fondues et les effets spéciaux comme les conversions n’ont aucune signification particulière. elles peuvent donc être utilisées librement.

Un vocabulaire approprié affecte les animations qui modélisent le comportement physique réel d’un objet. Si vous devez assigner une animation à un objet ou une action qui n’a pas d’équivalent réel, choisissez une animation qui montre comment l’objet peut se comporter comme réel.

![capture d’écran de l’éclat du logo Windows ](images/vis-animations-image17.png)

Alors que le menu Démarrer n’est pas un objet réel, son effet de survol s’illumine comme un objet réel.

Chaque animation dans un vocabulaire doit être clairement distincte. Les animations doivent avoir des comportements similaires uniquement si leurs actions associées sont liées de manière similaire. Par exemple, les transitions de mouvement suggèrent la navigation. vous pouvez donc utiliser des transitions de mouvement à partir de différentes directions pour indiquer les différents types de navigation.

Vous saurez que vos animations et transitions ne communiquent pas correctement lorsque les utilisateurs trouvent les résultats confus, étonnants ou inattendus. En règle générale, il est préférable d’atteindre un objectif unique bien que plusieurs objectifs.

Dans l’idéal, votre vocabulaire d’animation doit être complet dans toutes les zones de votre programme qui en ont besoin. Si seules quelques interactions ont des animations naturelles, cela attire l’attention sur ceux qui ne le sont pas.

Pour en savoir plus sur le vocabulaire Windows animation, consultez la section [modèles d’utilisation](#usage-patterns) de cet article.

### <a name="designing-the-right-personality"></a>Conception de la personnalité appropriée

Tandis que le type d’animation détermine ce qu’il communique, la façon dont l’animation est exécutée parle de la personnalité du programme et renforce sa réputation.

La personnalité de votre programme doit refléter la nature de ses tâches et la personnalité de ses utilisateurs, de sorte qu’il ne s’agit pas d’un choix arbitraire. Au lieu de cela, une personnalité bien conçue devrait paraître authentique ; n’essayez jamais de le forcer. La personnalité doit établir une connexion émotionnelle à l’utilisateur. Certains facteurs à prendre en compte :

-   **Tâches :** Grave ou amusante ; facultatif ou obligatoire.
-   **Conséquences :** Grave ou mineur.
-   **Coût :** Gratuit ou acheté ; en cas d’achat, à tarif modéré ou onéreux.
-   **Focus de l’utilisateur :** Groupe relativement étroit d’utilisateurs cibles, ou public large, général.
-   **Environnement de l’utilisateur :** Professionnel, informel ou familial.
-   **Âge de l’utilisateur :** Jeune ou plus ancienne.
-   **Fréquence d’utilisation :** Fréquentes ou peu fréquentes.

La combinaison de ces facteurs permet de déterminer la personnalité appropriée pour votre programme. Voici quelques combinaisons appropriées pour les types de programmes courants :

**Applications de productivité**

Naturellement, les applications de productivité doivent se concentrer sur la productivité. Bien qu’il puisse y avoir quelques expériences spéciales, la plupart des autres animations doivent avoir les caractéristiques suivantes :

-   Petite
-   Naturel, réaliste
-   Discret, subdued
-   Rapide et efficace
-   Souple

**Utilitaires**

Les utilitaires sont généralement utilisés brièvement, de sorte que leur utilisation de l’animation peut être plus agressive :

-   Réaliste, illustrative, explicite
-   Safe
-   Captiv

**Divertissement, jeux**

Étant donné que l’objectif de ces programmes est d’impliquer et de faire plaisir aux utilisateurs, les animations et les transitions peuvent être bien plus agressives en ayant ces caractéristiques :

-   Grande (peut devenir partie intégrante de l’expérience)
-   Artificiel, Surreal
-   Impact, éclatant
-   Émotionnel, Playful, saugrenu
-   Énergique

La création d’une connexion émotionnelle est si importante pour les programmes de divertissement qu’il est acceptable de plier certaines règles si cela permet de faire en sorte que les utilisateurs soient ravis du programme. Par exemple, il est acceptable si une animation ou une transition devient pénible après le centième de temps si la plupart des utilisateurs sont peu susceptibles d’utiliser le programme souvent.

En général, les animations et les transitions qui sont de petite taille, naturelle, subdued, efficace, mais souple, sont le pari le plus sûr. Les transitions avec ces caractéristiques prennent généralement le chemin le plus rapide du début à la fin, démarrent rapidement, se terminent de manière douce et ne sont pas dépassés. En outre, les transitions bien conçues sont conçues pour fonctionner correctement sur toute la plage de distances dans laquelle elles seront utilisées.

### <a name="animation-performance"></a>Performances de l’animation

Lors de la conception d’animations, assurez-vous qu’elles n’affectent pas la capacité des utilisateurs à utiliser votre programme efficacement. En règle générale, rendez vos animations suffisamment lentes pour atteindre leur objectif, mais suffisamment rapidement qu’elles n’interfèrent pas avec la réactivité, demandent trop d’attention ou deviennent pénible.

**Incorrect :**

![figure de la transformation de page de droite à gauche ](images/vis-animations-image18.png)

Alors que cette page transforme l’animation a une sensation réaliste, elle réduit la productivité des utilisateurs en mettant plus de temps à tourner les pages.

Les transitions brèves (200 millisecondes ou moins) sont un cas particulier (surtout lorsqu’il s’agit souvent d’un retard), car les utilisateurs savent qu’ils doivent attendre une seconde division pour eux. Les utilisateurs sont prêts à attendre ces animations dans les cas suivants :

-   L’attente perçue est extrêmement courte (200 millisecondes ou moins).
-   La transition rend l’interaction plus lisse et naturelle.
-   La transition rend le sentiment d’interaction plus réactif.
-   Tout délai permet à l’utilisateur de garder le contrôle de l’interaction.

![Figure des boutons de la barre des tâches déplacés vers la nouvelle position ](images/vis-animations-image19.png)

Les utilisateurs acceptent un bref délai pour que le bouton de la barre des tâches réorganise l’animation, car il est très bref et il rend l’interaction plus naturelle.

Les animations peuvent nuire aux performances de trois façons : vitesse, réactivité et perception.

Pour accélérer, certaines animations sont des placages visuels sur des tâches nécessitant beaucoup de ressources processeur. la dernière chose que vous devez faire est que ces tâches sont plus lentes avec les animations gourmandes en ressources processeur. Les animations les plus gourmandes en ressources processeur (« animations lourdes ») ont tendance à :

-   Impliquent de nombreux éléments qui se déplacent indépendamment.
-   Jouez pour une longue durée ou distance.
-   Implique une grande quantité d’espace à l’écran.
-   Sont beaucoup plus gourmands.

Animations avec moins d’impact sur les performances :

-   Implique un objet unique.
-   Jouez pour une brève durée ou distance.
-   Implique une petite quantité d’espace à l’écran.
-   Ne sont pas beaucoup trop gourmands.

Pour garantir des performances optimales, les animations lourdes doivent être utilisées uniquement pour les tâches qui ne nécessitent pas beaucoup de ressources processeur, tandis que les animations légères peuvent être utilisées n’importe où.

Pour des réactivités, la plupart des animations et des transitions doivent être conçues pour que les utilisateurs puissent interagir pendant l’exécution de l’animation. À moins qu’une animation fasse partie d’un processus, rendez-la indépendante de l’interaction principale de l’utilisateur et autorisez les utilisateurs à l’interrompre.

Une animation peut ne pas nuire aux performances d’une tâche en réalité, mais les utilisateurs peuvent avoir la perception qu’elle fait. Par exemple, n’utilisez pas une animation qui semble lourde pour une tâche lente et gourmande en ressources processeur, même si elle ne nuit pas aux performances, car les utilisateurs peuvent conclure que l’animation est la raison pour laquelle la tâche est lente. **Si les choses semblent lentes, cela semble ralentir. il est donc préférable d’utiliser des animations qui semblent simples, légères et rapides.** L’utilisation d’animations avec des débuts d’accrochage pour les tâches nécessitant beaucoup de ressources du processeur aide.

**Déconseillé**

![capture d’écran de la boîte de dialogue Copier avec la barre de progression ](images/vis-animations-image20.png)

Tandis que l’animation dans la boîte de dialogue copie de fichiers de Windows n’endommage pas les performances de copie de fichiers, elle risque de faire croire aux utilisateurs que c’est le cas.

**Également risqué :**

![capture d’écran de la progression affichée dans la barre d’adresses ](images/vis-animations-image21.png)

Dans cet exemple, l’animation de la progression de l’exploration la plus lente dans la barre d’adresse de l’Explorateur Windows rend les tâches très lentes.

Les animations et les transitions n’ont aucune valeur si leur qualité est tellement médiocre qu’elles rendent l’expérience moins lisse et moins attrayante. Pour maintenir leur qualité, les animations doivent être conçues pour se dégrader de manière appropriée chaque fois que des ressources système suffisantes ne sont pas disponibles. Les animations peuvent se dégrader en ayant des variations qui nécessitent moins de ressources (par exemple, des longueurs plus courtes ou des taux d’images inférieurs), voire pas du tout. Quelles que soient les ressources disponibles, assurez-vous que les animations ont une qualité élevée et qu’elles ressemblent à des animations au lieu des bogues logiciels.

Enfin, si les utilisateurs pensent que les animations et les transitions de votre programme détournent leur productivité, il y a de bonnes chances que certains utilisateurs puissent les désactiver. Pour prendre en charge cette fonctionnalité, respectez l’option permettant de **désactiver toutes les animations inutiles** trouvées dans la facilité d’accès de Windows.

### <a name="attracting-the-right-level-of-attention"></a>Attirer le niveau d’attention approprié

Alors que seuls certains types d’animations et de transitions sont spécifiquement conçus pour attirer l’attention de l’utilisateur, ils doivent être conçus pour attirer l’attention du mieux possible sur la réalisation de leur objectif. Quelles sont les différentes façons d’attirer votre attention et comment choisir celle qui vous convient ?

**Effets d’animation**

Différents effets d’animation attirent différents niveaux d’attention. La liste suivante résume les méthodes les plus courantes, en commençant par la plus grande attention :

-   **Clignotement rapide.** Requiert une attention immédiate. Peut rompre la concentration des utilisateurs, quel que soit l’endroit où le clignotement se produit.
-   **Clignotement modéré.** Même, mais exige moins d’attention avec une fréquence inférieure.
-   **Rebondissement.** Perceptible en matière de vision des périphériques et relativement exigeante en nature. Les utilisateurs sont susceptibles de le constater, mais ils peuvent continuer à se concentrer ailleurs uniquement si la durée est limitée.
-   **Films.** Visible dans la vision du périphérique, mais n’est pas exigeant. Toutefois, les mouvements complexes ou 3D attirent davantage l’attention que des mouvements simples ou 2D. Les utilisateurs sont susceptibles de voir, mais ils peuvent continuer à se concentrer ailleurs.
-   **Pulsation modérée.** Visible mais ne gêne pas la vision du périphérique. Les utilisateurs peuvent continuer à se concentrer ailleurs. Peut impulsions de la luminosité, des couleurs et des tailles.
-   **Pulsations/lueurs lentes.** Visible mais subtile. Attirez l’attention sur un effet statique, mais les utilisateurs ne remarqueront pas l’animation, sauf s’ils le souhaitent déjà.
-   **Retrait.** Encore moins perceptible. Attirez l’attention sur un effet statique, mais les utilisateurs ne remarqueront pas l’animation, sauf s’ils le souhaitent déjà.
-   **Mise en surbrillance statique/Gleam.** Visible si les utilisateurs choisissent de regarder, mais ne demande pas d’attention s’ils sont ailleurs.
-   **Ambiant/naturel.** Intentionnellement non perceptible en ayant une apparence naturelle du monde réel.

Pour déterminer l’approche adaptée à votre programme ou à votre fonctionnalité, réfléchissez à la façon dont ces facteurs sont en rapport avec les scénarios de votre fonctionnalité.

Supposons, par exemple, que vous conceviez un programme de messagerie instantanée et que quelqu’un envoie simplement un message à l’utilisateur. Ce scénario nécessite l’attention de l’utilisateur, il doit être visible partout, et l’utilisateur souhaite généralement réagir rapidement. Ce scénario suggère qu’une animation modérée clignotante serait un bon choix. En revanche, supposons que vous souhaitiez informer les utilisateurs qu’un travail d’impression est terminé. Les utilisateurs doivent pouvoir continuer à se concentrer et à travailler de manière productive ailleurs, et cela est acceptable si les utilisateurs ne le sont pas. Ce scénario suggère un bon choix pour une impulsion lente ou une lueur.

**Durée**

La durée appropriée pour attirer l’attention sur l’animation dépend du scénario et du type spécifique d’animation utilisé. Plus un effet d’animation est important, plus la durée doit être faible. Bien que les effets très subtils nécessitant une attention particulière (comme l’impulsion lente) puissent être joués indéfiniment, les effets exigeants doivent être joués uniquement entre 1 et 3 secondes. Tout ce qui est plus important risque de rendre l’animation écrasante et ennuyeux.

![capture d’écran du bouton en surbrillance de la barre des tâches ](images/vis-animations-image22.png)

Dans Windows 7, la barre des tâches clignote uniquement pour une seconde. Tout est plus ennuyeux.

**Atténuation des effets**

Vous devez faire attention aux animations en supposant que si les utilisateurs ne répondent pas immédiatement, c’est parce qu’ils sont occupés à effectuer d’autres opérations et qu’ils ne souhaitent pas être interrompus. Par conséquent, votre objectif doit être d’attirer votre attention sans l’exiger.

Pour tirer le meilleur équilibre de attirer l’attention sans l’exiger, désactivez l’intensité d’un effet au fil du temps. Par exemple, pour attirer l’attention, vous pouvez faire en sorte que l’effet soit initialement fort, mais vous pouvez ensuite ralentir l’effet rapidement. En procédant ainsi, la puissance intéressante est principalement déterminée par l’effet initial, mais l’impression globale de l’utilisateur est généralement déterminée par son achèvement.

![capture d’écran montrant le taux de clignotement réduit ](images/vis-animations-image23.png)

Dans Windows 7, l’effet flash de la barre des tâches ralentit à la fin.

### <a name="what-about-powerpoint"></a>Qu’en est-il de PowerPoint ?

Les transitions Microsoft PowerPoint enfreignent souvent délibérément ces instructions, car elles sont conçues pour attirer l’attention sur les transitions de diapositives et obliger les utilisateurs à attendre. En outre, ils n’ont aucune signification particulière afin qu’ils ne communiquent rien au-delà du fait qu’une diapositive change.

Les transitions de style PowerPoint, quand elles sont utilisées correctement, ont les fonctions suivantes :

-   Ils décomposent de longues présentations en plus petits segments en forçant le présentateur à s’interrompre.
-   Ils attirent l’attention du public sur les modifications apportées à la présentation, ce qui permet aux utilisateurs de se concentrer sur les personnes qui se sont demandées.
-   Ils donnent à la présentation un rythme qui ne semble pas monotone ou écrasant.
-   Leur style reflète la personnalité du présentateur ou du matériau.

Bien qu’il s’agit d’objectifs importants pour une présentation, ces transitions attirent l’attention sur l’interface utilisateur de la plupart des types de programmes et deviendront pénible rapidement.

**Ligne inférieure :** N’utilisez pas de transitions de style PowerPoint comme modèle pour votre programme.

**Si vous ne faites que six choses...**

1.  Utilisez des animations et des transitions pour faciliter la compréhension de votre programme, et vous sentir plus lisse et plus attrayant. Ils doivent avoir un objectif clair. N’utilisez pas les animations comme vous le pouvez, ou pour attirer l’attention inutile sur votre programme.
2.  Définissez un vocabulaire d’animation et utilisez-le de manière cohérente dans votre programme. Utilisez le vocabulaire d’animation Windows 7 le cas échéant.
3.  Utilisez les caractéristiques de vos animations pour offrir la personnalité de votre programme et renforcer sa personnalisation.
4.  Rendez la plupart des animations simples, courtes et subtiles. N’oubliez pas que les animations n’ont pas besoin de faire attention à la réussite. Si une animation est appropriée et naturelle, les utilisateurs ne remarqueront que son absence.
5.  Rendez vos animations rapides et réactives, et donnez-leur une sensation légère. Quelle que soit l’implication de vos animations, personne ne souhaiterait qu’elles attendent. Concevez des animations plus lourdes pour une dégradation normale.
6.  Conception pour une longue exécution. Si une animation est ennuyeuse, gênante ou pénible, remaniez-la ou supprimez-la.

## <a name="usage-patterns"></a>Modèles d’usage

Les animations ont plusieurs modèles d’utilisation :



|                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commentaires sur le survol**<br/> pour afficher l’emplacement du point d’interaction. <br/>                                | Indique que le point d’interaction est actif. le pointage peut également être affiché à l’aide d’un effet statique.<br/> Windows vocabulaire : afficher l’effet de survol (rectangle englobant, mettre en surbrillance, agrandissement) avec un effet d’atténuation/disparition en fondu pour le lissage. <br/> ![capture d’écran de l’un des six couvertures de l’album en surbrillance ](images/vis-animations-image24.png)<br/> Dans le lecteur multimédia numérique Zune, l’album couvre la mise en surbrillance et ajoute des contrôles de lecture au survol.<br/>                                                                                                                                                                                                                 |
| **Cliquez sur Commentaires**<br/> pour montrer qu’un objet cliquable est réactif et a reçu un clic. <br/>    | Indique qu’un clic a été effectué sur un objet.<br/> Windows vocabulaire : arrière-plan de l’objet flash sur l’événement de clic. pour afficher Touch contact, utilisez un effet ondulation. <br/> ![photo de doigt sur un écran tactile présentant des ondulations ](images/vis-animations-image25.png)<br/> Touch affiche une animation d’ondulation afin que l’utilisateur sache que l’interaction a été reconnue.<br/>                                                                                                                                                                                                                                                                                                         |
| **Commentaires sur la sélection**<br/> pour indiquer qu’un objet est sélectionné. <br/>                                | Indique qu’un objet est sélectionné. la sélection peut également être affichée à l’aide d’un effet statique.<br/> vocabulaire Windows : dessinez un rectangle de sélection avec un effet d’atténuation/disparition en fondu pour la lisse. <br/> ![figure d’un couvercle de l’album sur lequel vous avez cliqué, puis sélectionné ](images/vis-animations-image26.png)<br/> Dans Zune, l’album recouvre le clic, puis obtient un rectangle de sélection sur la sélection.<br/>                                                                                                                                                                                                                                                                      |
| **Commentaires sur la progression**<br/> pour indiquer qu’une tâche est en cours d’exécution. <br/>                             | Les commentaires de progression indiquent qu’une tâche progresse, en général avec les indicateurs d’activité, les barres de progression ou les animations qui illustrent la tâche. Les commentaires sur la progression de l’annulation indiquent approximativement la quantité de tâche effectuée et la quantité restante, alors que la progression indéterminée indique uniquement que la tâche est en cours.<br/> Windows vocabulaire : indicateurs d’activité en rotation, barres de progression, arrière-plans de progression, animations d’illustration. <br/> ![capture d’écran de la boîte de dialogue avec le texte « connexion » ](images/vis-animations-image27.png)<br/> Dans cet exemple, Windows Live Messenger affiche des commentaires de progression indéterminés au cours de la connexion.<br/> |
| **Attirer**<br/> pour montrer qu’un utilisateur a besoin de l’attention de l’utilisateur. <br/>                          | Attirez le niveau d’attention approprié lorsque des objets significatifs sont créés ou si vous avez besoin d’être attentifs (souvent dus à des modifications), ou lorsque des événements importants ou urgents se produisent. consultez [attirer le niveau d’attention approprié](#attracting-the-right-level-of-attention) pour les techniques de conception.<br/> Windows vocabulaire : clignotement, déplacement, impulsion, lueur, Gleam. <br/> ![capture d’écran illustrant l’animation de la barre d’outils ](images/vis-animations-image28.png)<br/> La barre d’outils Windows Live s’anime à la première apparition pour la rendre évidente.<br/>                                                                                                                                 |
| **Relationship**<br/> pour afficher la relation entre les objets ou la causalité dans Effects. <br/>        | Afficher les relations, en particulier lorsque la relation peut ne pas être comprise ou attendue, d’une manière qui ne gêne pas ou ne déroutant.<br/> Windows vocabulaire : transformation, transport, modification physique, comme le basculement, la croissance d’une source de point, la réduction jusqu’à une destination de point. <br/> ![capture d’écran de la boîte de dialogue étalonnage des couleurs](images/vis-animations-image29.png)<br/> Dans cet exemple, l’animation montre la relation entre le paramètre gamma et son impact sur l’affichage.<br/>                                                                                                                                                    |
| **Illustration/aperçu**<br/> expliquer visuellement un concept, une tâche ou l’effet d’une commande. <br/> | Animation ou vidéo qui explique un concept ou comment un travail fonctionne visuellement, soit pour compléter ou remplacer une explication textuelle. Cela permet aux utilisateurs d’effectuer des tâches ou de choisir des commandes de manière efficace et en toute confiance. <br/> ![capture d’écran du stylet corriger la faute d’orthographe ](images/vis-animations-image30.png)<br/> Dans cet exemple, les commandes « afficher » du panneau de saisie Tablet PC utilisent des illustrations pour montrer comment corriger, supprimer, fractionner et joindre.<br/>                                                                                                                                                                                                        |



 

Les transitions ont plusieurs modèles d’utilisation :



|                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Agrandissement/réduction de l’objet/affichage**<br/> pour modifier la taille ou l’état d’un objet en douceur. <br/>                                                                                                         | Modifications des objets entre les États, éventuellement en cours de déplacement. la transition permet aux utilisateurs d’être orientés pendant les modifications.<br/> Windows vocabulaire : Morph, change Size, Object slides in ou out. <br/> ![capture d’écran de trois tailles de gadgets météo ](images/vis-animations-image31.png)<br/> Dans cet exemple, le gadget Météo est basé sur son état concis pour afficher sa boîte de dialogue Options.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Afficher/masquer/modifier le contenu**<br/> pour afficher, masquer ou modifier facilement le contenu, en général pour une divulgation progressive. <br/>                                                                       | Formes intérieures des fenêtres pour afficher plus, moins ou un contenu différent. la transition permet aux utilisateurs d’être orientés pendant les modifications.<br/> Windows vocabulaire : volet diapositives. les fenêtres volantes sont en fondu et en sortie. des conversions de contenu ou des basculements différents. <br/> ![capture d’écran de trois tailles de calculatrice ](images/vis-animations-image32.png)<br/> La calculatrice Windows a une transition sans heurts entre les modes d’affichage.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Contrôle ou le prix de l’offre (Afficher/Masquer)**<br/> pour afficher ou masquer en douceur les contrôles ou leur intuitivité au survol ou au déplacement de la souris afin de simplifier l’aspect visuel normal. <br/>                | Affiche des contrôles lorsque les utilisateurs pointent le pointeur sur une zone de commande, ou affichent des intuitivité quand les utilisateurs pointent sur un contrôle. le fait de pointer sur ces zones indique que l’utilisateur a l’intention d’interagir. intuitivité peut masquer si le pointeur devient stationnaire. <br/> ![capture d’écran des contrôles ternis avant le survol ](images/vis-animations-image33.png)<br/> Dans cet exemple, les contrôles du lecteur Windows Media sont en fondu au survol en mode plein écran.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transitions de scènes**<br/> pour effectuer une transition de scène lisse et transparente afin d’éviter toute attention. <br/>                                                                                   | Les changements de scène brusques peuvent être transférerez, en particulier pour les grandes zones d’écran. Utilisez donc des transitions de scène pour créer des lissages et des continuités, et pour fournir un contexte. les transitions de scène sont conçues pour être des clés naturelles et basses, afin d’éviter d’attirer l’attention sur le processus de transition proprement dite.<br/> vocabulaire Windows : fondu en entrée/sortie ; fondu croisé ; glissement/gauche, arrière, vers le haut, vers le haut, vers le haut, vers le haut Push et couvertures. <br/> ![capture d’écran d’un fondu d’une photo dans une autre ](images/vis-animations-image34.png)<br/> Dans cet exemple, le papier peint du bureau Windows effectue un fondu délicat entre les images pour rendre la transition lisse et contrôlée.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transitions de scènes spéciales**<br/> pour attirer l’attention sur un changement de scène afin de le rendre spécial ou de recentrer l’attention de l’utilisateur. <br/>                                                               | Alors que la plupart des transitions de scène ne doivent pas attirer l’attention sur le processus de transition, certaines sont conçues pour rompre le Flow et attirer l’attention afin de mettre l’accent sur le fait qu’un autre point est sur le point de se produire. pour attirer l’attention, les transitions de scène spéciales sont conçues de façon non naturelle et ont un impact visuel élevé. <br/> ![capture d’écran de la diapositive de transition d’accrochage ](images/vis-animations-image35.png)<br/> Dans cet exemple, PowerPoint utilise des transitions d’avertissement pour attirer l’audience sur la modification.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulations directes**<br/> pour afficher l’effet des manipulations directes (telles que déplacer, faire défiler, faire pivoter, faire pivoter et zoomer). <br/>                                                                   | La transition montre l’effet de la manipulation en temps réel. l’effet devrait avoir une apparence fluide, continue et cohérente avec le monde réel. le déplacement et la rotation peuvent ne pas être continus à certains endroits pour indiquer des restrictions ou des choix préférés. le zoom rend le contenu plus grand ou plus petit, ce qui modifie éventuellement le niveau de détail en conséquence. <br/> ![capture d’écran de trois tailles de loupe ](images/vis-animations-image36.png)<br/> Dans cet exemple, la loupe effectue un zoom en douceur entre les niveaux.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulations directes incorrectes**<br/> pour indiquer qu’une manipulation directe (par exemple, déplacement, défilement/panoramique) a été tentée mais n’a pas pu être effectuée. <br/>                                           | La transition indique que la manipulation est tentée, mais revient à l’état d’origine. l’effet semble souvent que la manipulation ne peut pas être effectuée en raison d’une restriction physique réelle. ces animations sont utilisées à la place des messages d’erreur textuels, ce qui perturbe le sentiment réel de la manipulation.<br/> vocabulaire Windows : Bounce <br/> ![figure de communication de l’animation visuellement ](images/vis-animations-image4.png)<br/> Dans cet exemple, le document rebondit pour montrer que l’utilisateur a atteint la fin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Trier, filtrer, réorganiser les transitions**<br/> pour indiquer que la présentation ou le contenu d’une collection d’éléments a changé. <br/>                                                            | La transition indique (ou pour les modifications complexes, suggère) l’effet de la modification. <br/> ![capture d’écran des appareils photo avec trois retraits ](images/vis-animations-image37.png)<br/> ![capture d’écran similaire avec des caméras différentes supprimées ](images/vis-animations-image38.png)<br/> ![capture d’écran similaire avec les autres caméras supprimées ](images/vis-animations-image39.png)<br/> dans cet exemple, Bing Visual Search utilise une transition de filtre.<br/> ![capture d’écran de la couverture de l’album modifiant son apparence ](images/vis-animations-image40.png)<br/> Dans cet exemple, Windows Media Center utilise une transition de réorganisation comme une expérience spéciale lors de la diffusion d’une chanson.<br/>                                                                                                                                                                                                                                                                                   |
| **Transitions de performances**<br/> pour qu’une action apparaisse plus rapidement. <br/>                                                                                                              | Bien qu’une transition ait le potentiel de faire apparaître plus rapidement une action, l’objectif principal de ces transitions est d’améliorer la perception des performances et de la réactivité. une bonne technique est de montrer que la tâche est exécutée dans des étapes délibérées. en revanche, le retardement de l’action, le rendu des résultats de manière aléatoire, ou l’utilisation d’un indicateur d’activité est lent.<br/> Windows vocabulaire : effectuez des actions par étapes, avec des transitions lisses entre les étapes. <br/> ![capture d’écran de l’ajout de destinations à la liste de raccourcis ](images/vis-animations-image41.png)<br/> Dans cet exemple, une liste de raccourcis de la barre des tâches affiche immédiatement les éléments standard, puis les diapositives affichent les destinations une fois la liste prête. Cela permet de masquer le temps nécessaire à la création de la liste. En revanche, le retardement de l’affichage initial semblerait ne pas répondre et l’affichage d’une liste incomplète ou de commentaires de progression serait beaucoup plus lent.<br/> |
| **Expériences spéciales**<br/> pour attirer et faire plaisir aux utilisateurs pendant des [expériences spéciales](glossary.md) et peu fréquentes qui sont importantes pour votre programme et pour que l’utilisateur ait une attention toute particulière. <br/>    | Bien qu’une transition ait le potentiel pour être une expérience spéciale, ces transitions sont mieux réservées pour les expériences peu fréquentes qui sont véritablement spéciales pour votre programme. les transitions personnalisées sont utilisées pour fournir une apparence particulière. la personnalisation et la personnalité sont souvent des éléments de conception importants. Contrairement à d’autres modèles, les expériences spéciales peuvent nécessiter une attention, être lourdes et obliger les utilisateurs à attendre un moment. par conséquent, ces transitions s’usent rapidement en cas de surutilisation, car l’expérience n’est plus spéciale. <br/> ![capture d’écran du logo Windows modification du nouvel écran ](images/vis-animations-image42.png)<br/> Dans cet exemple, Windows Media Center affiche une animation lors du chargement de pour qu’il contacte immédiatement les utilisateurs.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Consignes

### <a name="effective-communication"></a>Communication efficace

-   **Définissez et utilisez un vocabulaire d’animation** pour vous assurer que vos animations et transitions ont une signification cohérente et l’utiliser de manière cohérente dans votre programme. La plupart des vocabulaires doivent inclure des entrées pour l’apparence des scènes et des objets, ainsi que pour la disparition, la navigation, l’interaction de base (pointage, sélection, clic), la manipulation et l’interaction des objets (déplacement, suppression, redimensionnement, défilement, panoramique, zoom, rotation, filtrage) et attirer l’attention. Une signification cohérente est essentielle pour une communication efficace.
-   **Dans la mesure du possible, utilisez le vocabulaire Animation Windows.** Bien que votre programme puisse avoir un public différent et des besoins différents, les avantages de la cohérence et de la familiarité compensent souvent les avantages de la différence. Si le vocabulaire de votre programme doit être différent, utilisez les mêmes types d’animation de base que Windows, mais donnez-leur la bonne personnalité pour votre programme.
-   **N’assignez pas de significations spécifiques aux animations et aux transitions génériques dans un vocabulaire d’animation.** Les transitions génériques comme les effets de fondu et les effets spéciaux comme les dissolutions n’ont aucune signification particulière (au-delà de l’affichage ou de la disparition), elles peuvent donc être utilisées librement.

    **Incorrect :**

    ![capture d’écran d’une boîte de dialogue en fondu dans une autre ](images/vis-animations-image43.png)

    Dans cet exemple, un fondu croisé est incorrectement utilisé pour accéder à l’élément suivant. Étant donné que les fondus croisés n’ont aucune signification particulière, cette transition ne fournit pas de contexte.

-   **Rendre les entrées de vocabulaire clairement distinctes.** Les actions connexes peuvent avoir des effets similaires (par exemple, le zoom avant et le zoom arrière doivent avoir des transitions inverses), mais les actions non liées doivent avoir des effets clairement distincts (par exemple, le zoom ne doit jamais être confondu avec rotation).
-   **Conservez des effets réels réalistes et cohérents.** Si vous utilisez des animations et des transitions réalistes, faites en sorte que l’expérience soit cohérente avec le monde réel. Les résultats ne doivent jamais être surpris, confus ou trompeurs. Et pour des fins de cohérence, ne mélangez pas les métaphores.
-   **Donnez aux animations des actions inverses.** Cela répond aux attentes des utilisateurs et simplifie le vocabulaire. Par exemple, si un volet s’affiche en glissant dans, supprimez-le en le faisant glisser vers un autre effet.
-   **Rendez les animations compréhensibles.** Les utilisateurs doivent pouvoir comprendre rapidement l’objectif d’une animation. Il est possible de rendre une animation trop petite, trop courte (moins de 50 millisecondes), ou si subtile que les utilisateurs ne sont pas en mesure de comprendre leur objectif. Dans ce cas, vous pouvez soit reconcevoir pour que la signification soit claire ou supprimée.

    **Incorrect :**

    ![capture d’écran de l’animation lors de la suppression de la boîte de dialogue ](images/vis-animations-image44.png)

    Dans cet exemple, l’effet est tellement petit et subtil que peu d’utilisateurs peuvent comprendre son objectif. Mieux pour la reconception ou la suppression.

### <a name="patterns"></a>Modèles

**Commentaires sur le survol**

-   **Pour paraître réactif, efforcez-vous de lire l’animation dans un délai de 50 millisecondes d’entrée ou de sortie de l’état de survol.**
-   **Pour qu’elle s’affiche rapidement, faites en sorte que la durée des animations au survol soit inférieure à 50 millisecondes.**
-   **Utilisez un effet d’atténuation/disparition en fondu de pointage.** Cela rend clairement les effets de pointage distincts des commentaires de clic et de sélection.

**Cliquez sur Commentaires**

-   **Pour paraître réactif, efforcez-vous de lire l’animation dans les 50 millisecondes de l’événement de clic.** Cliquer sur événements n’a pas besoin de cliquer sur commentaires.
-   **Pour qu’elle s’affiche rapidement, faites passer la durée des animations de clic à moins de 50 millisecondes.**
-   **Utilisez un effet flash ou clignotement de l’arrière-plan.** Cela rend les effets de clic clairement distincts des commentaires de survol et de sélection. En cliquant sur nécessite un pointage, cliquez sur Commentaires pour un ajout en douceur aux commentaires sur le survol.

**Commentaires sur la sélection**

-   **Pour paraître réactif, efforcez-vous de lire l’animation dans un délai de 50 millisecondes de la sélection ou de la désélection.**
-   **Pour qu’elle s’affiche rapidement, faites en sorte que la durée des animations de sélection soit inférieure à 50 millisecondes.**
-   **Utilisez un effet de rectangle de sélection de fondu/disparition en fondu.** Cela rend la sélection clairement différente du pointage et clique sur feedback.

**Commentaires sur la progression**

-   **Utilisez un indicateur d’activité lorsqu’une action ne peut pas être exécutée dans une seconde.** Cela indique que la commande a été reçue.
-   **Utilisez une barre de progression lorsque la tâche prend plus de cinq secondes.** Pour plus d’instructions, consultez [barres de progression](progress-bars.md).
-   **Utilisez les animations de commentaires de progression qui aident les utilisateurs à visualiser l’effet des tâches de longue durée.** Évitez les animations de commentaires de progression inutiles si une animation ne communique rien, utilisez une barre de progression à la place.
-   **Avoir des États d’achèvement et d’échec identifiables clairement.** Les utilisateurs doivent être en mesure de déterminer rapidement ces États finaux.
-   **Arrête l’indication de la progression lorsque la tâche sous-jacente n’est pas en cours d’exécution.** Les utilisateurs doivent être en mesure de déterminer si la progression n’est pas effectuée et de réagir en conséquence.

**Les attireurs**

-   **Utilisez des attireurs avec la contrainte.** À moins que les informations ne soient urgentes, critiques ou susceptibles d’affecter le comportement immédiat de l’utilisateur, il est généralement préférable de modifier l’état de façon invisible et de permettre aux utilisateurs de découvrir la modification de leur propre manière. [Résolvez les distractions, et non la détectabilité](/windows/desktop/uxguide/how-to-design-desktop-ux).

    ![capture d’écran des icônes d’État sans fil ](images/vis-animations-image45.png)

    Dans cet exemple, l’icône de la zone de notification du réseau sans fil utilise une animation pour les problèmes critiques, mais permet aux utilisateurs de découvrir leurs signaux faibles de manière autonome.

-   **Choisissez une animation qui attire le niveau d’attention approprié.** Les animations d’attirer doivent juste attirer l’attention sur elles-mêmes pour accomplir leur objectif, mais pas plus. Si l’utilisateur doit agir immédiatement, choisissez un effet qui requiert votre attention, quel que soit l’emplacement de l’utilisateur. Pour d’autres situations, reportez-vous à la section [attirer l’attention sur le niveau approprié](#attracting-the-right-level-of-attention) pour obtenir une bonne combinaison d’attention, d’avertissement et d’urgence.

    **Incorrect :**

    ![capture d’écran de l’Assistant Office du trombone ](images/vis-animations-image46.png)

    Les assistants de Microsoft Office ont attiré leur attention inutile.

-   **Si l’utilisateur ne répond pas, ne répétez pas l’animation ou utilisez des animations continues.** Au lieu de cela, supposons que l’utilisateur a choisi de ne pas agir maintenant, mais peut agir ultérieurement. Les animations continues permettent aux utilisateurs de se concentrer sur quoi que ce soit.

**Animations de relation**

-   **Utilisez les animations de relation pour indiquer l’origine ou l’emplacement des objets.**
-   **Les animations de relation doivent commencer ou se terminer par l’objet sélectionné.** N’affiche pas les relations entre les objets avec lesquels l’utilisateur n’interagit pas actuellement. Si les utilisateurs remarquent le tout, ce qu’ils remarquent est la gêne.

**Illustrations/aperçus**

-   **Utilisez des aperçus pour montrer l’effet d’une commande sans que les utilisateurs aient à l’exécuter en premier.** En utilisant des préversions utiles, vous pouvez améliorer l’efficacité et la facilité d’apprentissage de votre programme, et réduire la nécessité d’une évaluation et d’une erreur.
-   **Utilisez des illustrations et des aperçus qui ont une interprétation claire.** Ils ont peu de valeur en cas de confusion.
-   **Lisez une seule illustration à la fois** pour éviter d’allourder les utilisateurs. Si plusieurs illustrations simultanées sont possibles, utilisez le pointage de la souris ou un bouton de lecture pour permettre aux utilisateurs d’indiquer leur intérêt.
-   **Lire une illustration automatiquement si elle est le principal objectif de la fenêtre ou de la page.** Dans le cas contraire, laissez les utilisateurs le lire lorsqu’ils sont prêts.
-   **Jouez les animations à la vitesse optimale**: pas si rapides, elles sont difficiles à comprendre, mais pas si lentes, elles sont fastidieuses à regarder.

**Agrandissement/réduction de l’objet**

-   **Ne pas découper le contenu pendant un redimensionnement.** Développez conteneurs avant d’ajouter du contenu. Supprimer le contenu avant de réduire les conteneurs.

    **Incorrect :**

    ![capture d’écran de la calculatrice tronquée ](images/vis-animations-image47.png)

    Dans cet exemple, le contenu est découpé pendant un redimensionnement.

**Afficher/masquer/modifier le contenu**

-   **Affichez les informations importantes de manière statique.** Les utilisateurs ne doivent pas avoir à accéder à des informations importantes par le biais d’une divulgation progressive.

**Contrôle ou le prix de l’offre (Afficher/Masquer)**

-   **Affichez des contrôles importants lorsque l’utilisateur place le pointeur n’importe où dans la fenêtre ou le volet, ou si le bouton est plein écran, lors du déplacement de la souris.** Les utilisateurs ne doivent pas avoir à rechercher ces contrôles.

    ![Figure illustrant la façon dont le pointage affiche les contrôles ](images/vis-animations-image48.png)

    Dans cet exemple, Windows Media Center affiche ses contrôles chaque fois que le pointeur se trouve sur la fenêtre.

-   **Affiche les contrôles secondaires ou le contrôle intuitivité lorsque l’utilisateur place le pointeur sur les commandes.** Pour faciliter la découverte, rendez l’emplacement visible et la cible de grande taille.

    ![capture d’écran d’un pointeur révélant une commande secondaire ](images/vis-animations-image49.png)

    Dans cet exemple, Windows Live Messenger affiche une commande secondaire lorsque le pointeur se trouve près de l’angle supérieur droit.

**Transitions de scènes**

-   **Effectuez des transitions de scène physiques cohérentes avec le mappage naturel.** Les utilisateurs lisent de gauche à droite dans les cultures occidentales, et les diagrammes hiérarchiques se déplacent de haut en bas. Par conséquent, le déplacement vers l’avant dans le temps est indiqué par un déplacement de gauche à droite. Les transitions de scène physiques suivantes ont un mappage naturel :



    | Transition                          | Signification                                     |
    |---------------------------|--------------------------------------|
    | De gauche<br/>      | Revenir en arrière dans le déroulement des tâches<br/>    |
    | De droite<br/>     | Avancer dans le déroulement des tâches<br/> |
    | À partir du haut<br/>       | Déplacer la hiérarchie des tâches vers le haut<br/>    |
    | À partir du bas<br/>    | Descendre dans la hiérarchie des tâches<br/>  |



 

-   **Si votre programme émet des sons, concevez des transitions de scène et des transitions audio ensemble.** Par exemple, si une scène disparaît graduellement, tout son doit également être progressivement fondu. Ne pas gâcher des transitions visuelles transparents en ayant des transitions sonores brusques. Pour plus d’instructions sur le son, consultez [son](vis-sound.md).

**Manipulations directes**

-   **Lorsque vous utilisez des mouvements physiques dans l’interaction (comme le rejettement), concevez l’animation de manière à ce qu’elle ressemble à une réponse naturelle au geste.** Liez la cause de l’interaction avec l’effet de transition. Donnez à l’animation des caractéristiques physiques réelles, telles que l’accélération, la décélération, l’inertie, la résistance, le poids, le rebond et la rotation.
-   **Pour conserver une sensation directe, conservez les points de contact d’un objet sous le pointeur de manière régulière tout au long de l’interaction.** Tout décalage, réponse hachée ou perte de contact détruit la perception de la manipulation directe. Les objets ne doivent jamais disparaître lorsqu’ils sont manipulés.

**Trier, filtrer ou réorganiser des transitions**

-   **Pour les modifications simples, affichez la transition entière.** Les utilisateurs pourront facilement suivre la totalité de la transition. Les modifications simples impliquent quatre éléments ou moins.
-   **Pour les modifications complexes, insistez sur la fin du mouvement au fur et à mesure qu’il ralentit et laissez l’œil remplir le reste.** Cela rend le sentiment de mouvement bien plus réactif et ordonné.

**Transitions de performances**

-   **Envisagez d’effectuer des transitions lentes en deux ou trois étapes pour qu’elles apparaissent plus rapidement et immédiatement interactives.** Utilisez l’ordre de composition suivant, le cas échéant :
    -   Frame externe
    -   Arrière-plan
    -   Contenu initial (à l’aide d’une représentation temporaire si nécessaire)
    -   Contrôles principaux (afin que les utilisateurs puissent interagir immédiatement)
    -   Contrôles secondaires et tout autre élément d’interface utilisateur
    -   Contenu final (si une représentation temporaire a été utilisée) utilisez des transitions comme des fondus et des diapositives pour que la composition s’affiche de manière lisse, ordonnée et affinée.

![capture d’écran de la carte avec une photo et une grille satellites ](images/vis-animations-image50.png)

Lorsque vous faites défiler l’affichage « œil de l’oiseau », Bing Maps affiche un arrière-plan de grille temporaire. Cela permet aux utilisateurs de continuer à faire défiler immédiatement, bien avant le rendu du contenu final.

**Animations d’expérience spéciale**

-   **Reconsidérez les écrans de démarrage animés (ainsi que les écrans de démarrage statiques).** Souvent, les écrans de démarrage attirent l’attention sur le temps nécessaire au chargement d’un programme et s’acquittent rapidement. Si les écrans de démarrage sont acceptables s’ils s’affichent uniquement lorsque l’interaction utilisateur n’est pas possible, il est préférable de concevoir votre programme afin que les utilisateurs puissent interagir immédiatement, même s’ils sont en cours de chargement.
-   **Fournissez une commande ignorer l’introduction si un écran de démarrage animé prend plus de trois secondes.** Cliquer n’importe où sur l’écran de démarrage doit également le faire disparaître. Vous pouvez également utiliser une version abrégée de l’animation après une période initiale.

### <a name="performance"></a>Performances

-   **Ne faites pas en sorte que les utilisateurs attendent les animations et les transitions de votre programme.** Utilisez de brèves animations et transitions (moins de 200 millisecondes) chaque fois que cela est possible. Utilisez des animations plus rapides (100 millisecondes) pour les opérations plus fréquentes. Conception d’animations plus longues (plus d’une seconde généralement, les commentaires de progression, les illustrations et les modèles d’expérience spéciaux) pour que les utilisateurs puissent continuer à travailler pendant leur exécution.
-   **Concevez des animations de longue durée pour que les utilisateurs puissent interagir pendant que l’animation est en cours d’exécution.** Les utilisateurs ne tenteront pas de continuer à travailler si les indices visuels suggèrent qu’ils ne le sont pas.

    ![capture d’écran d’une barre de progression dans une barre d’État ](images/vis-animations-image51.png)

    Dans cet exemple à partir de Windows Internet Explorer, la barre de progression de clé basse dans la barre d’État suggère que les utilisateurs n’ont pas besoin d’attendre la fin de leur exécution pour pouvoir interagir.

-   **Utilisez des animations légères pour les tâches nécessitant beaucoup de ressources processeur.** Cela offre une puissance de traitement complète à la tâche. En outre, les utilisateurs ne perçoivent pas que l’animation légère est la raison pour laquelle la tâche est gourmande en ressources processeur.
-   **N’affiche pas d’indicateur d’activité pendant une animation ou une transition.** Cela détruit l’effet. Concevez des animations et des transitions afin qu’elles puissent commencer immédiatement.
-   **Concevez des animations pour une dégradation normale lorsqu’il y a des ressources système insuffisantes.** Les animations peuvent se dégrader en ayant des variations qui nécessitent moins de ressources (par exemple, des longueurs plus courtes ou des taux d’images inférieurs), voire pas du tout. Quelles que soient les ressources disponibles, assurez-vous que les animations ont une qualité élevée et qu’elles ressemblent à des animations au lieu des bogues logiciels.

    **Incorrect :**

    ![capture d’écran du détourage du cadre de programme sur le Bureau ](images/vis-animations-image52.png)

    Dans cet exemple, la transition de la restauration de la fenêtre est utilisée même si les ressources système ne sont pas suffisantes pour le lire correctement. Par conséquent, le frame figé semble être un bogue. Si les ressources ne sont pas disponibles, il est préférable d’afficher simplement la fenêtre sans transition.

### <a name="animation-characteristics"></a>Caractéristiques de l’animation

Les animations et les transitions bien conçues ont généralement les caractéristiques suivantes :

-   **Courte durée.** La plupart des animations doivent être comprises entre 100 et 300 millisecondes, de préférence 1/6 seconde (167 millisecondes) ou 1/4 seconde (250 millisecondes). (Des expériences spéciales et des commentaires de progression peuvent être plus longs.) Utilisez des durées d’animation plus rapides pour les opérations plus fréquentes. En règle générale, les animations plus longues prennent plus de temps, prennent plus de temps à comprendre et se sentent lentes.
-   **Réactivité.** Les animations doivent démarrer dans les 50 millisecondes de l’événement ou de l’action utilisateur initiateur. Les heures de début plus longues semblent ne pas répondre.
-   **Accélération/décélération.** Pour une apparence naturelle, la plupart des effets d’animation doivent être accélérés au démarrage et à la décélération lors de l’arrêt. Pour que les animations de conception soient réactives, démarrez rapidement. Pour qu’elles apparaissent contrôlées, créez des animations à la fin. Bien que cela s’applique aux effets de mouvement, elle s’applique également à tous les effets qui suggèrent des mouvements, tels que les zooms et même les fondus.

    ![figure d’un graphique présentant une vitesse réduite dans le temps ](images/vis-animations-image53.png)

    La plupart des animations doivent avoir des Démarrages rapides et des fins conditionnelles pour avoir une sensation réactive et néanmoins contrôlée.

-   **Films.** Les animations qui illustrent le mouvement en particulier doivent accélérer et ralentir, donc n’utilisez pas le mouvement linéaire, sauf si la durée de l’animation est très brève. Les mouvements doivent prendre le chemin Shorts du début à la fin, sans dépassement. Le chemin de mouvement complet n’est pas toujours obligatoire. Le cas échéant, insistez sur la fin du mouvement au fur et à mesure qu’il ralentit et laissez l’œil remplir le reste. Cela rend le sentiment de mouvement bien plus réactif et ordonné. Quand vous animez le mouvement de plusieurs objets simultanément, donnez-leur des chemins légèrement différents avec des minutages légèrement différents afin de vous sentir plus naturels.
-   **Fréquence d’images.** La plupart des animations doivent utiliser une fréquence d’images de 20 images par seconde. Si l’animation est destinée à une expérience spéciale ou est liée à l’objectif principal du programme, envisagez d’utiliser un taux plus élevé de 24 30 images par seconde pour améliorer la fluidité et le réalisme.
-   **Mise à l’échelle** Concevez des animations pour fonctionner correctement dans l’ensemble de leur plage d’utilisation prévue. Par exemple, les transitions de page doivent être conçues pour fonctionner pour toutes les tailles de page.
-   **Personnalité.** Concevez les animations de manière naturelle, subdued et efficace plutôt que artificielle, saugrenu ou lente.

### <a name="animated-text"></a>Texte animé

-   Vous pouvez afficher du texte à l’aide d’une transition, **sans animer le texte en continu.** Le texte animé est souvent distrait et difficile à lire que le texte statique. **Exceptions :**
    -   Vous pouvez animer du texte dans des situations où il est traditionnellement animé et vous fournissez une alternative accessible.
    -   Vous pouvez animer du texte si l’objectif du texte est principalement décoratif.

![capture d’écran de l’interface Zune conçue de façon créative ](images/vis-animations-image13.png)

Dans cet exemple, Zune anime du texte, mais son objectif est principalement décoratif. Il n’y a pas de problème si les utilisateurs ne lisent pas le texte avec soin.

### <a name="reducing-power-consumption"></a>Réduction de la consommation d’énergie

-   **Concevez vos animations pour réduire la consommation d’énergie.** Lorsqu’elles sont correctement conçues, les animations ne doivent pas augmenter de manière significative la consommation énergétique. Pour réduire la consommation d’énergie :
    -   **Arrêter l’animation lorsque l’affichage est désactivé.** L’affichage peut être désactivé à des fins d’économie d’énergie.
    -   **N’utilisez pas les animations de longue durée qui ne sont pas initiées par l’utilisateur.** Les animations qui utilisent des minuteries périodiques haute résolution réduisent l’efficacité de la gestion de l’alimentation du processeur. Veillez également à désactiver les minuteurs périodiques à haute résolution lorsque les animations sont terminées.
    -   **Interrompez toutes les animations lorsque le système devient inactif.** La période d’inactivité de l’utilisateur à devenir inactive est déterminée par les options d’alimentation dans le panneau de configuration.

### <a name="accessibility"></a>Accessibilité

-   **N’utilisez pas l’animation comme seule façon de transmettre des informations essentielles.** Les animations doivent communiquer des informations utiles, mais pas critiques, car elles ne sont pas accessibles aux utilisateurs ayant des handicaps.
-   Assurez-vous que les **informations équivalentes sont disponibles par d’autres moyens,** par exemple :

    -   **Par inspection.** Les utilisateurs peuvent déterminer des informations équivalentes en examinant l’écran ou les objets impliqués dans l’animation.
    -   **Par simple interaction.** Les utilisateurs peuvent déterminer des informations équivalentes en pointant sur, en cliquant ou en double-cliquant sur.

    ![capture d’écran de la page d’accueil de Bing avec des zones réactives ](images/vis-animations-image54.png)

    La page d’origine Bing contient une animation initiale qui révèle plusieurs zones réactives. Les utilisateurs peuvent également afficher les zones réactives en déplaçant le curseur près.

    Notez que les « informations équivalentes » ne signifient pas des informations identiques. Les informations peuvent être dans un format différent ou nécessitent une déduction simple.

-   **Le cas échéant, définissez le focus d’entrée sur l’objet modifié pendant une transition.** Cela permet aux technologies d’assistance de détecter l’endroit où la modification s’est produite. Mais ne modifiez pas le focus d’entrée lorsque l’utilisateur utilise le clavier.
-   **N’utilisez pas les animations ou les transitions qui flashent ou redimensionnent les objets rapidement.** Les changements d’écran clignotants et rapides peuvent engendrer des problèmes pour les personnes souffrant de crises et d’autres troubles neurologiques.
-   **Autorisez les utilisateurs à désactiver les animations et les transitions de votre programme.** Pour prendre en charge cette fonctionnalité, respectez l’option désactiver toutes les animations inutiles dans la facilité d’accès de Windows.

    **Développeurs :** Vous pouvez déterminer si les animations sont activées à l’aide de l’API SystemParametersInfo.

-   **Tâches de conception supposant que les utilisateurs vont désactiver les animations de votre programme.** Assurez-vous que cela n’interrompt pas le workflow de manière significative.

Pour plus d’informations sur les consignes d’accessibilité, consultez [accessibilité](inter-accessibility.md).

## <a name="documentation"></a>Documentation

-   Évitez de faire référence aux animations chaque fois que cela est possible. Au lieu de cela, reportez-vous à l’objet animé et, si nécessaire, au type d’animation.
-   Ne faites pas référence aux transitions, sauf dans la documentation technique. Au lieu de cela, faites référence à l’objet dans son état final ou initial.
-   Si l’utilisateur lance explicitement une animation, utilisez le verbe Play ; Sinon, utilisez le verbe pour obtenir de la documentation technique.

Exemples :

-   Vous savez qu’un élément nécessite votre attention lorsque son icône commence à rebondir.
-   Tout d’abord, sélectionnez les photos que vous souhaitez imprimer (Notez que les photos sont agrandies lors de la sélection).
-   Utilisez une transition de fondu croisé pour modifier l’état d’un objet en toute transparence.

