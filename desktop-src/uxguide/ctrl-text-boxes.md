---
title: Zones de texte
description: Avec une zone de texte, les utilisateurs peuvent afficher, entrer ou modifier un texte ou une valeur numérique.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f8627ad5069dc6bb34c490a3eea964e5c6abb654
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988432"
---
# <a name="text-boxes"></a>Zones de texte

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une zone de texte, les utilisateurs peuvent afficher, entrer ou modifier un texte ou une valeur numérique.

![capture d’écran d’une zone de texte et d’une étiquette typiques ](images/ctrl-text-boxes-image1.png)

Zone de texte standard.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md), aux [polices](vis-fonts.md)et aux [bulles](ctrl-balloons.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Est-il pratique d’énumérer toutes les valeurs valides efficacement ?** Dans ce cas, envisagez une [liste de sélection unique](ctrl-list-boxes.md), un [affichage de liste](ctrl-list-views.md) [, une](/windows/desktop/uxguide/ctrl-drop)liste déroulante modifiable, une liste déroulante modifiable ou un [curseur](ctrl-sliders.md) à la place.
-   **Les données valides sont-elles entièrement non restreintes ? Ou les données valides sont-elles uniquement restreintes par le format (longueur restreinte ou types de caractères) ?** Dans ce cas, utilisez une zone de texte.
-   **La valeur représente-t-elle un type de données auquel correspond un contrôle courant spécialisé ?** Les exemples incluent la date, l’heure ou l’adresse IPv4 ou IPv6. Si c’est le cas, utilisez le contrôle approprié, tel qu’un contrôle de date plutôt qu’une zone de texte.
-   Si les données sont numériques :
    -   **Les utilisateurs perçoivent-ils le paramètre comme une quantité relative ?** Si tel est le cas, utilisez un curseur.
    -   **L’utilisateur va-t-il bénéficier d’un feedback instantané sur l’effet des modifications apportées aux paramètres ?** Dans ce cas, utilisez un curseur, éventuellement avec une zone de texte. Par exemple, les utilisateurs peuvent facilement choisir une couleur à l’aide d’un curseur, car ils peuvent immédiatement voir l’effet des modifications des valeurs de teinte, de saturation ou de luminosité.

## <a name="design-concepts"></a>Principes de conception

Bien que les zones de texte présentent l’avantage d’être très souples, elles présentent l’inconvénient d’avoir des contraintes minimales. Les seules contraintes sur une zone de texte modifiable sont les suivantes :

-   Vous pouvez éventuellement définir le nombre maximal de caractères.
-   Vous pouvez éventuellement limiter l’entrée aux caractères numériques (0 9) uniquement.
-   Si vous utilisez un [contrôle spin](ctrl-spin-controls.md), vous pouvez limiter les choix de contrôle spin aux valeurs valides.

Outre leur longueur et la présence facultative d’un contrôle spin, les zones de texte n’ont pas d’indications visuelles qui suggèrent les valeurs valides ou leur format. Cela signifie que vous pouvez utiliser des étiquettes pour communiquer ces informations aux utilisateurs. Si les utilisateurs entrent du texte qui n’est pas valide, vous devez gérer l’erreur avec un message d’erreur.

En règle générale, **vous devez utiliser le contrôle le plus restreint que vous pouvez**. Utilisez des contrôles sans contrainte comme des zones de texte en dernier recours. Cela dit, lorsque vous envisagez des contraintes, gardez à l’esprit les besoins des utilisateurs généraux. Par exemple, un contrôle qui est contraint à États-Unis codes POSTaux n’est pas globalisé, mais une zone de texte sans contrainte qui accepte n’importe quel format de code postal est.

## <a name="usage-patterns"></a>Modèles d’usage

Une zone de texte est un contrôle flexible avec plusieurs utilisations possibles.




| Étiquette | Valeur |
|--------|-------|
| <strong>Entrée de données</strong><br /> Zone de texte à une seule ligne, sans contrainte, utilisée pour entrer ou modifier des chaînes courtes.<br /> | <img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br /> Zone de texte à une seule ligne et sans contrainte.<br /> | 
| <strong>Saisie de données mises en forme</strong><br /> Ensemble de zones de texte d’une seule ligne de taille fixe, qui permettent d’entrer des données avec un format spécifique. <br /> | <img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br /> Zone de texte utilisée pour l’entrée de données mises en forme.<br /><blockquote>[!Note]<br />La fonctionnalité de <a href="glossary.md">fermeture automatique</a> avance automatiquement le focus d’entrée d’une zone de texte à la suivante. L’un des inconvénients de cette approche est que les données ne peuvent pas être copiées ou collées en tant qu’unité unique.</blockquote><br /><br /> | 
| <strong>Saisie de données assistée</strong><br /> Zone de texte sur une seule ligne, sans contrainte, utilisée pour entrer ou modifier des chaînes, combinée avec un bouton de commande qui aide les utilisateurs à sélectionner des valeurs valides.<br /> | <img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br /> Dans cet exemple, la commande parcourir aide les utilisateurs à sélectionner des valeurs valides.<br /> | 
| <strong>Entrée textuelle</strong><br /> Zone de texte multiligne, sans contrainte, utilisée pour entrer ou modifier des chaînes longues. <br /> | <img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br /> Zone de texte multiligne, sans contrainte.<br /> | 
| <strong>Entrée numérique</strong><br /> Zone de texte à une seule ligne, numérique uniquement utilisée pour entrer ou modifier des nombres, avec un <a href="ctrl-spin-controls.md">contrôle spin</a> facultatif pour faciliter l’entrée à l’aide de la souris. <br /> | <img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br /> Zone de texte utilisée pour l’entrée numérique.<br /> La combinaison d’une zone de texte et de son contrôle spin associé est appelée <a href="ctrl-spin-controls.md">zone de sélection numérique</a>.<br /> | 
| <strong>Saisie du mot de passe et du code confidentiel</strong><br /> Zone de texte sur une seule ligne, sans contrainte, utilisée pour entrer des mots de passe et des codes confidentiels en toute sécurité.<br /> | <img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br /> Zone de texte utilisée pour entrer des mots de passe.<br /> | 
| <strong>Sortie des données</strong><br /> Zone de texte sur une seule ligne, en lecture seule, toujours affichée sans bordure, utilisée pour afficher des chaînes courtes. <br /> | Contrairement au texte statique, les données affichées à l’aide d’une zone de texte peuvent être défilées (utiles si les données sont plus larges que le contrôle), sélectionnées et copiées.<br /><img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br /> Zone de texte d’une seule ligne, en lecture seule, utilisée pour afficher les données.<br /> | 
| <strong>Sortie textuelle</strong><br /> Zone de texte multiligne en lecture seule utilisée pour afficher des chaînes longues. <br /> | <img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br /> Zone de texte en lecture seule utilisée pour afficher les données.<br /> | 




 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Lors de la désactivation d’une zone de texte, désactivez également les étiquettes, les étiquettes d’instruction, les contrôles spin et les boutons de commande associés.**
-   **Utilisez la saisie semi-automatique pour aider les utilisateurs à entrer des données susceptibles d’être utilisées à plusieurs reprises**. Les noms d’utilisateur, les adresses et les noms de fichiers sont des exemples. Toutefois, n’utilisez pas la saisie semi-automatique pour les zones de texte qui peuvent contenir des informations sensibles, telles que des mots de passe, des codes confidentiels, des numéros de carte de crédit ou des informations médicales.
-   **Ne faites pas défiler inutilement les utilisateurs.** Si vous vous attendez à ce que les données soient plus volumineuses que la zone de texte et que vous puissiez facilement rendre la zone de texte plus grande sans nuire à la disposition, redimensionnez-la pour éviter d’avoir à faire défiler la liste.

    **Incorrect :**

    ![capture d’écran d’une zone de texte de nom d’ordinateur ](images/ctrl-text-boxes-image10.png)

    Dans cet exemple, la zone de texte doit être bien plus longue pour gérer ses données.

-   Barres de défilement :
    -   **Ne placez pas de barres de défilement horizontales sur des zones de texte à plusieurs lignes.** Utilisez à la place le défilement vertical et le retour à la ligne.
    -   **Ne placez pas de barres de défilement sur des zones de texte sur une seule ligne.**
-   **Pour une entrée numérique, vous pouvez utiliser un contrôle spin.** Pour entrée textuelle, utilisez une liste déroulante ou une liste déroulante modifiable à la place.
-   **N’utilisez pas la fonctionnalité de sortie automatique, à l’exception des entrées de données mises en forme.** Le déplacement automatique du Focus peut surprendre en surprise les utilisateurs.

### <a name="editable-text-boxes"></a>Zones de texte modifiables

-   **Lorsque vous le pouvez, limitez la longueur du texte d’entrée.** Par exemple, si l’entrée valide est un nombre compris entre 0 et 999, utilisez une zone de texte numérique limitée à trois caractères. Toutes les parties de zones de texte qui utilisent une entrée de données mises en forme doivent avoir une longueur fixe brève.
-   **Soyez flexible avec les formats de données.** Si les utilisateurs sont susceptibles de saisir du texte à l’aide d’un grand nombre de formats, essayez de gérer tous les types les plus courants. Par exemple, de nombreux noms, chiffres et identificateurs peuvent être entrés avec des espaces et des signes de ponctuation facultatifs, et la mise en majuscules n’a souvent pas d’importance.
-   Si vous ne pouvez pas gérer les formats probables, vous devez utiliser un format spécifique à l’aide d’une entrée de données mises en forme ou indiquer les formats valides dans l’étiquette.

    **Acceptable:**

    ![capture d’écran d’une zone de texte pour une entrée numérique ](images/ctrl-text-boxes-image11.png)

    Dans cet exemple, une zone de texte requiert une entrée dans un format spécifique.

    **Conseillé**

    ![capture d’écran de la zone de texte entrée des données mises en forme ](images/ctrl-text-boxes-image12.png)

    Dans cet exemple, le modèle d’entrée de données mis en forme est utilisé pour exiger un format spécifique.

    **Meilleures**

    ![capture d’écran d’une zone de texte sans contrainte ](images/ctrl-text-boxes-image13.png)

    Dans cet exemple, une zone de texte gère tous les formats probables.

-   Tenez compte de la flexibilité de mise en forme lors du choix de la longueur d’entrée maximale. Par exemple, un numéro de carte de crédit valide peut utiliser jusqu’à 19 caractères, ce qui permet de limiter la longueur à toute valeur plus petite, ce qui rend difficile l’entrée de nombres à l’aide des formats plus longs.
-   **N’utilisez pas le modèle d’entrée de données mis en forme si les utilisateurs sont plus susceptibles de coller des données longues et complexes.** Au lieu de cela, réservez le modèle d’entrée de données mis en forme pour les situations où les utilisateurs sont plus susceptibles de saisir les données.

    ![capture d’écran d’une zone de texte avec étiquette : adresse IPv6 ](images/ctrl-text-boxes-image14.png)

    Dans cet exemple, le modèle d’entrée de données mis en forme n’est pas utilisé, afin que les utilisateurs puissent coller des adresses IPv6.

-   **Si les utilisateurs sont plus susceptibles de ressaisir la valeur entière, sélectionnez tout le texte sur le focus d’entrée.** Si les utilisateurs sont plus susceptibles de modifier, placez le signe insertion à la fin du texte.

    ![capture d’écran d’une zone de texte de mot de passe ](images/ctrl-text-boxes-image15.png)

    Dans cet exemple, il est plus probable que les utilisateurs remplacent la modification, donc la valeur entière est sélectionnée dans le focus d’entrée.

    ![capture d’écran d’une zone de texte pour la saisie de mots clés ](images/ctrl-text-boxes-image16.png)

    Dans cet exemple, les utilisateurs sont plus susceptibles d’ajouter des mots clés que de remplacer le texte ; le signe insertion est donc placé à la fin du texte.

-   **Utilisez toujours une zone de texte multiligne si les caractères de nouvelle ligne sont des entrées valides.**
-   **Lorsque la zone de texte correspond à un fichier ou à un chemin d’accès, indiquez toujours un bouton Parcourir.**

### <a name="numeric-text-boxes"></a>Zones de texte numériques

-   **Choisissez l’unité la plus pratique et étiquetez les unités.** Par exemple, envisagez d’utiliser milliliters au lieu de litres (ou vice versa), des pourcentages au lieu de valeurs directes (ou vice versa), etc.

    **Correct :**

    ![capture d’écran de la zone de texte avec litres comme unité ](images/ctrl-text-boxes-image17.png)

    Dans cet exemple, l’unité est étiquetée, mais elle nécessite que les utilisateurs entrent des nombres décimaux.

    **Conseillé**

    ![capture d’écran de la zone de texte avec milliliters en tant qu’unité ](images/ctrl-text-boxes-image18.png)

    Dans cet exemple, la zone de texte utilise une unité plus pratique.

-   **Utilisez un contrôle spin à chaque fois qu’il est utile.** Toutefois, parfois, les contrôles spin ne sont pas pratiques, par exemple lorsque les utilisateurs doivent entrer un grand nombre de grands nombres. Utilisez des contrôles spin dans les cas suivants :
    -   L’entrée est probablement un petit nombre, généralement sous 100.
    -   Les utilisateurs sont susceptibles d’apporter une petite modification à un nombre existant.
    -   Les utilisateurs sont plus susceptibles d’utiliser la souris que le clavier.
-   **Aligner le texte numérique à droite chaque fois :**

    -   Il existe plusieurs zones de texte numériques.
    -   Les zones de texte sont alignées verticalement.
    -   Les utilisateurs sont susceptibles d’ajouter ou de comparer les valeurs.

    **Correct :**

    ![capture d’écran des zones de texte des frais (hôtel, etc.) ](images/ctrl-text-boxes-image19.png)

    Dans cet exemple, le texte numérique est aligné à droite pour faciliter la comparaison des valeurs.

    **Incorrect :**

    ![capture d’écran des zones de texte pour les valeurs RVB ](images/ctrl-text-boxes-image20.png)

    Dans cet exemple, le texte numérique est aligné à gauche de manière incorrecte.

-   **Aligner toujours à droite les valeurs monétaires.**
-   **N’affectez pas de significations particulières à des valeurs numériques spécifiques**, même si ces significations particulières sont utilisées en interne par votre application. Utilisez plutôt des cases à cocher ou des cases d’option pour une sélection explicite de l’utilisateur.

    **Incorrect :**

    ![capture d’écran de l’étiquette : utilisez-1 pour désactiver la mise en cache ](images/ctrl-text-boxes-image21.png)

    Dans cet exemple, la valeur-1 a une signification particulière.

    **Correct :**

    ![capture d’écran de l’étiquette de case à cocher : Caching ](images/ctrl-text-boxes-image22.png)

    Dans cet exemple, une case à cocher rend l’option explicite.

### <a name="password-and-pin-input"></a>Saisie du mot de passe et du code confidentiel

-   **Utilisez toujours le contrôle commun de mot de passe au lieu de créer le vôtre.** Les mots de passe et les codes confidentiels nécessitent un traitement spécial pour être gérés en toute sécurité.

Pour obtenir des instructions et des exemples supplémentaires, consultez [bulles](ctrl-balloons.md).

### <a name="textual-output"></a>Sortie textuelle

-   **Envisagez d’utiliser la couleur du système d’arrière-plan blanc pour du texte en lecture seule à plusieurs lignes.** Un arrière-plan blanc rend le texte plus facile à lire. Un grand nombre de texte sur un arrière-plan gris découragent la lecture.

Pour plus d’informations sur les couleurs d’arrière-plan, consultez [polices](vis-fonts.md).

### <a name="data-output"></a>Sortie des données

-   **N’utilisez pas de bordure pour les zones de texte à une seule ligne et en lecture seule.** La bordure est un indice visuel indiquant que le texte est modifiable.
-   **Ne désactivez pas les zones de texte en lecture seule sur une seule ligne.** Cela empêche les utilisateurs de sélectionner et de copier le texte dans le presse-papiers. Il empêche également les utilisateurs de faire défiler les données si elles dépassent la taille de leurs limites.
-   **Ne définissez pas de taquet de tabulation sur une seule ligne, zone de texte en lecture seule, à moins que l’utilisateur ait besoin de faire défiler ou de copier le texte.**

## <a name="input-validation-and-error-handling"></a>Validation des entrées et gestion des erreurs

Étant donné que les zones de texte ne sont généralement pas converties pour accepter uniquement des entrées valides, vous devrez peut-être valider l’entrée et gérer les problèmes éventuels. Validez les différents types de problèmes d’entrée comme suit :

-   Si l’utilisateur entre un caractère qui n’est pas valide, ignorez le caractère et affichez une [bulle de problème d’entrée](ctrl-balloons.md) qui explique les caractères valides.

    ![capture d’écran de la zone de texte clé de produit](images/ctrl-text-boxes-image23.png)

    Dans cet exemple, une bulle signale un caractère d’entrée incorrect.

-   Si les données d’entrée ont une valeur ou un format qui n’est pas valide, affichez une bulle de problème d’entrée lorsque la zone de texte perd le focus d’entrée.
-   Si les données d’entrée ne sont pas cohérentes avec les autres contrôles de la fenêtre, affichez un message d’erreur lorsque la totalité de l’entrée est complète, par exemple lorsque les utilisateurs cliquent sur OK pour obtenir une boîte de dialogue modale.

**Ne supprimez pas les données d’entrée non valides, sauf si les utilisateurs ne peuvent pas facilement corriger les erreurs.** Cela permet aux utilisateurs de corriger les erreurs sans recommencer. Par exemple, vous devez effacer les codes confidentiels et les mots de passe incorrects, car les utilisateurs ne peuvent pas les corriger facilement.

Pour obtenir des instructions et des exemples supplémentaires, consultez [messages d’erreur](mess-error.md) et [bulles](ctrl-balloons.md).

## <a name="prompts"></a>Invites

Une invite est une étiquette ou une brève instruction placée dans une zone de texte comme valeur par défaut. Contrairement au texte statique, les invites disparaissent de l’écran une fois que les utilisateurs ont tapé un texte dans la zone de texte ou qu’il obtient le focus d’entrée.

![capture d’écran de la zone de texte d’invite avec étiquette : Rechercher ](images/ctrl-text-boxes-image24.png)

Invite classique.

Utilisez une invite dans les cas suivants :

-   L’espace à l’écran est d’une qualité telle que l’utilisation d’une étiquette ou d’une instruction n’est pas souhaitable, par exemple dans une barre d’outils.
-   L’invite est principalement destinée à identifier l’objectif de la zone de texte de manière compacte. Il ne doit pas s’agir d’informations essentielles que l’utilisateur doit voir lors de l’utilisation de la zone de texte.

N’utilisez pas les invites uniquement pour demander aux utilisateurs de taper un texte ou de cliquer sur les boutons. Par exemple, n’écrivez pas de texte d’invite indiquant entrez un nom de fichier, puis cliquez sur Envoyer.

Quand vous utilisez des invites :

-   Dessinez le texte de l’invite en italique gris et le texte d’entrée réel en noir normal. Le texte de l’invite ne doit pas être confondu avec du texte réel.
-   Conservez le texte de l’invite concis. Vous pouvez utiliser des fragments au lieu de phrases entières.
-   Utilisez les majuscules comme pour les phrases.
-   N’utilisez pas de ponctuation de fin ni de points de suspension.
-   Le texte de l’invite ne doit pas être modifiable et doit disparaître une fois que les utilisateurs cliquent dans ou sur l’onglet dans la zone de texte.
    -   **Exception :** Si la zone de texte a le focus d’entrée par défaut, l’invite s’affiche et disparaît lorsque l’utilisateur commence à taper.
-   Le texte d’invite est restauré si la zone de texte est toujours vide lorsqu’il perd le focus d’entrée.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![Figure des zones de texte d’une ligne et de deux lignes ](images/ctrl-text-boxes-image25.png)

Dimensionnement et espacement recommandés pour les zones de texte.

La largeur d’une zone de texte est un indice visuel de la taille d’entrée attendue. Lors du dimensionnement des zones de texte :

-   **Choisissez une largeur appropriée pour les données valides les plus longues.** Dans la plupart des cas, les utilisateurs ne doivent pas avoir à faire défiler la chaîne la plus longue possible qu’ils entrent ou affichent.
-   **Incluez 30 pour cent supplémentaires** (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte (mais pas les nombres) qui sera localisé.
-   **Si l’entrée attendue n’a pas de taille particulière, choisissez une largeur qui est cohérente avec les autres zones de texte ou contrôles de la fenêtre.**
-   **Dimensionnez les zones de texte sur plusieurs lignes pour afficher un nombre entier de lignes de texte.**

## <a name="labels"></a>Étiquettes

### <a name="text-box-labels"></a>Étiquettes de zone de texte

-   Toutes les zones de texte ont besoin d’étiquettes. Écrivez l’étiquette en tant que mot ou expression, pas en tant que phrase, en terminant par un signe deux-points et en utilisant du [texte statique](glossary.md).

    **Exceptions :**

    -   Zones de texte avec des invites à l’endroit où l’espace est au niveau Premium.
    -   Pour l’étiquetage, un groupe de zones de texte utilisé pour l' **entrée de données mises en forme** doit être traité comme une seule zone de texte.
    -   Si une zone de texte est subordonnée à une case d’option ou à une case à cocher et qu’elle est introduite par son étiquette se terminant par un signe deux-points, ne placez pas d’étiquette supplémentaire sur la zone de texte.
    -   **Omettez les étiquettes de contrôle qui restatent l’instruction principale.** Dans ce cas, l’instruction principale prend le signe deux-points (sauf s’il s’agit d’une question) et la clé d’accès.

        **Acceptable:**

        ![capture d’écran de la zone de texte avec l’étiquette répétitive](images/ctrl-text-boxes-image26.png)

        Dans cet exemple, l’étiquette de la zone de texte n’est qu’une REstate de l’instruction principale.

        **Conseillé**

        ![capture d’écran de la zone de texte avec l’instruction principale uniquement ](images/ctrl-text-boxes-image27.png)

        Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend le signe deux-points et la clé d’accès.

-   Attribuez une clé d’accès unique. Pour connaître les instructions d’attribution de clé d’accès, consultez [clavier](inter-keyboard.md).
-   Utilisez les majuscules comme pour les phrases.
-   Placez l’étiquette à gauche ou au-dessus de la zone de texte, puis alignez l’étiquette sur le bord gauche de la zone de texte. Si l’étiquette est située à gauche, aligne verticalement le texte de l’étiquette avec le texte de la zone de texte.

    **Correct :**

    ![capture d’écran de l’étiquette alignée à gauche au-dessus de la zone de texte ](images/ctrl-text-boxes-image28.png)

    ![capture d’écran de l’étiquette alignée sur le texte à gauche de la zone de texte ](images/ctrl-text-boxes-image29.png)

    Dans ces exemples, l’étiquette en haut est alignée sur le bord gauche de la zone de texte, et l’étiquette à gauche s’aligne sur le texte de la zone de texte.

    **Incorrect :**

    ![capture d’écran de l’étiquette alignée sur le texte au-dessus de la zone de texte ](images/ctrl-text-boxes-image30.png)

    ![capture d’écran de l’étiquette alignée en haut à gauche de la zone de texte ](images/ctrl-text-boxes-image31.png)

    Dans ces exemples incorrects, l’étiquette en haut est alignée sur le texte de la zone de texte, et l’étiquette à gauche s’aligne sur le haut de la zone de texte.

-   Vous pouvez spécifier des unités (par exemple, des secondes ou des connexions) entre parenthèses après l’étiquette.
-   Si une zone de texte accepte un nombre de caractères arbitrairement réduit, vous pouvez indiquer l’entrée maximale dans l’étiquette. La largeur de la zone de texte doit également suggérer la taille maximale.

    ![capture d’écran de la zone de texte mot de passe ](images/ctrl-text-boxes-image32.png)

    Dans cet exemple, l’étiquette indique le nombre maximal de caractères.

-   Ne faites pas du contenu de la zone de texte (ou de son étiquette d’unités) une partie d’une phrase, car cela n’est pas localisable.
-   Si la zone de texte peut être utilisée pour entrer plusieurs éléments, indiquez clairement comment séparer les éléments dans l’étiquette.

    ![capture d’écran de noms séparés par un point-virgule ](images/ctrl-text-boxes-image33.png)

    Dans cet exemple, le séparateur d’éléments est indiqué dans l’étiquette.

-   Pour obtenir des instructions sur l’indication des entrées requises, consultez entrée requise dans les [boîtes de dialogue](win-dialog-box.md).

### <a name="instruction-labels"></a>Étiquettes d’instruction

-   Si vous devez ajouter du texte d’instructions sur une zone de texte, ajoutez-la au-dessus de l’étiquette. Utilisez des phrases complètes avec la ponctuation finale.
-   Utilisez les majuscules comme pour les phrases.
-   Les informations supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes. Placez ces informations entre parenthèses entre l’étiquette et le signe deux-points, ou sans parenthèses sous la zone de texte.

    ![capture d’écran des informations ajoutées en dessous de la zone de texte ](images/ctrl-text-boxes-image34.png)

    Dans cet exemple, des informations supplémentaires sont placées sous la zone de texte.

### <a name="prompt-labels"></a>Étiquettes d’invite

-   Conservez le texte de l’invite concis. Vous pouvez utiliser des fragments au lieu de phrases entières.
-   Utilisez les majuscules comme pour les phrases.
-   N’utilisez pas de ponctuation de fin ni de points de suspension.
-   Si l’invite indique aux utilisateurs d’entrer des informations qui seront traitées par un bouton en regard de la zone de texte, placez simplement le bouton en regard de la zone de texte. N’utilisez pas l’invite pour demander aux utilisateurs de cliquer sur le bouton (par exemple, n’écrivez pas de texte d’invite indiquant, faites glisser un fichier, puis cliquez sur Envoyer).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des zones de texte :

-   Utilisez type pour faire référence aux interactions de l’utilisateur qui nécessitent une saisie ou un collage ; Sinon, utilisez la touche entrée si les utilisateurs peuvent placer des informations dans la zone de texte à l’aide d’autres moyens, par exemple en sélectionnant la valeur dans une liste ou en utilisant un bouton Parcourir.
-   Utilisez SELECT pour faire référence à une entrée dans une zone de texte en lecture seule.
-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez le mot zone. N’incluez pas le trait de soulignement ou le signe deux-points. Ne faites pas référence à une zone de texte sous la forme d’une zone de texte ou d’un champ.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

    Exemple : tapez votre mot de passe dans la zone **mot de passe** , puis cliquez sur **OK**.

-   Si la zone de texte requiert un format spécifique, documentez uniquement le format acceptable le plus couramment utilisé. Permet aux utilisateurs de découvrir eux-mêmes d’autres formats. Vous souhaitez être flexible avec les formats de données, mais cela ne devrait pas aboutir à une documentation complexe.

    **Correct :**

    Entrez le numéro de série du composant en utilisant le format 1234-56-7890.

    **Incorrect :**

    Entrez le numéro de série du composant en utilisant l’un des formats suivants :

    1234567890

    1234-56-7890

    1234 56 7890

