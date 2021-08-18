---
description: Les lignes d’une zone de liste ne sont pas traitées comme des contrôles individuels, mais elles font partie d’une zone de liste qui fonctionne comme un contrôle. La table ListBox définit les valeurs de toutes les zones de liste.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Table ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8877db002185cd675914eca6d5be38454796c7b50af6a48f88e0e63c10c195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043189"
---
# <a name="listbox-table"></a>Table ListBox

Les lignes d’une zone de liste ne sont pas traitées comme des contrôles individuels, mais elles font partie d’une zone de liste qui fonctionne comme un contrôle. La table ListBox définit les valeurs de toutes les zones de liste.

La table ListBox contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Commande    | [Integer](integer.md)       | O   | N        |
| Valeur    | [Correct](formatted.md)   | N   | N        |
| Texte     | [Correct](formatted.md)   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Propriété nommée à être liée à cet élément. Tous les éléments liés à la même propriété deviennent partie intégrante de la même zone de liste.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Entier positif utilisé pour déterminer l’ordre des éléments qui s’affichent dans une zone de liste unique. Si la zone de liste est définie comme étant ordonnée, tous les éléments doivent avoir une valeur d’ordre. Il n’est pas nécessaire que les entiers soient consécutifs. Si la zone de liste est définie comme non triée, cette colonne est ignorée.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Chaîne de valeur associée à cet élément. La sélection de la ligne affecte cette valeur à la propriété associée.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Texte visible localisable à assigner à l’élément. Si cette entrée ou la colonne entière est manquante, le texte prend par défaut l’entrée correspondante dans la valeur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction **MsiFormatRecord** peut interpréter. La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



