---
title: À propos des contrôles de sélecteur de date et d’heure
description: Un contrôle de sélecteur de date et d’heure (PAO) fournit une interface simple et intuitive par le biais de laquelle échanger des informations de date et d’heure avec un utilisateur.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04604c01a73aa8f2ebb8542061412372faee5282
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031974"
---
# <a name="about-date-and-time-picker-controls"></a>À propos des contrôles de sélecteur de date et d’heure

Un *contrôle de sélecteur de date et d’heure (PAO)* fournit une interface simple et intuitive par le biais de laquelle échanger des informations de date et d’heure avec un utilisateur. Par exemple, avec un contrôle de PAO, vous pouvez demander à l’utilisateur d’entrer une date, puis de récupérer facilement la sélection.

Les rubriques suivantes sont présentées :

-   [Interface utilisateur du sélecteur de date et heure](#date-and-time-picker-user-interface)
-   [Styles et formats de contrôle de sélecteur de date et d’heure](#date-and-time-picker-control-styles-and-formats)
    -   [Formats prédéfinis](#preset-formats)
    -   [Formats personnalisés](#custom-formats)
    -   [Chaînes de format](#format-strings)
    -   [Champs de rappel](#callback-fields)
-   [Messages de notification de contrôle de sélecteur de date et heure](#date-and-time-picker-control-notification-messages)
-   [Rubriques connexes](#related-topics)

> [!Note]
> Windows ne prend pas en charge les dates antérieures à 1601. Pour plus d’informations, consultez la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
>
> Le contrôle est basé sur le calendrier grégorien, qui a été introduit dans 1753. Elle ne calcule pas les dates qui sont cohérentes avec le calendrier julien.

## <a name="date-and-time-picker-user-interface"></a>Interface utilisateur du sélecteur de date et heure

La zone cliente d’un contrôle de sélecteur de date et d’heure (PAO) affiche des informations de date ou d’heure, ou les deux, et agit comme l’interface par le biais de laquelle les utilisateurs modifient les informations. La date peut être sélectionnée à partir d’un calendrier ou à l’aide d’un contrôle up-up. l’heure peut être modifiée en tapant dans les champs définis par les [chaînes de format](#format-strings)du contrôle. Éventuellement, le contrôle affiche une case à cocher. Lorsqu’elle est activée, la valeur dans le contrôle peut être Récupérée ; dans le cas contraire, le contrôle est considéré comme non initialisé.

L’illustration suivante montre une fenêtre qui contient trois contrôles de sélecteur de dates. Le premier contrôle de sélecteur de dates a été créé avec le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , le deuxième avec le style [**\_ UpDown de DTS**](date-and-time-picker-control-styles.md) et le troisième sans style spécial. Dans le troisième contrôle, l’utilisateur a cliqué sur la flèche vers le bas pour afficher le calendrier.

![capture d’écran d’une fenêtre qui illustre trois styles de contrôles de sélecteur de dates](images/dtpdatepick.png)

L’illustration suivante montre une fenêtre avec trois contrôles qui contiennent l’heure.

Le premier contrôle a été créé avec le style [**DTS \_ TimeFormat**](date-and-time-picker-control-styles.md) et affiche l’heure par défaut, qui se compose de quatre champs. L’utilisateur peut taper une valeur valide dans l’un de ces champs, ou sélectionner le champ et modifier la valeur à l’aide du contrôle up-up ou des touches de direction.

Le deuxième contrôle affiche un jeu de formats personnalisé à l’aide de [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat). Comme pour le premier contrôle, l’utilisateur peut modifier les champs d’heure en tapant ou en utilisant les touches de direction. Le jour de la semaine peut être modifié en sélectionnant une date dans le calendrier qui s’ouvre lorsque l’utilisateur clique sur la flèche orientée vers le bas.

Le troisième contrôle montre comment un texte arbitraire peut être ajouté au contrôle. L’utilisateur peut sélectionner une heure (de 1 à 24) en tapant, en utilisant les touches de direction ou en utilisant le contrôle up-up.

![capture d’écran d’une fenêtre qui affiche trois contrôles qui contiennent l’heure](images/dtpdatetimepick.png)

Le contrôle PAO met automatiquement à jour les informations internes en fonction de l’entrée de l’utilisateur. Le contrôle reconnaît ce qui suit comme une entrée valide.



| Catégorie d’entrée | Description                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Touches de direction     | Le contrôle accepte les touches de direction pour parcourir les champs dans le contrôle et modifier les valeurs. L’utilisateur peut appuyer sur les touches ou pour se déplacer dans le contrôle si l’utilisateur tente de se déplacer au-delà du dernier champ dans une direction donnée, le focus clavier « habille » dans le champ du côté opposé du contrôle. Les clés et modifient de façon incrémentielle les valeurs dans le champ actuel. |
| Fin et démarrage   | Le contrôle accepte les \_ clés virtuelles VK end et VK \_ Virtual pour remplacer la valeur dans le champ actuel par ses limites supérieure et inférieure, respectivement.                                                                                                                                                                                                                          |
| Touches de fonction  | La clé active le mode édition. La clé permet au contrôle d’afficher un contrôle de calendrier mensuel déroulant (en appuyant sur le fait également).                                                                                                                                                                                                                                          |
| Nombres        | Le contrôle accepte une entrée numérique dans des segments à deux caractères. Si la valeur entrée par l’utilisateur n’est pas valide (par exemple, si vous définissez le mois sur 14), le contrôle le rejette et réinitialise l’affichage à la valeur précédente.                                                                                                                                                                |
| Plus et moins | Le contrôle accepte les \_ touches virtuelles VK Add et VK \_ Subtract du pavé numérique pour incrémenter et décrémenter la valeur dans le champ actuel.                                                                                                                                                                                                                             |



 

Les contrôles de PAO qui n’utilisent pas le style de [**\_ déverrouillage DTS**](date-and-time-picker-control-styles.md) affichent un bouton fléché. Si l’utilisateur clique sur ce bouton, un contrôle Month Calendar disparaît. L’utilisateur peut sélectionner une date spécifique en cliquant sur une zone du calendrier.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Styles et formats de contrôle de sélecteur de date et d’heure

Les contrôles de sélecteur de date et d’heure (PAO) ont plusieurs [styles de contrôle de sélecteur de date et d’heure](date-and-time-picker-control-styles.md) qui déterminent l’apparence et le comportement d’un contrôle. Spécifiez le style lors de la création du contrôle avec le paramètre *dwStyle* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Pour récupérer ou modifier le style de la fenêtre après avoir créé le contrôle, utilisez [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

### <a name="preset-formats"></a>Formats prédéfinis

Trois formats prédéfinis sont disponibles pour l’affichage de la date et l’autre pour l’affichage de l’heure. Définissez ces formats en choisissant l’un des styles de fenêtre suivants.



|                                                                                                       |                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_LONGDATEFORMAT Dts**](date-and-time-picker-control-styles.md)                 | L’affichage ressemble à ce qui suit : « vendredi 19 avril 1996 ».      |
| [**\_SHORTDATEFORMAT Dts**](date-and-time-picker-control-styles.md)               | L’affichage ressemble à ce qui suit : « 4/19/96 ».                     |
| [**\_SHORTDATECENTURYFORMAT Dts**](date-and-time-picker-control-styles.md) | **Version 5,80**. L’affichage ressemble à ce qui suit : « 4/19/1996 ». |
| [**DTS \_ TimeFormat**](date-and-time-picker-control-styles.md)                         | L’affichage ressemble à ce qui suit : « 5:31:42 PM ».                  |



 

### <a name="custom-formats"></a>Formats personnalisés

Un contrôle de PAO s’appuie sur une chaîne de format pour déterminer comment elle affichera des champs d’informations. Si les formats prédéfinis ne sont pas suffisants, vous pouvez créer un format personnalisé en définissant votre propre chaîne de format. Les formats personnalisés offrent une plus grande souplesse pour une application. Elles vous permettent de spécifier l’ordre dans lequel le contrôle affichera les champs d’informations. Vous pouvez inclure du texte de corps et des champs de rappel pour demander des informations à l’utilisateur. Une fois la chaîne créée, vous devez l’assigner au contrôle PAO avec un message [**DTM \_ SETFORMAT**](dtm-setformat.md) .

### <a name="format-strings"></a>Chaînes de format

Une chaîne de format PAO se compose d’une série d’éléments qui représentent une information particulière et qui définissent son format d’affichage. Les éléments s’affichent dans l’ordre dans lequel ils apparaissent dans la chaîne de format.

Les éléments de format de date et d’heure seront remplacés par la date et l’heure réelles. Ils sont définis par les groupes de caractères suivants.



| Élément | Description                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Jour à un ou deux chiffres.                                                        |
| "dd"    | Jour à deux chiffres. Les valeurs de jour à un seul chiffre sont précédées d’un zéro.                |
| "ddd"   | Abréviation du jour de la semaine à trois caractères.                                         |
| "dddd"  | Nom complet du jour de la semaine.                                                            |
| "h"     | Heure à une ou deux chiffres au format 12 heures.                                     |
| "hh"    | Heure à deux chiffres au format 12 heures. Les valeurs à un seul chiffre sont précédées d’un zéro. |
| "H"     | Heure à une ou deux chiffres au format 24 heures.                                     |
| "HH"    | Heure à deux chiffres au format 24 heures. Les valeurs à un seul chiffre sont précédées d’un zéro. |
| "m"     | Minute à un ou deux chiffres.                                                     |
| "mm"    | Minute à deux chiffres. Les valeurs à un seul chiffre sont précédées d’un zéro.                 |
| "M"     | Numéro de mois à une ou deux chiffres.                                               |
| "MM"    | Numéro de mois à deux chiffres. Les valeurs à un seul chiffre sont précédées d’un zéro.           |
| "MMM"   | Abréviation de trois caractères du mois.                                           |
| "MMMM"  | Nom complet du mois.                                                              |
| "t"     | L’abréviation AM/PM d’une lettre (c’est-à-dire, AM est affichée sous la forme « A »).              |
| "tt"    | Abréviation AM/PM à deux lettres (c’est-à-dire que AM est affiché sous la forme « AM »).             |
| "yy"    | Les deux derniers chiffres de l’année (c’est-à-dire, 1996 s’affichent sous la forme « 96 »).       |
| "yyyy"  | L’année complète (c’est-à-dire, 1996 s’affichera sous la forme « 1996 »).                       |



 

Pour rendre les informations plus lisibles, vous pouvez ajouter du texte de corps à la chaîne de format en l’entourant de guillemets simples. Les espaces et les signes de ponctuation n’ont pas besoin d’être placés entre guillemets.

> [!Note]  
> Les caractères sans format qui ne sont pas délimités par des guillemets simples entraînent un affichage imprévisible par le contrôle PAO.

Par exemple, pour afficher la date actuelle au format « aujourd’hui : 04:22:31 mardi 23 mars 1996 », la chaîne de format est « » aujourd’hui : «HH » : « m » : dddd MMM JJ « s », « yyyy ». Pour inclure un guillemet simple dans le corps du texte, utilisez deux guillemets simples consécutifs. Par exemple, « n’oubliez pas «MMM JJ », « yyyy » produit une sortie qui ressemble à ceci : n’oubliez pas 23 Mar 1996. Il n’est pas nécessaire d’utiliser des guillemets avec la virgule, donc «« n’oubliez pas » MMM JJ, AAAA» est également valide et produit la même sortie.

### <a name="callback-fields"></a>Champs de rappel

Outre les [chaînes de format](#format-strings) standard et le corps de texte, vous pouvez également définir certaines parties de l’affichage en tant que [champs de rappel](#callback-fields). Ces champs peuvent être utilisés pour demander des informations à l’utilisateur. Pour déclarer un champ de rappel, incluez un ou plusieurs caractères « X » (code ASCII 88) n’importe où dans la chaîne de format. Vous pouvez créer des champs de rappel qui ont une identité unique en répétant le caractère « X ». Par conséquent, la chaîne de format « XX dddd MMM JJ », « yyy XXX » contient deux champs de rappel uniques, « XX » et « XXX ». Comme les autres champs de contrôle de PAO, les champs de rappel sont affichés dans l’ordre de gauche à droite en fonction de leur emplacement dans la chaîne de format.

Lorsque le contrôle de PAO analyse la chaîne de format et rencontre un champ de rappel, il envoie [le \_ format DTN](dtn-format.md) et les codes de notification de [DTN \_ FORMATQUERY](dtn-formatquery.md) . L’élément de chaîne de format correspondant au champ de rappel est inclus avec les notifications pour permettre à l’application réceptrice de déterminer quel champ de rappel est interrogé. Le propriétaire du contrôle doit répondre à ces notifications pour s’assurer que les informations personnalisées s’affichent correctement.

## <a name="date-and-time-picker-control-notification-messages"></a>Messages de notification de contrôle de sélecteur de date et heure

Un contrôle de sélecteur de date et d’heure (PAO) envoie des codes de notification lorsqu’il reçoit des entrées d’utilisateur ou des processus et réagit à des champs de rappel. Le parent du contrôle reçoit ces codes de notification sous la forme de messages [**WM \_ Notify**](wm-notify.md) .

Les codes de notification suivants sont utilisés avec les contrôles de PAO.



| Code de notification                             | Description                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ gros plan](dtn-closeup.md)               | Indique que le calendrier du mois déroulant va être supprimé.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Signale une modification au sein du contrôle PAO.                                                                                                                                                                          |
| [\_liste déroulante DTN](dtn-dropdown.md)             | Indique que le calendrier du mois déroulant va être affiché.                                                                                                                                             |
| [\_format DTN](dtn-format.md)                 | Demande le texte à afficher dans une partie de la chaîne de format décrite comme un champ de rappel.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Demande des informations sur la taille maximale autorisée du texte à afficher dans un champ de rappel.                                                                                                            |
| [DTN \_ USERSTRING](dtn-userstring.md)         | Signale la fin de l’opération de modification d’un utilisateur dans le contrôle. Cette notification est envoyée uniquement par les contrôles PAO qui utilisent le style [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Signale que l’utilisateur a appuyé sur une touche dans un champ de rappel du contrôle PAO.                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle de sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 