---
title: Polices
description: Les utilisateurs interagissent avec le texte plus qu’avec tout autre élément dans Microsoft Windows. Segoe UI (prononcer \ 0034 ; Voir-Go \ 0034 ;) police système de Windows. La taille de police standard a été augmentée à 9 points.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6c5fad1459d4ce45f2d677d4bd5864d89b125e4e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761222"
---
# <a name="fonts"></a>Polices

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les utilisateurs interagissent avec le texte plus qu’avec tout autre élément dans Microsoft Windows. Segoe UI (prononcez « SEE-Go ») est la police système Windows. La taille de police standard a été augmentée à 9 points.

![illustration de l’alphabet dans la police de l’interface utilisateur Segoe ](images/vis-fonts-image1.png)

Police de Segoe UI.

Segoe UI et Segoe ne sont pas de la même police. Segoe UI est la police Windows destinée aux chaînes de texte de l’interface utilisateur. Segoe est une police de personnalisation utilisée par Microsoft et ses partenaires pour produire des documents pour l’impression et la publicité.

Segoe UI est une police d’interfonctionnement, ouverte et conviviale, et par conséquent, elle offre une meilleure lisibilité que Tahoma, Microsoft sans serif et Arial. Il a les caractéristiques d’un Humanist sans serif : la largeur variable de ses majuscules (E et S étroites, par exemple, par rapport à Helvetica, où les largeurs sont plus semblables, relativement larges); la contrainte et la letterforms de ses minuscules ; et son vrai italique (au lieu d’un « oblique » ou d’un chiffre romain incliné, comme de nombreux sans serifs à l’aspect industriel). La police est destinée à fournir le même effet visuel à l’écran et à l’impression. Il a été conçu pour être un Humanist sans serif sans caractère fort ou quirkiness gênant.

Segoe UI est optimisée pour ClearType, qui est activée par défaut dans Windows. Avec ClearType activé, Segoe UI est une police élégante et lisible. Si ClearType n’est pas activé, Segoe UI n’est acceptable que de façon marginale. Ce facteur détermine quand vous devez utiliser Segoe UI.

Segoe UI comprend des caractères latins, grecs, cyrilliques et arabes. Il existe de nouvelles polices, également optimisées pour ClearType, créées pour d’autres jeux de caractères et utilisations. Il s’agit notamment de Meiryo pour le japonais, Malgun Gothic pour le coréen, Microsoft JhengHei pour le chinois (traditionnel), Microsoft YaHei pour le chinois (simplifié), gisha pour l’hébreu et Leelawadee pour le thaï, et les polices de collection ClearType conçues pour l’utilisation de documents.

Meiryo comprend des caractères latins basés sur Verdana. Malgun Gothic, Microsoft JhengHei et Microsoft YaHei utilisent une Segoe UI personnalisée. L’utilisation de versions en italique de ces polices n’est pas recommandée. Malgun Gothic, Microsoft JhengHei et Microsoft YaHei sont fournis uniquement en styles standard et en gras, ce qui signifie que les caractères italiques sont synthétisés en inclinant les styles de droite. Bien que Meiryo comprenne des italiques true et gras, ces styles s’appliquent uniquement aux caractères latins. les caractères japonais restent debout lorsque le style italique est appliqué.

Une variation de Meiryo, appelée interface utilisateur Meiryo, est préférable dans l’interface utilisateur de la commande [rubans](cmd-ribbons.md) .

Pour prendre en charge les paramètres régionaux à l’aide de ces jeux de caractères, Segoe UI est remplacé par les polices appropriées en fonction de chaque paramètre régional au cours du processus de [localisation](glossary.md) .

Pour obtenir une licence Segoe UI et d’autres polices Microsoft en vue de leur distribution avec un programme Windows, contactez [Monotype](https://www.monotype.com/).

**Remarque :** Les instructions relatives au [style et](text-style-tone.md) au [texte de l’interface utilisateur](text-ui.md) et du style sont présentées dans des articles distincts.

## <a name="design-concepts"></a>Principes de conception

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Polices, caractères de police, tailles de points et attributs

Dans la typographie traditionnelle, une police décrit une combinaison d’une police, d’une taille de point et d’attributs. Une police est l’apparence de la police. Segoe UI, Tahoma, Verdana et Arial sont toutes des polices. La taille en points fait référence à la taille de la police, mesurée à partir du haut des hampes supérieures jusqu’au bas des descendants, moins l’espacement interne (appelé début). Un point est approximativement de 1/72 cm. Enfin, une police peut avoir des attributs gras ou italique.

De manière informelle, les gens utilisent souvent la police à la place de la police comme c’est le cas dans cet article, mais techniquement, Segoe UI est un type de caractères, et non une police. Chaque combinaison d’attributs est une police unique (par exemple, 9 points Segoe UI normal, 10 points Segoe UI gras, etc.).

### <a name="serif-and-sans-serif"></a>Serif et sans serif

Les polices sont soit Serif, soit sans serif. Serif fait référence aux petits tours qui terminent souvent les traits des lettres d’une police. Une police sans serif n’a pas de Serif.

En général, les lecteurs préfèrent les polices Serif utilisées en tant que corps de texte dans un document. Les serifs fournissent une sensation de formalisation et d’élégance à un document. Pour le texte de l’interface utilisateur, la nécessité d’une apparence propre et la résolution inférieure des moniteurs d’ordinateur font du meilleur choix les polices sans serif.

### <a name="contrast"></a>Comparez

Le texte est plus facile à lire lorsqu’il existe une grande différence entre la luminance du texte et l’arrière-plan. Le texte noir sur un arrière-plan blanc donne le contraste le plus élevé au texte le plus clair sur un arrière-plan très clair peut également fournir un contraste élevé. Cette combinaison est idéale pour les surfaces d’interface utilisateur principales.

Le texte clair sur un arrière-plan foncé offre un bon contraste, mais pas aussi bien que du texte foncé sur un arrière-plan clair. Cette combinaison fonctionne bien pour les surfaces de l’interface utilisateur secondaires, telles que les volets des tâches de l’Explorateur, que vous souhaitez mettre en évidence par rapport aux surfaces principales de l’interface utilisateur.

**Si vous souhaitez vous assurer que les utilisateurs lisent votre texte, utilisez du texte foncé sur un arrière-plan clair.**

### <a name="affordances"></a>Intuitivité

Le texte peut utiliser le [intuitivité](glossary.md) suivant pour indiquer comment il est utilisé :

-   **Dirigé.** Le pointeur I-bar (« texte SELECT ») indique que le texte est sélectionnable, tandis que le pointeur pointant vers la gauche (« normal Select ») indique que le texte n’est pas.
-   **Signe insertion.** Quand le texte a le focus d’entrée, le signe insertion est la barre verticale clignotante qui indique le point d’insertion/sélection dans du texte sélectionnable ou modifiable.
-   **Boîte.** Zone autour du texte qui indique qu’il est modifiable. Pour réduire le poids de la présentation, la zone peut s’afficher dynamiquement uniquement lorsque le texte modifiable est sélectionné.
-   **Couleur de premier plan.** Gris clair indique que le texte est désactivé. Les couleurs non grises, en particulier bleu et violet, indiquent que le texte est un lien.
-   **Couleur d’arrière-plan.** Un arrière-plan gris clair suggère faiblement que le texte est en lecture seule, mais dans la pratique, le texte en lecture seule peut avoir n’importe quel arrière-plan de couleur.

Ces intuitivité sont combinés pour les significations suivantes :

-   **Modifiée.** Texte affiché dans une zone, avec un pointeur de sélection de texte, un signe insertion (sur le focus d’entrée) et généralement sur un arrière-plan blanc.
-   **Lecture seule, sélectionnable.** Texte avec un pointeur sélectionner et un signe insertion (sur le focus d’entrée).
-   **Lecture seule, non sélectionnable.** Texte avec pointeur en forme de flèche.
-   **Désactivé.** Texte gris clair avec pointeur en forme de flèche, parfois sur un arrière-plan gris.

Le texte en lecture seule a généralement un arrière-plan gris, mais un arrière-plan gris n’est pas nécessaire. En fait, un arrière-plan gris peut être indésirable, en particulier pour les grands blocs de texte, car il suggère que le texte est désactivé et découragera la lecture.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Accessibilité et la police, les tailles et les couleurs système

Les directives pour rendre le texte accessible aux utilisateurs souffrant de handicaps ou de troubles peuvent être réduites à une règle simple : respectez les paramètres de l’utilisateur en utilisant toujours la police, les tailles et les couleurs système.

**Si vous n’avez qu’une seule chose...**

Respectez les paramètres de l’utilisateur en utilisant toujours la police, les tailles et les couleurs système.

**Développeurs :** À partir du code, vous pouvez déterminer les propriétés de police système (y compris sa taille) à l’aide de la fonction d’API GetThemeFont. Vous pouvez déterminer les couleurs système à l’aide de la fonction d’API GetThemeSysColor.

Étant donné que vous ne pouvez pas faire d’hypothèses sur les paramètres de thème système des utilisateurs, vous devez :

-   Basez toujours les couleurs de police et les arrière-plans des couleurs de thème du système. Ne créez pas vos propres couleurs en fonction des valeurs RVB (rouge, vert, bleu) fixes.
-   Faire correspondre toujours les couleurs du texte du système avec les couleurs d’arrière-plan correspondantes. Par exemple, si vous choisissez \_ la couleur STATICTEXT pour la couleur du texte, vous devez également choisir couleur \_ statique comme couleur d’arrière-plan.
-   Créez toujours des polices basées sur des variations de taille proportionnelle de la police système. Étant donné les métriques de police système, vous pouvez créer des variations gras, italique, plus grande et plus petites.

**Un moyen simple de s’assurer que votre programme respecte les paramètres des utilisateurs consiste à tester à l’aide d’une taille de police différente et d’un modèle de couleurs à contraste élevé.** Tout le texte doit être redimensionné et s’afficher correctement dans le jeu de couleurs choisi.

## <a name="usage-patterns"></a>Modèles d’usage

Le texte a plusieurs modèles d’utilisation :



|                                                                                                                                                                                                                                                           |                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre de titre Texte**<br/> Texte sur la barre de titre qui identifie la fenêtre.<br/>                                                                                                                                                                | ![exemple de police de texte de la barre de titre ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Instructions principales**<br/> Texte qui explique ce qu’il faut faire sur une page, une fenêtre ou une boîte de dialogue. <br/>                                                                                                                                              | ![exemple de police de texte d’instructions principales ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Instructions secondaires**<br/> Texte supplémentaire qui explique ce qu’il faut faire sur une page, une fenêtre ou une boîte de dialogue. <br/>                                                                                                                            | ![exemple de police de texte d’instructions secondaires ](images/vis-fonts-image4.png)<br/>                                                               |
| **Texte normal**<br/> Texte ordinaire (en lecture seule) affiché dans une interface utilisateur. <br/>                                                                                                                                                           | ![exemple de police de texte normale ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Texte mis en évidence**<br/> Le texte en gras est utilisé pour faciliter l’analyse du texte et attirer l’attention sur le texte que les utilisateurs doivent lire. le texte en italique est utilisé pour faire référence à du texte littéralement (au lieu de guillemets) et pour mettre en évidence des mots spécifiques. <br/> | ![exemple de police de texte en surbrillance ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Texte modifiable**<br/> Le texte que les utilisateurs peuvent modifier est affiché dans une zone. pour réduire le poids de la présentation, la zone peut s’afficher uniquement lorsque le texte modifiable est sélectionné. <br/>                                                          | ![exemple de police de texte modifiable ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Texte désactivé**<br/> Texte qui ne s’applique pas au contexte actuel, par exemple les étiquettes des contrôles désactivés. le texte désactivé indique que les utilisateurs (normalement) ne doivent pas se soucier de la lecture du texte. <br/>                                           | ![exemple de police de texte désactivé ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Liens**<br/> Texte utilisé pour naviguer vers une autre page, fenêtre ou rubrique d’aide, ou pour lancer une commande. <br/>                                                                                                                                     | ![exemple de police de texte de lien ](images/vis-fonts-image9.png)<br/> ![exemple de police de texte de liens (pointage) ](images/vis-fonts-image10.png)<br/> |
| **En-tête de groupe**<br/> Texte utilisé pour regrouper des éléments en mode liste. <br/>                                                                                                                                                                          | ![exemple de police de texte d’en-tête de groupe ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nom de fichier**<br/> Texte du nom de fichier (dans l’affichage du contenu uniquement). <br/>                                                                                                                                                                               | ![exemple de nom de fichier (dans l’affichage du contenu) de la police de texte ](images/vis-fonts-image12.png)<br/>                                                         |
| **Texte du document**<br/> Texte utilisé dans les documents (par opposition au texte de l’interface utilisateur). <br/>                                                                                                                                                                  | ![exemple de police de texte de document ](images/vis-fonts-image13.png)<br/>                                                                            |
| **En-têtes de document**<br/> Texte utilisé comme titre dans un document. <br/>                                                                                                                                                                    | ![exemple de police de texte des en-têtes de document ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Consignes

### <a name="fonts-and-colors"></a>Polices et couleurs

-   **Les polices et couleurs suivantes sont des valeurs par défaut pour Windows Vista et Windows 7.**



|                                                                                               |                             |                                                            |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| **Modèle**<br/>                                                                        | **Symbole du thème**<br/> | **Police, couleur**<br/>                                 |
| ![exemple de police de texte de la barre de titre ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![exemple de police de texte d’instructions principales ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt. bleu ( \# 003399) Segoe UI<br/>                 |
| ![exemple de police de texte d’instructions secondaires ](images/vis-fonts-image4.png)<br/>       | Instruction<br/>      | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![exemple de police de texte normale ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI<br/>                 |
| ![exemple de police de texte en surbrillance ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI, gras ou italique<br/> |
| ![exemple de police de texte modifiable ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 PT. noir ( \# 000000) Segoe UI, dans une zone<br/>       |
| ![exemple de police de texte désactivé ](images/vis-fonts-image8.png)<br/>                     | Désactivé<br/>         | 9 PT. gris foncé ( \# 323232) Segoe UI<br/>             |
| ![exemple de police de texte de lien ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 PT. bleu ( \# 0066CC) Segoe UI<br/>                  |
| ![exemple de police de texte de liens (pointage) ](images/vis-fonts-image10.png)<br/>               | Chaud<br/>              | 9 PT. bleu clair ( \# 3399FF) Segoe UI<br/>            |
| ![exemple de police de texte d’en-tête de groupe ](images/vis-fonts-image11.png)<br/>                |                             | 11 PT bleu ( \# 003399) Segoe UI<br/>                 |
| ![exemple de nom de fichier (dans l’affichage du contenu) de la police de texte ](images/vis-fonts-image12.png)<br/> |                             | 11 PT noir ( \# 000000) Segoe UI<br/>                |
| ![exemple de police de texte de document ](images/vis-fonts-image13.png)<br/>                    | (aucun)<br/>           | 9 PT. noir ( \# 000000) Calibri<br/>                  |
| ![exemple de police de texte des en-têtes de document ](images/vis-fonts-image14.png)<br/>           | (aucun)<br/>           | 17 PT. noir ( \# 000000) Calibri<br/>                 |



 

-   **Choisissez des polices et optimisez les dispositions de fenêtres en fonction de la technologie de l’interface utilisateur et de la version cible de Windows :**



|                                            |                                                       |                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Technologie d’interface utilisateur**<br/>               | **Version de Windows cible**<br/>                 | **Polices à utiliser et optimiser pour**<br/>                                                                                                                                                                                                                                                                                                                     |
| Windows Presentation Foundation<br/> | Tous<br/>                                        | Utilisez des parties de thème WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 ou WinForms<br/>               | Windows Vista ou version ultérieure ;<br/>                     | Utilisez la police de Segoe UI appropriée.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Composants extensibles ou pré-Windows Vista<br/> | Pour cibler Windows XP et Windows 2000, utilisez la Pseudo-police MS Shell Dlg 2 de 8 points, qui est mappée à Tahoma.<br/> Pour cibler des versions antérieures de Windows, utilisez une Pseudo-police MS Shell Dlg de 8 points, qui correspond à Tahoma sur Windows 2000 et Windows XP, et à MS sans serif sur Windows 95, Windows 98, Windows Millennium Edition et Windows NT 4,0.<br/> |



 

-   **Les développeurs**
    -   Pour les éléments qui utilisent une disposition fixe (tels que les modèles de boîte de dialogue Windows et WinForms), codez en dur la police appropriée du tableau précédent.
    -   Pour les éléments qui utilisent une disposition dynamique (par exemple, Windows Presentation Foundation), utilisez les polices de thème. Utilisez des API de thème comme DrawThemeText pour dessiner du texte en fonction du symbole de thème. Veillez à disposer d’une alternative basée sur les mesures système si le service de thème n’est pas en cours d’exécution.
-   **Pour Segoe UI, utilisez une taille de police de 9 points ou plus.** La police Segoe UI est optimisée pour ces tailles. Évitez donc d’utiliser des tailles plus petites.
-   **Faire correspondre toujours les couleurs du texte du système avec les couleurs d’arrière-plan correspondantes.** Par exemple, si vous choisissez \_ la couleur STATICTEXT pour la couleur du texte, vous devez également choisir couleur \_ statique comme couleur d’arrière-plan.
-   **Créez toujours des polices basées sur des variations de taille proportionnelle de la police système.** Étant donné les métriques de police système, vous pouvez créer des variations gras, italique, plus grande et plus petites.
-   Affichez des blocs de grande taille de texte en lecture seule (tels que les termes du contrat de licence) sur un arrière-plan clair plutôt qu’un arrière-plan gris. Les arrière-plans gris suggèrent que le texte est désactivé et décourage la lecture.
-   **Considérez une longueur de ligne maximale de 65 caractères** pour faciliter la lecture du texte. (Les caractères incluent des lettres, des signes de ponctuation et des espaces.)

### <a name="attributes"></a>Attributs

-   La plupart des textes d’interface utilisateur doivent être simples sans attributs. Les attributs peuvent être utilisés comme suit :
    -   **Format.** Utilisez dans les étiquettes de contrôle pour faciliter l’analyse du texte. Utilisez avec modération pour attirer l’attention sur le texte que les utilisateurs doivent lire. L’utilisation d’un trop grand gras réduit son impact.
    -   **Italique.** Utilisez pour faire référence à du texte littéralement plutôt qu’à des guillemets. Utilisez avec modération pour mettre en évidence des mots spécifiques. Utilisez pour les [invites](glossary.md) dans les [zones de texte](ctrl-text-boxes.md) et les [listes déroulantes modifiables](/windows/desktop/uxguide/ctrl-drop).
    -   **Italique gras.** N’utilisez pas.
    -   **Souligner.** N’utilisez pas Except pour les liens. Utilisez Italic à la place pour l’accentuation.
-   Toutes les polices ne prennent pas en charge le gras et l’italique, donc elles ne doivent jamais être cruciales pour comprendre le texte.

