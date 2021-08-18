---
description: Les lignes d’un ListView ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un ListView qui fonctionne comme un contrôle. Le tableau ListView définit les valeurs de tous les ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tableau ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a84ebab6c90486283c3dd8d4731cc0b7f3aff11a5459a0e93496bab83d7c277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013077"
---
# <a name="listview-table"></a>Tableau ListView

Les lignes d’un ListView ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un ListView qui fonctionne comme un contrôle. Le tableau ListView définit les valeurs de tous les ListView.

La table ListView contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Commande    | [Integer](integer.md)       | O   | N        |
| Valeur    | [Correct](formatted.md)   | N   | N        |
| Texte     | [Correct](formatted.md)   | N   | O        |
| Binaire2\_ | [Identificateur](identifier.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Propriété nommée à être liée à cet élément. Tous les éléments liés à la même propriété deviennent partie intégrante du même ListView.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Entier positif utilisé pour déterminer l’ordre des éléments qui s’affichent dans une liste ListView unique. Il n’est pas nécessaire que les entiers soient consécutifs. Si un ListView est défini comme étant ordonné, tous les éléments doivent avoir une valeur de classement. Si le ListView est défini comme non ordonné, cette colonne est ignorée.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Chaîne de valeur associée à cet élément. La sélection de la ligne affecte cette valeur à la propriété associée.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Texte visible et localisable à assigner à l’élément. Si cette entrée ou la colonne entière est manquante, le texte prend par défaut l’entrée correspondante dans la valeur.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binaire2\_
</dt> <dd>

Données de l’image de l’icône. Il s’agit d’une clé étrangère de la [table binaire](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction MsiFormatRecord peut interpréter. La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



