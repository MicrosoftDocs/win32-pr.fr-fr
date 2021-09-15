---
title: Contrôles spin
description: Avec un contrôle spin, les utilisateurs peuvent cliquer sur les boutons fléchés pour modifier de manière incrémentielle la valeur dans la zone de texte numérique qui lui est associée.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411431"
---
# <a name="spin-controls"></a>Contrôles spin

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un contrôle spin, les utilisateurs peuvent cliquer sur les boutons fléchés pour modifier de manière incrémentielle la valeur dans la [zone de texte numérique](ctrl-text-boxes.md)qui lui est associée. Le terme zone de sélection numérique fait référence à la combinaison d’une zone de texte et de son contrôle spin associé.

![capture d’écran de la zone de texte et du contrôle spin ](images/ctrl-spin-controls-image1.png)

Zone de sélection numérique classique.

Les utilisateurs préfèrent souvent les contrôles spin, car ils peuvent apporter des modifications sans déplacer les mains de la souris. Lorsque le contrôle spin est associé à une zone de texte, les utilisateurs peuvent taper ou coller une entrée directement dans la zone de texte, de sorte que l’utilisation du contrôle spin est facultative.

Alors que les contrôles spin sont utilisés pour l’entrée numérique, l’entrée n’a pas besoin d’être un nombre entier pur. L’entrée peut être un nombre décimal et peut avoir des signes négatifs, des délimiteurs (tels que les signes deux-points ou des traits d’Union) et des modificateurs d’unités.

> [!Note]  
> Les instructions relatives aux [zones de texte](ctrl-text-boxes.md) et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Le contrôle est-il utilisé pour les entrées numériques ?** Si ce n’est pas le cas, utilisez un autre contrôle, tel qu’une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) ou un [curseur](ctrl-sliders.md), pour effectuer une sélection à partir d’un ensemble fixe de valeurs. Utilisez des barres de défilement pour le défilement.
-   **Les utilisateurs considèrent-ils la valeur comme une quantité relative, et non une valeur numérique ?** Dans ce cas, utilisez un curseur à la place. Utilisez des zones de sélection numérique uniquement pour les valeurs numériques exactes et connues. Par exemple, dans le cas du volume, ils le régleront sur faible ou moyen, et pas sur 2 ou 5.
-   **Le contrôle est-il associé à une zone de texte ?** Si ce n’est pas le cas, n’utilisez pas. Les contrôles spin ne doivent pas être utilisés seuls ou avec d’autres types de contrôles en dehors d’une zone de texte.

    **Incorrect :**

    ![capture d’écran du contrôle spin, graphique, aucune zone de texte ](images/ctrl-spin-controls-image2.png)

    Dans cet exemple, un contrôle spin est utilisé pour contrôler un graphique dynamique.

-   **Les plages de valeurs contiguës sont-elles valides ?** Si ce n’est pas le cas, utilisez plutôt une liste déroulante de valeurs valides.

    ![capture d’écran de la liste déroulante ](images/ctrl-spin-controls-image3.png)

    Dans cet exemple, tous les lecteurs de disque ne sont pas valides, donc une liste déroulante est un meilleur choix.

-   **L’utilisation du contrôle spin est-elle pratique ?** L’utilisation d’un contrôle spin est pratique pour :

    -   En entrant un petit nombre, généralement sous 100.
    -   Apporter de petites modifications à une valeur existante ou par défaut.

    Alors que les contrôles spin peuvent être utilisés pour n’importe quelle entrée numérique, ils sont inefficaces dans les situations autres que celles-ci.

-   **Le contrôle spin est-il utile ?** Le contrôle est-il utilisé dans un contexte où les utilisateurs sont susceptibles d’utiliser leur souris ? Si ce n’est pas le cas, envisagez d’utiliser un contrôle spin facultatif.
-   **Les listes déroulantes des contrôles frères sont-elles ?** S’il existe d’autres listes déroulantes, envisagez d’utiliser une liste déroulante pour la cohérence.

    ![capture d’écran de la boîte de dialogue avec des listes déroulantes ](images/ctrl-spin-controls-image4.png)

    Dans cet exemple, une zone de sélection numérique peut être utilisée, mais une liste déroulante est utilisée à des fins de cohérence.

-   **Les utilisateurs tactiles ou PEN sont-ils une cible principale ?** Si c’est le cas, envisagez plutôt d’utiliser une liste déroulante. Les boutons fléchés dans un contrôle spin sont trop petits pour être utilisés efficacement avec Touch ou un stylet.

Si un curseur ou une zone de sélection numérique est possible, utilisez une zone de sélection numérique si :

-   l’espace de l’écran est réduit ;
-   Il est probable qu’un utilisateur préfère utiliser le clavier.

Utilisez un curseur si :

-   les utilisateurs bénéficieront d’un résultat instantané.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Utilisez des contrôles spin chaque fois qu’ils sont pratiques et utiles.** [S’agit-il du bon contrôle ?](#is-this-the-right-control)

    -   **Exception :** Pour être cohérent avec d’autres zones de texte sur la même interface utilisateur, utilisez des contrôles spin même s’ils ne sont pas toujours pratiques.

    **Correct :**

    ![capture d’écran des contrôles de rotation du mois, du jour, de l’année ](images/ctrl-spin-controls-image5.png)

    Dans cet exemple, un contrôle spin est utilisé avec le contrôle Year pour des raisons de cohérence, même s’il n’est pas toujours pratique.

    **Incorrect :**

    ![capture d’écran du contrôle spin de l’adresse IP ](images/ctrl-spin-controls-image6.png)

    Dans cet exemple, le contrôle spin est inutilisable.

-   **Faites toujours d’un contrôle toupie l' « ami » de la zone de texte.** Cela place le contrôle spin à l’intérieur de la zone de texte.

    **Correct :**

    ![capture d’écran du contrôle spin placé à l’intérieur de la zone de texte ](images/ctrl-spin-controls-image7.png)

    **Incorrect :**

    ![capture d’écran du contrôle spin placé en dehors de la zone de texte ](images/ctrl-spin-controls-image8.png)

    Dans l’exemple correct, le contrôle spin est placé à l’intérieur de sa zone de texte associée.

-   **Désactiver un contrôle spin lorsque sa zone de texte associée est désactivée.** Le contrôle spin est une méthode d’entrée supplémentaire, qui n’est jamais la seule méthode d’entrée.

### <a name="values"></a>Valeurs

-   **Définissez le bouton du haut pour augmenter la valeur d’une unité et le bouton inférieur pour réduire d’une unité.** En règle générale, l’unité est un, mais il doit s’agir de la plus petite modification courante de la valeur. Dans l’idéal, le contrôle spin doit couvrir toutes les valeurs valides et doit être plus pratique que la saisie dans le texte.

    ![capture d’écran du contrôle spin « Margins » ](images/ctrl-spin-controls-image9.png)

    Dans cet exemple, le fait de cliquer sur un contrôle spin modifie les valeurs par 1, ce qui correspond à la plus petite modification courante de la valeur. L’utilisation d’une unité plus petite couvre la plage de valeurs valides, mais rend les contrôles spin inutilisables.

-   **Utilisez le contrôle spin pour limiter l’entrée aux valeurs valides.** L’utilisation d’un contrôle spin ne doit jamais aboutir à une valeur incorrecte.
-   **À la fin d’une plage de valeurs valides, redémarrez la plage.** La métaphore du contrôle spin est que l’utilisateur tourne une roue de valeurs, ce qui est le comportement de type roue.
    -   **Exception :** Ne redémarrez pas la plage si la valeur résultante est incorrecte.

        ![capture d’écran du contrôle spin « nombre de copies » ](images/ctrl-spin-controls-image10.png)

        Dans cet exemple, le fait de cliquer sur le bouton fléché vers le bas ne redémarre pas la plage (en allant à la valeur maximale), car cette valeur est incorrecte.

-   **Utilisez du texte au lieu de valeurs numériques spéciales.** Autorisez les utilisateurs à faire tourner ces valeurs spéciales au lieu de les connaître et de les taper.

    ![capture d’écran du contrôle spin « mettre en veille après (jamais) » ](images/ctrl-spin-controls-image11.png)

    Dans cet exemple, n’est jamais une valeur spéciale, mais les utilisateurs peuvent y faire tourner.

-   **Si la valeur a des délimiteurs, la zone de texte associée doit avoir plusieurs points de focus d’entrée.** Cela permet de manipuler les segments numériques individuellement.

    ![capture d’écran du contrôle de rotation de l’heure, minutes sélectionnées ](images/ctrl-spin-controls-image12.png)

    Dans cet exemple, le contrôle spin affecte les valeurs pour les heures, les minutes, les secondes et le matin.

-   **Si la valeur a des unités, utilisez le contrôle spin pour modifier également ces unités.**

    ![capture d’écran du contrôle de rotation du temps, « a.m. » activé ](images/ctrl-spin-controls-image13.png)

    Dans cet exemple, le contrôle spin peut être utilisé pour modifier des unités.

## <a name="labels"></a>Étiquettes

-   Appliquez les indications relatives à l’étiquetage de la [zone de texte](ctrl-text-boxes.md) pour étiqueter la zone de texte associée. Les contrôles spin ne sont jamais étiquetés directement.

## <a name="documentation"></a>Documentation

Quand vous faites référence à des contrôles spin :

-   Ne faites pas référence aux contrôles spin dans la documentation de l’utilisateur. Au lieu de cela, reportez-vous à l’étiquette de la zone de texte associée.
-   Reportez-vous à des contrôles spin et à des zones de sélection numérique uniquement dans la programmation et dans d’autres documents techniques.

Exemple : dans la zone **Date** , tapez ou sélectionnez la partie de la date que vous souhaitez modifier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Glossaire](glossary.md)
</dt> </dl>

 

 