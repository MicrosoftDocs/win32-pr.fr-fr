---
description: La table de contrôle définit les contrôles qui apparaissent dans chaque boîte de dialogue.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Table de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e1832a2cb600e8d7a27b43bc28c94836396d74a50a90b44d0e5013bde973c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638531"
---
# <a name="control-table"></a>Table de contrôle

La table de contrôle définit les contrôles qui apparaissent dans chaque boîte de dialogue.

La table de contrôle contient les colonnes suivantes.



| Colonne        | Type                               | Clé | Nullable |
|---------------|------------------------------------|-----|----------|
| Boîte de dialogue\_      | [Identificateur](identifier.md)       | O   | N        |
| Contrôler       | [Identificateur](identifier.md)       | O   | N        |
| Type          | [Identificateur](identifier.md)       | N   | N        |
| X             | [Integer](integer.md)             | N   | N        |
| O             | [Integer](integer.md)             | N   | N        |
| Width         | [Integer](integer.md)             | N   | N        |
| Height        | [Integer](integer.md)             | N   | N        |
| Attributs    | [DoubleInteger](doubleinteger.md) | N   | O        |
| Propriété      | [Identificateur](identifier.md)       | N   | O        |
| Texte          | [Correct](formatted.md)         | N   | O        |
| Contrôle \_ suivant | [Identificateur](identifier.md)       | N   | O        |
| Aide          | [Text](text.md)                   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_
</dt> <dd>

Clé externe de la première colonne de la [table de boîte de dialogue](dialog-table.md), nom de la boîte de dialogue.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Régulation
</dt> <dd>

Nom du contrôle. Ce nom doit être unique dans une boîte de dialogue, mais il peut être répété dans différentes boîtes de dialogue. La colonne de contrôle associée à la \_ colonne de boîte de dialogue forment la clé primaire de cette table.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Type du contrôle. Pour obtenir la liste des types de contrôle, consultez [contrôles](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordonnée horizontale de l’angle supérieur gauche de la limite rectangulaire du contrôle. Il doit s’agir d’un nombre non négatif. Consultez [attribut de contrôle de position](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordonnée verticale de l’angle supérieur gauche de la limite rectangulaire du contrôle. Il doit s’agir d’un nombre non négatif. Consultez [attribut de contrôle de position](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largeur
</dt> <dd>

Largeur de la limite rectangulaire du contrôle. Il doit s’agir d’un nombre non négatif. Consultez [attribut de contrôle de position](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Celle
</dt> <dd>

Hauteur de la limite rectangulaire du contrôle. Il doit s’agir d’un nombre non négatif. Consultez [attribut de contrôle de position](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Un mot 32 bits qui spécifie les indicateurs binaires à appliquer à ce contrôle. Il doit s’agir d’un nombre non négatif, et les valeurs autorisées dépendent du type de contrôle. Pour obtenir la liste de tous les attributs de contrôle et la valeur à entrer dans ce champ, consultez [attributs du contrôle](control-attributes.md).

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Nom d’une propriété définie à lier à ce contrôle. La case d’option, la zone de liste et les valeurs de zone de liste déroulante sont liées à un groupe en étant liées à la même propriété. Cette colonne est requise pour les contrôles actifs.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Chaîne localisable utilisée pour définir le texte initial contenu dans un contrôle. La chaîne peut également contenir des propriétés incorporées. Pour la syntaxe d’une chaîne mise en forme contenant des propriétés, consultez la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Spécifiez la taille, la police et la couleur du texte en ajoutant un préfixe à la chaîne de texte { \\ style}, où style est un style de texte créé dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). La chaîne de texte est tronquée si elle est trop longue pour tenir sur le contrôle. La chaîne de texte peut être vide.

La création spéciale de la chaîne de texte [mise en forme](formatted.md) dans ce champ est obligatoire si le texte doit être affiché par un [contrôle de texte](text-control.md) situé dans une boîte de dialogue avec l’attribut TrackDiskpace. C’est le cas spécifié par le [bit de style de la boîte de dialogue TrackDiskSpace](trackdiskspace-dialog-style-bit.md) qui apparaît dans les attributs de la [table Dialog](dialog-table.md). Dans ce cas, si la chaîne mise en forme dans la colonne text de la table de contrôle commence par « \[ » et se termine par « \] », vous devez ajouter un espace à la fin de la chaîne. Par exemple, si DlgTextFont est une propriété qui est définie sur « { \\ DlgFontBold} », la chaîne mise en forme « \[ DlgTextFont \] mytext \[ ProductName \] » requiert l’espace à la fin après le crochet fermant. Cet espace supplémentaire est requis par le programme d’installation pour afficher correctement le texte dans le contrôle de texte.

Vous pouvez entrer une brève chaîne de texte descriptive pour les contrôles [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md)et [SelectionTree](selectiontree-control.md). Ce texte n’est pas visible par l’utilisateur, mais il peut être lu par les lecteurs d’écran comme description du contrôle.

Voir aussi [accessibilité](accessibility.md).

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Contrôle \_ suivant
</dt> <dd>

Nom d’un autre contrôle dans la même boîte de dialogue et une clé externe pour la deuxième colonne de la table de contrôle. Si le focus dans la boîte de dialogue se trouve sur le contrôle dans la colonne de contrôle, le fait d’appuyer sur la touche Tab déplace le focus sur le contrôle figurant dans la \_ colonne contrôle suivant. Par conséquent, cette colonne est utilisée pour spécifier l’ordre de tabulation des contrôles dans la boîte de dialogue. Les liens entre les contrôles doivent former un cycle fermé. Certains contrôles, tels que les contrôles de texte statique, peuvent être omis du cycle. Dans ce cas, ce champ peut être laissé vide.

Voir aussi [accessibilité](accessibility.md).

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Aide
</dt> <dd>

Chaînes de texte localisables et facultatives qui sont utilisées avec le bouton aide. La chaîne est divisée en deux parties par un caractère de séparation ( \| ). La première partie de la chaîne est utilisée comme texte info-bulle. Ce texte est utilisé par les lecteurs d’écran pour les contrôles qui contiennent une image. La deuxième partie de la chaîne est réservée à une utilisation ultérieure. Le caractère de séparation est requis même si un seul des deux genres de texte est présent.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs entières de x, y, Width et Height se trouvent dans les [unités d’installation](installer-units.md), et non dans les unités de boîte de dialogue. Une unité d’installation est égale à 1 douzième la hauteur de la taille de police MS sans serif à 10 points. Les coordonnées des contrôles sont relatives au panneau.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 



