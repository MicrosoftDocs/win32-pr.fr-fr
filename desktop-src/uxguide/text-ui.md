---
title: Texte de l’interface utilisateur
description: En savoir plus sur le texte de l’interface utilisateur qui apparaît sur les surfaces de l’interface utilisateur.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a0ab5025407d5149d1747fbd083fed7df345e3f3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444740"
---
# <a name="user-interface-text"></a>Texte de l’interface utilisateur

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Le texte de l’interface utilisateur apparaît sur les surfaces de l’interface utilisateur. Ce texte comprend des étiquettes de contrôle et du texte statique :

-   Les étiquettes de contrôle identifient les contrôles et sont placées directement sur ou en regard des contrôles.
-   Le texte statique, qui est appelé parce qu’il ne fait pas partie d’un contrôle interactif, fournit aux utilisateurs des instructions ou des explications détaillées pour qu’ils puissent prendre des décisions éclairées.

**Remarque :** Les instructions relatives au [style et au ton](text-style-tone.md), aux [polices](vis-fonts.md)et aux étiquettes de [contrôle communs](controls.md) sont présentées dans des articles distincts.

## <a name="usage-patterns"></a>Modèles d’usage

Le texte de l’interface utilisateur a plusieurs modèles d’utilisation :



|   Usage                                                                                                                                                                                          |    Description                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre de titre Texte**<br/> Utilisez le texte de la barre de titre pour identifier une fenêtre ou la source d’une boîte de dialogue. <br/>                                                                            | ![capture d’écran de la barre de titre options des dossiers](images/text-ui-image1.png)<br/> Dans cet exemple, le texte de la barre de titre identifie une fenêtre.<br/>                                                                                                                                                                                                                                                                                                             |
| **Instructions principales**<br/> Utilisez l’instruction principale bien visible pour expliquer de façon concise ce que vous devez faire dans la fenêtre ou la page. <br/>                                                      | L’instruction doit être une instruction spécifique, une direction impérative ou une question. les bonnes instructions principales communiquent l’objectif de l’utilisateur au lieu de se concentrer uniquement sur la manipulation de l’interface utilisateur. <br/> ![capture d’écran de la question : voulez-vous obtenir l’aide la plus récente ? ](images/text-ui-image2.png)<br/> Dans cet exemple, le texte d’instruction principal implique directement à l’utilisateur une question en termes d’avantage ou d’intérêt de l’utilisateur.<br/>             |
| **Instructions supplémentaires**<br/> Si nécessaire, utilisez une instruction supplémentaire pour présenter des informations supplémentaires utiles pour comprendre ou utiliser la fenêtre ou la page. <br/> | Vous pouvez fournir des informations plus détaillées, fournir un contexte et définir la terminologie. les instructions supplémentaires sont élaborées sur l’instruction principale sans simplement le reformulation. <br/> ![capture d’écran du texte lors du basculement vers le compte d’administrateur ](images/text-ui-image3.png)<br/> Dans cet exemple, les instructions supplémentaires fournissent deux cours d’action possibles à prendre en réponse aux informations présentées dans l’instruction principale.<br/> |
| **Étiquettes de contrôle**<br/> étiquettes directement sur ou en regard de contrôles. <br/>                                                                                                           | ![capture d’écran des options d’horloge du Bureau ](images/text-ui-image4.png)<br/> Dans cet exemple, les étiquettes de contrôle identifient les paramètres d’horloge du Bureau que les utilisateurs peuvent sélectionner ou modifier.<br/>                                                                                                                                                                                                                                                                       |
| **Explications supplémentaires**<br/> une élaboration des étiquettes de contrôle (généralement pour les liens de commande, les cases d’option et les cases à cocher). <br/>                                    | ![Capture d’écran montrant une boîte de dialogue Paramètres de sécurité.](images/text-ui-image5.png)<br/> Dans cet exemple, les explications supplémentaires clarifient les choix.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Principes de conception

Les développeurs de logiciels considèrent souvent que le texte est relégué à la documentation du produit et au support technique. « Tout d’abord, nous allons écrire le code, puis nous engageons quelqu’un pour nous aider à expliquer ce que nous avons développé ». En réalité, le texte important est écrit plus tôt dans le processus, car l’interface utilisateur est conçue et codée. Ce texte est, après tout, vu plus souvent et par plus de personnes que d’autres types d’écriture technique.

**Le texte compréhensible est essentiel à l’interface utilisateur efficace.** Les rédacteurs et éditeurs professionnels doivent travailler avec les développeurs de logiciels sur le texte de l’interface utilisateur en tant que partie intégrante du processus de conception. Qu’ils travaillent sur du texte plus tôt, car les problèmes de texte révèlent souvent des problèmes de conception. Si votre équipe a des difficultés à expliquer une conception, il s’agit souvent de la conception, et non pas de l’explication, qui nécessite une amélioration.

### <a name="a-design-model-for-ui-text"></a>Modèle de conception pour le texte de l’interface utilisateur

Lorsque vous pensez au texte de l’interface utilisateur et à son positionnement sur vos surfaces d’interface utilisateur, tenez compte des points suivants :

-   Pendant la lecture en focus et immersif, les utilisateurs lisent dans un ordre de gauche à droite et de haut en bas (dans les cultures occidentales).
-   Lors de l’utilisation de logiciels, les utilisateurs ne sont pas immergés dans l’interface utilisateur, mais dans leur travail. Par conséquent, les utilisateurs ne lisent pas le texte de l’interface utilisateur qu’ils analysent.
-   Lors de l’analyse d’une fenêtre, les utilisateurs peuvent sembler lire du texte lorsqu’ils le filtrent en réalité. Ils ne composent souvent pas véritablement le texte de l’interface utilisateur, sauf s’ils perçoivent la nécessité de.
-   Dans une fenêtre, les différents éléments d’interface utilisateur reçoivent des niveaux d’attention différents. Les utilisateurs ont tendance à lire d’abord les étiquettes de contrôle, en particulier celles qui semblent pertinentes pour accomplir la tâche en cours. En revanche, les utilisateurs ont tendance à lire le texte statique uniquement lorsqu’ils pensent qu’ils en ont besoin.

Pour un modèle de conception général, ne partez pas du principe que les utilisateurs lisent soigneusement le texte dans l’ordre de gauche à droite et de haut en bas. Au lieu de cela, supposons que les utilisateurs commencent par numériser rapidement la fenêtre entière, puis lisent le texte de l’interface utilisateur dans l’ordre suivant :

-   Contrôles interactifs au centre
-   [Boutons de validation](glossary.md)
-   Contrôles interactifs trouvés ailleurs
-   Instruction principale
-   Explications supplémentaires
-   Titre de la fenêtre
-   Autre texte statique dans le corps principal
-   Notes de bas de page

Vous devez également supposer qu’une fois que les utilisateurs ont décidé de faire, ils arrêtent immédiatement la lecture et le fait.

### <a name="eliminate-redundancy"></a>Éliminer la redondance

Le texte redondant permet non seulement de gagner de l’espace à l’écran, mais affaiblit l’efficacité des idées ou actions importantes que vous essayez de transmettre. Il s’agit également d’un gaspillage du temps du lecteur, et de plus, dans un contexte où l’analyse est la norme. **Windows s’efforce d’expliquer ce que les utilisateurs doivent faire une fois correctement et de manière concise.**

Passez en revue chaque fenêtre et éliminez les mots et les instructions en double, à la fois dans et dans les contrôles. N’évitez pas que du texte important soit explicite là où cela est nécessaire, mais ne soyez pas redondant et n’Expliquez pas ce qui est évident.

### <a name="avoid-over-communication"></a>Éviter les communications excédentaires

Même si le texte n’est pas redondant, il peut simplement être trop simple pour expliquer chaque détail. **Une trop grande déconseillée pour la lecture de l’œil a tendance à s’ignorer tout de suite, ce qui aurait pour effet de réduire le nombre de communications.** Dans le texte de l’interface utilisateur, communiquent de façon concise les informations essentielles. Si des informations supplémentaires sont nécessaires pour certains utilisateurs ou certains scénarios, fournissez un lien vers du [contenu d’aide](winenv-help.md)plus détaillé, ou peut-être une entrée de Glossaire pour clarifier un terme.

**Incorrect :**

![capture d’écran de la boîte de dialogue avec 6 paragraphes](images/text-ui-image6.png)

Dans cet exemple, il y a trop de texte à analyser facilement. Bien qu’il ne soit pas prévu par le concepteur, il est très probable que les utilisateurs cliquent sur suivant sans rien lire.

Pour éviter que du texte ne recommande de lire, concevez votre texte afin de faire chaque nombre de mots. Ce qui n’ajoute pas de soustractions, utilisez du texte simple et concis.

### <a name="use-the-inverted-pyramid"></a>Utiliser la pyramide inversée

L’écriture universitaire utilise généralement un style structurel « pyramidal » qui établit un fondement des faits, travaille avec ces faits et s’appuie sur une conclusion qui forme une structure similaire à la pyramide. En revanche, les journalistes utilisent un style de « pyramide inversé » qui commence par la conclusion du « fait » fondamental que les lecteurs doivent avoir. Il remplit ensuite progressivement plus de détails que les lecteurs peuvent souhaiter peut-être simplement analyser. L’avantage de ce style est qu’il est juste jusqu’au point, et permet aux lecteurs d’arrêter la lecture à tout moment et de comprendre les informations essentielles.

Vous devez appliquer la structure pyramidale inversée au texte de l’interface utilisateur. Accédez directement au point avec les informations essentielles, laissez les utilisateurs arrêter la lecture à tout moment et utilisez un lien d’aide pour présenter le reste de la pyramide.

![capture d’écran du message lors de la jonction du programme Windows ](images/text-ui-image7.png)

Dans cet exemple, les informations essentielles se trouvent dans la requête du texte d’instruction principal, des informations utiles supplémentaires se trouvent dans les instructions supplémentaires et les détails sont disponibles en cliquant sur un lien d’aide.

**Si vous ne faites que cinq choses...**

1.  Travaillez au début du texte, car les problèmes de texte révèlent souvent des problèmes de conception.
2.  Concevez votre texte pour la numérisation.
3.  Éliminez le texte redondant.
4.  Utilisez du texte facile à comprendre ; ne pas dépasser la communication.
5.  Si nécessaire, fournissez des liens vers du contenu d’aide pour obtenir des informations plus détaillées.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Généralités

-   **Supprimez le texte redondant.** Recherchez du texte redondant dans les titres de la fenêtre, les instructions principales, les instructions supplémentaires, les zones de contenu, les liens de commande et les boutons de validation. En règle générale, laissez le texte intégral dans les instructions principales et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
-   **Évitez les grands blocs de texte de l’interface utilisateur.** Voici les différentes façons de procéder :
    -   Segmentation du texte en phrases et paragraphes plus courts.
    -   Si nécessaire, en fournissant [des liens d’aide vers des](winenv-help.md) informations utiles, mais pas essentielles.
-   **Choisissez des noms d’objets et des étiquettes qui communiquent clairement et différencient ce que fait l’objet.** Les utilisateurs ne doivent pas avoir à déterminer ce que signifie vraiment l’objet ou la manière dont il diffère des autres objets.

    Incorrect :

    ![capture d’écran de la liste des moniteurs sans nom](images/text-ui-image8.png)

    Mieux :

    ![capture d’écran de la liste des cartes réseau spécifiques](images/text-ui-image9.png)

    Dans l’exemple incorrect, les noms d’objets ne se différencient pas du tout. le meilleur exemple montre une différenciation forte par nom de produit.

-   **Si vous souhaitez vous assurer que les utilisateurs lisent du texte spécifique lié à une action, placez-les sur un contrôle interactif.**
    -   **Acceptable:**
    -   ![capture d’écran de l’avertissement de mise en forme à l’aide du bouton OK ](images/text-ui-image10.png)
    -   Dans cet exemple, il y a un risque que les utilisateurs ne lisent pas le texte qui explique ce qu’ils confirment.
    -   **Conseillé**
    -   ![capture d’écran du bouton d’avertissement et de mise en forme ](images/text-ui-image11.png)
    -   Dans cet exemple, vous pouvez être sûr qu’au moins les utilisateurs comprennent qu’ils sont sur le format d’un disque.
-   **Utilisez un espace entre les phrases.** Non deux.

### <a name="text-fonts-sizes-and-colors"></a>Polices, tailles et couleurs de texte

-   **Utilisez du texte bleu uniquement pour les liens et les instructions principales.**
-   **Utilisez du texte vert uniquement pour les URL dans les résultats de recherche.**

Les polices et couleurs suivantes sont des valeurs par défaut pour Windows.



| Modèle                                                                                     | Symbole du thème                            | Police, couleur                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![première colonne : texte de la barre de titre ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![première colonne : instructions principales ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. bleu ( \# 003399) Segoe UI<br/>                 |
| ![première colonne : instructions secondaires ](images/text-ui-image14.png)<br/>      | Instruction<br/>      | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![première colonne : texte normal ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![première colonne : texte mis en évidence ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI, gras ou italique<br/> |
| ![première colonne : texte modifiable ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI, dans une zone<br/>       |
| ![première colonne : texte désactivé ](images/text-ui-image18.png)<br/>               | Désactivé<br/>         | 9 PT. gris foncé ( \# 323232) Segoe UI<br/>             |
| ![première colonne : lien ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 PT. bleu ( \# 0066CC) Segoe UI<br/>                  |
| ![première colonne : liens (pointage) ](images/text-ui-image20.png)<br/>               | À chaud<br/>              | 9 PT. bleu clair ( \# 3399FF) Segoe UI<br/>            |
| ![première colonne : en-tête de groupe ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 PT bleu ( \# 003399) Segoe UI<br/>                 |
| ![première colonne : nom de fichier (dans l’affichage du contenu) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 PT noir ( \# 000000) Segoe UI<br/>                |
| ![première colonne : texte du document ](images/text-ui-image23.png)<br/>               | (aucun)<br/>           | 9 PT. noir ( \# 000000) Calibri<br/>                  |
| ![première colonne : en-têtes de document ](images/text-ui-image24.png)<br/>           | (aucun)<br/>           | 17 PT. noir ( \# 000000) Calibri<br/>                 |



 

Pour plus d’informations et d’exemples, consultez [polices](vis-fonts.md) et [couleurs](vis-color.md).

### <a name="other-text-characteristics"></a>Autres caractéristiques du texte

**Gras**

-   **Utilisez l’attribut gras avec modération pour attirer l’attention sur le texte que les utilisateurs doivent lire.** Par exemple, les utilisateurs qui parcourent une liste d’options de case d’option peuvent avoir à voir les étiquettes en gras, afin de détailler le texte qui ajoute des informations supplémentaires sur chaque option. N’oubliez pas que l’utilisation d’un trop grand gras atténue son impact.
-   **Avec les données étiquetées, utilisez le gras pour mettre en évidence celle qui est la plus importante pour les données dans son ensemble.**
    -   Pour la plupart des données génériques (où les données ont une signification faible sans les étiquettes, comme des chiffres ou des dates), utilisez des étiquettes en gras et des données brutes afin que les utilisateurs puissent facilement analyser et comprendre les types de données.
    -   Pour la plupart des données explicites, utilisez des étiquettes simples et des données en gras afin que les utilisateurs puissent se concentrer sur les données elles-mêmes.
    -   Vous pouvez également utiliser du texte gris foncé pour mettre en évidence les informations les moins importantes au lieu d’utiliser le gras pour mettre en évidence les informations les plus importantes.

        ![capture d’écran de l’affichage miniature de l’Explorateur Windows ](images/text-ui-image25.png)

        Dans cet exemple, au lieu de mettre en évidence les données en gras, les étiquettes sont mises en surbrillance à l’aide de gris foncé.

-   **Toutes les polices ne prenant pas en charge le gras, elles ne doivent jamais être cruciales pour comprendre le texte.**

**Italique**

-   Utilisez pour faire référence à du texte littéralement. N’utilisez pas de guillemets à cette fin.

    **Correct :**

    Les termes document et fichier sont souvent utilisés indifféremment.

-   Utilisez pour les [invites](glossary.md) dans les [zones de texte](ctrl-text-boxes.md) et les [listes déroulantes modifiables](/windows/desktop/uxguide/ctrl-drop).

    ![capture d’écran de la zone de texte de recherche ](images/text-ui-image26.png)

    Dans cet exemple, l’invite dans la zone de recherche est mise en forme en texte italique.

-   Utilisez avec modération pour mettre en évidence des mots spécifiques afin de faciliter la compréhension.
-   **Toutes les polices ne prenant pas en charge l’italique, elles ne doivent jamais être cruciales pour comprendre le texte.**

**Italique gras**

-   N’utilisez pas dans le texte de l’interface utilisateur.

**Souligner**

-   N’utilisez pas, à l’exception des liens.
-   N’utilisez pas pour l’accent. Utilisez à la place Italic.

### <a name="punctuation"></a>Ponctuation

**Points**

-   **Ne placez pas à la fin des étiquettes de contrôle, des instructions principales ou des liens d’aide.**
-   Placez à la fin des instructions supplémentaires, des explications supplémentaires ou tout autre texte statique qui forme une phrase complète.

**Points d’interrogation**

-   **Placez à la fin de toutes les questions.** Contrairement aux points, les points d’interrogation sont utilisés pour tous les types de texte.

**Points d’exclamation**

-   Dans les applications métier, évitez.
    -   **Exceptions :** Les points d’exclamation sont parfois utilisés dans le contexte de la fin du téléchargement (« Done ! ») et pour attirer l’attention sur le contenu Web (« New ! »).

**Des virgules**

-   Dans une liste de trois éléments ou plus, placez toujours une virgule après le dernier élément de la liste.

**Virgules**

-   **Utilisez des signes deux-points à la fin des étiquettes de contrôle externes.** Ceci est particulièrement important pour l’accessibilité, car certaines technologies d’assistance recherchent les signes deux-points pour identifier les étiquettes de contrôle.
-   Utilisez un signe deux-points pour introduire une liste d’éléments.

**Suspension**

-   **Les ellipses signifient incomplète.** Utilisez des ellipses dans le texte de l’interface utilisateur comme suit :
    -   **Commandes :** Indique qu’une commande a besoin d’informations supplémentaires. N’utilisez pas de points de suspension chaque fois qu’une action affiche une autre fenêtre uniquement lorsque des informations supplémentaires sont requises. Pour plus d’informations, consultez [boutons de commande](ctrl-command-buttons.md).
    -   **Données :** Indique que le texte est tronqué.
    -   **Étiquettes :** Indique qu’une tâche est en cours (par exemple, « recherche en cours... »).

        **Conseil :** Le texte tronqué dans une fenêtre ou une page avec un espace inutilisé indique une mauvaise disposition ou une taille de fenêtre par défaut trop petite. S’efforcer des dispositions et des tailles de fenêtre par défaut qui éliminent ou réduisent la quantité de texte tronqué. Pour plus d’informations, consultez [Disposition](vis-layout.md).

-   **N’effectuez pas de sélections interactives.** Pour afficher du texte tronqué, laissez les utilisateurs redimensionner le contrôle pour afficher davantage de texte ou utilisez un [contrôle de divulgation progressif](ctrl-progressive-disclosure-controls.md) à la place.

**Guillemets et apostrophes**

-   Pour faire référence à du texte littéralement, utilisez une mise en forme en italique plutôt que des guillemets.
-   Placez les titres de fenêtre et les étiquettes de contrôle entre guillemets uniquement si nécessaire pour éviter toute confusion et que vous ne pouvez pas mettre en forme en gras à la place.
-   Pour les guillemets, préférez les guillemets doubles (""); Évitez les guillemets simples.

    **Correct :**

    Voulez-vous vraiment supprimer le « dossier Cat Sparky » ?

    **Incorrect :**

    Voulez-vous vraiment supprimer le « dossier Cat Sparky » ?

### <a name="capitalization"></a>Mise en majuscules

-   **Utilisez la mise en majuscules de style titre pour les titres, en majuscules pour tous les autres éléments de l’interface utilisateur.** Cela est plus approprié pour le [ton Windows](text-style-tone.md).

    -   **Exception :** Pour les applications héritées, vous pouvez utiliser la mise en majuscules de style titre pour les boutons de commande, les menus et les en-têtes de colonnes si nécessaire pour éviter de mélanger les styles de mise en majuscules.

        ![capture d’écran de la feuille de propriétés générique ](images/text-ui-image27.png)

    Cet exemple générique illustre la mise en majuscules et la ponctuation appropriées pour les feuilles de propriétés.

    ![capture d’écran de la boîte de dialogue générique ](images/text-ui-image28.png)

    Cet exemple générique illustre la mise en majuscules et les signes de ponctuation corrects pour les boîtes de dialogue.

-   **Pour les noms de fonctionnalités et de technologies, soyez prudent en majuscules.** En règle générale, seuls les principaux composants doivent être en majuscules (à l’aide de la mise en majuscules du style titre).

    **Correct :**

    Analysis Services, cubes, dimensions

    Analysis Services est un composant majeur de SQL Server, la mise en majuscules de type titre est donc appropriée. les cubes et les dimensions sont des éléments communs du logiciel d’analyse de base de données. il n’est donc pas nécessaire de les mettre en majuscules.

-   **Pour les noms de fonctionnalités et de technologies, soyez cohérent en majuscules.** Si le nom apparaît plusieurs fois sur un écran de l’interface utilisateur, il doit toujours apparaître de la même façon. De même, dans tous les écrans de l’interface utilisateur du programme, le nom doit être présenté de manière cohérente.
-   Ne mettez pas en majuscules les noms des éléments génériques de l’interface utilisateur, tels que la barre d’outils, le menu, la barre de défilement, le bouton et l’icône.
    -   **Exceptions :** Barre d’adresses, barre de liens.
-   N’utilisez pas toutes les lettres majuscules pour les touches du clavier. Au lieu de cela, suivez la casse utilisée par les claviers standard ou en minuscules si la touche n’est pas étiquetée sur le clavier.

    **Correct :**

    barre d’espace, tabulation, entrée, page précédente, Ctrl + Alt + Suppr

    **Incorrect :**

    BARRE D’ESPACE, TABULATION, ENTRÉE, PG. PRÉC., CTRL + ALT + SUPPR

-   **N’utilisez pas toutes les lettres majuscules pour l’accentuation.** Des études ont montré que cela est difficile à lire, et les utilisateurs ont tendance à les considérer comme « hurlant ». Pour les avertissements, utilisez une icône d’avertissement et une explication clairement formulée sur la situation. Il n’est pas nécessaire d’ajouter, par exemple, le terme avertissement en majuscules.

Pour plus d’informations, consultez la section « texte » ou « étiquettes » dans les instructions relatives aux composants d’interface utilisateur spécifiques.

### <a name="dates-and-times"></a>Dates et heures

-   **Ne codez pas en dur le format des dates et des heures.** Respectez les options de paramètres régionaux et de personnalisation de l’utilisateur pour les formats de date et d’heure. L’utilisateur les sélectionne dans l’élément région et langue du panneau de configuration.

    ![capture d’écran du format de date : lundi 06 juillet, 2009](images/text-ui-image29.png)![capture d’écran du format de date : 06 juillet 2009](images/text-ui-image30.png)

    Dans ces exemples de Microsoft Outlook, les deux formats pour la date longue sont corrects. Ils reflètent différents choix effectués par les utilisateurs dans l’élément du panneau de configuration région et langue.

-   **Utilisez le format de date longue pour les scénarios qui tirent parti de l’utilisation d’informations supplémentaires.** Utilisez le format de date abrégé pour les contextes qui n’ont pas suffisamment d’espace pour le format long. Tandis que les utilisateurs choisissent les informations qu’ils souhaitent inclure dans les formats longs et courts, les concepteurs choisissent le format à afficher dans leurs programmes en fonction du scénario et du contexte.

    ![capture d’écran du format avec dates de début et échéance](images/text-ui-image31.png)

    Dans cet exemple, le format de date longue aide les utilisateurs à organiser les tâches et les échéances.

### <a name="globalization-and-localization"></a>Globalisation et localisation

La globalisation signifie créer des documents ou des produits utilisables dans n’importe quel pays, région ou culture. La localisation consiste à adapter des documents ou des produits pour une utilisation dans des paramètres régionaux autres que le pays ou la région d’origine. Envisagez la globalisation et la localisation lors de l’écriture de texte d’interface utilisateur. Votre programme peut être traduit dans d’autres langues et utilisé dans des cultures très différentes de votre choix.

-   Pour les contrôles avec contenu de variable (tels que les affichages de liste et les arborescences), **Choisissez une largeur appropriée pour les données valides les plus longues.**
-   **Incluez suffisamment d’espace dans la surface de l’interface utilisateur pour 30 pour cent supplémentaires** (jusqu’à 200 pour cent pour du texte plus court) pour tout texte (mais pas les nombres) qui sera localisé. La traduction d’une langue à une autre modifie souvent la longueur de ligne du texte.
-   Ne composez pas de chaînes à partir de sous-chaînes au moment de l’exécution. Utilisez plutôt des phrases complètes afin qu’il n’existe aucune ambiguïté pour le traducteur.
-   **N’utilisez pas de contrôle subordonné, les valeurs qu’il contient ou son étiquette Units pour créer une phrase ou une expression.** Une telle conception n’est pas localisable, car la structure de phrases varie en fonction de la langue.

    **Incorrect :**

    ![capture d’écran de la zone de texte dans une étiquette de case à cocher ](images/text-ui-image32.png)

    **Correct :**

    ![capture d’écran de la zone de texte après une étiquette de case à cocher ](images/text-ui-image33.png)

    Dans l’exemple incorrect, la zone de texte est placée à l’intérieur de l’étiquette de la case à cocher.

-   Ne faites pas partie d’une phrase un lien, car lorsqu’il est traduit, ce texte peut ne pas rester ensemble. Le texte du lien doit donc former une phrase complète.
    -   **Exception :** Des liens de Glossaire peuvent être insérés inline dans le cadre d’une phrase.

Pour plus d’informations, consultez le [Centre de développement Go Global](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Barre de titre Texte

-   Choisissez le texte de la barre de titre en fonction du type de fenêtre :
    -   **Fenêtres de programme de niveau supérieur, centrées sur les documents :** Utilisez le format « nom du programme nom du document ». Les noms de documents s’affichent en premier pour fournir une apparence centrée sur les documents.
    -   **Fenêtres de programme de niveau supérieur qui ne sont pas centrées sur les documents :** Affiche uniquement le nom du programme.
    -   **Boîtes de dialogue :** Affiche la commande, la fonctionnalité ou le programme à partir duquel la boîte de dialogue a été fournie. N’utilisez pas le titre pour expliquer l’objectif de la boîte de dialogue qui est l’objectif des instructions principales. Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).
    -   **Assistants :** Affichez le nom de l’Assistant. Notez que le mot « Wizard » ne doit pas être inclus dans les noms d’Assistant. Pour plus d’instructions, consultez [assistants](win-wizards.md).
-   **Pour les fenêtres de programme de niveau supérieur, si la légende et l’icône de la barre de titre sont affichées de manière visible vers le haut de la fenêtre, vous pouvez masquer la légende et l’icône de la barre de titre pour éviter la redondance.** Toutefois, vous devez toujours définir en interne un titre approprié pour une utilisation par Windows.
-   **Pour les boîtes de dialogue, n’incluez pas les mots « boîte de dialogue » ou « progression » dans les titres.** Ces concepts sont implicites et les absences de ces mots rendent les titres plus faciles à analyser par les utilisateurs.

### <a name="main-instructions"></a>Instructions principales

-   **Utilisez l’instruction principale pour décrire de façon concise ce que les utilisateurs doivent faire dans une fenêtre ou une page donnée.** Les bonnes instructions principales communiquent l’objectif de l’utilisateur au lieu de se concentrer uniquement sur la manipulation de l’interface utilisateur.
-   **Exprimez l’instruction principale sous la forme d’une direction impérative ou d’une question spécifique.**

    **Incorrect :**

    ![capture d’écran du nom du programme en tant qu’instruction principale ](images/text-ui-image34.png)

    Dans cet exemple, l’instruction principale indique simplement le nom du programme. Il n’invite pas explicitement un cours d’action que l’utilisateur doit prendre.

    **Exceptions :** Les messages d’erreur, les messages d’avertissement et les confirmations peuvent utiliser des structures de phrases différentes dans leurs instructions principales.

-   **Utilisez des verbes spécifiques chaque fois que cela est possible.** Les verbes spécifiques (exemples : connexion, enregistrement, installation) sont plus explicites pour les utilisateurs que les verbes génériques (exemples : configurer, gérer, définir).
    -   Si vous ne pouvez pas utiliser un verbe spécifique pour les pages du panneau de configuration et les pages de l’Assistant, vous préférerez peut-être omettre complètement le verbe.

        **Acceptable:**

        Entrez vos paramètres régionaux, votre région et votre langue

        **Conseillé**

        Paramètres régionaux, région et langue

    -   Pour les boîtes de dialogue, telles que les messages d’erreur et les avertissements, n’oubliez pas le verbe.

-   Ne vous inquiétez pas d’utiliser le texte d’instruction principal si son ajout ne serait pas redondant ou évident dans le contexte de l’interface utilisateur.

    ![capture d’écran de la boîte de dialogue Enregistrer sous ](images/text-ui-image35.png)

    Dans cet exemple, le contexte de l’interface utilisateur est déjà très clair. Il n’est pas nécessaire d’ajouter le texte d’instruction principal.

-   **N’utilisez qu’une seule phrase complète.** Réduisez l’instruction principale aux informations essentielles. Si vous devez apporter des explications supplémentaires, envisagez d’utiliser une instruction supplémentaire.
-   Utilisez les majuscules comme pour les phrases.
-   **N’incluez pas de périodes finales si l’instruction est une instruction.** Si l’instruction est une question, incluez un point d’interrogation final.
-   **Pour les boîtes de dialogue de progression, utilisez une expression gerund pour expliquer brièvement l’opération en cours,** en terminant par des points de suspension. Exemple : « impression de vos images... »
-   **Conseil :** Vous pouvez évaluer une instruction principale en imaginant ce que vous indiquez à un ami lorsque vous expliquez comment faire avec la fenêtre ou la page. En cas de réponse avec l’instruction principale, il ne s’agit pas d’une instruction naturelle, sans aide ou difficile à retravailler.

Pour plus d’informations, consultez la section « instructions principales » dans les instructions relatives aux composants d’interface utilisateur spécifiques.

### <a name="supplemental-instructions"></a>Instructions supplémentaires

-   Si nécessaire, **Utilisez une instruction supplémentaire pour présenter des informations supplémentaires utiles pour comprendre ou utiliser la fenêtre ou la page,** par exemple :
    -   Fournir un contexte pour expliquer pourquoi la fenêtre est affichée si elle est lancée par le programme ou par le système.
    -   Informations de qualification qui aident les utilisateurs à décider comment agir sur l’instruction principale.
    -   Définition de la terminologie importante.
-   **N’utilisez pas d’instruction supplémentaire si aucune instruction n’est nécessaire.** Préférez tout communiquer avec l’instruction principale si vous pouvez le faire de façon concise.
-   **Ne répétez pas l’instruction principale avec un libellé légèrement différent.** Au lieu de cela, omettez l’instruction supplémentaire s’il n’y a rien d’autre à ajouter.
-   Utilisez les phrases complètes et les majuscules de style de phrase.

### <a name="control-labels"></a>Étiquettes de contrôle

-   **Étiquetez chaque contrôle ou groupe de contrôles. Exceptions**
    -   Les zones de texte et les listes déroulantes peuvent être étiquetées à l’aide d’invites.
    -   Les contrôles de divulgation progressive sont généralement sans étiquette.
    -   **Les contrôles subordonnés utilisent l’étiquette du contrôle associé.** Les contrôles spin sont toujours des contrôles subordonnés.
    -   **Omettez les étiquettes de contrôle qui restatent l’instruction principale.** Dans ce cas, l’instruction principale prend la clé d’accès.

        **Acceptable:**

        ![capture d’écran de la zone de texte avec l’instruction et l’étiquette ](images/text-ui-image36.png)

        Dans cet exemple, l’étiquette de la zone de texte n’est qu’une REstate de l’instruction principale.

        **Conseillé**

        ![capture d’écran de la zone de texte avec des instructions uniquement ](images/text-ui-image37.png)

        Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend la clé d’accès.

-   Emplacement de l’étiquette :
    -   Les bulles, les cases à cocher, les boutons de commande, les zones de groupe, les liens, les onglets et les conseils sont étiquetés directement par le contrôle lui-même.
    -   Les listes déroulantes, les zones de liste, les affichages de liste, les barres de progression, les curseurs, les zones de texte et les arborescences sont étiquetés ci-dessus, aligné à gauche ou à gauche.
    -   Les contrôles de divulgation progressive sont généralement sans étiquette. Les boutons en chevrons sont étiquetés à droite.
-   **Assignez une clé d’accès unique pour chaque contrôle interactif** , à l’exception des liens. Pour plus d’informations, consultez [clavier](inter-keyboard.md).
-   **Conserver les étiquettes brièvement.** Notez, toutefois, que l’ajout d’un ou deux mots à une étiquette peut aider à clarifier et, parfois, élimine la nécessité d’explications supplémentaires.
-   **Préférer des étiquettes spécifiques à des étiquettes génériques.** Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette.

    **Incorrect :**

    ![capture d’écran du bouton de commande OK ](images/text-ui-image38.png)

    **Correct :**

    ![capture d’écran du bouton de commande publier ](images/text-ui-image39.png)

    Dans l’exemple correct, une étiquette spécifique est utilisée pour le bouton valider.

-   **Pour les listes d’étiquettes, telles que les cases d’option, utilisez une formulation parallèle** et essayez de conserver la même longueur pour toutes les étiquettes.
-   **Pour les listes d’étiquettes, concentrez le texte de l’étiquette sur les différences entre les options.** Si toutes les options ont le même texte d’introduction, déplacez ce texte vers l’étiquette de groupe.

    **Incorrect :**

    ![capture d’écran des étiquettes avec des premières expressions dupliquées](images/text-ui-image40.png)

    **Correct :**

    ![capture d’écran de la première phrase déplacée vers l’étiquette de groupe](images/text-ui-image41.png)

    L’exemple correct déplace la formulation d’introduction identique vers l’étiquette, de sorte que les deux options sont différenciées correctement.

-   **En général, préférez une formulation positive.** Par exemple, utilisez do au lieu de do not, et avertis au lieu de ne pas notifier.
    -   **Exception :** L’étiquette de case à cocher « ne plus afficher ce message » est largement utilisée.
-   **Omettez les verbes pédagogiques qui s’appliquent à tous les contrôles du type donné.** Au lieu de cela, concentrez-vous sur ce qui est unique sur les contrôles. Par exemple, il va sans dire que les utilisateurs doivent taper dans un contrôle de zone de texte ou que les utilisateurs doivent cliquer sur un lien.

    **Incorrect :**

    ![capture d’écran de l’étiquette : « tapez votre nom » ](images/text-ui-image42.png)

    **Correct :**

    ![capture d’écran de l’étiquette : « Your Name » ](images/text-ui-image43.png)

    Dans les exemples incorrects, les étiquettes de contrôle ont des verbes d’instructions qui s’appliquent à tous les contrôles de leur type.

-   Dans certains cas, les annotations entre parenthèses suivantes pour contrôler les étiquettes peuvent être utiles :
    -   **Si une option est facultative, ajoutez « (facultatif) » à l’étiquette.**
    -   **Si une option est fortement recommandée, ajoutez « (recommandé) » à l’étiquette.** Cela signifie que le paramètre est facultatif, mais doit être défini quand même.
    -   **Si une option est destinée uniquement aux utilisateurs expérimentés, envisagez d’ajouter « (avancé) » à l’étiquette.**
-   Vous pouvez spécifier des unités (secondes, connexions, etc.) entre parenthèses après l’étiquette.

    ![capture d’écran de l’étiquette : taille initiale (Mo) ](images/text-ui-image44.png)

    Cet exemple montre que l’unité de mesure est exprimée en mégaoctets (Mo).

Pour plus d’informations, consultez la section « texte » ou « étiquettes » dans les instructions relatives aux composants d’interface utilisateur spécifiques.

### <a name="supplemental-explanations"></a>Explications supplémentaires

-   **Utilisez des explications supplémentaires lorsque les contrôles requièrent plus d’informations que ceux qui peuvent être transmis par leur étiquette.** Mais n’utilisez pas d’explication supplémentaire si vous n’avez pas besoin de tout communiquer avec l’étiquette de contrôle si vous pouvez le faire de façon concise. En général, les explications supplémentaires sont utilisées avec des liens de commande, des cases d’option et des cases à cocher.
-   Si nécessaire, **Utilisez l’attribut gras dans les étiquettes des contrôles pour faciliter l’analyse du texte** lorsqu’il existe des explications supplémentaires.

    ![capture d’écran de la boîte de dialogue Paramètres de sécurité ](images/text-ui-image45.png)

    Dans cet exemple, les étiquettes des cases d’option sont en gras pour faciliter leur analyse.

-   **L’ajout d’une explication supplémentaire à un contrôle dans un groupe ne signifie pas que vous devez fournir des explications pour tous les autres contrôles du groupe.** Fournissez les informations pertinentes dans l’étiquette si vous pouvez et utilisez des explications uniquement lorsque cela est nécessaire. N’ont pas d’explications supplémentaires qui restatent simplement l’étiquette pour des fins de cohérence.

    ![capture d’écran de trois cases d’option ](images/text-ui-image46.png)

    Dans cet exemple, deux contrôles du groupe incluent des explications supplémentaires, mais pas le troisième.

-   Si une explication supplémentaire suit un lien de commande, écrivez le texte supplémentaire dans la deuxième personne.

    **Exemple :** Lien de commande : créer des paramètres de réseau sans fil et les enregistrer sur un disque mémoire flash USB

    Explication supplémentaire : cette opération permet de créer des paramètres que vous pouvez transférer sur le routeur à l’aide d’un disque mémoire flash USB. Procédez ainsi uniquement si vous disposez d’un routeur sans fil prenant en charge la configuration de disque mémoire flash USB.

-   Utilisez des phrases complètes et terminez la ponctuation.

### <a name="commit-button-labels"></a>Étiquettes de bouton de validation

Le tableau suivant répertorie les étiquettes de bouton de validation les plus courantes et leur utilisation.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Étiquette du bouton</strong><br/></td>
<td><strong>Signification</strong><br/></td>
<td><strong>Quand utiliser</strong><br/></td>
<td><strong>Clé d’accès</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK</strong><br/></td>
<td><ul>
<li>Dans les boîtes de dialogue : appliquer les modifications ou valider la tâche et fermer la fenêtre.</li>
<li>Dans les fenêtres de propriétés du propriétaire : appliquez les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application) et fermez la fenêtre.</li>
<li>Dans les fenêtres de propriétés détenues : conserver les modifications, fermer la fenêtre et appliquer les modifications lorsque les modifications de la fenêtre propriétaire sont appliquées.</li>
</ul></td>
<td><ul>
<li>Utilisez avec les fenêtres qui ne sont pas spécifiques aux tâches, telles que les feuilles de propriétés.</li>
<li>Pour les fenêtres utilisées pour effectuer une tâche spécifique, utilisez une étiquette spécifique à la place, qui commence par un verbe (exemple : Print).</li>
<li>Pour les fenêtres dans lesquelles les utilisateurs ne peuvent pas apporter de modifications, utilisez fermer.</li>
</ul></td>
<td>Entrez<br/></td>
</tr>
<tr class="odd">
<td><strong>Oui/non</strong><br/></td>
<td>Oui est la réponse affirmative à une question oui ou non, alors que non correspond à la réponse négative.<br/></td>
<td><ul>
<li>Utilisez les boutons Oui et non uniquement pour répondre à des questions oui ou non. N’utilisez jamais OK et annuler pour les questions oui ou aucune.</li>
<li>Préférer des réponses spécifiques sur les boutons Oui et non. Bien qu’il n’y ait rien de mal à utiliser Oui et non, les réponses spécifiques peuvent être comprises plus rapidement, ce qui permet une prise de décision efficace.</li>
<li>Toutefois, envisagez d’utiliser Oui et aucune réponse si la formulation de réponses spécifiques s’avère trop longue ou maladroite.</li>
<li>N’utilisez pas de boutons Oui et non si la signification de la réponse no n’est pas claire. Dans ce cas, utilisez des réponses spécifiques à la place.</li>
<li>Oui et non doivent toujours être utilisés en tant que paire.</li>
</ul></td>
<td>O et N<br/></td>
</tr>
<tr class="even">
<td><strong>Annuler</strong><br/></td>
<td><ul>
<li>Dans les boîtes de dialogue : ignorer toutes les modifications ou le travail en cours, revenir à l’état précédent (sans effet secondaire visible) et fermer la fenêtre.</li>
<li>Dans les feuilles de propriétés : ignorer toutes les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application) et fermer la fenêtre.</li>
<li>Dans les éléments du panneau de configuration : ignorer toutes les modifications ou travailler en cours, revenir à l’état précédent et revenir à la page Hub à partir de laquelle la tâche a été lancée. S’il n’existe pas de page de concentrateur de ce type, fermez la fenêtre de l’élément du panneau de configuration à la place.</li>
</ul></td>
<td><ul>
<li>À utiliser lorsque toutes les modifications ou actions en attente peuvent être ignorées et que tous les effets secondaires peuvent être annulés.</li>
<li>Pour les modifications qui ne peuvent pas être ignorées, utilisez fermer. Pour les actions en cours qui peuvent être arrêtées, utilisez arrêter. Si des modifications ou des actions initiales peuvent être ignorées, vous pouvez utiliser Cancel initialement, puis modifier pour fermer ou arrêter une fois qu’il ne peut pas être annulé.</li>
</ul></td>
<td>Échap<br/></td>
</tr>
<tr class="odd">
<td><strong>Fermer</strong><br/></td>
<td>Fermez la fenêtre. Les modifications ou les effets secondaires ne sont pas ignorés.<br/></td>
<td><ul>
<li>À utiliser lorsque les modifications ou les effets secondaires ne peuvent pas être ignorés. Utilisez fermer au lieu de annuler pour les fenêtres principales.</li>
<li>Utilisez pour Windows dans lequel les utilisateurs ne peuvent pas apporter de modifications.</li>
</ul></td>
<td>ALT + F4, CTRL + F4<br/></td>
</tr>
<tr class="even">
<td><strong>Stop</strong><br/></td>
<td>Arrêter une tâche en cours d’exécution et fermer la fenêtre. Les travaux en cours ou les effets secondaires ne sont pas ignorés.<br/></td>
<td><ul>
<li>À utiliser lorsque le travail en cours et les effets secondaires ne peuvent pas ou ne sont pas ignorés, en général avec les barres de progression ou les animations.</li>
</ul></td>
<td>Échap<br/></td>
</tr>
<tr class="odd">
<td><strong>Appliquer</strong><br/></td>
<td>Dans les feuilles de propriétés de propriétaire : appliquez les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application), mais laissez la fenêtre ouverte. Cela permet aux utilisateurs d’évaluer les modifications avant de fermer la feuille de propriétés. Dans les feuilles de propriétés détenues : n’utilisez pas.<br/></td>
<td><ul>
<li>Utilisez uniquement dans les feuilles de propriétés.</li>
<li>Ne fournissez un bouton appliquer que si la feuille de propriétés contient des paramètres (au moins un) avec des effets que les utilisateurs peuvent évaluer de manière explicite. En règle générale, les boutons appliquer sont utilisés lorsque les paramètres apportent des modifications visibles. Les utilisateurs doivent pouvoir appliquer une modification, évaluer la modification et apporter d’autres modifications en fonction de cette évaluation. Si ce n’est pas le cas, supprimez le bouton appliquer au lieu de le désactiver.</li>
</ul></td>
<td>Un<br/></td>
</tr>
<tr class="even">
<td><strong>Next</strong><br/></td>
<td>Dans les assistants et les tâches à plusieurs étapes : passez à l’étape suivante sans valider la tâche.<br/></td>
<td><ul>
<li>À utiliser uniquement dans les assistants et les tâches à plusieurs étapes pour passer à l’étape suivante sans engagement.</li>
<li>L’effet d’un bouton suivant peut toujours être annulé en cliquant sur précédent.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Terminer</strong><br/></td>
<td>Dans les assistants et les tâches à plusieurs étapes : fermez la fenêtre. Si la tâche n’a pas encore été effectuée, effectuez la tâche. Si cette tâche a déjà été effectuée, les modifications ou les effets secondaires ne sont pas ignorés.<br/></td>
<td><ul>
<li>À utiliser uniquement dans les assistants et les tâches à plusieurs étapes. Toutefois, l’utilisation de la finition est déconseillée, car il existe généralement un bouton de validation mieux adapté :
<ul>
<li>Si le fait de cliquer sur le bouton est validé sur la tâche (donc la tâche n’a pas déjà été exécutée), utilisez une étiquette spécifique qui commence par un verbe (exemples : Print, Connect, Start) qui est une réponse à l’instruction principale.</li>
<li>Si la tâche a déjà été effectuée dans l’Assistant, utilisez à la place la fermeture.</li>
</ul></li>
<li>Toutefois, vous pouvez utiliser terminer lorsque :
<ul>
<li>L’étiquette spécifique est toujours générique, par exemple enregistrer, sélectionner, choisir ou récupérer.</li>
<li>La tâche implique la modification d’un paramètre ou d’une collection de paramètres.</li>
</ul></li>
</ul></td>
<td>Entrez<br/></td>
</tr>
<tr class="even">
<td><strong>Done</strong><br/></td>
<td>Non applicable.<br/></td>
<td><ul>
<li>Ne pas utiliser. Une commande est incorrecte par programmation.</li>
</ul></td>
<td>Non applicable.<br/></td>
</tr>
</tbody>
</table>



 

