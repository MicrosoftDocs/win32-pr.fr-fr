---
title: Accessibilité (notions de base de la conception)
description: La conception de logiciels pour l’accessibilité permet de s’assurer que les programmes et les fonctionnalités sont facilement disponibles pour le plus grand nombre d’utilisateurs, y compris ceux qui présentent des handicaps et des handicaps.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c38eb3993880d820a4e65fa25a1e910e9e842de823779aaf3ef24dab8635e60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212442"
---
# <a name="accessibility-design-basics"></a>Accessibilité (notions de base de la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La conception de logiciels pour l’accessibilité permet de s’assurer que les programmes et les fonctionnalités sont facilement disponibles pour le plus grand nombre d’utilisateurs, y compris ceux qui présentent des handicaps et des handicaps.

Le nombre d’utilisateurs que les fonctionnalités d’accessibilité peuvent vous étonner peut vous surprendre. par exemple, dans le États-Unis, les enquêtes ont montré que plus de la moitié de tous les utilisateurs de l’ordinateur connaissent des difficultés ou des handicaps liés à l’accessibilité, et sont susceptibles de tirer parti de l’utilisation de la technologie accessible. De plus, l’approche de la conception de logiciels avec la flexibilité et l’inclusif qui sont la spécificités de l’accessibilité entraîne souvent une plus grande facilité d’utilisation et la satisfaction des clients.

![capture d’écran de la boîte de dialogue’Ease of Access Center' ](images/inter-accessibility-image1.png)

La facilité d’accès, accessible à partir du panneau de configuration, fournit un emplacement central où les utilisateurs peuvent choisir et personnaliser les fonctionnalités d’accessibilité de leur choix.

**Remarque :** Les instructions relatives au [clavier](inter-keyboard.md), à [la souris](inter-mouse.md), à la [couleur](vis-color.md)et au [son](vis-sound.md) sont présentées dans des articles distincts.

## <a name="design-concepts"></a>Principes de conception

De nombreux facteurs physiques, de perception et cognitifs entrent en vigueur lorsque les utilisateurs interagissent avec le matériel et les logiciels de l’ordinateur. Avant de prendre en compte les moyens de rendre les fonctionnalités de votre programme plus accessibles, il est utile d’en savoir plus sur les types de handicaps et les handicaps, ainsi que sur les technologies d’assistance pour lesquelles ces utilisateurs peuvent travailler lorsqu’ils interagissent avec les ordinateurs.

### <a name="types-of-impairments"></a>Types de handicaps

Le tableau suivant décrit les handicaps utilisateur et les déficiences courantes, et répertorie quelques-unes des solutions les plus importantes utilisées pour rendre les ordinateurs plus accessibles.



| Handicap    | Description   | Solutions  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments visuels<br/>             | S’étend de modéré (ce qui affecte 17% des utilisateurs) à grave (ce qui affecte 9% des utilisateurs).<br/>                                                                                                   | Agrandissement, couleurs et contraste personnalisables ; Utilitaires en braille ; lecteurs d’écran.<br/>                                                                                       |
| Ouïe<br/>            | S’étend de modéré (ce qui affecte 18% des utilisateurs) à grave (ce qui affecte 2% des utilisateurs).<br/>                                                                                                   | Redondance des informations : le son utilisé uniquement comme complément à la communication de texte ou visuelle.<br/>                                                                                     |
| Acuité<br/>          | S’étend de modéré (ce qui affecte 19% des utilisateurs) à grave (ce qui affecte 5% des utilisateurs). Cet handicap implique souvent des difficultés à effectuer certaines compétences motrices avec le clavier ou la souris.<br/> | Redondance de méthode d’entrée : fonctionnalités de programme accessibles par des équivalents de souris ou de clavier.<br/>                                                                                       |
| Cognitif<br/>          | Comprend les écarts de mémoire et les différences de perception. Affecte 16% des utilisateurs.<br/>                                                                                                         | Interface utilisateur (IU) hautement personnalisable ; utilisation de la [Divulgation progressive](ctrl-progressive-disclosure-controls.md) pour masquer la complexité ; utilisation d’icônes et d’autres aides visuelles.<br/> |
| Cessation<br/>            | Offre une sensibilité visuelle au mouvement et au clignotement.<br/>                                                                                                                                        | Approche conservatrice de la modulation des interfaces, telles que l’utilisation des animations ; éviter le scintillement de l’écran dans la plage comprise entre 2 Hertz (Hz) et 55 Hz.<br/>                        |
| Discours ou langage<br/> | Comprend des problèmes de dyslexie et de communication orale.<br/>                                                                                                                                       | Outils de vérification orthographique et grammaticale ; la reconnaissance vocale et la technologie de conversion de texte par synthèse vocale.<br/>                                                                                 |



 

Pour plus d’informations sur la façon d’aider les utilisateurs avec ces handicaps, consultez la section [traitant des handicaps particuliers](#addressing-particular-impairments) plus loin dans cet article.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Types de technologies d’assistance et fonctionnalités d’accessibilité

**Lecteurs d’écran**

Un lecteur d’écran permet aux utilisateurs ayant des handicaps visuels ou des handicaps de naviguer dans une interface utilisateur en transformant les éléments visuels en données audio. Ainsi, le texte de l’interface utilisateur, les contrôles, les menus, les barres d’outils, les graphiques et les autres éléments de l’écran sont prononcés par la voix informatisée du lecteur d’écran. Pour créer un programme optimisé pour la technologie d’assistance de lecteur d’écran, vous devez planifier la manière dont le lecteur d’écran identifie chaque élément d’interface utilisateur.

Chaque élément d’interface utilisateur avec lequel l’utilisateur peut interagir doit être accessible via le clavier, et être exposé via une interface de programmation d’applications (API) d’accessibilité. nous vous recommandons d’utiliser UI Automation, la nouvelle infrastructure d’accessibilité pour toutes les versions de Microsoft Windows qui prennent en charge Windows Presentation Foundation (WPF). UI Automation fournit un accès par programme à la plupart des éléments sur le bureau, permettant ainsi aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir des informations sur l’interface utilisateur aux utilisateurs et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard (par exemple, en parlant plutôt que ou en plus de la manipulation de la souris ou du clavier). Pour plus d’informations, consultez [vue d’ensemble d’UI Automation](/dotnet/framework/ui-automation/ui-automation-overview).

Sachez que bien que les lecteurs d’écran constituent une technologie d’assistance très importante, il en existe d’autres également. Pour plus d’informations sur la gamme de technologies disponibles, consultez [types de produits de technologie d’assistance](https://www.microsoft.com/enable/at/types.aspx).

**Reconnaissance vocale**

la reconnaissance vocale est une fonctionnalité d’accessibilité de Windows qui permet aux utilisateurs d’interagir avec leurs ordinateurs par voix, réduisant ainsi le besoin d’interaction du moteur avec la souris ou le clavier. Les utilisateurs peuvent dicter des documents et des messages électroniques, utiliser des commandes vocales pour démarrer et basculer entre les programmes, contrôler le système d’exploitation et même remplir des formulaires sur le Web.

**Loupe**

L’agrandissement aide les utilisateurs avec une acuité visuelle réduite en agrandissant les éléments à l’écran partout de 2 à 16 fois l’original. Les utilisateurs peuvent définir cette fonctionnalité pour effectuer le suivi de la souris (pour voir une version agrandie de l’emplacement de la souris), du clavier (pour voir la zone où le pointeur se déplace lorsque vous faites une tabulation) ou de l’édition de texte (pour voir ce qu’ils tapent).

**Paramètres visuels et modèles de couleurs**

En plus de rendre les éléments à l’écran plus volumineux, les utilisateurs ayant un handicap peut tirer parti des paramètres système, tels que le [mode de contraste élevé](glossary.md) ou la possibilité de personnaliser les jeux de couleurs d’arrière-plan et de premier plan.

**Narrateur**

le narrateur est un lecteur d’écran réduit en Windows qui permet aux utilisateurs d’entendre le texte à l’écran et les éléments d’interface utilisateur lus à voix haute, y compris certains événements (y compris les messages d’erreur) qui se produisent spontanément. L’utilisateur peut entendre les menus du narrateur sans quitter la fenêtre active.

![capture d’écran de la boîte de dialogue « Microsoft Narrator » ](images/inter-accessibility-image2.png)

Les utilisateurs peuvent personnaliser l’étendue de l’utilisation du narrateur Microsoft.

**Clavier visuel**

Pour les utilisateurs qui ont des difficultés avec les claviers physiques et qui doivent utiliser un autre périphérique d’entrée, tel qu’un commutateur, les claviers à l’écran sont une nécessité. Les utilisateurs peuvent sélectionner des clés à l’aide de la souris ou d’un autre dispositif de pointage, d’un petit groupe de clés ou d’une seule clé, en fonction de la façon dont vous configurez le clavier visuel.

**Touches souris**

Lorsque les touches souris sont activées, les utilisateurs qui préfèrent le clavier peuvent utiliser les touches de direction du pavé numérique pour déplacer le pointeur de la souris.

pour obtenir la liste complète des fonctionnalités d’accessibilité, consultez [accessibilité dans Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) sur le site Web de Microsoft.

### <a name="keyboard-based-navigation"></a>Navigation à l’aide du clavier

La touche Tab, les touches de direction, la barre d’espace et la touche entrée sont importantes pour la navigation à l’aide du clavier. En appuyant sur les cycles [d'](glossary.md) onglets, vous parcourez les différents groupes de contrôles et les touches de direction se déplacent dans un contrôle ou parmi les contrôles d’un groupe. Le fait d’appuyer sur la barre d’espace équivaut à cliquer sur le contrôle avec le focus d’entrée, tandis que l’appui sur entrée revient à cliquer sur le bouton de commande par défaut ou sur le lien de commande, quel que soit le focus d’entrée.

![capture d’écran de la boîte de dialogue « Vider la corbeille » ](images/inter-accessibility-image3.png)

Dans cet exemple, les utilisateurs peuvent appuyer sur la touche Tab jusqu’à ce que l’option souhaitée ait le focus d’entrée, puis appuyer sur entrée pour ouvrir l’objet.

### <a name="access-keys"></a>Clés d'accès

Les clés d’accès permettent aux utilisateurs de choisir des options et d’exécuter des commandes directement sans avoir à naviguer d’abord vers le contrôle. Les touches d’accès sont indiquées par un soulignement de l’un des caractères de l’étiquette de chaque contrôle. Les utilisateurs activent ensuite l’option ou la commande en appuyant sur la touche Alt et sur le caractère souligné. Les clés d’accès ne respectent pas la casse.

![capture d’écran du menu fichier et des touches d’accès ](images/inter-accessibility-image4.png)

Dans cet exemple, en appuyant sur Alt + O, vous activez la commande ouvrir.

Le choix de clés d’accès logique pour les contrôles ne pose généralement aucune difficulté. plus il y a de contrôles dans une fenêtre, plus la possibilité de choix de clé d’accès est importante. Dans ce cas, affectez des clés d’accès aux groupes de contrôle plutôt qu’à chacun d’eux.

![capture d’écran des groupes de contrôle et des clés d’accès ](images/inter-accessibility-image5.png)

Dans cet exemple, les clés d’accès sont affectées à des groupes de contrôle, plutôt qu’à des contrôles individuels.

Les touches d’accès rapide sont souvent confondues avec les touches de raccourci, mais les touches de raccourci sont affectées différemment des clés d’accès et ont des objectifs différents. Par exemple, les touches de raccourci utilisent des séquences de touches Ctrl et fonction. elles sont principalement destinées à un raccourci pour les utilisateurs expérimentés et non pour l’accessibilité.

Pour plus d’informations, consultez [clavier](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Conception pour l’accessibilité : trois pratiques fondamentales

Les programmes accessibles aident tous les utilisateurs d’une certaine manière, car les objectifs d’accessibilité et d’utilisation se chevauchent. Par exemple, les fonctionnalités conçues pour offrir aux utilisateurs avancés aussi efficaces que possible bénéficient également des utilisateurs qui préfèrent utiliser le clavier en raison de l’altération de Dexterity.

Trois pratiques fondamentales vous aideront à créer une conception accessible : prévoyez un degré de flexibilité dans votre interface utilisateur, prenez en compte les besoins et les préférences des utilisateurs jouent un rôle majeur dans les décisions de conception et fournissez un accès par programmation à votre interface utilisateur.

**Fournir une interface utilisateur flexible**

La conception accessible est, au moins en partie, de donner des choix aux utilisateurs. Il ne s’agit pas d’un ensemble de choix vertigineux, mais d’un nombre limité de choix qui anticipe les besoins des utilisateurs. «Vous n’aimez pas naviguer à travers la souris ? Ici, vous pouvez effectuer les mêmes opérations en utilisant uniquement le clavier. Vous n’aimez pas les claviers physiques ? Voici un exemple virtuel que vous pouvez utiliser à l’écran.»

Par exemple, assurez-vous que :

-   Fournir des équivalents sélectionnables par l’utilisateur pour les éléments non textuels (par exemple, texte de remplacement pour les graphiques et légendes pour l’audio).

    ![capture d’écran du bouton de connexion](images/inter-accessibility-image6.png)

    ![capture d’écran du texte de remplacement pour le bouton de connexion](images/inter-accessibility-image7.png)

    Les utilisateurs qui ont choisi de ne pas restituer les graphiques doivent voir le texte alt à la place, en décrivant ce que fait le contrôle et comment interagir avec lui.

-   Fournir des alternatives à la couleur (par exemple, différenciation des icônes ou utilisation des sons).

    ![capture d’écran des icônes en nuances de gris (nuances de gris) ](images/inter-accessibility-image8.png)

    Dans cet exemple, les icônes standard sont facilement distinguées en fonction de leurs conceptions.

-   Vérification de l’accès au clavier (par exemple, un taquet de tabulation pour chaque contrôle interactif) afin que les utilisateurs puissent accomplir les mêmes opérations dans votre programme avec la souris ou le clavier.
-   S’assurer que votre programme offre de bonnes options de contraste des couleurs pour les utilisateurs. Windows fournit une option à contraste élevé, mais elle est vraiment conçue pour être une solution pour un sérieux handicap. D’autres options de contraste servent mieux aux utilisateurs présentant un handicap léger, tels que la vision faible et le daltonisme.
-   S’assurer que les utilisateurs ont un moyen d’ajuster la taille du texte dans l’interface utilisateur de votre programme (par exemple, à l’aide d’un contrôle Slider ou d’une zone de liste déroulante pour la taille de police). Si possible, prenez en charge le mode haute résolution en points par pouce (dpi).
-   S’assurer que votre programme est multimodal, ce qui signifie que si le mode principal du programme est inaccessible pour certains, ces utilisateurs ont la possibilité de contourner le problème. Par exemple, lorsque l’animation est affichée, les informations doivent être affichables dans au moins un mode de présentation non animé à l’option de l’utilisateur.

Les interfaces multimodales et la navigation flexible offrent essentiellement à l’utilisateur l’architecture de la redondance des informations. La redondance a parfois des connotations négatives ; dans le texte de l’interface utilisateur, par exemple, nous vous recommandons de supprimer la redondance pour simplifier l’expérience de lecture. Mais dans le contexte de l’accessibilité, la redondance correspond à des mécanismes et des expériences de prévention de défaillance.

**Respect de vos utilisateurs**

En règle générale, le principe du guidage est essentiel pour la conception de programmes accessibles. Même en tant qu’exercice intellectuel, imaginez ce qu’il doit être de votre choix pour rencontrer votre programme en tant qu’utilisateur qui est désactivé. Prenez le temps de tester les écrans de l’interface utilisateur en mode de contraste élevé et à différentes résolutions, pour vous assurer que l’expérience est idéale pour les utilisateurs ayant des troubles de la vision. Pour tester l’accessibilité du clavier, activez la case à cocher **souligner les raccourcis clavier et les touches d’accès** dans l’élément facilité du panneau de configuration du centre d’accès (afin que les clés d’accès soient toujours visibles). Vous pouvez même aller au-delà des tests rigoureux en recruter des développeurs et des concepteurs qui ont une aptitude naturelle à la empathizing avec d’autres utilisateurs.

Vous devez également démontrer ce qui suit :

-   À l’aide de paramètres au niveau du système (par exemple, la couleur système) plutôt que de paramètres hardwiring pour votre programme particulier. Respectez non seulement les paramètres que les utilisateurs ont spécifiquement sélectionnés pour interagir avec leurs programmes, mais également les fonctionnalités d’accessibilité intégrées au système d’exploitation que l’utilisateur souhaite en effet quel que soit le programme qu’il utilise. pour plus d’informations, consultez [à propos des fonctionnalités d’accessibilité Windows](/previous-versions//ms695605(v=vs.85)).
-   préférer les contrôles communs aux contrôles personnalisés, car les contrôles communs ont déjà implémenté les api d’accessibilité Windows.
-   Documentation de toutes les options et fonctionnalités d’accessibilité (par exemple, tous les raccourcis clavier). Les utilisateurs ayant des handicaps sont très motivés par la découverte des fonctionnalités d’accessibilité et attendent souvent des informations complètes d’être collectées dans l’aide.
-   Création de la documentation accessible dans les formats accessibles. Ainsi, la documentation elle-même doit respecter les mêmes règles d’accessibilité que l’interface utilisateur principale, y compris la possibilité d’agrandir la taille de police, l’utilisation de texte de remplacement pour les graphiques et l’architecture d’informations redondante (par exemple, en utilisant le codage de couleurs uniquement comme supplément à du texte).

Dans les produits logiciels, le respect des utilisateurs peut se manifester dans la convivialité et la recherche sur le marché, dans les services de support et la documentation de efficacious, et bien évidemment pour les décisions de conception. Par exemple, en pensant à nouveau en termes de conception pour les utilisateurs expérimentés : vous mettez-vous à la nouvelle fonctionnalité de pointe dans parce que vous le souhaitez, ou parce que vous savez que vos utilisateurs avancés vous en demandent ? Ce dernier cas indique que votre processus de prise de décision de conception est bien informé par la valeur de respect.

**Fourniture de l’accès par programme**

Fournir un accès par programme à l’interface utilisateur est essentiel afin que les technologies d’assistance (telles que les lecteurs d’écran, les autres périphériques d’entrée et les programmes de reconnaissance vocale) interprètent l’écran correctement pour leurs utilisateurs. En créant un « mappage » de chaque écran d’interface utilisateur dans votre programme, vous le rendez à la disposition des utilisateurs de technologies d’assistance.

Procédez ainsi :

-   Activation de l’accès par programmation à tous les éléments et au texte de l’interface utilisateur (par exemple, à l’aide de l’interface COM Active Accessibility, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Placement des noms (ou titres) et des descriptions sur les objets, les cadres et les pages de l’interface utilisateur (par exemple, à l’aide de la propriété de nom [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ).
-   S’assurer que les événements de programmation sont déclenchés par toutes les activités de l’interface utilisateur (par exemple, les événements de focus pour toutes les activités d’interface utilisateur impliquant le déplacement du focus).

**Si vous ne faites que quatre choses...**

1.  Vérifiez que chaque utilisateur peut exploiter tout le potentiel de votre programme.
2.  Imaginez l’accessibilité comme une occasion de résoudre des problèmes créatifs et un autre moyen d’améliorer la satisfaction globale de l’utilisateur.
3.  Respectez les paramètres système.
4.  Utilisez des contrôles communs chaque fois que cela est possible.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **N’interrompez pas ou ne désactivez pas les fonctionnalités activées du système d’exploitation ou d’autres produits identifiés comme fonctionnalités d’accessibilité.** Vous pouvez identifier ces fonctionnalités en vous référant à la documentation du système d’exploitation ou du produit en question.
-   **Ne forcez pas les utilisateurs à interagir avec votre programme comme fenêtre supérieure à l’écran.** Si une fonction ou une fenêtre est requise continuellement pour permettre aux utilisateurs d’effectuer une tâche, cette fenêtre doit toujours rester visible, si l’utilisateur les choisit, quelle que soit sa position par rapport à d’autres fenêtres. Par exemple, si l’utilisateur dispose d’un clavier visuel mobile qui se trouve au-dessus de toutes les autres fenêtres afin qu’il soit visible à tout moment, votre programme ne doit jamais le masquer en position obligatoire en haut de l' [ordre de plan](glossary.md).
-   **Utilisez les couleurs système, les polices et les contrôles communs dans la mesure du possible.** En procédant ainsi, vous réduisez considérablement le nombre de problèmes d’accessibilité rencontrés par les utilisateurs.

### <a name="addressing-particular-impairments"></a>Résoudre des problèmes particuliers

**Éléments visuels**

-   **Ne vous fiez jamais à la couleur seule pour transmettre la signification.** Utilisez la couleur uniquement pour renforcer la signification fournie par le texte, la conception, l’emplacement ou le son.

    ![capture d’écran de l’icône et de l’info-bulle du Communicator rouge ](images/inter-accessibility-image9.png)

    Dans cet exemple, la méthode principale de communication est le texte d’info-bulle concis. L’utilisation de Color facilite la communication de la signification, mais elle est secondaire.

-   **Utilisez un info-bulles de texte alternatif pour décrire les graphiques.**
-   **N’utilisez pas de texte dans les graphiques.** Les utilisateurs avec des troubles de la vision peuvent avoir des graphiques désactivés (par exemple, dans un navigateur Web), ou ils ne peuvent tout simplement pas voir ou Rechercher le texte placé dans les graphiques.
-   **Vérifiez que les boîtes de dialogue et les fenêtres ont des noms explicites,** afin qu’un utilisateur qui entende, au lieu d’afficher l’écran (par exemple, à l’aide d’un lecteur d’écran), obtient des informations contextuelles appropriées.
-   **respectez les paramètres de l’utilisateur pour l’affichage visuel** en obtenant systématiquement des polices, des tailles et des couleurs de police, Windows des tailles d’éléments d’affichage et des paramètres de configuration du système à partir des api theme et GetSystemMetrics.
-   **Laissez le texte info-bulle concis** afin qu’il soit plus facile à lire et minimise l’interruption des lecteurs d’écran.

    ![capture d’écran de l’info-bulle indiquant les limites du code PIN ](images/inter-accessibility-image10.png)

    Bien que les bulles puissent utiliser du texte de corps supplémentaire si nécessaire, cet exemple montre que le texte du titre peut parfois atteindre le même objectif d’une manière plus économique et plus accessible.

**Ouïe**

-   **Ne vous fiez jamais à un son seul pour transmettre la signification.** Utilisez le son uniquement pour renforcer la signification fournie par le texte, la conception, l’emplacement ou la couleur.
-   **Permet aux utilisateurs de contrôler le volume de sortie audio.** utilisez la Mixer de Volume Windows à cet effet. Pour plus d’informations, consultez [son](vis-sound.md).
-   **Ciblez le son de votre programme pour qu’il se produise dans une plage comprise entre 500 Hz et 3000 Hz** , ou soyez facilement réglable par l’utilisateur dans cette plage. Les sons de cette plage sont susceptibles d’être détectables par des personnes ayant un handicap auditif.

**Acuité**

-   **Définissez les valeurs de délai d’attente de l’interface utilisateur par rapport à GetDoubleClickTime () au lieu d’utiliser des heures absolues.** Cela permet d’ajuster les délais d’attente à la vitesse de l’utilisateur.
-   **Affectez des clés d’accès à tous les éléments de menu** afin que les utilisateurs qui préfèrent travailler avec le clavier aient la même possibilité de naviguer dans votre programme que les utilisateurs qui travaillent avec la souris.
-   **N’effectuez pas de double-clic et en faisant glisser le seul moyen d’effectuer une action.** Il peut s’agir de mouvements difficiles pour certains utilisateurs.
-   **Ne supprimez pas les barres de menus de votre programme.** Les barres de menus sont plus faciles que les barres d’outils auxquelles les utilisateurs du clavier peuvent accéder. Si vous ne souhaitez pas que la barre de menus soit visible par défaut, masquez-la à la place.
-   **Rendez l’aide accessible à partir du clavier en fournissant des taquets de tabulation pour les boutons d’aide et les liens.**
-   **Pour améliorer la sensibilisation des affectations de touches d’accès dans votre programme, vous pouvez les afficher à tout moment.** Dans le panneau de configuration, accédez à la facilité d’accès, puis cliquez sur **rendre le clavier plus facile à utiliser**. Activez ensuite la case à cocher **souligner les raccourcis clavier et les touches d’accès** .

**Cognitif**

-   **Utilisez la divulgation progressive** pour masquer la complexité.

    ![capture d’écran des boutons fractionnés avec des triangles inversés ](images/inter-accessibility-image11.png)

    Dans ces exemples, les options disponibles à partir du bouton de commande sont masquées par défaut, et les utilisateurs peuvent choisir d’afficher les options en tirant parti des contrôles de divulgation progressive.

-   **Utilisez des icônes, des barres d’outils et d’autres aides visuelles** pour réduire la charge cognitive de lecture du texte.
-   Dans la mesure du possible, **fournissez une fonctionnalité de saisie semi-automatique dans les zones de texte et les listes déroulantes modifiables**, afin que les utilisateurs n’aient pas à taper le nom complet des commandes, des noms de fichiers ou des choix similaires à partir d’un ensemble limité d’options. Cela réduit la charge cognitive pour tous les utilisateurs et réduit le nombre de frappes pour les utilisateurs pour lesquels l’orthographe ou le typage est difficile, lent ou pénible.
-   **Montrez les concepts difficiles de l’aide en incluant des didacticiels et des animations.** Notez que les animations peuvent être difficiles pour les utilisateurs ayant des problèmes de saisie et ne doivent donc être utilisées que lorsque cela est nécessaire.

**Cessation**

-   **N’utilisez pas de texte clignotant ou clignotant, d’objets ou d’autres éléments dont la fréquence clignote ou clignote entre 2-55 Hz.**
-   **Limitez l’utilisation des animations.** Certains utilisateurs sont particulièrement sensibles au mouvement de l’écran, en particulier dans la périphérie de leur champ visuel. Si vous utilisez l’animation pour attirer l’attention sur un événement, assurez-vous que l’attention est déconseillée et qu’elle est digne d’interrompre l’utilisateur.

**Discours ou langage**

-   **Organisez et écrivez du texte clair, concis et facile à comprendre.** Les tests d’utilisation montrent que le dépliage des informations de clé à la fin d’une expression améliore la compréhension. Pour plus d’instructions, consultez [style et Tone](text-style-tone.md).

**Incorrect :**

Le chiffre suivant est-il trois ?

Cliquez sur OK pour commencer.

**Correct :**

Le chiffre suivant est-il trois ?

Pour commencer, cliquez sur OK.

### <a name="access-keys"></a>Clés d'accès

-   **Préférer les caractères dont la largeur est large,** par exemple w, m et les majuscules.
-   **Préférez une consonne distinctive ou une voyelle,** telle que « x » dans « Exit ».
-   **Évitez d’utiliser des caractères qui rendent le soulignement difficile à voir,** par exemple (de la plupart des problèmes aux moins problématiques) :
    -   Caractères d’une largeur de 1 pixel, tels que i et l.
    -   Caractères avec descendants, tels que g, j, p, q et y.
    -   Caractères en regard d’une lettre avec un descendant.

### <a name="menu-access-keys"></a>Touches d’accès au menu

-   **Affectez des clés d’accès à tous les éléments de menu.** Aucune exception.
-   **Pour les éléments de menu dynamiques (tels que les fichiers récemment utilisés), assignez des touches d’accès numérique.**

    ![capture d’écran du menu Ouvrir avec les fichiers récemment utilisés ](images/inter-accessibility-image12.png)

    dans cet exemple, le programme Paint dans Windows affecte des clés d’accès numériques aux fichiers récemment utilisés.

-   **Assigner des clés d’accès uniques au sein d’un niveau de menu.** Vous pouvez réutiliser des clés d’accès dans différents niveaux de menu.
-   **Rendez les clés d’accès faciles à trouver :**
    -   Pour les éléments de menu les plus fréquemment utilisés, choisissez caractères au début du premier ou du deuxième mot de l’étiquette, de préférence le premier caractère.
    -   Pour les éléments de menu moins fréquemment utilisés, choisissez des lettres qui sont une consonne distinctive ou une voyelle dans l’étiquette.

### <a name="dialog-box-access-keys"></a>Clés d’accès aux boîtes de dialogue

-   **Dans la mesure du possible, assignez des clés d’accès uniques à tous les contrôles interactifs ou à leurs étiquettes.** Les [zones de texte en lecture seule](ctrl-text-boxes.md) sont des contrôles interactifs (dans la mesure où les utilisateurs peuvent les faire défiler et copier du texte). ils bénéficient donc des clés d’accès. **N’affectez pas de clés d’accès à :**
    -   **Boutons OK, annuler et fermer.** Enter et ESC sont utilisés pour leurs clés d’accès. Toutefois, attribuez toujours une clé d’accès à un contrôle qui signifie OK ou annuler, mais qui a une étiquette différente.

        ![capture d’écran des contrôles avec clés d’accès affectées ](images/inter-accessibility-image13.png)

        Dans cet exemple, une clé d’accès est assignée au bouton de validation positif.

-   **Étiquettes de groupe.** Normalement, les contrôles individuels d’un groupe sont affectés à des clés d’accès, de sorte que l’étiquette du groupe n’a pas besoin d’une. Toutefois, attribuez une clé d’accès à l’étiquette de groupe et non aux contrôles individuels en cas de pénurie de clés d’accès.
-   Les **boutons d’aide génériques,** accessibles via la touche F1.
-   **Étiquettes de lien.** Il y a souvent trop de liens pour affecter des clés d’accès uniques et les traits de soulignement de lien masquent les traits de soulignement des touches d’accès. Les utilisateurs accèdent aux liens avec la touche Tab à la place.
-   **Noms d’onglets.** Les onglets sont recycles à l’aide des touches CTRL + TAB et Ctrl + Maj + Tab.
-   **Boutons de navigation étiquetés « ... ».** Il n’est pas possible d’affecter des clés d’accès de manière unique.
-   **Contrôles sans étiquette,** tels que les contrôles spin, les boutons de commande graphique et les contrôles de divulgation progressive sans étiquette.
-   **Texte ou étiquettes statiques sans étiquette pour les contrôles qui ne sont pas interactifs,** tels que les barres de progression.
-   **Affectez d’abord les clés d’accès du bouton de validation pour vous assurer qu’elles ont les attributions de clés standard.** S’il n’existe pas d’affectation de clé standard, utilisez la première lettre du premier mot. Par exemple, les boutons clé d’accès pour Oui et pas de validation doivent toujours être « Y » et « N », quels que soient les autres contrôles de la boîte de dialogue.
-   **Pour les boutons de validation négatifs (autres que annuler) formulées en tant que « ne pas », attribuez la clé d’accès au « n » dans « ne pas ».** S’il n’est pas formulées, utilisez l’attribution de clé d’accès standard ou affectez la première lettre du premier mot. En procédant ainsi, tous ne sont pas et n’ont pas de clé d’accès cohérente.
-   **Pour faciliter la recherche des clés d’accès, assignez les touches d’accès rapide à un caractère qui apparaît au début de l’étiquette,** idéalement le premier caractère, même s’il existe un mot clé qui apparaît plus tard dans l’étiquette.

Pour obtenir des instructions et des exemples supplémentaires, consultez [clavier](inter-keyboard.md).

## <a name="text"></a>Texte

-   **Utilisez des signes deux-points à la fin des étiquettes de contrôle externes.** Certaines technologies d’assistance recherchent les signes deux-points pour identifier les étiquettes de contrôle.
-   **Positionner des étiquettes de manière cohérente par rapport aux éléments qu’ils enlibellent.** Cela permet aux technologies d’assistance d’associer correctement les étiquettes aux contrôles correspondants et aide les utilisateurs des agrandisseurs d’écran à savoir où rechercher une étiquette ou un contrôle.

    ![capture d’écran des étiquettes placées de manière cohérente ](images/inter-accessibility-image14.png)

    Dans cet exemple, les étiquettes de chacune des listes déroulantes sont placées de manière cohérente et utilisent le signe deux-points.

-   **Limitez le texte de remplacement à 150 caractères au maximum.** Décrivez l’action permettant d’activer le contrôle (par exemple, cliquez sur, cliquez avec le bouton droit, et ainsi de suite), puis décrivez la fonction du contrôle.

    **Acceptable:**

    Bouton.

    Collines bleues.

    **Conseillé**

    Cliquez pour vous connecter à votre compte.

    Photo des collines distantes qui montrent comment les couleurs apparaissent en fondu sur la distance.

-   **N’utilisez pas de texte pour dessiner des lignes, des zones ou d’autres symboles graphiques.** Les caractères utilisés de cette manière peuvent dérouter les utilisateurs des lecteurs d’écran. Par exemple, une zone dessinée avec la lettre « X » autour d’une zone de texte est lue par le logiciel du lecteur d’écran en tant que « X x x x x » sur la première ligne, suivi de « X » et du contenu et de « X ».

## <a name="documentation"></a>Documentation

-   Documentez toutes les options et fonctionnalités d’accessibilité (par exemple, tous les raccourcis clavier).
-   Créer une documentation accessible dans des formats accessibles. Ainsi, la documentation elle-même doit respecter les mêmes règles d’accessibilité que l’interface utilisateur principale.
-   Reportez-vous aux clés d’accès, et non aux touches de raccourci (qui ont une signification et une utilisation différentes), à des touches mnémoniques ou à des accélérateurs.
-   En général, reportez-vous à une personne dont le type de handicap n’est pas une personne désactivée. Considérez la personne en premier, pas l’étiquette.



| Utilisez ces termes           | À la place de                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| A une dextérité limitée, a des handicaps de mouvement<br/>     | Handicap, inapproprié<br/>                                                        |
| Sans handicap<br/>                               | Normal, en capacité nulle, sain<br/>                                          |
| Une seule mains, les personnes qui tapent avec une main<br/>          | Une seule droitier <br/>                                                        |
| Personnes handicapées<br/>                           | Les personnes désactivées, les personnes handicapées, les personnes handicapées, le handicap<br/> |
| Handicaps cognitifs, handicaps de développement<br/> |                                                                                  |



 

