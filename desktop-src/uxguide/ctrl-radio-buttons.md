---
title: Cases d’option
description: Avec une case d’option, les utilisateurs font un choix parmi un ensemble d’options associées s’excluant mutuellement.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234948"
---
# <a name="radio-buttons"></a>Cases d’option

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une case d’option, les utilisateurs font un choix parmi un ensemble d’options associées s’excluant mutuellement. Les utilisateurs peuvent choisir une seule et unique option. Les cases d’option sont appelées, car elles fonctionnent comme les présélections de canal sur les radios.

![capture d’écran de trois cases d’option ](images/radio-buttons-image1.png)

Groupe classique de cases d’option.

Un groupe de cases d’option se comporte comme un contrôle unique. Seul le choix sélectionné est accessible à l’aide de la touche Tab, mais les utilisateurs peuvent parcourir le groupe à l’aide des touches de direction.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) et à la [navigation au clavier](inter-keyboard.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Le contrôle est-il utilisé pour choisir une option parmi un ensemble de choix s’excluant mutuellement ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour choisir plusieurs options, utilisez à la place des [cases à cocher](ctrl-check-boxes.md), une [liste à sélection multiple](ctrl-list-boxes.md) ou une liste de cases à cocher.
-   **Le nombre d’options entre deux et sept ?** Étant donné que l’espace à l’écran utilisé est proportionnel au nombre d’options, conservez le nombre d’options dans un groupe entre deux et sept. Pour huit options ou plus, utilisez une liste [déroulante](/windows/desktop/uxguide/ctrl-drop) ou une [liste de sélection unique](ctrl-list-boxes.md).
-   **Une case à cocher sera-t-elle un meilleur choix ?** S’il n’existe que deux options, vous pouvez utiliser une seule case [à cocher](ctrl-check-boxes.md) . Toutefois, les cases à cocher conviennent uniquement à l’activation ou à la désactivation d’une seule option, tandis que les cases d’option peuvent être utilisées pour des solutions de remplacement complètement différentes. Si les deux solutions sont possibles :
    -   Utilisez les cases d’option si la signification de la case à cocher désactivée n’est pas complètement évidente.

        **Incorrect :**

        ![capture d’écran de la case à cocher paysage ](images/radio-buttons-image2.png)

        **Correct :**

        ![capture d’écran des cases d’option Paysage/Portrait ](images/radio-buttons-image3.png)

        Dans l’exemple approprié, les choix ne sont pas opposés afin que les cases d’option soient le meilleur choix.

    -   Utilisez les cases d’option des pages de l’Assistant pour désactiver les alternatives, même si une case à cocher est acceptable.
    -   Utilisez les cases d’option si vous avez suffisamment d’espace à l’écran et si les options sont suffisamment importantes pour constituer une bonne utilisation de cet espace d’écran. Dans le cas contraire, utilisez une case à cocher ou une liste déroulante.

        **Incorrect :**

        ![capture d’écran des cases d’option Afficher/ne pas afficher ](images/radio-buttons-image4.png)

        Dans cet exemple, les options ne sont pas assez importantes pour utiliser des cases d’option.

        **Correct :**

        ![capture d’écran de la case à cocher ne pas afficher ce message ](images/radio-buttons-image5.png)

        Dans cet exemple, une case à cocher est une utilisation efficace de l’espace à l’écran pour cette option de périphérique.

    -   Utilisez une case à cocher si d’autres cases sur la page sont cochées.

-   **Une liste déroulante sera-t-elle un meilleur choix ?** Si l’option par défaut est recommandée pour la plupart des utilisateurs dans la plupart des cas, les cases d’option peuvent attirer davantage l’attention sur les options que nécessaire.
    -   Envisagez d’utiliser une liste déroulante si vous ne souhaitez pas attirer l’attention sur les options ou si vous ne souhaitez pas encourager les utilisateurs à apporter des modifications. Une liste déroulante se concentre sur la sélection actuelle, tandis que les cases d’option mettent également en évidence toutes les options.

        ![capture d’écran de la qualité la plus élevée comme bouton par défaut ](images/radio-buttons-image6.png)

        Dans cet exemple, une liste déroulante se concentre sur la sélection actuelle et décourage les utilisateurs d’apporter des modifications.

    -   Prenons l’exemple d’une liste déroulante s’il existe d’autres listes déroulantes sur la page.

-   **Un ensemble de boutons de commande, de liens de commande ou de bouton partagé est-il préférable ?** Si les cases d’option sont utilisées uniquement pour affecter la façon dont une commande est exécutée, il est souvent préférable de présenter les variantes de commande à la place. Cela permet aux utilisateurs de choisir la commande appropriée avec une seule interaction.
-   **Les options présentent-elles des options de programme plutôt que des données ?** Les valeurs des options ne doivent pas être basées sur le contexte ou d’autres données. Pour les données, utilisez une liste déroulante ou une liste de sélection unique.
-   Si le contrôle est utilisé sur une page de l’Assistant ou dans le panneau de configuration, **le contrôle répond-il à l’instruction principale et les utilisateurs peuvent-ils modifier ultérieurement le choix ?** Si c’est le cas, envisagez d’utiliser des liens de commande plutôt que des cases d’option pour rendre l’interaction plus efficace.
-   **Les valeurs ne sont-elles pas numériques ?** Pour les données numériques, utilisez les [zones de texte](ctrl-text-boxes.md), les [listes déroulantes](/windows/desktop/uxguide/ctrl-drop)ou les [curseurs](ctrl-sliders.md).

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Répertoriez les options dans un ordre logique,** par exemple, les plus susceptibles d’être sélectionnées pour l’opération la plus simple, la plus simple pour la plus complexe, ou le moins risqué. L’ordre alphabétique n’est pas recommandé, car il dépend de la langue et ne peut donc pas être localisé.
-   **Si aucune des options n’est un choix valide, ajoutez une autre option pour refléter ce choix,** par exemple aucun ou ne s’applique pas.
-   **Préférez aligner les cases d’option verticalement plutôt que horizontalement.** L’alignement horizontal est plus difficile à lire et à localiser.

    **Correct :**

    ![capture d’écran de l’alignement vertical du bouton radio ](images/radio-buttons-image7.png)

    Dans cet exemple, les cases d’option sont alignées verticalement.

    **Incorrect :**

    ![capture d’écran de l’alignement du bouton radio horizontal ](images/radio-buttons-image8.png)

    Dans cet exemple, l’alignement horizontal est plus difficile à lire.

-   **Reconsidérez l’utilisation des zones de groupe pour organiser les groupes de cases d’option, ce qui se** traduit souvent par un encombrement inutile de l’écran.
-   **N’utilisez pas les étiquettes de cases d’option comme étiquettes de zone de groupe.**
-   **N’utilisez pas la sélection d’une case d’option pour :**
    -   Exécuter des commandes.
    -   Affichez d’autres fenêtres, telles qu’une boîte de dialogue pour recueillir davantage d’entrées.
    -   Afficher ou masquer dynamiquement d’autres contrôles en rapport avec le contrôle sélectionné (les lecteurs d’écran ne peuvent pas détecter de tels événements). Toutefois, vous pouvez modifier le texte dynamiquement en fonction de la sélection.

### <a name="subordinate-controls"></a>Contrôles subordonnés

-   Placez les contrôles subordonnés à droite ou en dessous (mise en retrait, vidage avec l’étiquette de case d’option) de la case d’option et de son étiquette. Mettez fin à l’étiquette de la case d’option avec un signe deux-points.

    ![capture d’écran de contrôle à droite de son étiquette ](images/radio-buttons-image9.png)

    Dans cet exemple, la case d’option et son contrôle subordonné partagent l’étiquette de case d’option et sa clé d’accès. Dans ce cas, les touches de direction déplacent le focus de la case d’option vers sa zone de texte subordonnée.

-   **Laissez les zones de texte modifiables dépendantes et les listes déroulantes activées si elles partagent l’étiquette de la case d’option.** Lorsque les utilisateurs tapent ou collent quoi que ce soit dans la zone, sélectionnez automatiquement l’option correspondante. Cela simplifie l’interaction.

    ![capture d’écran de la boîte de dialogue plage de pages avec zone de texte ](images/radio-buttons-image10.png)

    Dans cet exemple, l’entrée d’un numéro de page sélectionne automatiquement des pages.

-   **Évitez d’imbriquer des cases d’option avec d’autres cases d’option ou cases à cocher.** Si possible, conservez toutes les options au même niveau.

    **Correct :**

    ![capture d’écran des cases d’option alignées à gauche ](images/radio-buttons-image11.png)

    Dans cet exemple, les options se trouvent au même niveau.

    **Incorrect :**

    ![capture d’écran des cases d’option imbriquées ](images/radio-buttons-image12.png)

    Dans cet exemple, l’utilisation d’options imbriquées ajoute une complexité inutile.

-   Si vous imbriquez des cases d’option avec d’autres cases d’option ou cases à cocher, **désactivez ces contrôles subordonnés jusqu’à ce que l’option de haut niveau soit sélectionnée.** Cela évite toute confusion quant à la signification des contrôles subordonnés.

### <a name="default-values"></a>Valeurs par défaut

-   Étant donné qu’un groupe de cases d’option représente un ensemble de choix s’excluant mutuellement, une case d' **option est toujours sélectionnée par défaut. Sélectionnez le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée et privée.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez l’option la plus probable ou la plus pratique.
-   **Exceptions :** Aucune sélection par défaut si :
    -   **Il n’existe pas d’option par défaut acceptable pour des raisons de sécurité ou de sécurité, et par conséquent, l’utilisateur doit faire un choix explicite.** Si l’utilisateur n’effectue pas de sélection, affichez un message d’erreur pour en imposer un.
    -   **L’interface utilisateur (IU) doit refléter l’état actuel et l’option n’a pas encore été définie.** Une valeur par défaut ne signifie pas que l’utilisateur n’a pas besoin d’effectuer une sélection.
    -   **L’objectif est de collecter des données non biaisées.** Les valeurs par défaut sont le biais de la collecte de données.
    -   **Le groupe de cases d’option représente une propriété dans un État mixte**, qui se produit lors de l’affichage d’une propriété pour plusieurs objets qui n’ont pas le même paramètre. N’affiche pas de message d’erreur dans le cas où chaque objet a un état valide.
-   **Définissez la première option comme option par défaut**, car les utilisateurs attendent souvent cela, sauf si cette commande n’est pas logique. Pour ce faire, vous devrez peut-être modifier les étiquettes des options.

    **Incorrect :**

    ![capture d’écran de la dernière case d’option comme option par défaut ](images/radio-buttons-image13.png)

    Dans cet exemple, l’option par défaut n’est pas la première option.

    **Correct :**

    ![capture d’écran de la première case d’option comme valeur par défaut ](images/radio-buttons-image14.png)

    Dans cet exemple, les étiquettes d’option sont reformulées pour faire de la première option l’option par défaut.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran de la taille et de l’espacement des cases d’option ](images/radio-buttons-image15.png)

Dimensionnement et espacement recommandés pour les cases d’option.

## <a name="labels"></a>Étiquettes

### <a name="radio-button-labels"></a>Étiquettes des cases d’option

-   Étiquette chaque case d’option.

<!-- -->

-   Attribuez une [clé d’accès](glossary.md) unique à chaque étiquette. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Écrivez l’étiquette en tant qu’expression, pas en tant que phrase, et n’utilisez pas de ponctuation finale.
    -   **Exception :** Si une étiquette de case d’option étiquette également un contrôle subordonné qui la suit, terminez l’étiquette par un signe deux-points.
-   Utilisez une formulation parallèle et essayez de conserver la même longueur pour toutes les étiquettes.
-   Concentrez le texte de l’étiquette sur les différences entre les options. Si toutes les options ont le même texte d’introduction, déplacez ce texte vers l’étiquette de groupe.
-   Utilisez une formulation positive. Par exemple, utilisez do au lieu de do not, et imprimez au lieu de ne pas imprimer.
-   Décrivez simplement l’option avec l’étiquette. Conservez les étiquettes pour qu’elles se réfèrent facilement aux messages et à la documentation. Si l’option nécessite une explication supplémentaire, fournissez l’explication dans un contrôle de [texte statique](glossary.md) à l’aide de phrases complètes et de signes de ponctuation finale.

    ![capture d’écran des cases d’option avec du texte explicatif](images/radio-buttons-image16.png)

    Dans cet exemple, les options sont expliquées à l’aide de contrôles de texte statique distincts.

    > [!Note]  
    > L’ajout d’une explication à une case d’option ne signifie pas que vous devez fournir des explications pour toutes les cases d’option. Fournissez les informations pertinentes dans l’étiquette, si possible, et utilisez les explications uniquement lorsque cela est nécessaire. Ne renommez pas simplement l’étiquette à des fins de cohérence.

     

-   **Si une option est fortement recommandée, ajoutez « (recommandé) » à l’étiquette.** Veillez à ajouter à l’étiquette de contrôle, et non aux notes supplémentaires.
-   **Si une option est destinée uniquement aux utilisateurs expérimentés, ajoutez « (avancé) » à l’étiquette.** Veillez à ajouter à l’étiquette de contrôle, et non aux notes supplémentaires.
-   Si vous devez utiliser des étiquettes sur plusieurs lignes, alignez le haut de l’étiquette sur la case d’option.
-   N’utilisez pas de contrôle subordonné, les valeurs qu’il contient ou son étiquette Units pour créer une phrase ou une expression. Une conception de ce type n’est pas localisable, car la structure de phrase varie en fonction de la langue.

### <a name="radio-button-group-labels"></a>Étiquettes de groupe de cases d’option

-   Utilisez l’étiquette de groupe pour expliquer l’objectif du groupe, et non comment effectuer la sélection. Supposons que les utilisateurs savent comment utiliser des cases d’option. Par exemple, ne dites pas « sélectionnez l’une des options suivantes ».
-   Tous les groupes de cases d’option ont besoin d’étiquettes. Écrivez l’étiquette sous la forme d’un mot ou d’une expression, et non pas en tant que phrase, en terminant par un signe deux-points utilisant du texte statique ou une zone de groupe.

    **Exception :** Omettez l’étiquette s’il s’agit simplement d’une refonte de l' [instruction principale](glossary.md)d’une boîte de dialogue. Dans ce cas, l’instruction principale prend le signe deux-points (sauf s’il s’agit d’une question) et la clé d’accès (le cas échéant).

    **Acceptable:**

    ![capture d’écran de l’étiquette de groupe de cases d’option redondantes ](images/radio-buttons-image17.png)

    Dans cet exemple, l’étiquette de groupe de cases d’option est simplement une REstate de l’instruction principale.

    **Conseillé**

    ![capture d’écran de l’instruction principale de case d’option uniquement ](images/radio-buttons-image18.png)

    Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend le signe deux-points.

-   N’attribuez pas de clé d’accès à l’étiquette. Cela n’est pas nécessaire et rend les autres clés d’accès plus difficiles à assigner.
    -   **Exception :** Si tous les contrôles ne peuvent pas avoir des clés d’accès uniques, vous pouvez assigner une touche d’accès à l’étiquette au lieu des contrôles individuels. Pour plus d’informations, consultez [clavier](inter-keyboard.md).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des cases d’option :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points.
-   Dans programmation et autres documents techniques, reportez-vous aux cases d’option sous forme de cases d’option. Partout ailleurs, utilisez les cases d’option, en particulier dans la documentation utilisateur.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : cliquez sur **page active**, puis sur **OK**.

 

 