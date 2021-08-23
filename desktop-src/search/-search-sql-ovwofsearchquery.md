---
description: le langage SQL de recherche Windows (SQL) est similaire à une requête de SQL standard.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: vue d’ensemble de la syntaxe de SQL de recherche Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f34f321bef35ab9f5198345a2630d20b80275b794f53a0c47aabf7667f2e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594739"
---
# <a name="overview-of-windows-search-sql-syntax"></a>vue d’ensemble de la syntaxe de SQL de recherche Windows

le langage SQL de recherche Windows (SQL) est similaire à une requête de SQL standard. Il est illustré dans les deux syntaxes suivantes :


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

Dans l’exemple de requête suivant, les valeurs nombre de pages et date de création sont retournées pour tous les documents contenant plus de 50 pages, triés par ordre croissant de nombre de pages.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

la syntaxe de requête de recherche Windows prend en charge de nombreuses options, ce qui permet d’obtenir des requêtes plus compliquées.

Le tableau suivant décrit chaque clause dans les instructions SELECT ou GROUP ON et les fonctionnalités prises en charge.

| Clause                                              | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [REGROUPER... ...](-search-sql-group-on-over.md) | Spécifie comment regrouper les résultats retournés par la requête. Vous pouvez spécifier les plages de regroupement et spécifier plusieurs colonnes pour le regroupement. Par exemple, vous pouvez regrouper les résultats sur une plage de tailles de fichier (taille < 100, 100 <= taille < 1000 ; 1000 <= taille) et imbriquer des regroupements.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Spécifie les colonnes retournées par la requête.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Spécifie l’ordinateur et le catalogue dans lesquels effectuer la recherche.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Spécifie ce qui constitue un document correspondant. Cette clause présente de nombreuses options, permettant ainsi un contrôle riche sur les conditions de recherche. Par exemple, vous pouvez effectuer une mise en correspondance avec des mots, des expressions, des formes de mots infléchis, des chaînes, des valeurs numériques et de bits, ainsi que des tableaux à valeurs multiples. Vous pouvez également appliquer des pondérations statistiques aux conditions de correspondance et combiner des conditions de correspondance avec des opérateurs booléens. |
| [ORDER BY](-search-sql-orderby.md)                 | Spécifie l’ordre de tri pour les résultats retournés par la requête. Vous pouvez spécifier plusieurs champs sur lesquels les résultats sont triés, et vous pouvez utiliser l’ordre croissant ou décroissant.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Exemples de code

l’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via SQL. l’exemple de code WSOleDB illustre Active Template Library (ATL) OLE DB l’accès aux applications de recherche Windows, ainsi que deux méthodes supplémentaires pour récupérer les résultats de Windows recherche. Les deux exemples sont disponibles sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Informations de référence

[Littéraux](-search-sql-literals.md)

[Utilisation de recherches localisées](-search-sql-usinglocsearches.md)

[Compréhension des valeurs de pertinence](-search-sql-understandingrelevancevalues.md)

[Mappages de propriétés](-search-3x-wds-propertymappings.md)

[Syntaxe de requête avancée](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Conceptuel

[SQL Extensions dans Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL fonctionnalités non disponibles dans Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificateurs](-search-sql-identifiers.md)

[Respect de la casse dans les recherches](-search-sql-casesensitivityinsearches.md)

[Respect des signes diacritiques dans les recherches](-search-sql-accentinsensitivitysearches.md)

[Conversion du type de données d’une colonne](-search-sql-castingdatacolumntype.md)

[Mappages de type de données](-search-sql-datatypemappings.md)
