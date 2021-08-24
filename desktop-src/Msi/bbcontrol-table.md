---
description: Le tableau BBControl répertorie les contrôles à afficher sur chaque panneau.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Table BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70198167c866195204ec6cbcf644b92f3489a4ff44e14e719efbf5c6647e30c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754369"
---
# <a name="bbcontrol-table"></a>Table BBControl

Le tableau BBControl répertorie les contrôles à afficher sur chaque panneau.

La table BBControl contient les colonnes suivantes.



| Colonne      | Type                               | Clé | Nullable |
|-------------|------------------------------------|-----|----------|
| Blanc\_ | [Identificateur](identifier.md)       | O   | N        |
| BBControl   | [Identificateur](identifier.md)       | O   | N        |
| Type        | [Identificateur](identifier.md)       | N   | N        |
| X           | [Integer](integer.md)             | N   | N        |
| O           | [Integer](integer.md)             | N   | N        |
| Largeur       | [Integer](integer.md)             | N   | N        |
| Hauteur      | [Integer](integer.md)             | N   | N        |
| Attributs  | [DoubleInteger](doubleinteger.md) | N   | O        |
| Texte        | [Text](text.md)                   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Blanc\_
</dt> <dd>

Nom du panneau.

Clé externe vers la colonne de l’une des [tables du tableau blanc](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nom du contrôle. Ce nom doit être unique au sein d’un panneau, mais il peut être répété sur différents panneaux. Cette colonne associée à la \_ colonne de tableau blanc constitue la clé primaire de la table.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Type du contrôle. Seuls les contrôles statiques, tels qu’un [texte](text-control.md), une [bitmap](bitmap-control.md), une [icône](icon-control.md)ou un contrôle personnalisé peuvent être placés sur un panneau. Pour obtenir la liste complète des contrôles, consultez la section [contrôles](controls.md) .

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordonnée horizontale de l’angle supérieur gauche de la limite rectangulaire du contrôle. Les unités sont des [unités d’installation](installer-units.md). Cette coordonnée est mesurée par rapport au contrôle de tableau blanc et non par rapport à la boîte de dialogue. Utilisez uniquement des nombres non négatifs.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordonnée verticale de l’angle supérieur gauche de la limite rectangulaire du contrôle. Les unités sont des [unités d’installation](installer-units.md). Cette coordonnée est mesurée par rapport au contrôle de tableau blanc et non par rapport à la boîte de dialogue. Ce nombre ne doit pas être négatif.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largeur
</dt> <dd>

Largeur de la limite rectangulaire du contrôle. Les unités sont des [unités d’installation](installer-units.md). Ce nombre ne doit pas être négatif.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Celle
</dt> <dd>

Hauteur de la limite rectangulaire du contrôle. Les unités sont des [unités d’installation](installer-units.md). Ce nombre ne doit pas être négatif.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Mot 32 bits spécifiant les indicateurs d’attribut à appliquer à ce contrôle. Ce nombre ne doit pas être négatif et spécifie un attribut pour un contrôle statique qui est valide pour le positionnement sur un panneau. Pour plus d’informations sur les valeurs numériques à entrer dans ce champ, consultez l’attribut particulier sous [attributs de contrôle](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Cette colonne contient une chaîne localisable utilisée pour définir le texte initial dans le contrôle si le contrôle affiche du texte. La chaîne est tronquée si le texte est trop long pour tenir sur le contrôle. Cette colonne contient une clé dans la [table binaire](binary-table.md) si le contrôle est un bouton de commande ou une case à cocher contenant une icône ou une image bitmap. Il n’est pas possible d’afficher à la fois le texte et une image sur le même bouton. Cette colonne peut être laissée vide.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs entières de x, y, Width et Height se trouvent dans les [unités d’installation](installer-units.md), et non dans les unités de boîte de dialogue. Une unité d’installation est égale à 1 douzième la hauteur de la taille de police MS sans serif à 10 points. Les coordonnées des contrôles sont relatives au contrôle de tableau blanc et non à la boîte de dialogue.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



