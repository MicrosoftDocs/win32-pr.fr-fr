---
title: Couleur
description: La couleur est un élément visuel important de la plupart des interfaces utilisateur.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ade1c87606aa14831220e501a5f39f5d2ce2d1ebb4016ad04822634b7735c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936753"
---
# <a name="color"></a>Couleur

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La couleur est un élément visuel important de la plupart des interfaces utilisateur. Au-delà de l’esthétique pure, la couleur a des significations associées et entraîne des réponses émotionnelles. Pour éviter toute confusion en ce sens, la couleur doit être utilisée de manière cohérente. Pour obtenir les réponses émotionnels souhaitées, la couleur doit être utilisée de manière appropriée.

La couleur est souvent considérée comme un espace de couleurs, où RVB (rouge, vert, bleu), TSL (teinte, saturation, luminosité) et HSV (teinte, saturation, valeur) sont les espaces de couleurs les plus couramment utilisés.

![figure d’un cube présentant les relations de couleur ](images/vis-color-image1.png)

L’espace colorimétrique RVB peut être visualisé sous la forme d’un cube.

Alors que la technologie d’affichage utilise des valeurs RVB et, par conséquent, les développeurs considèrent souvent les couleurs en termes de RVB, l’espace de couleurs RVB ne correspond pas à la façon dont les gens perçoivent la couleur. Par exemple, si vous ajoutez du rouge au cyan foncé, le résultat n’est pas perçu comme plus rouge, mais comme plus clair.

![illustration des carrés cyan foncé et clair ](images/vis-color-image2.png)

Dans cet exemple, l’ajout de rouge au cyan foncé rend plus clair, et non plus rouge. L’espace de couleurs RVB ne correspond pas à la façon dont les utilisateurs perçoivent la couleur.

Les espaces colorimétriques TSL/HSV sont constitués de trois composants : teinte, saturation, luminosité ou valeur. Ces espaces colorimétriques sont souvent utilisés à la place de RGB, car ils correspondent mieux à la façon dont les utilisateurs perçoivent la couleur.

L’espace colorimétrique TSL forme un double cône qui est blanc en haut, noir en bas et neutre au milieu :

-   **Teinte :** Couleur de base de la roue de couleur, comprise entre 0 et 360 degrés, où 0 et 360 degrés sont rouges.

    ![figure d’un cercle présentant les relations de couleur ](images/vis-color-image3.png)

    La roue de couleur, où rouge correspond à 0 degré, jaune correspond à 60 degrés, vert à 120 degrés, cyan à 180 degrés, bleu à 240 degrés, et magenta à 300 degrés.

-   **Saturation :** La valeur de la couleur (par rapport à la valeur « terne ») est, entre 0 et 100, où 100 est entièrement saturé et 0 est gris.
-   **Luminosité :** Le niveau de luminosité de la couleur, allant de 0 à 100, où 100 est le plus clair possible (blanc, quelle que soit la teinte et la saturation) et 0 le plus foncé possible (noir).

    ![Figure illustrant l’espace colorimétrique TSL ](images/vis-color-image4.png)

    L’espace colorimétrique TSL peut être visualisé sous la forme d’un double cône.

L’espace colorimétrique HSV est similaire, à ceci près que son espace forme un cône unique :

-   **Teinte :** Couleur de base de la roue de couleur, comprise entre 0 et 360 degrés, où 0 et 360 degrés sont rouges.
-   **Saturation :** La valeur de la couleur (par rapport à la valeur « terne ») est, entre 0 et 100, où 100 est entièrement saturé et 0 est gris.
-   **Valeur :** La luminosité de la couleur, allant de 0 à 100, où 100 est le plus lumineux possible (c’est-à-dire la demi-luminosité dans l’espace TSL) et 0 est le plus foncé possible (noir).

    ![Figure illustrant l’espace colorimétrique HSV ](images/vis-color-image5.png)

    L’espace colorimétrique HSV peut être visualisé sous la forme d’un cône unique.

Dans les espaces TSL et HSV, si la saturation est égale à 0, la luminosité spécifie une nuance de gris. dans Windows, les espaces tsl et HSV sont généralement remappés à une échelle comprise entre 0 et 240 afin que les couleurs puissent être représentées par une valeur de 32 bits.

**Remarque :** Les instructions relatives aux [polices](vis-fonts.md) et à l' [accessibilité](inter-accessibility.md) sont présentées dans des articles distincts.

## <a name="design-concepts"></a>Principes de conception

L’utilisation efficace de Color peut rendre l’interface utilisateur de votre programme plus efficace. La couleur peut aider les utilisateurs à comprendre certaines significations d’un coup d’œil. La couleur peut également améliorer l’esthétique et l’affinage de votre produit.

Malheureusement, il est très facile d’utiliser la couleur de manière inefficace, surtout si vous n’êtes pas formé dans la conception visuelle. Une mauvaise utilisation des couleurs entraîne des conceptions qui semblent inprofessionnels, datées, confuses ou simples. Une mauvaise utilisation de la couleur peut être moins grave que la non-utilisation de la couleur.

Cette section explique ce que vous devez savoir pour utiliser efficacement la couleur.

### <a name="how-color-is-used"></a>Mode d’utilisation de la couleur

La couleur est généralement utilisée dans l’interface utilisateur pour communiquer :

-   **C.-à-d.** La signification d’un message peut être résumée par couleur. Par exemple, la couleur est souvent utilisée pour communiquer l’État lorsque le rouge est un problème ou une erreur, que le jaune est prudent ou averti et que le vert est correct.
-   **Département.** L’état d’un objet peut être indiqué par la couleur. par exemple, Windows utilise la couleur pour indiquer les états de sélection et de survol. Les liens dans les pages Web utilisent Blue pour les points de vue invisités et violet pour les visiteurs.
-   **Différenti.** Les utilisateurs partent du principe qu’il existe une relation entre les éléments de la même couleur, de sorte que le codage en couleurs est un moyen efficace de faire la différence entre les objets. Par exemple, dans un élément du panneau de configuration, les volets des tâches utilisent un arrière-plan vert pour les séparer visuellement du contenu principal. en outre, Microsoft Outlook permet aux utilisateurs d’attribuer différents indicateurs de couleur aux messages.
-   **Privilégié.** La couleur peut être utilisée pour attirer l’attention des utilisateurs. par exemple, Windows utilise [des instructions principales](text-ui.md) bleues pour les aider à sortir de l’autre texte.

Bien entendu, la couleur est souvent utilisée dans les graphiques pour des raisons purement esthétiques. Bien que les esthétiques soient importantes, vous devez choisir les couleurs des éléments de l’interface utilisateur principalement en fonction de ce qu’ils signifient, et non de leur aspect.

### <a name="color-interpretation"></a>Interprétation des couleurs

**L’interprétation des couleurs des utilisateurs dépend souvent de la culture.** Par exemple, dans le États-Unis, le mariage attire pour la mariée est en grande partie associé au blanc de couleur, tandis que le noir est associé à des funéraires. Toutefois, il y a longtemps, dans le Japon, le symbole de couleur était l’opposé : le blanc était la couleur dominante à travers les funéraires, et le noir a été considéré comme une couleur qui apporte une bonne chance pour les mariages.

Cela dit, **l’interprétation du rouge, du jaune et du vert pour l’État est cohérente dans le monde entier.** Cela est dû à la [Convention d’UNESCO Vienne sur les signes et les signaux routiers](https://www.unece.org/trans/conventn/signalse.pdf), qui définit la convention mondiale pour les feux de circulation (où rouge signifie arrêter, vert signifie continuer et jaune signifie procéder à la prudence). Vous pouvez utiliser ces couleurs d’État sans vous préoccuper des interprétations dépendantes de la culture.

au-delà des couleurs d’état, Windows affecte des significations aux couleurs en fonction de la convention, comme indiqué dans la section instructions de cet article. Assurez-vous que l’utilisation des couleurs de votre programme est compatible avec ces conventions de couleur.

### <a name="color-accessibility"></a>Accessibilité des couleurs

L’utilisation de la couleur affecte l’accessibilité de votre logiciel au public le plus vaste possible. Les utilisateurs disposant d’un aveugle ou d’une vision faible peuvent ne pas être en mesure de voir les couleurs correctement, voire pas du tout. Environ 8% des hommes adultes ont une certaine forme de confusion des couleurs (souvent appelée « cécité des couleurs »), dont la confusion des couleurs rouge-vert est la plus courante.

![Figure présentant les couleurs primaires normalement affichées ](images/vis-color-image6.png)

Les couleurs principales, telles qu’elles apparaissent avec une vision des couleurs normale.

![Figure présentant les mêmes couleurs que celles affichées avec protanopia ](images/vis-color-image7.png)

Les couleurs principales, telles qu’elles apparaissent avec Protanopia (1% de population masculine).

![Figure présentant les mêmes couleurs que celles détectées avec Deuteranopia ](images/vis-color-image8.png)

Les couleurs principales, telles qu’elles apparaissent avec Deuteranopia (6% de la population masculine).

![Figure présentant les mêmes couleurs que celles affichées avec tritanopia ](images/vis-color-image9.png)

Les couleurs principales, telles qu’elles apparaissent avec Tritanopia (1% de population masculine).

Pour plus d’informations, consultez [Color-Blind les utilisateurs peuvent voir votre site ?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Utiliser la couleur pour renforcer visuellement

La meilleure solution pour les problèmes d’interprétation et d’accessibilité des couleurs consiste à utiliser des couleurs pour renforcer visuellement la signification de l’une de ces principales méthodes de communication :

-   **Text.** Le texte concis correspond généralement à la communication principale la plus efficace, soit directement sur l’interface utilisateur, soit via une info-bulle.

![capture d’écran de l’icône rouge de petite taille avec info-bulle ](images/vis-color-image10.png)

Dans cet exemple, le texte info-bulle est utilisé pour communiquer la signification d’une icône.

-   **Nomination.** Les icônes sont facilement distinguées par les conceptions, en particulier leur forme plan.

![capture d’écran des icônes en nuances de gris (nuances de gris) ](images/vis-color-image11.png)

Dans cet exemple, les icônes standard sont facilement distinguées en fonction de leurs conceptions.

-   **Emplacement.** L’emplacement relatif peut également être utilisé, mais cette approche est plus faible que les alternatives. Pour être efficace, l’emplacement doit être standard et bien connu, comme avec les feux de circulation.

Alors que la couleur est l’attribut le plus évident de nombreuses conceptions, elle doit toujours être redondante.

### <a name="designing-with-color"></a>Conception avec couleur

Ironiquement, la meilleure façon de concevoir des couleurs consiste à commencer par concevoir sans couleur, à l’aide de [des maquettes](glossary.md) ou monochrome, puis à ajouter de la couleur ultérieurement. Cela permet de s’assurer que les informations ne sont pas communiquées à l’aide de la seule couleur. Cela permet également de s’assurer que vos impressions s’affichent parfaitement sur les imprimantes monochrome.

### <a name="use-theme-or-system-colors"></a>Utiliser le thème ou les couleurs système

bien qu’il existe de nombreux facteurs complexes dans l’utilisation efficace de la couleur, dans Windows interface utilisateur choisir la couleur fait souvent bouillir pour choisir simplement la couleur de [thème](glossary.md) ou la [couleur système](glossary.md) appropriée en fonction de quelques règles simples. Les utilisateurs peuvent ensuite sélectionner et personnaliser ces modèles de couleurs en fonction de leur choix.

En procédant ainsi, vous pouvez non seulement prendre en charge les préférences de couleur de tous vos utilisateurs, mais vous éliminez le choix du jeu de couleurs parfait qui fonctionne pour tous les goûts, styles et cultures (ce qui, bien sûr, n’est pas impossible).

**Si vous n’avez qu’une seule chose...**

Choisissez couleurs en sélectionnant la couleur de thème ou la couleur système appropriée. N’utilisez jamais la couleur comme méthode principale de communication, mais comme méthode secondaire pour renforcer visuellement la signification. Créez à l’aide de des maquettes ou de monochrome pour vous assurer que la couleur est secondaire.

### <a name="use-theme-or-system-colors-correctly"></a>Utiliser correctement les couleurs du thème ou du système

Supposons que les utilisateurs choisissent des couleurs de thème ou de système en fonction de leurs besoins personnels et que les couleurs du thème ou du système soient construites de manière appropriée. Sur la base de cette hypothèse, si vous choisissez toujours des couleurs de thème ou de système en fonction de leur rôle prévu et des préversions de paire avec les arrière-plans associés, il est garanti que les couleurs sont lisibles et respectent les souhaits des utilisateurs dans tous les modes vidéo, y compris le [mode de contraste élevé](glossary.md). Par exemple, il est garanti que la couleur système de texte de la fenêtre est lisible par rapport à la couleur système d’arrière-plan de la fenêtre.

Plus précisément, toujours :

-   **Choisissez des couleurs en fonction de leur objectif.** Ne choisissez pas de couleurs en fonction de leur apparence actuelle, car l’apparence peut être modifiée par l’utilisateur ou les versions ultérieures de Windows.
-   **Faire correspondre les couleurs de premier plan avec les couleurs d’arrière-plan associées.** Il est garanti que les couleurs de premier plan sont lisibles uniquement par rapport aux couleurs d’arrière-plan qui leur sont associées. N’associez pas les couleurs de premier plan à d’autres couleurs d’arrière-plan, ou pire encore, à d’autres couleurs de premier plan.
-   **Ne mélangez pas les types de couleurs.** Autrement dit, les couleurs de thème sont toujours identiques avec les couleurs de thème associées, les couleurs système avec les couleurs système associées et les couleurs câblées avec d’autres couleurs câblées. Par exemple, il n’est pas garanti que la couleur du texte d’un thème soit lisible sur un arrière-plan câblé.
-   **Si vous devez vous conformer à des broches, gérez le mode de contraste élevé comme un cas spécial.**

**Si vous n’avez qu’une seule chose...**

Choisissez toujours le thème ou les couleurs système en fonction de leur rôle prévu, et associez les premier plan aux arrière-plans associés.

### <a name="using-other-colors"></a>Utilisation d’autres couleurs

tandis que le thème Windows définit un ensemble complet de parties de thèmes, vous constaterez peut-être que votre programme a besoin de couleurs qui ne sont pas définies dans le fichier de thème. Bien que vous puissiez universer ces couleurs, une meilleure approche consiste à dériver les couleurs du thème ou des couleurs système. À l’aide de cette approche, vous bénéficiez de tous les avantages de l’utilisation des couleurs de thème et système, mais avec une plus grande flexibilité.

Par exemple, supposons que vous ayez besoin d’un arrière-plan de fenêtre plus sombre que la couleur d’arrière-plan de la fenêtre de thème. Dans l’espace de couleurs TSL, une couleur plus sombre correspond à une couleur avec une luminosité inférieure. Par conséquent, vous pouvez dériver une couleur d’arrière-plan de fenêtre plus sombre en procédant comme suit :

-   Obtenez la couleur du thème d’arrière-plan de la fenêtre RVB.
-   Convertit le RVB en sa valeur TSL.
-   Réduisez la valeur de la luminosité (par exemple, 20 pour cent).
-   Revenez aux valeurs RVB.

À l’aide de cette approche, il est garanti que la couleur dérivée est perçue comme une nuance plus sombre de la couleur d’origine (à moins que la couleur d’origine était très sombre pour commencer.)

![Illustration montrant les effets d’une luminosité réduite ](images/vis-color-image12.png)

Dans cet exemple, une couleur d’arrière-plan de fenêtre plus sombre est dérivée de la couleur de thème.

### <a name="testing-colors"></a>Test des couleurs

Pour déterminer si l’utilisation de la couleur de votre programme est accessible et n’est pas utilisée comme méthode principale de communication, nous vous recommandons d’utiliser les utilitaires [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) ou [Vischeck](https://www.vischeck.com/) pour vérifier les éléments suivants :

-   Dépendance globale sur la couleur à l’aide du filtre de mise à l’échelle gris.
-   Problèmes spécifiques de confusion des couleurs à l’aide des filtres Protanopia, Deuteranopia et Tritanopia.

Pour déterminer si l’utilisation de la couleur de votre programme est programmée correctement, testez votre programme dans les modes suivants :

-   thèmes activés à l’aide du thème Windows par défaut.
-   Thèmes activés à l’aide d’un thème autre que celui par défaut.
-   thèmes désactivés (« Windows style classique » dans le thème Paramètres dans l’élément du panneau de configuration de personnalisation).
-   Contraste élevé noir (texte blanc sur un arrière-plan noir).
-   Contraste élevé blanc (texte noir sur un arrière-plan blanc).

Tous les éléments de l’écran doivent être lisibles et s’afficher comme prévu, même juste après les modifications du mode.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **N’utilisez jamais la couleur comme méthode principale de communication,** mais comme méthode secondaire pour renforcer visuellement la signification.

### <a name="using-theme-and-system-colors"></a>Utilisation des couleurs de thème et système

-   **Dans la mesure du possible, choisissez couleurs en sélectionnant la couleur de thème ou la couleur système appropriée.** En procédant ainsi, vous pouvez toujours respecter les préférences en matière de couleurs des utilisateurs.
-   **Choisissez des couleurs de thème et système en fonction de leur rôle.** Ne choisissez pas de couleurs en fonction de leur apparence actuelle, car l’apparence peut être modifiée par l’utilisateur ou les versions ultérieures de Windows.
-   **Faire correspondre les couleurs de premier plan avec les couleurs d’arrière-plan associées.** Il est garanti que les couleurs de premier plan sont lisibles uniquement par rapport aux couleurs d’arrière-plan qui leur sont associées. N’associez pas les couleurs de premier plan à d’autres couleurs d’arrière-plan, ou pire encore, à d’autres couleurs de premier plan.
-   **Ne mélangez pas les types de couleurs.** Autrement dit, les couleurs de thème sont toujours identiques avec les couleurs de thème associées, les couleurs système avec les couleurs système associées et les couleurs câblées avec d’autres couleurs câblées. Par exemple, il n’est pas garanti que la couleur du texte d’un thème soit lisible sur un arrière-plan câblé.
-   **Si vous devez utiliser une couleur qui n’est pas un thème ou une couleur système :**
    -   **Préférez dériver la couleur à partir d’un thème ou d’une couleur système sur hardwiring sa valeur.** Utilisez le processus décrit plus haut dans cet article, dans à l’aide d’autres couleurs.
    -   **Gérez le mode de contraste élevé comme un cas spécial.**
-   **Gérer les modifications de thème.** Les modifications de thème sont gérées automatiquement par Windows avec des frames de fenêtre standard et des contrôles communs. Windows avec des frames de fenêtre personnalisés, des contrôles personnalisés ou owner-draw, et d’autres utilisation de la couleur doivent gérer les modifications de thème explicitement.
    -   **Développeurs :** Vous pouvez répondre aux événements de changement de thème en gérant le \_ message WM THEMECHANGED.

### <a name="color-meaning"></a>Signification de la couleur

-   Si vous devez utiliser des couleurs de thème et système (ou des couleurs dérivées) chaque fois que vous le pouvez, assurez-vous que toute autre utilisation de la couleur est compatible avec l’utilisation de couleur dans Windows.



| Teinte | Signification | Utiliser dans Windows  |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bleu/vert<br/>                | Windows de la personnalisation<br/>                                                      | arrière-plan : personnalisation de la Windows.<br/>                                                                                                                        |
| verre, noir, gris, blanc<br/> | neutre<br/>                                                            | arrière-plan : frames de fenêtre standard, menu Démarrer, barre des tâches, encadré.<br/> Foreground : texte normal.<br/>                                                |
| blue<br/>                      | Démarrer, valider<br/>                                                      | Background : boutons de commande par défaut, Rechercher, ouvrir une session.<br/> Icônes : informations, aide.<br/> Premier plan : instructions principales, liens.<br/>           |
| rouge<br/>                       | erreur, arrêt, vulnérable, critique, attention immédiate, limité<br/> | Background : Status, Stopped Progress (barres de progression).<br/> Icônes : erreur, arrêter, fermer la fenêtre, supprimer, entrée requise, manquant, non disponible.<br/>     |
| yellow<br/>                    | avertissement, attention, douteux<br/>                                     | Background : Status, progressed Progress (barres de progression).<br/> Icônes : AVERTISSEMENT<br/>                                                                       |
| green<br/>                     | aller, continuer, progression, sécurisé<br/>                                        | Background : Status, normal Progress (barres de progression).<br/> Icônes : aller, terminer, actualiser.<br/> Foreground : chemins d’accès et URL (dans les résultats de la recherche).<br/> |
| purple<br/>                    | fréquent<br/>                                                            | premier plan : liens visités (pour les liens dans Windows Internet Explorer et les documents).<br/>                                                                |



 

-   **Pour éviter de communiquer avec les significations précédentes, choisissez les couleurs avec une saturation moyenne à basse et une luminosité élevée ou faible.** Les utilisateurs associent les significations précédentes aux couleurs qui ont une saturation complète ou élevée et une luminosité de niveau intermédiaire, afin que vous puissiez éviter ces associations en choisissant des nuances différentes.

![Figure illustrant la façon dont la luminosité affecte la couleur ](images/vis-color-image13.png)

Dans cet exemple, il y a trois nuances de couleur jaune, mais seule la nuance très saturée de luminosité au niveau intermédiaire communique l’avertissement. L’icône de dossier jaune ne ressemble pas à un avertissement.

### <a name="using-color-with-data"></a>Utilisation de la couleur avec des données

-   Lorsque **cela est utile, affectez des couleurs aux données pour aider les utilisateurs à les différencier.** Notez que les utilisateurs supposent que les données avec des couleurs similaires ont des significations similaires.
-   **Assignez des couleurs par défaut qui sont faciles à distinguer.** En règle générale, les couleurs sont faciles à distinguer si elles sont éloignées les unes des autres dans les espaces de couleurs TSL/HSV, tout en conservant un contraste élevé avec leur arrière-plan :
    -   Lorsque vous choisissez des couleurs, préférez les harmonies de la triple ou les teintes complémentaires, mais pas les teintes contiguës.

        ![Figure illustrant comment choisir des couleurs contrastées ](images/vis-color-image14.png)

        Dans cet exemple, si la première affectation de couleur est rouge, la couleur suivante doit être bleue, verte ou cyan, mais pas magenta, violet, orange ou jaune.

    -   Les couleurs présentent un contraste élevé s’il y a une grande différence de teinte, de saturation ou de luminosité.

        ![Figure présentant une couleur sur différents arrière-plans ](images/vis-color-image15.png)

        Dans cet exemple, la couleur de base du bleu clair est contrastée avec les arrière-plans avec de grandes différences de teinte, de saturation ou de luminosité.

    -   L’utilisation d’un arrière-plan blanc ou très clair rend le contraste des couleurs de premier plan plus facile à distinguer.

        ![Figure illustrant un contraste correct et médiocre ](images/vis-color-image16.png)

        Dans cet exemple, les couleurs d’arrière-plan White et clair rendent la couleur de premier plan plus facile à distinguer.

-   **Autorisez les utilisateurs à personnaliser ces affectations de couleurs** , car le choix de couleurs est subjectif et une préférence personnelle. S’il existe de nombreuses couleurs coordonnées, autorisez les utilisateurs à les modifier en tant que groupe à l’aide de jeux de couleurs.
-   **Autorisez les utilisateurs à étiqueter ces affectations de couleurs.** Cela permet de faciliter l’identification et la recherche.
-   **Contrairement aux couleurs de l’interface utilisateur, les données ne doivent pas changer lorsque les couleurs système changent.**

## <a name="documentation"></a>Documentation

-   **Reportez-vous aux éléments d’interface utilisateur par leurs noms, et non par leurs couleurs.** De telles références ne sont pas accessibles et les couleurs système peuvent changer. Si le nom d’un élément d’interface utilisateur n’est pas connu ou n’est pas assez descriptif, affichez une capture d’écran à clarifier.

**Correct :**

![capture d’écran du message contenant la barre d’informations ](images/vis-color-image17.png)

**Incorrect :**

![capture d’écran du message contenant’or bar' ](images/vis-color-image18.png)

dans l’exemple incorrect, le message fait référence au Windows barre d’informations d’Internet Explorer par sa couleur plutôt que par son nom.

