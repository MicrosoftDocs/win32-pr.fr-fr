---
description: La \_ Table Columns est une table système en lecture seule qui contient le catalogue de colonnes. Elle répertorie les colonnes de toutes les tables. Vous pouvez interroger cette table pour savoir si une colonne donnée existe.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Table _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093046"
---
# <a name="_columns-table"></a>\_Table colonnes

La \_ Table Columns est une table système en lecture seule qui contient le catalogue de colonnes. Elle répertorie les colonnes de toutes les tables. Vous pouvez interroger cette table pour savoir si une colonne donnée existe.

La \_ Table Columns contient les colonnes suivantes.



| Colonne | Type                   | Clé | Nullable |
|--------|------------------------|-----|----------|
| Table de charge de travail  | [Text](text.md)       | O   | N        |
| Number | [Integer](integer.md) | O   | N        |
| Nom   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Nom de la table qui contient la colonne.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Certain
</dt> <dd>

Ordre de la colonne dans la table.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de la colonne.

</dd> </dl>

## <a name="remarks"></a>Notes

étant donné que la \_ table columns est une table système qui ne peut pas être modifiée par le biais de requêtes SQL, vous ne pouvez pas obtenir les clés primaires avec la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou la [**propriété PrimaryKeys**](database-primarykeys.md).

Seules les colonnes persistantes sont stockées dans la \_ Table Columns. Pour déterminer s’il existe une colonne temporaire, vous devez créer une vue à l’aide d’une \* instruction SELECT sur la table, puis parcourir tous les champs d’un enregistrement retourné par la fonction [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) avec l' \_ option MSICOLINFO Names.

 

 



