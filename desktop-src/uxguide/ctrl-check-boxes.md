---
title: Cases à cocher
description: Avec une case à cocher, les utilisateurs font une décision entre deux choix manifestement opposés.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29666991d0a0659f7ff3a95f12953504b70c6dc782049ac8d93d70df73afa5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040610"
---
# <a name="check-boxes"></a>Cases à cocher

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une case à cocher, les utilisateurs font une décision entre deux choix manifestement opposés. L’étiquette de case à cocher indique l’état sélectionné, alors que la signification de l’État effacé doit être l’opposé non ambigu de l’état sélectionné. Par conséquent, les **cases à cocher doivent être utilisées uniquement pour activer ou désactiver une option ou pour sélectionner ou désélectionner un élément.**

![capture d’écran de l’une des quatre cases à cocher sélectionnées ](images/ctrl-check-boxes-image1.png)

Groupe typique de cases à cocher.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **La case à cocher est-elle utilisée pour activer ou désactiver une option ou pour sélectionner ou désélectionner un élément ?** Si ce n’est pas le cas, utilisez un autre contrôle.
-   **Les États sélectionnés et désactivés sont-ils clairs et non ambigus ?** Si ce n’est pas le cas, utilisez des [cases d’option](ctrl-radio-buttons.md) ou une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) afin de pouvoir étiqueter les États indépendamment.
-   **Lorsqu’il est utilisé dans un groupe, le groupe inclut-il des choix indépendants, à partir desquels les utilisateurs peuvent choisir zéro ou plus ?** Si ce n’est pas le cas, envisagez des contrôles pour les choix dépendants, tels que les cases d’option et les [arborescences](ctrl-tree-views.md)de cases.
-   **Lorsqu’il est utilisé dans un groupe, le groupe couvre-t-il les choix dépendants, à partir desquels les utilisateurs doivent choisir un ou plusieurs ?** Dans ce cas, utilisez un groupe de cases à cocher et gérez l’erreur quand aucune des options n’est sélectionnée.
-   **Le nombre d’options dans un groupe est-il inférieur ou égale à 10 ?** Étant donné que l’espace à l’écran utilisé est proportionnel au nombre d’options, conservez le nombre de cases à cocher à 10 ou moins. Pour plus de 10 options, utilisez une [liste de cases à cocher](ctrl-list-boxes.md).
-   **Une case d’option sera-t-elle un meilleur choix ?** Lorsque les cases à cocher conviennent uniquement à l’activation ou à la désactivation d’une option, les cases d’option peuvent être utilisées pour des options complètement différentes. Si les deux solutions sont possibles :
    -   Utilisez les cases d’option si la signification de la case à cocher désactivée n’est pas complètement évidente.

        **Incorrect :**

        ![capture d’écran d’une case à cocher paysage ](images/ctrl-check-boxes-image2.png)

        Dans cet exemple, le choix opposé du paysage n’est pas évident, donc la case à cocher n’est pas un bon choix.

        **Correct :**

        ![capture d’écran de deux cases d’option ](images/ctrl-check-boxes-image3.png)

        Dans cet exemple, les choix ne sont pas opposés afin que les cases d’option soient le meilleur choix.

    -   Utilisez les cases d’option des pages de l’Assistant pour désactiver les alternatives, même si une case à cocher est acceptable.
    -   Utilisez les cases d’option si vous avez suffisamment d’espace à l’écran et si les options sont suffisamment importantes pour constituer une bonne utilisation de cet espace d’écran. Dans le cas contraire, utilisez une case à cocher ou une liste déroulante.

        **Incorrect :**

        ![capture d’écran des boutons afficher et ne pas afficher le ratio ](images/ctrl-check-boxes-image4.png)

        Dans cet exemple, les options ne sont pas assez importantes pour utiliser des cases d’option.

        **Correct :**

        ![capture d’écran de la case à cocher sans afficher le message ](images/ctrl-check-boxes-image5.png)

        Dans cet exemple, une case à cocher est une utilisation efficace de l’espace à l’écran pour cette option de périphérique.

-   Utilisez une case à cocher s’il y a d’autres cases à cocher dans la fenêtre.
-   **L’option présente-t-elle une option de programme plutôt que des données ?** Les valeurs de l’option ne doivent pas être basées sur le contexte ou d’autres données. Pour les données, utilisez une liste de cases à cocher ou une [liste à sélection multiple](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Modèles d’usage

Les cases à cocher ont plusieurs modèles d’utilisation :



|    Usage                                                                          |         Exemple                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Un choix individuel** Une case à cocher unique est utilisée pour sélectionner un choix individuel. <br/>                                                                                                             | ![capture d’écran d’une case à cocher avec l’étiquette me le rappeler ](images/ctrl-check-boxes-image6.png)<br/> Une case à cocher unique est utilisée pour un choix individuel.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Choix indépendants (zéro, un ou plusieurs éléments)** Un groupe de cases à cocher est utilisé pour effectuer une sélection dans un ensemble de zéro ou plusieurs choix.<br/>                                                                              | Contrairement aux contrôles à sélection unique tels que les cases d' [option](ctrl-radio-buttons.md), les utilisateurs peuvent sélectionner n’importe quelle combinaison d’options dans un groupe de cases à cocher.<br/> ![capture d’écran de deux des trois cases à cocher sélectionnées ](images/ctrl-check-boxes-image7.png)<br/> Un groupe de cases à cocher est utilisé pour des choix indépendants.<br/>                                                                                                                                                  |
| **Choix dépendants (un ou plusieurs)** Un groupe de cases à cocher peut également être utilisé pour effectuer une sélection dans un ensemble d’un ou de plusieurs choix.<br/>                                                                         | **vous devrez peut-être représenter une sélection d’un ou de plusieurs choix dépendants**. étant donné que Microsoft ? Windows n’a pas de contrôle qui prend directement en charge ce type d’entrée, la meilleure solution consiste à utiliser un groupe de cases à cocher et à gérer l’erreur quand aucune des options n’est sélectionnée.<br/> ![capture d’écran de l’une des deux cases à cocher sélectionnées ](images/ctrl-check-boxes-image8.png)<br/> Un groupe de cases à cocher est utilisé lorsqu’au moins un protocole doit être sélectionné.<br/> |
| **Choix mixte** En plus des États sélectionnés et désactivés, les cases à cocher ont également un État mixte pour la sélection multiple pour indiquer que l’option est définie pour certains objets, mais pas tous.<br/> | ![capture d’écran d’une case à cocher en lecture seule bleue unie ](images/ctrl-check-boxes-image9.png)<br/> Case à cocher à état mixte.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Cases à cocher associées au groupe**. Combinez les options associées et séparez les options non liées en groupes de 10 ou moins, en utilisant plusieurs groupes si nécessaire.

    ![capture d’écran des cases à cocher associées et non associées ](images/ctrl-check-boxes-image10.png)

    Exemple de groupes d’options connexes indépendantes.

-   **Reconsidérez l’utilisation des zones de groupe pour organiser des groupes de cases à cocher** , ce qui entraîne souvent un encombrement inutile de l’écran.
-   **Répertoriez les cases à cocher dans un ordre logique**, telles que le regroupement d’options très associées ou le placement des options les plus courantes, ou la suite d’une autre progression naturelle. L’ordre alphabétique n’est pas recommandé, car il dépend de la langue et n’est donc pas localisable.
-   **Aligner les cases à cocher verticalement, et non horizontalement**. L’alignement horizontal est plus difficile à lire.

    **Correct :**

    ![capture d’écran des cases à cocher alignées verticalement ](images/ctrl-check-boxes-image11.png)

    Dans cet exemple, les cases à cocher sont correctement alignées.

    **Incorrect :**

    ![capture d’écran des cases à cocher alignées horizontalement ](images/ctrl-check-boxes-image12.png)

    Dans cet exemple, l’alignement horizontal est plus difficile à lire.

-   **N’utilisez pas l’État mixte pour représenter un troisième État.** L’État mixte est utilisé pour indiquer qu’une option est définie pour certains objets enfants, mais pas tous. Les utilisateurs ne doivent pas être en mesure de définir un État mixte directement, plutôt que l’État mixte est une réflexion des objets enfants. L’État mixte n’est pas utilisé comme troisième État pour un élément individuel. Pour représenter un troisième État, utilisez à la place des cases d’option ou une liste déroulante.

    **Incorrect :**

    ![capture d’écran de la case à cocher service de thème bleu fixe ](images/ctrl-check-boxes-image13.png)

    Dans cet exemple, l’État mixte est supposé indiquer que le service de thème n’est pas installé.

    **Correct :**

    ![capture d’écran de la liste déroulante avec trois options ](images/ctrl-check-boxes-image14.png)

    Dans cet exemple, les utilisateurs peuvent choisir parmi une liste de trois options claires.

-   **Si vous cliquez sur une case à cocher État mixte, vous devez parcourir tous les États mixtes sélectionnés, tous désactivés et d’origine.** Pour la récupération, il est important de pouvoir restaurer l’État mixte d’origine, car les paramètres peuvent être complexes ou inconnus de l’utilisateur. Dans le cas contraire, la seule manière de restaurer l’État mixte en toute confiance serait d’annuler la tâche et de recommencer.
-   **N’utilisez pas de cases à cocher comme indicateur de progression**. Utilisez un contrôle [indicateur de progression](progress-bars.md) à la place.

    **Incorrect :**

    ![capture d’écran de quatre cases à cocher montrant la progression ](images/ctrl-check-boxes-image15.png)

    Dans cet exemple, les cases à cocher sont utilisées de manière incorrecte en tant qu’indicateur de progression.

    **Correct :**

    ![capture d’écran d’une barre de progression partiellement remplie ](images/ctrl-check-boxes-image16.png)

    Exemple d’une barre de progression classique.

-   **Affiche les cases à cocher désactivées à l’aide de l’état de sélection approprié.** Même si les utilisateurs ne peuvent pas les modifier, les cases à cocher désactivées fournissent des informations pour qu’elles soient cohérentes avec les résultats.

    **Incorrect :**

    ![capture d’écran de l’une des deux cases à cocher grisée ](images/ctrl-check-boxes-image17.png)

    Dans cet exemple, l’option « toujours lire cette section à haute voix » doit être désactivée, car la section n’est pas lue lorsque l’option est désactivée.

-   **N’utilisez pas la sélection d’une case à cocher pour**:
    -   Exécuter des commandes.
    -   Affichez d’autres fenêtres, telles qu’une boîte de dialogue pour recueillir davantage d’entrées.
    -   Afficher dynamiquement d’autres contrôles en rapport avec le contrôle sélectionné (les lecteurs d’écran ne peuvent pas détecter de tels événements).

### <a name="dont-show-this-item-again"></a>Ne pas afficher <item> connecter

-   **Envisagez d’utiliser l' <item> option ne plus afficher cette option pour permettre aux utilisateurs de supprimer une boîte de dialogue périodique uniquement s’il n’existe pas d’autre solution.** Essayez de déterminer à l’avance si les utilisateurs ont vraiment besoin de la boîte de dialogue ; Si c’est le cas, affiche toujours la boîte de dialogue et, si ce n’est pas le cas, élimine la boîte de dialogue.

Pour obtenir des instructions et des exemples supplémentaires, consultez [boîtes de dialogue](win-dialog-box.md).

### <a name="subordinate-controls"></a>Contrôles subordonnés

-   Placez les contrôles subordonnés à droite ou en dessous (en retrait, en vidant avec l’étiquette de case à cocher) de la case à cocher et de son étiquette. Mettez fin à l’étiquette de la case à cocher avec un signe deux-points.

    ![capture d’écran de la zone de texte sous l’étiquette de case à cocher ](images/ctrl-check-boxes-image18.png)

    Dans cet exemple, la case à cocher et son contrôle subordonné partagent l’étiquette de case à cocher et sa clé d’accès.

-   **Laissez les zones de texte modifiables dépendantes et les listes déroulantes activées si elles partagent l’étiquette de la case à cocher.** Lorsque les utilisateurs tapent ou collent quoi que ce soit dans la zone, sélectionnez automatiquement l’option correspondante. Cela simplifie l’interaction.

    ![capture d’écran des zones de texte d’en-tête et de pied de page ](images/ctrl-check-boxes-image19.png)

    Dans cet exemple, l’entrée d’un en-tête ou d’un pied de page sélectionne automatiquement l’option.

-   Si vous imbriquez des cases à cocher avec des cases d’option ou d’autres cases à cocher, **désactivez ces contrôles subordonnés jusqu’à ce que l’option de haut niveau soit sélectionnée**. Cela évite toute confusion quant à la signification des contrôles subordonnés.
-   Rendez les contrôles subordonnés à une case à cocher contiguë à la case à cocher dans l’ordre de tabulation.
-   **Si la sélection d’une option implique la sélection de cases à cocher subordonnées, activez explicitement ces cases à cocher pour que la relation soit claire.**

    **Incorrect :**

    ![capture d’écran : bouton sélectionné, cases à cocher désactivées ](images/ctrl-check-boxes-image20.png)

    Dans cet exemple, les cases à cocher subordonnées ne sont pas sélectionnées.

    **Correct :**

    ![capture d’écran : bouton sélectionné, cases à cocher sélectionnées ](images/ctrl-check-boxes-image21.png)

    Dans cet exemple, les cases à cocher subordonnées sont activées, ce qui rend leur relation avec l’option sélectionnée désactivée.

-   **Utilisez les cases à cocher dépendantes si les alternatives ajoutent une complexité inutile**. Les cases à cocher doivent être des options indépendantes, parfois des alternatives telles que les cases d’option ajoutent une complexité inutile.

    **Correct :**

    ![capture d’écran des boutons déroutants et des cases à cocher ](images/ctrl-check-boxes-image22.png)

    Dans cet exemple, l’utilisation de cases d’option est exacte, mais crée une complexité inutile.

    **Conseillé**

    ![capture d’écran des cases à cocher uniquement ](images/ctrl-check-boxes-image23.png)

    Dans cet exemple, l’utilisation de cases à cocher est plus simple et permet aux utilisateurs de se concentrer sur la sélection des options souhaitées plutôt que sur leur relation complexe.

    **Important : appliquez cette instruction uniquement dans des circonstances très rares**, lorsque l’indication des dépendances ajoute une complexité significative sans augmenter la clarté. Dans l’exemple précédent, il est peu probable que les utilisateurs essaient de choisir l’exposant et l’indice, et si c’est le cas, il serait facile de comprendre qu’ils étaient des options exclusives.

### <a name="default-values"></a>Valeurs par défaut

-   Si une case à cocher est pour une option utilisateur, **définissez la plus sûre (pour empêcher la perte de données ou l’accès au système), la plus sécurisée et l’État privé par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la valeur la plus probable ou la plus pratique.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![figure du dimensionnement et de l’espacement suggérés des cases à cocher ](images/ctrl-check-boxes-image24.png)

Dimensionnement et espacement recommandés pour les cases à cocher.

## <a name="labels"></a>Étiquettes

**Étiquettes de case à cocher**

-   Étiquette chaque case à cocher.
-   Attribuez une [clé d’accès](glossary.md) unique à chaque étiquette. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Écrivez l’étiquette en tant qu’expression ou phrase impérative et n’utilisez pas de ponctuation finale.
    -   **Exception :** Si une étiquette de case à cocher étiquette également un contrôle subordonné qui la suit, terminez l’étiquette par un signe deux-points.
-   Écrivez l’étiquette pour qu’elle décrive l’état sélectionné de la case à cocher.
-   Pour un groupe de cases à cocher, utilisez une formulation parallèle et essayez de conserver la même longueur pour toutes les étiquettes.
-   Pour un groupe de cases à cocher, concentrez le texte de l’étiquette sur les différences entre les options. Si toutes les options ont le même texte d’introduction, déplacez ce texte vers l’étiquette de groupe.
-   Utilisez une formulation positive. N’effectuez pas d’expression sur une étiquette afin que la sélection d’une case à cocher signifie de ne pas exécuter d’action.

    -   **Exception : ne plus afficher <item> ces** cases à cocher.

    **Incorrect :**

    ![capture d’écran de l’étiquette négative’éteindre'](images/ctrl-check-boxes-image25.png)

    Dans cet exemple, l’option n’utilise pas une formulation positive.

-   Décrivez simplement l’option avec l’étiquette. Conservez les étiquettes pour qu’elles se réfèrent facilement aux messages et à la documentation. Si l’option nécessite une explication supplémentaire, fournissez l’explication dans un contrôle de [texte statique](./glossary.md) à l’aide de phrases complètes et de signes de ponctuation finale.

    > [!Note]
    >
    > L’ajout d’une explication à une case à cocher dans un groupe ne signifie pas que vous devez fournir des explications pour toutes les cases à cocher du groupe. Fournissez les informations pertinentes dans l’étiquette, si possible, et utilisez les explications uniquement lorsque cela est nécessaire. Ne renommez pas simplement l’étiquette à des fins de cohérence.

     

    ![capture d’écran de la case à cocher, de l’étiquette et de la description ](images/ctrl-check-boxes-image26.png)

    Dans cet exemple, une étiquette de case à cocher contient du texte explicatif supplémentaire.

-   Si une option est fortement recommandée, ajoutez « (recommandé) » à l’étiquette. Veillez à ajouter à l’étiquette de contrôle, et non aux notes supplémentaires.
-   Si vous devez utiliser des étiquettes sur plusieurs lignes, alignez le haut de l’étiquette sur la case à cocher.
-   N’utilisez pas de contrôle subordonné, les valeurs qu’il contient ou son étiquette Units pour créer une phrase ou une expression. Une conception de ce type n’est pas localisable, car la structure de phrase varie en fonction de la langue.

    **Incorrect :**

    ![capture d’écran de l’étiquette de case à cocher avec la zone de texte ](images/ctrl-check-boxes-image27.png)

    Dans cet exemple, la zone de texte est placée incorrectement à l’intérieur de l’étiquette de la case à cocher.

**Étiquettes de groupe de cases à cocher**

-   Utilisez l’étiquette de groupe pour expliquer l’objectif du groupe, et non comment effectuer la sélection. Supposons que les utilisateurs savent comment utiliser les cases à cocher. Par exemple, ne dites pas « sélectionnez l’une des options suivantes ».
-   Mettez fin à chaque étiquette avec un signe deux-points.
-   N’attribuez pas de clé d’accès à l’étiquette. Cela n’est pas nécessaire et rend les autres clés d’accès plus difficiles à assigner.
-   Pour une sélection d’un ou de plusieurs choix dépendants, expliquez la spécification sur l’étiquette.

    **Correct :**

    ![capture d’écran de l’étiquette pour deux contrôles : protocoles ](images/ctrl-check-boxes-image28.png)

    Dans cet exemple, les utilisateurs peuvent penser qu’ils ne peuvent effectuer qu’une seule sélection.

    **Conseillé**

    ![capture d’écran de l’étiquette : protocoles sélectionnez un ou plusieurs ](images/ctrl-check-boxes-image29.png)

    Dans cet exemple, il est clair que les utilisateurs peuvent effectuer plusieurs sélections.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des cases à cocher :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points. Incluez la case à cocher mot.
-   Reportez-vous à une case à cocher sous la forme d’une case à cocher, pas d’option, de case à cocher ou de zone simple, car Box seul est ambigu pour les localisateurs.
-   Pour décrire l’interaction de l’utilisateur, utilisez sélectionner et effacer.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

    Exemple : activez la case à cocher **souligner** .

