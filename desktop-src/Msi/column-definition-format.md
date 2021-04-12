---
description: MsiViewGetColumnInfo et la propriété ColumnInfo de l’objet View utilisent le format suivant pour décrire les définitions de colonne de base de données.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Format de définition de colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203219"
---
# <a name="column-definition-format"></a>Format de définition de colonne

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) et la [**propriété COLUMNINFO**](view-columninfo.md) de l’objet [**View**](view-object.md) utilisent le format suivant pour décrire les définitions de colonne de base de données. Chaque colonne est décrite par une chaîne dans le champ d’enregistrement correspondant retourné par la fonction ou la propriété. La chaîne de définition se compose d’une seule lettre représentant le type de données suivi de la largeur de la colonne (en caractères, le cas échéant, octets). Une largeur de zéro désigne une largeur illimitée (par exemple, des champs de texte longs et des flux). Une lettre majuscule indique que les valeurs NULL sont autorisées dans la colonne.



| Descripteur de colonne | Chaîne de définition                 |
|-------------------|-----------------------------------|
| x?                | Chaîne, longueur de variable ( ? = 1-255) |
| consommation                | Chaîne, longueur de variable           |
| i2                | Entier Short                     |
| i4                | Entier long                      |
| v0                | Flux binaire                     |
| activée?                | Chaîne temporaire ( ? = 0-255)        |
| j?                | Entier temporaire ( ? = 0, 1, 2, 4)     |
| O0                | Objet temporaire                  |



 

Les chaînes utilisées pour décrire les colonnes ont la relation suivante avec les chaînes de requête SQL utilisées par CREATe et ALTER. Pour plus d’informations, consultez [syntaxe SQL](sql-syntax.md).



| Valeur renvoyée | Syntaxe SQL                |
|----------------|---------------------------|
| consommation             | LONGCHAR                  |
| fusion             | LONGCHAR LOCALISABLE      |
| x \#           | CHAR ( \# )                  |
| x \#           | CARACTÈRE ( \# )             |
| budget \#           | CHAR ( \# ) localisable      |
| budget \#           | CARACTÈRE ( \# ) localisable |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Si la lettre n’est pas en majuscule, l’instruction SQL doit être ajoutée avec NOT NULL.



| Valeur renvoyée | Syntaxe SQL        |
|----------------|-------------------|
| consommation             | LONGCHAR NON NULL |



 

Le programme d’installation ne limite pas en interne la longueur des colonnes à la valeur spécifiée par le format de définition de colonne. Si les données entrées dans un champ dépassent la longueur de colonne spécifiée, le package ne réussit pas la [validation du package](package-validation.md). Pour passer la validation dans ce cas, les données ou le schéma de base de données doivent être modifiés. La seule méthode pour modifier la longueur de colonne d’une table standard consiste à exporter la table à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), à modifier le fichier. IDT exporté, puis à importer la table à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Les auteurs ne peuvent pas modifier les types de données de colonne, les valeurs null ou les attributs de localisation des colonnes dans les tables standard. Les auteurs peuvent créer des tables personnalisées avec des colonnes ayant des attributs de colonne.

Lorsque vous utilisez [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) pour fusionner une base de données de référence dans une base de données cible, les noms de colonnes, le nombre de clés primaires et les types de données de colonne doivent correspondre. **MsiDatabaseMerge** ignore les attributs de localisation et de longueur de colonne. Si une colonne de la base de données de référence a une longueur supérieure ou égale à la longueur de la colonne dans la base de données cible, **MsiDatabaseMerge** augmente la longueur de colonne dans la base de données cible à la longueur de la base de données de référence.

Lors de l’utilisation de Mergmod.dll version 2,0, l’application d’un module de fusion à un fichier. msi ne modifie jamais la longueur des colonnes ou les types de colonnes d’une table de base de données existante. L’application d’un module de fusion peut toutefois modifier le schéma d’une table de base de données existante si le module ajoute de nouvelles colonnes à une table pour laquelle il est valide pour ajouter des colonnes. Lors de l’utilisation d’une version Mergemod.dll antérieure à la version 2,0, l’application d’un module de fusion ne modifie jamais la longueur des colonnes et ne modifie jamais le schéma de la base de données cible.

 

 



