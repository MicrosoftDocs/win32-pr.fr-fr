---
description: Les cases d’option ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un groupe de cases d’option qui fonctionne comme un contrôle RadioButtonGroup. Le tableau RadioButton répertorie les boutons de tous les groupes.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: Table RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097f8fbe3081c865e3668631ed0fa9d43a4488cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202740"
---
# <a name="radiobutton-table"></a>Table RadioButton

Les cases d’option ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un groupe de cases d’option qui fonctionne comme un [contrôle RadioButtonGroup](radiobuttongroup-control.md). Le tableau RadioButton répertorie les boutons de tous les groupes.

La table RadioButton contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Commande    | [Integer](integer.md)       | O   | N        |
| Valeur    | [Correct](formatted.md)   | N   | N        |
| X        | [Integer](integer.md)       | N   | N        |
| O        | [Integer](integer.md)       | N   | N        |
| Largeur    | [Integer](integer.md)       | N   | N        |
| Hauteur   | [Integer](integer.md)       | N   | N        |
| Texte     | [Correct](formatted.md)   | N   | O        |
| Aide     | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Propriété nommée à être liée à cette case d’option. Tous les boutons liés à la même propriété deviennent partie intégrante du même groupe.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Entier positif utilisé pour déterminer l’ordre des éléments d’une liste. Il n’est pas nécessaire que les entiers soient consécutifs.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Chaîne de valeur associée à ce bouton. La sélection du bouton affecte la valeur à la propriété associée.

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordonnée horizontale dans le groupe de l’angle supérieur gauche du rectangle englobant de la case d’option. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordonnée verticale dans le groupe de l’angle supérieur gauche du rectangle englobant de la case d’option. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largeur
</dt> <dd>

Largeur du bouton. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Celle
</dt> <dd>

Hauteur du bouton. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Titre localisable et visible à assigner à la case d’option. Si le texte est trop long pour être contenu dans le contrôle, il est tronqué. Si le bouton affiche une icône ou une image bitmap, cette colonne contient le nom de l’image, qui est une clé dans la [table binaire](binary-table.md). Il n’existe aucun moyen d’afficher à la fois une image et du texte sur un bouton.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Aide
</dt> <dd>

Chaînes d’aide utilisées avec le bouton. Le texte est facultatif et peut être localisé. La chaîne est divisée en deux parties séparées par un caractère ( \| ). La première partie de la chaîne est utilisée comme texte info-bulle. Ce texte est affiché par les lecteurs d’écran pour les contrôles qui contiennent une image. La deuxième partie est utilisée pour l’aide contextuelle, bien que l’aide contextuelle n’ait pas encore été implémentée. Le caractère de séparation est requis même si un seul des deux genres de texte est présent.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs entières de x, y, Width et Height se trouvent dans les [unités d’installation](installer-units.md), et non dans les unités de boîte de dialogue. Une unité d’installation est égale à 1 douzième la hauteur de la taille de police MS sans serif à 10 points. Les coordonnées des contrôles sont relatives au panneau.

Les coordonnées des boutons sont données par rapport au groupe. Si les coordonnées du groupe sont modifiées, les boutons du groupe restent dans la même position relative.

Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction **MsiFormatRecord** peut interpréter. La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.

Chaque contrôle RadioButtonGroup est associé à une propriété. La valeur par défaut de cette propriété doit être initialisée dans la [table des propriétés](property-table.md). Dans chaque RadioButtonGroup spécifié dans la table RadioButton, il peut y avoir une case d’option qui a une valeur dans le champ de valeur qui correspond à la valeur par défaut de cette propriété. Il s’agit du bouton par défaut pour le contrôle RadioButtonGroup. Le bouton par défaut est initialement affiché comme sélectionné dans le contrôle.

Notez que l’utilisateur ne peut pas modifier le focus dans une boîte de dialogue en appuyant sur la touche TAB pour un contrôle RadioButtonGroup jusqu’à ce que l’un des boutons du groupe ait été sélectionné. Pour que le focus se déplace sur ce groupe de boutons en appuyant sur la touche TAB, spécifiez l’un des boutons comme bouton par défaut pour le groupe.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



