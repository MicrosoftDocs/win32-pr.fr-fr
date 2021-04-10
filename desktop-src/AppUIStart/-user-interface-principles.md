---
title: Principes de l’interface utilisateur
description: Cette rubrique explique comment implémenter une interface utilisateur intuitive et des principes de conception de l’expérience utilisateur dans des applications Windows.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98383f9379248570ef8b254c647ab8348d703696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031612"
---
# <a name="user-interface-principles"></a>Principes de l’interface utilisateur

Cette rubrique explique comment implémenter une interface utilisateur intuitive et des principes de conception de l’expérience utilisateur dans des applications Windows.

-   [Introduction](#introduction)
-   [Principes de base de l’interface utilisateur appropriée](#the-basic-principles-of-proper-ui)
    -   [Espacement et positionnement](#spacing-and-positioning)
    -   [Taille](#size)
    -   [Regroupement](#grouping)
    -   [Intuitive](#intuitiveness)
-   [20 conseils pour une expérience utilisateur plus efficace et fonctionnelle](#20-tips-for-a-better-functional-user-experience)
    -   [Utiliser les normes](#use-standards)
    -   [Attirer l’attention sur les boutons importants](#draw-attention-to-important-buttons)
    -   [Simplifier la reconnaissance avec les icônes](#simplify-recognition-with-icons)
    -   [Simplifier la reconnaissance avec les en-têtes](#simplify-recognition-with-headers)
    -   [Utiliser des boîtes de message personnalisées](#use-custom-message-boxes)
    -   [Inclure d’autres commandes](#include-alternate-commands)
    -   [Comment gérer des actions critiques](#how-to-handle-critical-actions)
    -   [Des cases d’option ou des ComboBoxs ?](#radiobuttons-or-comboboxes)
    -   [N’interrompez jamais l’utilisateur !](#never-disrupt-the-user)
    -   [Indiquer l’état de progression](#provide-progress-status)
    -   [Simplifier les étapes complexes avec les assistants](#simplify-complex-steps-with-wizards)
    -   [Tirez le ton de votre texte vers la droite](#get-the-tone-of-your-text-right)
    -   [Parfois, un ListView est plus performant](#sometimes-a-listview-is-better)
    -   [Simplifier la navigation avec les contrôles de navigation et les encadrés](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Utiliser des graphiques assez esthétiques](#use-pretty-graphics)
    -   [Fournir des formulaires redimensionnables lorsque cela est possible](#provide-resizable-forms-when-possible)
    -   [Fournir davantage de fonctionnalités avec les encadrés/volets de tâches](#provide-more-functionality-with-sidebarstask-panes)
    -   [Fournir un choix de notification](#give-a-notification-choice)
    -   [Fournir des info-bulles !](#provide-tooltips)
    -   [N’oubliez pas les petits éléments](#do-not-forget-the-little-things)
-   [Conclusion](#conclusion)

## <a name="introduction"></a>Introduction

Les développeurs ne parviennent souvent pas à prendre en compte le point de vue de l’utilisateur final. Les développeurs travaillent difficilement pour faire fonctionner l’application : les clients s’attendent à ce qu’ils travaillent et leur perception des centres logiciels autour de cette exigence. Cela est particulièrement vrai si vous développez un logiciel de vente au détail ou qui sera utilisé par des personnes non techniques. Les développeurs doivent connaître les besoins de l’utilisateur final tout au long du processus de conception de logiciels.

Une application logicielle doit être aussi facile à parcourir et à utiliser que possible. Avec la quantité de logiciels en cours de création, les 4 applications logicielles sur 10 estimées ont une interface utilisateur très intéressante que l’utilisateur final aime et est instantanément à l’aise avec.

Une quantité importante de logiciels à usage interne est créée pour les entreprises. Qu’il soit développé en interne ou sous le soin d’un consultant, souvent un minimum de temps, d’efforts ou d’argent est investi dans la création d’une meilleure interface utilisateur. Le rôle « concepteur » est rare dans le cycle de développement, en particulier dans le monde des applications Windows.

Il existe quelques règles de base à suivre pour obtenir une interface utilisateur plus attrayante et mieux opérationnelle pour votre application. Cela ne nécessite pas trop de temps ou d’argent en votre part et ajoute un bon retour sur investissement.

Avant d’aller plus loin, nous allons faire la différence entre l’interface utilisateur et l’expérience utilisateur, du moins dans le cadre de cet article. L’interface utilisateur, ou interface utilisateur, fait référence aux visuels et aux contrôles de votre application, tandis que l’expérience utilisateur, ou UX, englobe à la fois l’interface utilisateur et le comportement de l’application associée à l’interface utilisateur, ainsi que le « sentiment » que l’utilisateur obtient de votre application. Il ne s’agit pas seulement de concevoir une interface utilisateur attrayante, mais de s’assurer qu’elle fonctionne bien.

Ici, nous allons aborder 20 points de conception de l’expérience utilisateur que vous pouvez intégrer facilement à la phase de conception de votre application. Le résultat sera des applications plus riches avec de meilleures fonctionnalités intuitives, une « expérience utilisateur humaine ». Comme nous savons tous que la génération d’applications Windows Vista doit se présenter et se comporter différemment. Cette rubrique vous aidera à préparer les futures applications tout en donnant à vos utilisateurs actuels un aperçu du futur.

Les sections suivantes décrivent les principes fondamentaux de la conception d’interface utilisateur appropriée.

## <a name="the-basic-principles-of-proper-ui"></a>Principes de base de l’interface utilisateur appropriée

Une expérience utilisateur de qualité professionnelle dépend de ces quatre facteurs :

-   Espacement et positionnement
-   Taille
-   Regroupement
-   Intuitive

Avec les versions de Microsoft Visual Studio antérieures à 8,0, l’espacement et le dimensionnement étaient non optimaux. Une grille 4x4 ou x 4 ne fonctionne pas toujours. Avec l’inclusion des lignes d’alignement (SnapLines), le processus a été considérablement simplifié. L’alignement d’une étiquette avec une zone de texte, voire pire, l’alignement de plusieurs étiquettes avec leurs zones de texte correspondantes était extrêmement difficile dans les versions précédentes de Visual Studio. Les lignes d’alignement (SnapLines) ont considérablement simplifié ce processus.

Les sections suivantes décrivent quatre des aspects les plus importants de la conception de l’expérience utilisateur professionnelle.

### <a name="spacing-and-positioning"></a>Espacement et positionnement

L’espacement entre deux contrôles est important. La capture d’écran suivante montre un formulaire d’entrée d' **informations utilisateur** mal conçu : les deux premières zones de texte sont trop proches, la liste en dessous est trop éloignée et il y a beaucoup d’espace inutilisé sur le formulaire.

![capture d’écran d’un formulaire mal conçu.](images/humanux-01.png)

Dans la capture d’écran suivante, vous pouvez voir une boîte de dialogue plus professionnelle avec un espacement correct et des contrôles de taille appropriée. Il s’agit de la même forme que dans la capture d’écran précédente, mais elle a été modifiée pour utiliser l’espacement recommandé par les lignes d’alignement (SnapLines). Il est toujours recommandé d’aligner une étiquette avec la ligne de base du texte de la zone de texte ou d’un autre contrôle en regard de celle-ci, plutôt que la bordure inférieure réelle du contrôle. Les lignes d’alignement (SnapLines) transforment une autre couleur lorsque l’alignement est atteint, généralement quelques pixels au-dessus de la bordure inférieure.

![capture d’écran d’un formulaire plus bien conçu.](images/humanux-02.png)

Bien qu’il n’existe pas de règles exactes pour l’espacement, les lignes d’alignement fournissent des indications extrêmement utiles pour un espacement correct. D’autres outils pour vous aider à conserver un espacement correct sont les contrôles de disposition dans le groupe boîte à outils conteneurs. Le TableLayoutPanel est également très utile pour créer des boîtes de dialogue de style de formulaire d’entrée.

### <a name="size"></a>Taille

Les mêmes considérations s’appliquent à la taille. Quand vous faites glisser un bouton de la boîte à outils vers votre formulaire, sa hauteur et sa largeur sont parfaitement optimales. La largeur maximale recommandée (en excluant les raisons les plus importantes) consiste à doubler la largeur d’origine.

Si vous examinez la fenêtre **exécuter** dans le menu **Démarrer** ou la boîte de dialogue **Propriétés** de n’importe quel objet Explorateur Windows, les tailles de bouton sont « juste à droite ». Si vous avez une fonction très importante dont vous avez besoin pour que votre utilisateur final Remarque sans échec, il existe d’autres méthodes que l’utilisation d’un grand bouton ou de couleurs non standard criarde (vous en apprendrez davantage sur cela plus tard).

Dans l’image suivante, vous pouvez voir trois boutons. Le premier bouton est la taille recommandée et est la taille créée par défaut quand vous la faites glisser (ou double-cliquez) à partir de la boîte à outils. Parfois, du texte supplémentaire nécessite que vous agrandissiez le bouton. Le deuxième bouton affiche une taille importante mais acceptable. Elle ne crée pas de désordre pour la disposition d’autres contrôles. Le troisième bouton, toutefois, est une taille complètement inacceptable. Vous pouvez constater qu’elle déforme légèrement les bitmaps de thème que Windows utilise pour dessiner les contrôles à thème. Il est également difficile d’aligner d’autres contrôles de manière intuitive.

![image de trois boutons, d’une taille allant de gauche à droite.](images/humanux-03.png)

### <a name="grouping"></a>Regroupement

En règle générale, une application contient de nombreux contrôles. Seul le regroupement approprié et intuitif peut faciliter l’utilisation de tous ces contrôles. Le regroupement basé sur une fonction ou par catégorie est optimisé par les contrôles d’onglet. Par exemple, les rapports « comptes », « employés » et « projets » sont des candidats idéaux pour les onglets dans une application métier classique. Regroupement frère : les contrôles qui contribuent au même résultat final sont mieux réalisés par les contrôles de groupe. L’utilisation de panneaux avec des bordures pour ce type de regroupement n’est pas recommandée. Les contrôles de groupe vous font gagner du poids supplémentaire d’un contrôle Label, surtout si vos sous-contrôles sont explicites.

Les contrôles de groupe dans les contrôles de groupe ne sont pas recommandés, sauf s’il n’y en a pas plus de 2 ou 3 dans un contrôle de groupe de grande taille.

### <a name="intuitiveness"></a>Intuitive

Il s’agit de l’aspect le plus important d’une expérience utilisateur exceptionnelle. L’expérience utilisateur intuitive réduit la nécessité d’explications. L’utilisateur sait simplement ce que font les contrôles.

Un sujet important dans une conception intuitive est le codage de couleurs. Un bon exemple est présenté dans Windows XP, qui a présenté de nouveaux boutons flous pour des fonctions telles que la navigation dans les applications à thème, la **déconnexion** et la désactivation des boîtes de dialogue d' **ordinateur** , etc.

Les couleurs de ces contrôles ont été déterminées en fonction de la gravité du résultat de l’envoi du bouton. La navigation est verte, à l’instar d’un feu de circulation « Go ». L’arrêt, ce qui entraînerait une perte de travail potentielle, est coloré en rouge comme un signe d’avertissement. Les boutons semi-critiques, tels que la déconnexion ou la mise en veille prolongée, sont jaunes. Les boutons neutres qui n’ont aucun effet critique sur les processus de travail de l’utilisateur, tels que l’aide, sont un bleu léger. Lorsque vous créez une interface utilisateur dépouillée, ces aspects de couleur doivent être conservés à l’esprit.

Un bon exemple de reconnaissance de contenu par couleurs est Microsoft Office OneNote. Les onglets de l’application peuvent être définis sur des couleurs différentes, tout en faisant en sorte qu’elles ressemblent à une partie appropriée de la conception de style Windows XP globale.

Un autre aspect important est le texte dans vos applications. Récemment, il y a eu plusieurs efforts pour simplifier le langage utilisé pour les instructions écrites dans les logiciels Windows. L’utilisation du texte dans le logiciel sera abordée plus tard, mais notez les détails de petite taille, mais importants.

MSN Messenger avait une case à cocher dans la boîte de dialogue **options** marquée « fonctions de partage de la webcam ». Les développeurs et les gens du Tech savent ce que cela signifie, mais un utilisateur novice pourrait penser que vous pourriez permettre à un autre utilisateur à l’autre extrémité de votre conversation d’utiliser votre CAM Web. Dans une version récente, ils ont été remplacés par « mon Webcam : autoriser les autres utilisateurs à voir que je dispose d’une webcam ». Cela est parfait pour le public cible qui ne dispose peut-être pas de connaissances techniques et qui est utilisé pour une langue simple.

Bien qu’il soit plus facile de comprendre le langage plus simple, il y a également un avantage supplémentaire. Les études scientifiques montrent que notre esprit est plus facile avec un langage plus simple quand vous essayez de comprendre quoi que ce soit de nouveau. Souvent, notre cerveau traite des mots tels que « IT », « », «, » et d’autres mots courants, si rapidement et sans effort que davantage de « bande passante » est alloué à la compréhension des mots tels que « webcam » ou « autres », dans l’exemple ci-dessus.

Les titres de boîte de message, les légendes de zone de groupe et d’autres blocs de texte de ce type facilitent la communication de la fonction d’un groupe de contrôles à l’utilisateur final en quelques mots.

L’intuitive est également née de la familiarité. Par exemple, le positionnement des boutons **OK** et **Annuler** est tellement uniforme et bien placé dans l’esprit que si une boîte de dialogue contient ces boutons dans une séquence inverse **(annuler**, puis **OK**; au lieu de **OK**, puis **Annuler**), vous pouvez simplement cliquer sur **Annuler** . Après l’utilisation d’une norme particulière pour faire des choses (applications Windows, par exemple) depuis plus d’un an, les habitudes se développent. Les normes de l’industrie suivantes (mais sans État) rendent votre logiciel plus facile à utiliser.

Dans l’une des premières versions préliminaires de Windows Vista, les boutons **réduire**, **agrandir** et **Fermer** d’une fenêtre sont devenus différents. Dans les versions précédentes de Windows (notamment lors de l’utilisation d’une seule analyse), vous développez une habitude de déplacer le curseur dans l’angle supérieur droit de l’écran, puis en cliquant sur. Cela a toujours entraîné la fermeture de la fenêtre. Maintenant, dans cette version particulière de Windows Vista, il y avait environ 8 pixels de l’espace entre le bouton Fermer et la bordure la plus à droite de la fenêtre. L’espace supplémentaire a fait de l’air froid (et était probablement nécessaire pour que l’animation de l’éclat froid le bouton sport), mais était irritante, car elle ne permettait pas aux utilisateurs de fermer les fenêtres ouvertes aussi facilement. Il peut être difficile de reconditionner votre esprit. Heureusement, dans la build suivante, ce problème a été résolu. À présent, il y a toujours de l’espace entre la bordure de la fenêtre et le bouton Fermer, mais le fait de cliquer sur cet espace provoque également la fermeture de la fenêtre.

L’un des facteurs les plus importants de la conception intuitive est la quantité de bandwidth’mentales, le temps qu’il peut prendre en compte pour comprendre un élément, qu’il utilise. Plus l’utilisation de la bande passante est faible, plus votre expérience utilisateur est bonne.

Il s’agit de petits éléments qui contribuent à l’expérience de l’utilisation d’une application logicielle. Les exemples suivants fournissent des conseils sur l’amélioration de vos applications grâce à des conseils et astuces réels.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 conseils pour une expérience utilisateur plus efficace et fonctionnelle

L’objectif d’une meilleure expérience utilisateur est d’avoir une interface utilisateur plus simple, plus facile et fonctionnelle qui est également correcte. Ces conseils vous aideront à mettre en forme votre interface utilisateur pour qu’elle soit plus efficace.

### <a name="use-standards"></a>Utiliser les normes

Les normes établies d’un environnement logiciel, que ce soit au niveau du système d’exploitation, au niveau de la configuration ou au niveau de l’application, sont très importantes. Outre la personnalisation, les normes agissent comme un schéma de proverbes dans l’esprit de l’utilisateur. Lorsque l’utilisateur consacre de longues périodes de travail à une application logicielle, il augmente automatiquement la productivité en raison de la familiarité croissante.

Avant d’aborder les normes, voyons tout d’abord ce que sont exactement ces normes. Les normes incluent tout ce qui est de la disposition des contrôles d’une manière particulière sur les boîtes de dialogue, comme les boutons **OK** et **Annuler** , la forme de l’interface utilisateur, à savoir les angles arrondis du haut de la fenêtre comme dans les boîtes de dialogue Windows XP, les styles d’icônes, les styles des autres graphiques, le comportement interactif de votre application, etc.

Si votre application se trouve dans une niche spécifique, il peut être intéressant de suivre un ensemble de normes différent. Par exemple, si votre application prend en charge l’application, ou un module complémentaire pour, Office OneNote 2003, il est préférable de suivre les styles de l’interface utilisateur et les normes d’interactivité d’Office, et OneNote lui-même, en particulier. Cela comprend l’utilisation des barres de commandes de style Office à la place des barres d’outils standard, et d’autres choses, à la fois visuel et comportementale. Si votre application doit faire partie de la catégorie Microsoft Visual Studio .NET, vous disposez d’un ensemble de normes distinct. En fait, pour ces applications de support ou de complément, les entreprises telles que Microsoft ne publient pas de directives. Notez également que les concepts graphiques et de conception sont parfois des propriétés intellectuelles protégées. Vérifiez toujours la documentation appropriée pour vous assurer que vous disposez de la licence nécessaire à la création de ces conceptions.

Un troisième exemple de normes serait l’environnement Tablet PC. Ces normes franchissent les limites entre les instructions du système d’exploitation et les instructions relatives aux applications. La [documentation du kit de développement logiciel (SDK) Tablet PC](/previous-versions/ms840465(v=msdn.10)) contient des informations très utiles dans la rubrique « planification de votre application ». Contrairement aux instructions de theOffice 2003 ou Visual Studio, ces recommandations de conception affectent directement la manière dont l’utilisateur interagit avec votre application et comment il doit se comporter à son tour. Par exemple, si vous avez des fenêtres d’ancrage dans votre application, la documentation vous recommande de vérifier qu’elle peut détecter lorsque l’orientation de l’écran est modifiée, et que les fenêtres d’ancrage se réorganisent correctement dans une orientation portrait ou paysage si nécessaire. Même si vous ne concevez pas votre application pour qu’elle soit spécifique à une tablette, vous devez passer en revue ces instructions.

Avec la montée en charge de clients intelligents, les applications franchissent désormais les limites entre différents matériels : ordinateurs normaux, Tablet PC, appareils mobiles ou ultra mobiles, PC Media Center, etc. Chaque situation nécessite la suivi d’un ensemble de normes différent (ou supplémentaire).

Lorsque les applications partagent les normes au niveau du système d’exploitation ou au niveau de l’application, les utilisateurs se sentent plus à l’aise avec le logiciel, ce qui facilite l’apprentissage et l’utilisation. Il en résulte une amélioration directe de la productivité. Les utilisateurs veulent pouvoir être plus productifs avec les nouveaux logiciels le plus rapidement possible.

### <a name="draw-attention-to-important-buttons"></a>Attirer l’attention sur les boutons importants

Parfois, vous devez diriger l’utilisateur vers les boutons les plus importants, même si vous avez quatre ou cinq autres boutons qui l’entourent. Si vous expérimentez la taille, la couleur ou la police, vous risquez d’altérer les normes, ce qui n’est pas recommandé. Au lieu de cela, vous pouvez utiliser quelques astuces simples pour y parvenir.

La première consiste à convertir les autres boutons non critiques en LinkLabels comme indiqué dans l’image suivante. De cette façon, l’utilisateur sait que ces liens effectuent une tâche, mais leur attention passe tout d’abord au bouton qui s’affiche, sans rompre les règles de conception standard.

![image de trois boutons converties en linklabels.](images/humanux-04.png)

La seconde consiste à placer le bouton critique en premier dans la ligne, soit à gauche pour les dispositions horizontales, comme indiqué dans l’image suivante, soit en haut pour les dispositions verticales. Notez que cela peut varier en fonction de la culture de l’utilisateur cible. vous pouvez être plus intéressant si vous placez le bouton en question à l’extrême droite si votre application est une langue écrite de droite à gauche.

![image de trois boutons où le bouton critique est le plus à gauche dans une disposition horizontale.](images/humanux-05.png)

L’option recommandée consiste à définir pour recevoir le focus par défaut. Par exemple, dans une boîte de dialogue de confirmation de suppression, l’option **non** doit être mise en surbrillance, ce qui empêche l’utilisateur de supprimer accidentellement un événement.

### <a name="simplify-recognition-with-icons"></a>Simplifier la reconnaissance avec les icônes

Les icônes, en particulier les icônes Windows XP et Office 2003 et les bitmaps de barre d’outils, permettent d’accélérer le cognitives de l’interface utilisateur et la tâche que l’utilisateur doit effectuer.

Par exemple, lorsque vous voyez l’icône d’exclamation la plus souvent visible dans la boîte de message, vous êtes instantanément informé du niveau de risque associé aux contrôles en regard de cette icône. De même, lorsque votre application met en place un grand nombre de contrôles, quelle que soit la façon dont elle est correctement organisée, il peut être difficile de trouver l’ensemble des contrôles que vous recherchez.

Dans Windows XP Service Pack 2, un onglet mis à jour est ajouté à l’applet du panneau de configuration des **Propriétés système** appelée « mises à jour automatiques ». Quatre options sont disponibles : téléchargez automatiquement les mises à jour, téléchargez les mises à jour, mais laissez l’utilisateur décider quand les installer, avertissez l’utilisateur si des mises à jour sont disponibles, mais ne démarrez pas le téléchargement et désactivez complètement les mises à jour automatiques.

Un nouvel utilisateur de PC peut ne pas être conscient de ce que sont ces mises à jour et peut ne pas savoir quelle option choisir. Par conséquent, Microsoft a placé une icône de blindage verte avec une coche de grande taille en regard de l’option « sécurisé », et une icône de bouclier rouge avec un gros « x » à côté de celle qui serait potentiellement dangereuse pour l’utilisateur. Cela est très utile dans les situations critiques, en particulier lorsque l’utilisateur n’a pas le temps de lire trop de texte.

Dans la même application de **Propriétés système** , chaque onglet possède plusieurs GroupBoxes avec différents contrôles pour différentes tâches. Un graphique relatif est placé en regard de chaque groupe qui correspondrait facilement à la tâche du groupe de contrôles. Ce type de code graphique est semblable au codage en couleurs dans les fichiers physiques ou les lots de parking. Cela fonctionne également sur le même principe que le fait d’avoir au moins certains éléments visuels dans un article de magazine, mais elle garde l’intérêt du lecteur.

Le choix de l’icône appropriée est également important. Microsoft fournit de nombreux graphiques standard dans le cadre de Visual Studio 2005. Il s’agit du meilleur choix. Si vous créez vos propres icônes, il est vivement recommandé de suivre les normes au niveau du système d’exploitation ou de l’application pour ces graphiques, comme indiqué dans la section [utiliser les normes](#use-standards) ci-dessus.

Les [instructions relatives à l’interaction avec l’expérience utilisateur Windows](/windows/apps/desktop/) contiennent un guide très utile pour créer des [icônes](https://msdn.microsoft.com/library/aa511280.aspx)de style Windows.

### <a name="simplify-recognition-with-headers"></a>Simplifier la reconnaissance avec les en-têtes

Les en-têtes sont le moyen idéal d’expliquer l’intégralité de la boîte de dialogue dans une seule phrase (et éventuellement un graphique). Parfois, les en-têtes peuvent même vous aider à prendre également en charge la navigation et les commandes. Les en-têtes fonctionnent plus efficacement que les étiquettes de description normale, car il s’agit de la première chose qu’un utilisateur voit lorsque la boîte de dialogue s’affiche.

Les assistants Windows Installer sont peut-être les en-têtes les plus populaires : une simple icône à l’extrême droite. étiquette de titre décrivant la boîte de dialogue (par exemple, sélectionner le dossier d’installation); et un sous-titre qui décrit l’objectif de la boîte de dialogue (par exemple, sélectionnez le dossier dans lequel les fichiers logiciels seront installés).

Supposons que nous disposons d’une application métier typique avec une section Accounts. Suite au paradigme de conception de Windows Vista, nous pouvons fournir des informations critiques et des commandes associées dans l’en-tête (ou le pied de page, si le scénario les appelle) lui-même. Notre utilisateur a ouvert le fichier de compte pour la « grande société » et l’en-tête ressemble à ce qui est illustré dans la capture d’écran suivante.

![capture d’écran d’une boîte de dialogue qui contient un pied de page détaillé.](images/humanux-06.png)

La capture d’écran suivante montre un exemple d’en-tête détaillé dans une boîte de dialogue.

![capture d’écran d’une boîte de dialogue qui contient un en-tête détaillé.](images/humanux-07.png)

De même, vous pouvez éviter d’avoir à ajouter des volets des tâches de style Windows XP, en particulier lorsque vous n’avez qu’un petit nombre de commandes qui gaspillent beaucoup d’espace vertical, en déplaçant ces commandes vers l’en-tête.

Voici quelques points à prendre en compte lors de la conception d’en-têtes :

-   Vérifiez que la couleur d’arrière-plan est différente de la couleur d’arrière-plan de la boîte de dialogue. Plus souvent, un en-tête blanc sur une couleur de contrôle intrinsèque Windows standard est fait. Toutefois, si vous voulez vraiment vous assurer qu’aucun thème spécial ou aucune couleur personnalisée n’est en désordre dans votre en-tête, dessinez un **LinearGradient** à l’aide de **Color. FromKnownColor** avec les couleurs **ControlLight** et **ControlDark**.
-   Si possible, conservez la hauteur de votre en-tête sous 150 pixels. En règle générale, une hauteur de 100 ou 120. En règle générale, assurez-vous qu’il est inférieur à 1/4 de la hauteur du formulaire entier.
-   Si vous souhaitez ajouter une modification sur place pour les informations affichées dans l’en-tête ci-dessus, remplacez le LinkLabel de manière dynamique par une zone de texte et échangez-les une nouvelle fois la modification effectuée.
-   Si vous avez une étiquette de titre avec une police d’une taille supérieure à 10 PT, utilisez Arial ou Franklin Gothic Medium. MS sans serif sera trop irrégulier et ne serait pas professionnel. Franklin Gothic Medium est la recommandation de la documentation sur les instructions de conception de Windows XP. Pour les applications ciblant Windows Vista, utilisez la police Segoe UI qui est la police par défaut du système.

### <a name="use-custom-message-boxes"></a>Utiliser des boîtes de message personnalisées

Les options disponibles dans la boîte de message Windows standard sont très limitées. Lorsque vous devez demander à votre utilisateur une question qui ne peut pas être traitée avec un simple oui/non ou OK/Annuler, il devient compliqué.

Les applications Windows deviennent désormais plus simples à utiliser en raison du grand nombre d’utilisateurs non techniques. Parfois, il peut être beaucoup plus simple de fournir des boutons avec des textes plus conviviaux et même des contrôles supplémentaires, LinkLabels, par exemple, pour faciliter l’accomplissement de la tâche en cours.

L’infrastructure Microsoft .NET facilite l’implémentation de boîtes de dialogue personnalisées. En affectant simplement quelques propriétés à votre formulaire de boîte de dialogue personnalisé ou à une seule ligne de code, votre formulaire peut fonctionner comme une boîte de message standard. Dans un événement de clic de bouton, définissez la propriété **DialogResult** de la boîte de dialogue sur **DialogResult. OK** ou **DialogResult. Cancel**. Utilisez la méthode **ShowDialog ( \[ OwnerForm \] )** à partir du formulaire parent. Cette méthode de méthode retourne la valeur **DialogResult** .

Vous pouvez utiliser tous les membres **DialogResult** . Ces mêmes options sont utilisées par la méthode **MessageBox. Show** standard.

Vous pouvez également définir simplement la propriété **AcceptButton** de la boîte de dialogue sur **btnOK** et la propriété **CancelButton** sur **btnCancel**. Les touches **entrée** et **Échap** sont automatiquement mappées aux événements Click respectifs des boutons **btnOK** et **btnCancel** .

Voici quelques conseils pour agrémenter vos boîtes de dialogue personnalisées :

-   Pour les rubriques complexes, fournissez des liens vers l’aide en ligne ou locale avec le contrôle LinkLabel indiquant « en savoir plus » sous l’étiquette de texte appropriée.
-   Au lieu de /  / **supprimer** les boutons Oui, utilisez des textes qui indiquent clairement le résultat d’un clic sur le bouton, par exemple « enregistrer le fichier et quitter », « quitter sans enregistrer » et « ne pas quitter ». Toutefois, dans la mesure du possible, conservez la **valeur standard Oui** / **non**, **OK** / **Annuler** et de tels boutons standard. Une bonne connaissance apporte une grande productivité.
-   Conservez 50 pixels de l’espace de marge sur le côté gauche (ou côté droit en fonction des paramètres de culture cible) et ajoutez une icône représentant le scénario de la boîte de dialogue. S’il s’agit d’une boîte de dialogue d’information, vous pouvez utiliser l’icône « i » utilisée par les boîtes de message standard. s’il s’agit d’une boîte de dialogue de sécurité, vous pouvez utiliser une icône de verrou ou une icône de clé. Visual Studio 2005 est fourni avec des graphiques de grande qualité.
-   Veillez à toujours fournir une navigation au clavier appropriée pour ces boutons : les utilisateurs utilisent les raccourcis clavier pour les boîtes de message (par exemple, O pour OK, Y pour Oui, C pour annuler, etc.). Ils trouveraient sûrement ennuyeux si votre boîte de dialogue personnalisée ne les utilisait pas.

### <a name="include-alternate-commands"></a>Inclure d’autres commandes

Deux facteurs importants dictent la nécessité de méthodes d’entrée alternatives, à savoir frustration et paresse. La frustration est une opération trop fréquente pour les utilisateurs d’ordinateurs. Lorsque vous êtes frustré, vous devez faire en sorte que votre tâche soit effectuée rapidement. Un clic supplémentaire ou une attente supplémentaire de quelques secondes infuriates vraiment une personne en cours de stress : vous savez comment l’utiliser. Paresse vous conseille souvent de terminer la tâche uniquement avec le clavier ou la souris, selon la valeur que vous utilisez pour le moment. Toutefois, à l’exception de ces deux facteurs, l’utilisation de méthodes d’entrée alternatives permet à l’utilisateur d’effectuer facilement des tâches.

Par exemple, si vous avez une zone de liste avec deux boutons (« ajouter » et « supprimer ») de chaque côté, vous devez ajouter un menu contextuel pour cette zone de liste avec des commandes de menu analogues à ces boutons. Cela donne à l’utilisateur la possibilité de choisir la méthode la plus appropriée. Les utilisateurs débutants, en tant qu’État des recommandations de l’expérience utilisateur Windows Vista, utilisent beaucoup de menus contextuels et s’attendent à ce qu’ils soient partout où ils cliquent avec le bouton droit.

De même, nous utilisons des contrôles visuels pour le texte ou l’entrée numérique. Par exemple, les curseurs sont utilisés pour spécifier des entiers et les contrôles Calendar sont utilisés pour l’entrée de date. Parfois, il peut être plus facile d’entrer simplement en tapant. Il peut souvent faire la différence entre l’utilisateur si vous ajoutez un contrôle de Up-Down numérique lié à un curseur ou si vous utilisez un DateTimePicker au lieu du contrôle calendrier.

### <a name="how-to-handle-critical-actions"></a>Comment gérer des actions critiques

Lors de l’exécution d’une fonction critique et irrécupérable, il est généralement conseillé de faire en sorte qu’une boîte de message s’affiche pour confirmer l’action. Prenons un cran. Dans la capture d’écran suivante, vous pouvez voir une boîte de message personnalisée similaire, avec un avantage supplémentaire, un minuteur qui s’affiche visuellement avec l’aide d’une barre de progression.

![capture d’écran d’une boîte de dialogue d’action critique.](images/humanux-08.png)

Il existe quelques variantes spécifiques au scénario que vous pouvez utiliser. Si l’action à entreprendre est très critique (allant de la surcharge d’une centrale nucléaire à la suppression définitive de fichiers), l’action par défaut après l’exécution de la minuterie doit être annuler. La boîte de dialogue ne doit pas disparaître, mais l’étiquette de texte change pour indiquer que l’action a été annulée. L’utilisateur peut choisir de confirmer la commande ou l’annulation.

Assurez-vous toujours que les boutons qui effectuent des opérations critiques sont clairement marqués. Utilisez toujours un texte en clair qui décrit l’action avec précision. Si l’action est la suppression de fichiers, n’écrivez pas « supprimer des fichiers du référentiel ». écrivez « supprimer les fichiers du référentiel ». Lorsque vous utilisez des listes de fichiers, si une commande de menu Supprimer supprime les fichiers sélectionnés du disque dur lui-même (par opposition à la suppression uniquement de la liste des fichiers), vous devez souligner correctement la nature critique de cette opération et insister explicitement sur le fait que l’action supprimera définitivement les fichiers.

Une personne vous a dit : « vous êtes aussi bien que votre pire travail ». La même chose s’applique aux applications logicielles. Une mauvaise expérience avec votre application peut donner une impression négative importante sur l’utilisateur. Pour s’assurer que cela ne se produit pas, vous pouvez faire en sorte que si votre application se bloque, elle s’arrête correctement. Si vous pouvez ajouter une récupération de données ou autoriser l’utilisateur à essayer d’enregistrer une copie de ces données, il peut s’agir d’un grand plus. L’utilisateur doit être averti correctement en cas de blocage de l’application. Une JIT-Debugger ou une boîte de dialogue d’erreur critique n’est pas une bonne chose. Bien qu’il soit important de gérer les incidents au-delà du cadre de cet article, je recommanderai qu’une simple boîte de dialogue qui s’adresse à l’utilisateur et l’informe de la situation (et éventuellement avec un lien vers des informations supplémentaires sur la façon de récupérer de cet incident) serait très utile pour l’utilisateur.

Si vous souhaitez aller plus loin, vous pouvez faire ce que fait l’une de mes applications de conception graphique favorites. En cas de blocage, une boîte de dialogue de récupération s’affiche, qui vous permet d’enregistrer une copie distincte du fichier en cours de traitement, puis vous donne une boîte de dialogue de commentaires dans laquelle vous pouvez entrer des informations sur l’incident (informations personnelles facultatives, bien sûr) et les envoyer aux créateurs.

### <a name="radiobuttons-or-comboboxes"></a>Des cases d’option ou des ComboBoxs ?

À première vue, la méthode permettant de faire une sélection un-à-plusieurs n’est pas si difficile ou importante. Parfois, il peut s’agir de, surtout si le scénario est une application utilisée pour un travail qui respecte le temps.

Jetons un coup d’œil à un exemple concret. Microsoft a récemment publié une version préliminaire d’une application graphique, expression Graphics Designer (anciennement nommée « acrylique »). J’avais environ 20 objets graphiques auxquels j’ai dû assigner une certaine propriété séparément dans cette application. Il s’agissait d’un processus Dreary. Pour ce faire, j’ai dû sélectionner l’objet, cliquer sur le bouton pour activer la fenêtre Paramètres et définir les options. Dans une telle option, deux options devaient être choisies à partir d’une zone de liste déroulante, comme vous pouvez le voir dans la capture d’écran suivante.

![capture d’écran de la boîte de dialogue de texture de franges pour expression Graphics designer.](images/humanux-09.png)

Lorsque vous devez dérouler la liste de liste déroulante et sélectionner le deuxième élément (sur 2 éléments), il peut être vraiment irritant. Ce qui n’est généralement pas le cas, c’est le temps nécessaire pour que la liste déroulante s’affiche. Cela peut perdre beaucoup de temps et peut être frustrant. Cela peut être résolu facilement en plaçant un GroupBox avec deux cases d’option, en particulier lorsque l’espace disponible est trop important. J’ai rencontré des problèmes similaires dans des applications telles que CorelDRAW, Microsoft Access et d’autres.

En plus de perdre du temps en raison de l’animation de la liste déroulante, il gaspille également notre « bande passante mentale ». Avec deux cases d’option « Always visible », notre esprit subliminallyait de savoir à quel point la position du curseur doit être cliquée. Avec la zone de liste modifiable, elle est traitée uniquement après que la liste a été dessinée. Bien qu’il puisse paraître trop peu important, il est en fait très important.

Il est parfois préférable d’utiliser des cases d’option, surtout si vous avez 4 choix ou moins.

### <a name="never-disrupt-the-user"></a>N’interrompez jamais l’utilisateur !

Il s’agit de l’élément le plus destructeur qu’un développeur peut faire pour les utilisateurs. Lorsque votre application, inutilement ou autrement, interrompt l’utilisateur pendant qu’il travaille sur une autre application avec une boîte de message ou un flash de barre des tâches, vous gagnez des points négatifs de l’utilisateur.

Les clignotements de la barre des tâches peuvent être utiles, bien entendu, mais doivent être appelés uniquement lorsque le processus de votre application nécessite une entrée de la part de l’utilisateur pour continuer ou si vous avez des éléments essentiels à communiquer à l’utilisateur. Si l’utilisateur a conservé la barre des tâches sur le masquage automatique, un bouton clignotant de la barre des tâches peut empêcher l’utilisateur d’accéder à la barre d’État ou à d’autres contrôles à ancrage faible, car la barre des tâches serait au-dessus et ne se remasquera pas tant que l’utilisateur n’aura pas cliqué sur le bouton clignotant.

![capture d’écran d’une fenêtre Toast.](images/humanux-10.png)

Les fenêtres « Toast » (voir figure 10), devenues célèbres par des clients de messagerie instantanée tels que MSN Messenger, sont une solution idéale pour informer l’utilisateur d’un événement sans gêner ou perturber son travail. Il existe un excellent article ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) par Bill Wagner sur la création de fenêtres Toast. Il s’agit d’une bonne stratégie (et des mêmes manières) de ne pas perturber les toasts d’une autre application. L’obstruction de ces fenêtres peut être gênante et inproduite. Une solution consiste à utiliser le mutex ToastSemaphore (/library/WinMessenger/winmessenger/overview/toast.asp) fourni par le système d’exploitation pour éviter la collision de Toast.

Parfois, vous devrez peut-être afficher plusieurs éléments par le Toast. Il n’est pas vraiment conseillé d’utiliser au moins 3 toasts. Au lieu de cela, il est préférable de parcourir chacune d’elles en dépilant/déformant un toast. Microsoft Outlook met en œuvre une solution similaire pour notifier l’utilisateur des courriers électroniques entrants.

### <a name="provide-progress-status"></a>Indiquer l’état de progression

Il existe souvent des tâches qui nécessitent l’attente de l’utilisateur. Bien entendu, il s’agit de l’une des choses que l’utilisateur Hates simplement. Mais pire, c’est lorsqu’ils attendent sans savoir ce qui se passe. Parfois, votre application peut avoir besoin de se connecter à un service Web ou à un ordinateur distant, ou peut-être qu’elle traite de gros segments de données, quelle que soit la raison, l’utilisateur doit être informé de ce qui se passe ou, au moins vaguement, de ce qui se passe en coulisses. Il existe différentes méthodes pour ce faire, en fonction de la situation.

Si vous vous connectez à un objet éloigné, tel qu’un service Web, ou un composant placé sur un réseau ou un serveur Internet, il est recommandé d’afficher une boîte de dialogue de progression simple (Voir l’image suivante) ou une barre de progression hébergée dans la barre d’État. Une étiquette d’accompagnement doit décrire l’état actuel du processus. Par exemple, si vous vous connectez à un service Web pour traiter des données, dites simplement «connexion au service Web... "ou" Veuillez patienter, traitement... «Si ce processus est synchrone, il est recommandé de désactiver tous les contrôles auxquels l’utilisateur peut accéder jusqu’à ce que le processus soit terminé, ou d’afficher simplement la progression sous forme de boîte de dialogue modale.

![capture d’écran d’une boîte de dialogue barre de progression.](images/humanux-11.png)

Il est fortement recommandé de définir le style de barre de progression en mode texte défilant si vous utilisez une barre de progression et si le temps de traitement est inconnu, ou si vous n’avez pas de valeur maximale.

Une autre méthode qui devient populaire est une fenêtre « Toast » fixe qui affiche la progression. Le téléchargeur/programme de mise à jour Microsoft AntiSpyware ou les toasts d’analyse de courrier électronique Norton AntiVirus sont de bons exemples. Bien entendu, il ne doit être utilisé que pour les processus asynchrones. Dans le cas contraire, l’utilisateur peut paraître déconcerté. Ces fenêtres sont mieux utilisées pour le traitement en arrière-plan, telles que le téléchargement d’une mise à jour ou l’exécution d’une tâche planifiée, et ne doivent jamais être définies sur « Always on Top ».

### <a name="simplify-complex-steps-with-wizards"></a>Simplifier les étapes complexes avec les assistants

Il est possible de supposer que, si vous êtes confronté à une multitude de contrôles sur un formulaire unique, un utilisateur standard sera confus sans fin. Parfois, aucune quantité de regroupement, de dimensionnement ou d’espacement ne peut vous aider lorsque vous avez de nombreux contrôles importants.

Un Assistant est la meilleure solution pour de tels scénarios. Vous pouvez diviser les contrôles par tâche ou par catégories selon le cas, et les placer dans des étapes distinctes. Cela peut aider l’utilisateur à rester concentré et à ne pas être décourageant par la tâche. Vous pouvez fournir une aide spécifique à l’étape ou à la tâche à l’aide d’un bouton aide. Vous trouverez des instructions de création d’assistant dans MSDN Library.

Les assistants sont également un bon moyen d’aider à configurer la configuration initiale de votre application. De nombreuses applications utilisent ce type d’Assistant pour configurer une configuration personnalisée juste après la fin de l’installation ou lors de la première utilisation. Un tel Assistant initial doit également être rendu facultatif, si possible. si l’utilisateur annule à tout moment, les paramètres non spécifiés sont placés dans les valeurs par défaut. Si vous pouvez transformer l’Assistant en graphique (voir la section [use Pretty Graphics](#use-pretty-graphics) ), cela facilite grandement la tâche de configuration.

### <a name="get-the-tone-of-your-text-right"></a>Tirez le ton de votre texte vers la droite

Dans les [instructions d’interaction avec l’expérience utilisateur Windows](/windows/apps/desktop/), un point très important a été créé à propos de la « tonalité du texte ». Il s’agit de l’impression et du sentiment donnés par le texte dans votre application. Il peut s’agir de n’importe quel caractère d’une info-bulle simple à un contrôle Label d’instruction.

Nous avons abordé précédemment la modification de texte dans l’option webcam de MSN Messenger. Cela s’appelle une tonalité de texte appropriée. Lorsque vous êtes confronté à des utilisateurs non-techniques ou débutants, le fait de faire passer le message sur un aspect différent.

Si vous écrivez « chemin d’accès de destination » au-dessus d’une zone de texte dans une application à extraction automatique, un utilisateur technique peut facilement savoir que vous entrez un nom de type « C : \\ temp \\ myPath ». Un utilisateur novice (pensez à « MOM ») peut tout aussi facilement être chicane et doit faire référence au manuel, appeler le support technique, ou pire, abandonner. Une bonne solution consiste à spécifier ce que doit faire l’utilisateur : « sélectionnez le dossier dans lequel vous souhaitez placer ces fichiers ». Vous pouvez même renommer le bouton «Parcourir... «bouton qui se trouve en regard de cette zone de texte pour «sélectionner un dossier... "

En fournissant une description claire de ce que l’utilisateur doit faire, vous réduisez également le besoin de fichiers d’aide, ou au moins les détails que vous devez inclure dans les fichiers d’aide.

Une très bonne suggestion des [instructions relatives à l’interaction avec l’expérience utilisateur Windows](/windows/apps/desktop/) s’applique à tous les logiciels. Elle indique que le writer doit conserver le texte conversationnel. Les instructions définissent cela comme, « évitez les mots que vous ne voulez pas que quelqu’un d’autre en personne ».

Quelques conseils pour écrire du texte :

-   Évitez de parler de l’utilisateur dans la troisième personne. Dites « vous » au lieu de « l’utilisateur ».
-   Dans la mesure du possible, utilisez judicieusement « mon nom : » ou « mon adresse de messagerie : » au lieu de « nom : » ou « adresse de messagerie ».
-   Lorsque vous attribuez plusieurs options, écrivez le texte du point de vue de l’utilisateur. Par exemple, si vous avez deux cases d’option sous une étiquette, telles que « sélectionner l’autorisation pour le \[ nom d’utilisateur \] sur ce réseau » au-dessus de deux cases d’option, telles que « autoriser » et « refuser », remplacez le texte de RadioButton par « je souhaite autoriser le \[ nom d’utilisateur \] » et « je veux interdire le \[ nom d’utilisateur » \] .
-   Souligner le texte uniquement s’il est utilisé pour les liens. L’utilisateur est confondu si le texte souligné n’est pas un lien.
-   Attirez l’attention sur les informations importantes avec une étiquette en gras, mais utilisez-les avec précaution. Trop de texte en gras est confus et l’impact global du formulaire est réduit.
-   Lors de l’écriture du texte d’une case à cocher, assurez-vous qu’il est facile de savoir ce qui se produit lorsqu’il est sélectionné et le moment où il est désélectionné, ou effacé. L’option recommandée consiste à écrire le texte directement lorsque la case à cocher est sélectionnée. Par exemple, écrivez « m’envoyer des informations utiles de vos partenaires » au lieu de « ne pas m’envoyer d’informations utiles de vos partenaires ». Bien que je puisse imaginer de nombreuses personnes de marketing en cours d’appellation de cet exemple particulier, je suis sûr que vous savez ce que je veux dire.
-   Si vous avez un contrôle de type bouton (généralement un RadioButton avec une apparence de bouton de commande) qui contrôle activé/désactivé, assurez-vous que vous l’étiquetez correctement. Si le processus est activé, écrivez « activé » au lieu de « activer », ou « désactivé ». Si vous écrivez, il affiche l’état actuel. Si l’utilisateur clique sur le bouton (activé) et que le bouton indique « activer », il peut être déroutant et problématique. « Activer » peut inviter l’utilisateur à cliquer dessus pour penser que le processus n’est pas actif.

### <a name="sometimes-a-listview-is-better"></a>Parfois, un ListView est plus performant

Nous utilisons souvent un contrôle DataGrid ou ListBox ou même ComboBox pour les tâches de sélection, mais avec Windows XP et les versions ultérieures de Windows, l’utilisation d’un ListView peut vous offrir des options plus grandes.

Points précis du contrôle ListView :

-   Accélère la reconnaissance des éléments avec des icônes et des bitmaps.
-   Affiche des informations supplémentaires avec les affichages des détails ou des vignettes.
-   Avec Visual Studio 2005, vous pouvez même avoir des groupes pour une catégorisation supplémentaire. Les groupes s’étendent sur toutes les vues et sont flexibles. Les groupes peuvent également être utilisés pour aplatir une vue de hiérarchie (comme un TreeView) où il existe plus de nœuds enfants que de nœuds parents. Un bon exemple est la boîte de dialogue Connexions réseau dans Windows XP, affichée avec « afficher dans les groupes » et la vue définie sur détails.
-   Pour personnaliser un contrôle ListView, peignez-le manuellement en définissant la propriété **OwnerDraw** et en utilisant les événements **DrawItem** et **DrawSubItem** .
-   Prend en charge la modification rapide sur place des éléments ListView.
-   Prend facilement en charge la réorganisation manuelle.
-   Permet aux utilisateurs de sélectionner l’affichage (grandes icônes, petites icônes, liste, etc.) qu’ils ont le plus à l’aise.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Simplifier la navigation avec les contrôles de navigation et les encadrés

La « sous-navigation » est la clé de l’interface utilisateur complexe. Parfois, vous ne pouvez pas échapper à une interface utilisateur complexe. La meilleure chose à faire dans une telle situation est de rendre l’expérience aussi simple que possible pour l’utilisateur. Un encadré constitué d’étiquettes de lien ou d’un TreeView pour la navigation basée sur la hiérarchie suggère une navigation au niveau frère pour la tâche de la boîte de dialogue active. Il permet à l’utilisateur de passer facilement d’une étape à l’autre tout en sachant où il se trouve.

Si vous utilisez une navigation basée sur la hiérarchie avec des arborescences ou une navigation complexe similaire, un bon utilitaire pour l’utilisateur est un contrôle de navigation. Alors que Visual Studio n’est pas encore fourni avec un contrôle intégré, consultez Création d' [un contrôle de navigation](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) pour plus d’informations sur la création d’un contrôle de navigation. Un contrôle de navigation permet de trouver facilement l’emplacement actuel par rapport à la hiérarchie.

La navigation hiérarchique peut être facilement fusionnée dans l’en-tête si le formulaire en a un. Consultez la section précédente sur les [en-têtes](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Utiliser des graphiques assez esthétiques

Tout le monde aime les applications avec des graphiques sympas, la majorité le fait, au moins. Bien qu’une interface utilisateur avec Pretty Graphics ne soit pas un choix logique pour toutes les applications, elle vous aide à faire une bonne impression et peut être un plaisir de travailler dans. Bien entendu, les graphiques ne doivent pas nuire à la productivité, mais s’ils sont utilisés correctement, ils peuvent augmenter !

Il n’est pas nécessaire qu’il y ait de nombreux graphiques, pas plus qu’ils ne nécessitent beaucoup de travail. Un écran de démarrage professionnel ou un en-tête (comme celui dont nous avons parlé plus tôt) fait l’astuce. Si votre budget l’autorise, vous pouvez utiliser des graphiques conçus pour les barres d’outils, les assistants et bien plus encore. Elles rendent votre application plus conviviale et plus professionnelle. Il s’agit d’un effet subtil, mais un look professionnel véhicule la confiance et la stabilité. Si vous êtes une entreprise relativement petite qui crée des applications de vente au détail, il s’agit d’un aspect clé à prendre en compte.

Faites toujours un point pour utiliser des graphiques conçus de façon professionnelle. Les graphiques sans royalties sont facilement disponibles et abordables. Vous pouvez également embaucher un concepteur. Mais si les graphiques ne sont pas votre forte, ne l’essayez pas vous-même. Si vous ne pouvez pas acquérir ou utiliser des graphiques conçus de manière professionnelle, il est préférable de ne pas les utiliser du tout.

Pour les petits graphiques, vous pouvez toujours utiliser les icônes et les bitmaps fournis avec Visual Studio 2005. (Les graphiques livrés avec les versions précédentes ne sont pas recommandés.)

### <a name="provide-resizable-forms-when-possible"></a>Fournir des formulaires redimensionnables lorsque cela est possible

Les fenêtres redimensionnables sont comparables à des fenêtres indépendantes de la résolution. Les fenêtres indépendantes de la résolution ont le même aspect que vous utilisiez des écrans 96DPI ou 300DPI. Que l’interface utilisateur de votre application soit ou non indépendante de la résolution, elle est plus performante si elle est redimensionnable. Bien entendu, cela ne s’applique pas à de nombreux scénarios, mais est une bonne règle à usage général.

Si votre fenêtre traite des listes de n’importe quel type de tri, en particulier les ListViews, cela devient encore plus important. Le redimensionnement permet à l’utilisateur d’examiner plus de données en même temps.

Par exemple, nous avons une application dans laquelle l’utilisateur doit sélectionner une image à partir d’une grande collection. La boîte de dialogue Ouvrir vous permet de sélectionner une vue miniature, mais la boîte de dialogue a une taille fixe et la liste miniature affiche uniquement 4 miniatures à la fois. Si la collection comporte une centaine d’images, le défilement et la recherche (une tâche répétitive) peuvent être assez pénible et une baisse de l’efficacité. Si la boîte de dialogue est redimensionnable, l’utilisateur peut faire en sorte qu’elle soit à l’aise ou au moins aussi grande que l’écran le permet, et pouvoir terminer rapidement la tâche. Si votre liste a un défilement horizontal (comme un ListView ou DataGrid détaillé), il est encore plus pénible ! Les fenêtres redimensionnables sont très utiles dans une telle situation.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Fournir davantage de fonctionnalités avec les encadrés/volets de tâches

Comme les en-têtes que nous avons parlés précédemment, les encadrés et les volets de tâches sont un excellent moyen de fournir des fonctionnalités supplémentaires et des commandes utilitaires. Par exemple, les volets des tâches dans Office Word 2003 sont très pratiques, accessibles et non intrusives. Ils fonctionnent également de façon asynchrone lors de la connexion à des ressources en ligne, ce qui permet à l’utilisateur de choisir plusieurs tâches.

La création d’un volet de tâches ou d’un encadré est aussi simple que la création d’un panneau d’ancrage, avec la possibilité de placer un graphique rapide sur le haut pour agir en tant que barre de titre. Vous pouvez même utiliser un contrôle étiquette coloré pour cela. Les opportunités pour les volets de tâches sont nombreuses !

Si vous disposez de fonctionnalités supplémentaires et que vous souhaitez les fournir de manière non intrusive à votre utilisateur, il n’y a pas d’emplacement similaire au volet des tâches. Vous pouvez également créer des volets des tâches « Masquer automatiquement » ou réduire comme les fenêtres Outil Visual Studio.

### <a name="give-a-notification-choice"></a>Fournir un choix de notification

Nous avons précédemment vu comment créer une boîte de message personnalisée. Si une boîte de message de votre application est souvent affichée à l’utilisateur, il peut être prudent d’ajouter une case à cocher que l’utilisateur peut sélectionner pour désactiver cette boîte de dialogue à l’avenir. Une telle option est particulièrement intéressante pour les messages plus évidents.

Voici un exemple familier : la boîte de dialogue de recherche de Visual Studio. Lorsque vous recherchez ou remplacez du texte, Visual Studio affiche une boîte de message indiquant les résultats. Toutefois, vous avez également la possibilité de désactiver cette boîte de message. Il peut être très ennuyeux si vous devez appuyer sur entrée ou cliquez sur OK chaque fois que vous recherchez.

Visual Studio est également une autre chose intéressante : même si la boîte de dialogue est désactivée, elle affiche toujours les résultats de cette opération dans la barre d’État.

### <a name="provide-tooltips"></a>Fournir des info-bulles !

Parfois, les info-bulles peuvent vous faire gagner beaucoup de temps. Les boutons, les cases à cocher et d’autres contrôles peuvent être ambigus et l’utilisateur peut ne pas être sûr de ce qu’il doit faire. Les info-bulles fournissent la meilleure forme d’aide contextuelle en une seule ligne. L’utilisateur peut choisir rapidement ce qu’il faut faire sans Rechercher quoi que ce soit dans le fichier d’aide ou ouvrir une autre fenêtre.

Les gens les ignorent souvent dans leurs applications. Faites un point pour ajouter des info-bulles à tous les contrôles ambigus, ou à tous les contrôles, si possible. Ne répétez pas le texte d’une étiquette d’accompagnement ou le texte de ce contrôle, mais fournissez des informations supplémentaires sur ce contrôle. Le texte doit expliquer la fonction du contrôle en quelques mots.

### <a name="do-not-forget-the-little-things"></a>N’oubliez pas les petits éléments

Les petits éléments peuvent vous importuner, mais leur ignorance peut avoir un impact sur l’impression que vous apportez. J’ai utilisé une application créée par une personne importante dans le secteur des logiciels dont la BorderStyle du formulaire a été définie sur dimensionnable, mais les contrôles sur le côté droit du formulaire n’étaient pas ancrés. C’est la raison pour laquelle l’application créée par une haute densité de l’industrie a un sens non professionnel.

Ces types de « petits éléments » sont le cœur de l’impression globale. L’interface utilisateur et l’expérience utilisateur de votre application sont celles sur lesquelles les utilisateurs apprécieront votre application, au moins au début. S’ils voient des bogues évidents dans votre interface utilisateur, ils peuvent percevoir votre application comme étant moins puissante et efficace.

## <a name="conclusion"></a>Conclusion

Nous avons seulement touché une petite partie de l’expérience utilisateur humaine. À mesure que l’expérience utilisateur devient plus simple, efficace, amusante et plus conviviale, la tâche de création de cette expérience utilisateur devient beaucoup plus complexe. Mais avec une bonne planification et une bonne planification, vous pouvez créer une expérience utilisateur exceptionnelle.

La meilleure façon de créer l’expérience utilisateur parfaite consiste à effectuer des tests d’utilisation ciblés, en particulier au niveau de l’interface utilisateur, que ce soit avec un groupe de test spécial ou par vous-même. Plus vous consacrez du temps à tester l’expérience utilisateur avant de publier votre application, mieux c’est. Cela vous permettra d’éviter de nombreux problèmes plus tard.

 

 