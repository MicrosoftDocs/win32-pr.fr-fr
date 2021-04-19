---
description: Les lignes d’une zone de liste déroulante ne sont pas traitées comme des contrôles individuels. elles font partie d’une zone de liste déroulante unique qui fonctionne comme un contrôle. Ce tableau répertorie les valeurs de chaque zone de liste déroulante.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Table ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521298"
---
# <a name="combobox-table"></a>Table ComboBox

Les lignes d’une zone de liste déroulante ne sont pas traitées comme des contrôles individuels. elles font partie d’une zone de liste déroulante unique qui fonctionne comme un contrôle. Ce tableau répertorie les valeurs de chaque zone de liste déroulante.

La table de zone de liste déroulante contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Commande    | [Integer](integer.md)       | O   | N        |
| Valeur    | [Correct](formatted.md)   | N   | N        |
| Texte     | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Propriété nommée à être liée à cet élément. Tous les éléments liés à la même propriété deviennent partie intégrante de la même zone de liste déroulante.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Entier positif utilisé pour déterminer l’ordre des éléments qui s’affichent dans une liste de zone de liste déroulante unique. Il n’est pas nécessaire que les entiers soient consécutifs. Si une zone de liste déroulante est définie comme étant ordonnée, tous les éléments doivent avoir une valeur d’ordre. Si la zone de liste déroulante est définie comme non triée, cette colonne est ignorée.

Nombres positifs uniquement.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Chaîne de valeur associée à cet élément. La sélection de cette ligne de la zone de liste déroulante affecte cette valeur à la propriété associée (spécifiée dans la propriété).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Texte visible et localisable à assigner à l’élément. Si cette entrée ou la colonne entière est manquante, le texte par défaut est l’entrée de la valeur.

</dd> </dl>

## <a name="remarks"></a>Notes

Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction **MsiFormatRecord** peut interpréter. La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



