---
title: Contrôles de divulgation progressive
description: Avec un contrôle de la divulgation progressive, les utilisateurs peuvent afficher ou masquer des informations supplémentaires, notamment des données, des options ou des commandes.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1d561ea6e4f937c6e162f9eaa1f452e73d7de20c9f94c41785641062c21cd1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676074"
---
# <a name="progressive-disclosure-controls"></a>Contrôles de divulgation progressive

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un contrôle de la divulgation progressive, les utilisateurs peuvent afficher ou masquer des informations supplémentaires, notamment des données, des options ou des commandes. La divulgation progressive favorise la simplicité en se concentrant sur l’essentiel, tout en révélant des détails supplémentaires en fonction des besoins.

![capture d’écran des contrôles de divulgation progressive](images/progressive-disclosure-controls-image1.png)

Exemples de contrôles de divulgation progressive.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md), aux [menus](cmd-menus.md)et aux [barres d’outils](cmd-toolbars.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les utilisateurs doivent-ils voir les informations dans certains scénarios, mais pas dans tous, ou bien tout le temps ?** Dans ce cas, l’affichage des informations à l’aide de la divulgation progressive simplifie l’expérience de ligne de base, tout en permettant aux utilisateurs d’accéder facilement aux informations.

    ![Capture d’écran montrant l’affichage de l’état de Security Center.](images/progressive-disclosure-controls-image2.png)

    Dans cet exemple, Security Center affiche l’état de sécurité important en permanence, mais utilise la divulgation progressive pour afficher les détails à la demande.

-   **Si les informations sont affichées par défaut, les utilisateurs peuvent-ils choisir de les masquer ?** Existe-t-il des scénarios où les utilisateurs ont besoin de davantage d’espace ? Les utilisateurs sont-ils suffisamment motivés pour personnaliser l’interface utilisateur ? Si ce n’est pas le cas, affichez les informations sans recourir à la divulgation progressive.

    **Incorrect :**

    ![capture d’écran des choix de données affichés par défaut ](images/progressive-disclosure-controls-image3.png)

    Dans cet exemple, les utilisateurs ne seront pas motivés de masquer les informations.

-   **Les informations supplémentaires sont-elles avancées, importantes, complexes ou associées à une sous-tâche indépendante ?** Dans ce cas, envisagez d’afficher les informations dans une fenêtre distincte à l’aide des [boutons de commande](ctrl-command-buttons.md) ou [des liens](ctrl-command-links.md) au lieu d’utiliser un contrôle de divulgation progressif. (Les informations supplémentaires sont avancées si elles sont destinées aux utilisateurs expérimentés. C’est complexe s’il rend d’autres informations difficiles à lire ou à mettre en page.)

    ![capture d’écran de voulez-vous exécuter ce fichier ? ](images/progressive-disclosure-controls-image4.png)

    Dans cet exemple, les informations sur le nom et l’éditeur du logiciel sont significatives pour les utilisateurs expérimentés, de sorte que des liens vers des fenêtres distinctes sont utilisés.

-   **Les informations supplémentaires sont-elles un fragment de phrase ou de phrase qui décrit ce que fait un élément ou comment il peut être utilisé ?** Dans ce cas, envisagez d’utiliser une [info-bulle](ctrl-tooltips-and-infotips.md) ou une info-bulle.
-   **Les informations supplémentaires relatives à la tâche actuelle sont-elles indépendantes des informations actuellement affichées ?** Dans ce cas, envisagez plutôt d’utiliser des [onglets](ctrl-tabs.md) . Toutefois, les listes réductibles sont souvent préférables aux onglets, car elles sont plus flexibles et évolutives.
-   **Les informations supplémentaires sont-elles affichées ou masquées essentiellement par un filtre de données ?** Dans ce cas, envisagez d’utiliser une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) ou des [cases à cocher](ctrl-check-boxes.md) à la place pour appliquer le filtre à la liste entière.

## <a name="design-concepts"></a>Principes de conception

Les objectifs de la divulgation progressive sont les suivants :

-   **Simplifiez une interface utilisateur** en vous concentrant sur l’essentiel, tout en révélant des détails supplémentaires en fonction des besoins.
-   **Simplifiez l’apparence de l’interface utilisateur** en réduisant la perception de l’encombrement.

Les deux objectifs peuvent être atteints à l’aide de contrôles de divulgation progressive, où les utilisateurs cliquent pour afficher plus de détails. Toutefois, vous pouvez obtenir le deuxième objectif de simplifier l’apparence sans utiliser les contrôles de divulgation progressive explicites en :

-   **Présentation du détail contextuel uniquement en contexte.** Par exemple, vous pouvez afficher automatiquement des commandes ou des barres d’outils contextuelles lorsqu’elles sont pertinentes pour l’objet ou le mode sélectionné.
-   **Réduction du poids de intuitivité pour l’interface utilisateur secondaire.** [Intuitivité](glossary.md) sont des propriétés visuelles qui suggèrent la manière dont les objets sont utilisés. La tendance est d’avoir une interface utilisateur avec laquelle les utilisateurs peuvent interagir en place, mais pour que toute l’interface utilisateur soit dessinée sur SVP « cliquez me ! » provoque un trop grand encombrement visuel. Pour l’interface utilisateur secondaire, il est souvent préférable d’utiliser des intuitivité subtiles et d’obtenir des effets complets sur la souris.

    ![capture d’écran des icônes d’étoile utilisées pour noter les photos ](images/progressive-disclosure-controls-image5.png)

    Dans cet exemple, le champ d’évaluation est interactif, mais ne s’affiche pas jusqu’au pointage de la souris.

-   **L’indication des étapes de suivi uniquement une fois les conditions préalables terminées.** Cette approche est idéale pour les tâches familières dans lesquelles les utilisateurs peuvent prendre en confiance les premières étapes.

    ![capture d’écran des zones de texte nom d’utilisateur et mot de passe ](images/progressive-disclosure-controls-image6.png)

    Dans cet exemple, la page nom d’utilisateur et mot de passe affiche initialement uniquement les zones nom d’utilisateur et mot de passe facultatif. Les zones confirmation et Hint s’affichent une fois que l’utilisateur a entré un mot de passe.

Alors que la divulgation progressive est un excellent moyen de simplifier les interfaces utilisateur, elle présente les risques suivants :

-   **Manque de détectabilité.** Les utilisateurs peuvent supposer que s’ils ne peuvent pas voir un événement, il n’existe pas. Les utilisateurs peuvent ne pas pointer ou cliquer s’ils ne voient pas ce qu’ils recherchent. Il y a toujours un risque que les utilisateurs ne cliquent pas sur des éléments comme d’autres options.
-   **Manque de stabilité.** La divulgation progressive doit être attendue ou au moins sembler naturelle. Si les contrôles apparaissent et disparaissent de manière inattendue, l’interface utilisateur résultante peut paraître instable.

### <a name="progressive-disclosure-controls"></a>Contrôles de divulgation progressive

Les contrôles de divulgation progressive sont généralement affichés sans étiquettes directes qui décrivent leur comportement. les utilisateurs doivent donc être en mesure d’effectuer les opérations suivantes en fonction de l’apparence visuelle du contrôle uniquement :

-   Reconnaît que le contrôle fournit une divulgation progressive.
-   Détermine si l’état actuel est développé ou réduit.
-   Déterminez si des informations, des options ou des commandes supplémentaires sont nécessaires pour effectuer la tâche.
-   Déterminez le mode de restauration de l’état d’origine, si vous le souhaitez.

Alors que les utilisateurs peuvent déterminer les éléments ci-dessus par essai et par erreur, vous devez essayer de rendre cette expérimentation inutile.

Les contrôles de divulgation progressive ont un [intuitivité](glossary.md)relativement faible, ce qui signifie que leurs propriétés visuelles suggèrent la manière dont elles sont utilisées, bien que faiblement. Le tableau suivant compare l’apparence des contrôles de divulgation progressive courants :



| Contrôler | Objectif  | Apparence | Glyphe indique |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Chevrons**<br/> ![capture d’écran des chevrons gauche/droit et haut/flèche vers le haut ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Afficher tout :** Affichez ou masquez les éléments restants dans le contenu entièrement ou partiellement masqué. Les éléments sont affichés sur place (à l’aide d’un chevron simple) ou dans un menu contextuel (à l’aide d’un double Chevron).<br/> | Les chevrons pointent dans la direction dans laquelle l’action aura lieu.<br/>                                                        | État futur<br/>        |
| **Flèches**<br/> ![capture d’écran des flèches gauche/droite et haut/bas ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Afficher les options :** Affichez un menu contextuel.<br/>                                                                                                                                                    | Les flèches pointent dans la direction dans laquelle l’action doit se produire.<br/>                                                          | État futur<br/>        |
| **Contrôles plus et moins**<br/> ![capture d’écran de deux petits boutons plus et moins ](images/progressive-disclosure-controls-image9.png)<br/> | **Développer les conteneurs :** Développez ou réduisez le contenu du conteneur en place lors de la navigation dans une hiérarchie.<br/>                                                                                        | Les symboles plus et moins ne pointent pas, mais l’action se produit toujours à droite.<br/>                                    | État futur<br/>        |
| **Triangles rotatifs**<br/> ![capture d’écran de deux petits triangles ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Afficher les détails :** Affichez ou masquez des informations supplémentaires sur place pour un élément individuel. Ils sont également utilisés pour développer des conteneurs.<br/>                                                                  | Les triangles rotatifs ressemblent à des leviers rotatifs, donc ils pointent dans la direction où l’action s’est produite.<br/> | État présent<br/>       |



 

**Si vous n’avez qu’une seule chose...**

Les utilisateurs doivent être en mesure de prédire le comportement d’un contrôle de divulgation progressif correctement par inspection seule. Pour ce faire, sélectionnez les modèles d’utilisation appropriés et appliquez l’apparence, l’emplacement et le comportement de manière cohérente.

## <a name="usage-patterns"></a>Modèles d’usage

Les contrôles de divulgation progressive ont plusieurs modèles d’utilisation. Certaines d’entre elles sont intégrées à des contrôles communs.

### <a name="chevrons"></a>Chevrons

Les chevrons affichent ou masquent les éléments restants dans le contenu entièrement ou partiellement masqué. En général, les éléments sont affichés en place, mais ils peuvent également être affichés dans un menu contextuel. Lorsqu’il est en place, l’élément reste développé jusqu’à ce que l’utilisateur le réduit.

Les chevrons sont utilisés des manières suivantes :



|      Usage                                                                                                                                                          |    Exemple                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interface utilisateur sur place**<br/> l’objet associé reçoit le focus d’entrée et le Chevron simple est activé à l’aide de la barre d’espace.<br/>                       | ![capture d’écran de l’affichage de l’état de Security Center ](images/progressive-disclosure-controls-image11.png)<br/> Dans ces exemples, les chevrons simples sur place sont positionnés à droite de leur contrôle associé.<br/>                                                                            |
| **Boutons de commande avec des étiquettes externes**<br/> le bouton de commande reçoit le focus d’entrée et le Chevron simple est activé à l’aide de la barre d’espace.<br/> | ![capture d’écran des chevrons avec l’étiquette « More options » ](images/progressive-disclosure-controls-image12.png)<br/> Dans cet exemple, le bouton de Chevron simple est étiqueté et positionné à gauche de l’étiquette. Avec ce modèle, il serait difficile de comprendre le bouton sans son étiquette.<br/> |
| **Boutons de commande avec étiquettes internes**<br/> le bouton de commande reçoit le focus d’entrée et est activé à l’aide de la barre d’espace.<br/>                    | ![capture d’écran des boutons de commande « plus » et « moins » ](images/progressive-disclosure-controls-image13.png)<br/> Dans ces exemples, les boutons de commande normaux ont un double Chevron positionné pour suggérer leur signification.<br/>                                                                          |



 

### <a name="arrows"></a>Flèches

Les flèches affichent un menu contextuel. L’élément reste développé jusqu’à ce que l’utilisateur effectue une sélection ou clique n’importe où.

Si le bouton fléché est un contrôle indépendant, il reçoit le focus d’entrée et est activé à l’aide de la barre d’espace. Si le bouton fléché a un contrôle parent, le parent reçoit le focus d’entrée et la flèche est activée avec les touches Alt + flèche bas et Alt + haut, comme avec le contrôle de liste déroulante.

Les flèches sont utilisées des manières suivantes :



|    Usage                                                                                   |    Exemple                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Boutons distincts**<br/> la flèche se trouve dans un contrôle bouton distinct.<br/> | ![capture d’écran des flèches à droite des contrôles ](images/progressive-disclosure-controls-image14.png)<br/> Dans ces exemples, des boutons de direction distincts positionnés à droite indiquent un menu de commande.<br/>               |
| **Boutons de commande**<br/> la flèche fait partie d’un bouton de commande.<br/>      | ![capture d’écran de l’étiquette et de la flèche sur le bouton de commande ](images/progressive-disclosure-controls-image15.png)<br/> Dans ces exemples, les boutons de menu et les boutons partagés ont les flèches positionnées à droite du texte.<br/> |



 

### <a name="plus-and-minus-controls"></a>Contrôles plus et moins

Les contrôles plus et moins sont développés ou réduits pour afficher le contenu du conteneur lors de la navigation dans une hiérarchie. L’élément reste développé jusqu’à ce que l’utilisateur le réduit. Bien qu’elles ressemblent à des boutons, leur comportement est sur place.

L’objet associé reçoit le focus d’entrée. Le signe plus est activé avec la touche de direction droite et le signe moins avec la touche de direction gauche.

Les contrôles plus et moins sont utilisés des manières suivantes :



|       Usage                                                                                         |       Exemple                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Arborescences réductibles**<br/> hiérarchie à plusieurs niveaux pour afficher le contenu d’un conteneur.<br/> | ![capture d’écran montrant une arborescence de dossiers Windows Explorer avec « Behavior » sélectionné.](images/progressive-disclosure-controls-image16.png)<br/> Dans cet exemple, les contrôles plus et moins sont positionnés à gauche du conteneur associé.<br/>       |
| **Listes réductibles**<br/> hiérarchie à deux niveaux pour afficher le contenu du conteneur.<br/>   | ![capture d’écran de la liste développée pour afficher deux niveaux ](images/progressive-disclosure-controls-image17.png)<br/> Dans cet exemple, les contrôles plus et moins sont positionnés à gauche de l’en-tête de liste associé.<br/> |



 

### <a name="rotating-triangles"></a>Triangles rotatifs

Les triangles rotatifs affichent ou masquent des informations supplémentaires sur place pour un élément individuel. Ils sont également utilisés pour développer des conteneurs. L’élément reste développé jusqu’à ce que l’utilisateur le réduit.

L’objet associé reçoit le focus d’entrée. Le triangle réduit (pointant vers la droite) est activé à l’aide de la touche de direction droite et du triangle développé (pointant vers le bas) avec la touche de direction gauche.

Les triangles rotatifs sont utilisés des manières suivantes :



|     Usage                                                                                                       |    Exemple                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Arborescences réductibles**<br/> hiérarchie à plusieurs niveaux pour afficher le contenu d’un conteneur.<br/>             | ![capture d’écran de l’arborescence des dossiers de l’Explorateur Windows ](images/progressive-disclosure-controls-image18.png)<br/> Dans cet exemple, les triangles pivotés sont positionnés à gauche du conteneur associé.<br/>       |
| **Listes réductibles**<br/> hiérarchie à deux niveaux pour afficher des informations supplémentaires.<br/> | ![capture d’écran de la liste affichant des données supplémentaires ](images/progressive-disclosure-controls-image19.png)<br/> Dans cet exemple, les triangles pivotés sont positionnés à gauche de leurs éléments de liste associés.<br/> |



 

### <a name="preview-arrows"></a>Flèches d’aperçu

À l’instar des chevrons, des informations supplémentaires sont affichées ou masquées sur place. L’élément reste développé jusqu’à ce que l’utilisateur le réduit. Contrairement aux chevrons, les glyphes ont une représentation graphique de l’action, généralement avec une flèche indiquant ce qui se produit.

![capture d’écran des glyphes de flèche pointant en diagonale ](images/progressive-disclosure-controls-image20.png)

dans ces exemples de Microsoft Lecteur Windows Media, les glyphes ont des flèches qui suggèrent l’action qui se produira.

Les flèches d’aperçu sont réservées aux situations où un chevron standard ne communique pas correctement le comportement du contrôle, par exemple lorsque la divulgation est complexe ou qu’il existe plusieurs types de divulgation.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Sélectionnez le modèle de divulgation progressive en fonction de son utilisation.** Pour obtenir une description de chaque modèle d’utilisation, consultez le tableau précédent.
-   **N’utilisez pas de liens pour les contrôles de divulgation progressive.** Utilisez uniquement les contrôles de divulgation progressive présentés dans la section modèles d’utilisation. Toutefois, utilisez des liens pour accéder aux [rubriques d’aide](winenv-help.md).

    **Correct :**

    ![capture d’écran des chevrons avec l’étiquette « Show mixer » ](images/progressive-disclosure-controls-image21.png)

    **Incorrect :**

    ![capture d’écran du texte du lien « Afficher le mixer » ](images/progressive-disclosure-controls-image22.png)

    Dans l’exemple incorrect, un lien est utilisé pour afficher davantage d’options. Cette utilisation est correcte si le lien a accédé à une autre page ou boîte de dialogue ou qu’une rubrique d’aide est affichée.

### <a name="interaction"></a>Interaction

-   **Pour les chevrons et les flèches qui ne sont pas directement étiquetés, utilisez les info-bulles pour décrire ce qu’ils font.**

    ![capture d’écran de l’info-bulle « développer le générateur de requêtes » ](images/progressive-disclosure-controls-image23.png)

    Dans cet exemple, l’info-bulle indique l’effet d’un contrôle Chevron sans étiquette.

-   **Si un utilisateur développe ou réduit un élément, rendez l’état persistant afin qu’il prenne effet la prochaine fois que la fenêtre est affichée**, à moins que les utilisateurs soient susceptibles de commencer à utiliser l’État par défaut. Rendez l’état persistant en fonction de la fenêtre, par utilisateur.
-   **Assurez-vous que tous les contenus développés peuvent être réduits, et vice versa, et que l’opération inverse est évidente.** Cela favorise l’exploration et réduit la frustration. La meilleure façon de rendre l’opération inverse évidente consiste à conserver le contrôle dans le même emplacement fixe. Si vous devez déplacer le contrôle, conservez-le dans le même emplacement relatif dans une zone visuellement distincte.

    **Incorrect :**

    ![capture d’écran du bouton’replace’avec Chevron ](images/progressive-disclosure-controls-image24.png)

    ![capture d’écran du bouton’replace’sans Chevron ](images/progressive-disclosure-controls-image25.png)

    Dans cet exemple, le fait de cliquer sur le bouton remplacer par le Chevron révèle la zone de texte **remplacer par** . Une fois cette opération effectuée, l’Expander de remplacement devient la commande Replace. il n’existe donc aucun moyen de restaurer l’état d’origine.

-   **Utilisez uniquement les clés d’accès appropriées pour le modèle de divulgation progressive**, comme indiqué dans la section modèles d’utilisation. N’utilisez pas entrée pour activer la divulgation progressive.

### <a name="presentation"></a>Présentation

-   **N’utilisez pas de flèches triangulaires à des fins autres que la divulgation progressive.**

    **Incorrect :**

    ![capture d’écran de l’étiquette avec le triangle pointant vers la droite ](images/progressive-disclosure-controls-image26.png)

    Même si cet exemple n’est pas un modèle de divulgation progressive, l’utilisation d’une flèche suggère que les commandes s’affichent dans une fenêtre contextuelle.

    **Correct :**

    ![capture d’écran de l’étiquette avec la puce à gauche du texte ](images/progressive-disclosure-controls-image27.png)

    Dans cet exemple, une puce est correctement utilisée à la place.

-   **Supprimez (ne désactivez pas) les contrôles de divulgation progressive qui ne s’appliquent pas au contexte actuel.** Les contrôles de divulgation progressive doivent toujours remettre leur promesse. Supprimez-les lorsqu’il n’y a pas d’informations à fournir.

    **Incorrect :**

    ![capture d’écran d’un contrôle « More options » grisé ](images/progressive-disclosure-controls-image28.png)

    Dans cet exemple, un contrôle de divulgation progressif qui ne s’applique pas est désactivé de manière incorrecte.

### <a name="chevrons"></a>Chevrons

-   **Utilisez des chevrons simples pour afficher ou masquer sur place. Utilisez des guillemets doubles pour afficher ou masquer à l’aide d’un menu contextuel.** Toutefois, vous devez toujours utiliser des guillemets doubles pour les boutons de commande avec des étiquettes internes.

    **Correct :**

    ![capture d’écran de contrôle d’options supplémentaires à un chevron ](images/progressive-disclosure-controls-image29.png)

    **Incorrect :**

    ![capture d’écran du contrôle d’options supplémentaires à deux chevrons ](images/progressive-disclosure-controls-image30.png)

    Dans l’exemple incorrect, un double Chevron est utilisé pour la divulgation progressive sur place.

    **Correct :**

    ![capture d’écran d’un double Chevron-bouton de commande ](images/progressive-disclosure-controls-image31.png)

    Dans cet exemple, un double Chevron est utilisé pour la divulgation progressive sur place, car il s’agit d’un bouton de commande avec une étiquette interne.

-   **Fournissez une relation visuelle entre le Chevron et son contrôle associé.** Étant donné que les chevrons sur place sont placés à droite de leur interface utilisateur associée et alignés à droite, il peut y avoir une distance entre un chevron et son contrôle associé.

    **Correct :**

    ![capture d’écran des contrôles d’ombrage dégradés en arrière-plan ](images/progressive-disclosure-controls-image32.png)

    Dans cet exemple, il existe une relation claire entre le Chevron sur place et l’interface utilisateur associée.

    **Incorrect :**

    ![capture d’écran de l’arrière-plan blanc Uni pour les contrôles ](images/progressive-disclosure-controls-image33.png)

    Dans cet exemple, il n’existe aucune relation visuelle claire entre le Chevron sur place et l’interface utilisateur associée. il semble donc être flottant dans l’espace.

### <a name="arrows"></a>Flèches

-   **N’utilisez pas de graphiques fléchés qui peuvent être confondus avec les touches précédent, suivant, aller ou lire.** Utilisez des flèches triangulaires simples (flèches sans tiges) sur les arrière-plans neutres.

    **Correct :**

    ![capture d’écran de deux petits triangles noirs ](images/progressive-disclosure-controls-image34.png)

    Ces flèches sont clairement des contrôles de divulgation progressive.

    **Incorrect (pour la divulgation progressive) :**

    ![capture d’écran de deux petites flèches vertes ](images/progressive-disclosure-controls-image35.png)

    Ces flèches ne sont pas similaires aux contrôles de divulgation progressive.

    **Incorrect (pour précédent, suivant) :**

    ![capture d’écran de deux boutons avec des triangles noirs ](images/progressive-disclosure-controls-image36.png)

    Ces flèches ressemblent à des contrôles de divulgation progressive, mais pas.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran du dimensionnement et de l’espacement recommandés ](images/progressive-disclosure-controls-image37.png)

Dimensionnement et espacement recommandés pour les contrôles de divulgation progressive.

## <a name="labels"></a>Étiquettes

-   Pour les chevrons sur un bouton de commande avec une étiquette externe :
    -   Attribuez une [clé d’accès](glossary.md)unique. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
    -   Utilisez la mise [en majuscules de style phrase](glossary.md).
    -   Écrivez l’étiquette en tant qu’expression et n’utilisez pas de ponctuation finale.
    -   Écrivez l’étiquette pour qu’elle décrive l’effet d’un clic sur le bouton, et modifiez l’étiquette lorsque l’état change.
    -   Si la surface affiche toujours des options, des commandes ou des détails, utilisez les paires d’étiquettes suivantes :
        -   **Plus ou moins d’options.** Utilisez pour les options ou un mélange d’options, de commandes et de détails.
        -   **Plus ou moins de commandes.** Utilisez uniquement pour les commandes.
        -   **Plus ou moins de détails.** À utiliser pour plus d’informations uniquement.
        -   **Plus ou moins <object name> .** Utilisez pour d’autres types d’objets, tels que les dossiers.
    -   Sinon :
        -   **Options d’affichage/de masquage.** Utilisez pour les options ou un mélange d’options, de commandes et de détails.
        -   **Afficher/masquer les commandes.** Utilisez uniquement pour les commandes.
        -   **Afficher/masquer les détails.** À utiliser pour plus d’informations uniquement.
        -   **Afficher/masquer <object name> .** Utilisez pour d’autres types d’objets, tels que les dossiers.
-   Pour les chevrons sur un bouton de commande avec une étiquette interne, suivez les instructions du [bouton de commande](ctrl-command-buttons.md) standard.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des contrôles de divulgation progressive :

-   Si le contrôle a une étiquette fixe, reportez-vous au contrôle uniquement par son étiquette. n’essayez pas de décrire le contrôle. Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement de clé d’accès.
-   Si le contrôle n’a pas d’étiquette ou qu’il n’est pas fixe, reportez-vous au contrôle par son type : Chevron, flèche, triangle ou bouton plus/moins. Si nécessaire, décrivez également l’emplacement du contrôle. Si le contrôle s’affiche dynamiquement, tel que le contrôle d' [espace de page](glossary.md) , démarrez la référence en décrivant comment faire apparaître le contrôle.

    **Exemple :** Pour afficher les fichiers dans un dossier, déplacez le pointeur vers le début du nom de dossier, puis cliquez sur le triangle en regard du dossier.

-   Ne faites pas référence au contrôle en tant que bouton, sauf en cas de différence avec d’autres contrôles de divulgation progressive qui ne sont pas des boutons.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic. Si nécessaire pour plus de clarté, utilisez cliquer sur... pour développer ou réduire.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemples :

-   (Pour un chevron) Pour déterminer la taille du fichier, cliquez sur **Détails**.
-   (Pour une flèche) Pour afficher toutes les options, cliquez sur la flèche en regard de la zone de **recherche** .
-   (Pour plus/moins) Pour afficher votre image, cliquez sur **images**.

