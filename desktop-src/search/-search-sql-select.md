---
description: 'L’exemple suivant illustre la syntaxe de base de l’instruction SELECT pour une requête locale :'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instruction SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227194"
---
# <a name="select-statement"></a>Instruction SELECT

L’exemple suivant illustre la syntaxe de base de l’instruction SELECT pour une requête locale :


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



L’exemple suivant illustre la partie colonne de la syntaxe de l’instruction SELECT :


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Le ou les spécificateurs de colonne doivent être des colonnes de noms de propriété valides, séparées par des virgules. Les noms de colonnes valides sont des descriptions de propriété inscrites ou sont définis par le schéma de système de propriétés de l’interpréteur de commandes. Vous pouvez sélectionner uniquement les colonnes qui sont marquées comme récupérables dans le schéma du système de propriétés. Si vous utilisez la casse mixte pour identifier les propriétés qui ne sont pas des propriétés définies par le système, vous devez placer le spécificateur de colonne entre guillemets doubles. Les noms de propriété définis par le système incluent toutes les propriétés commençant par « System » (par exemple, System. contact. FirstName) et ne requièrent pas de guillemets.

> [!Note]  
> Vous pouvez également placer les noms des propriétés définies par le système entre guillemets doubles pour une meilleure lisibilité. Cela n’affecte pas la compatibilité.

 

Lorsque la requête retourne un document qui n’a pas la colonne demandée, la valeur de cette colonne pour le document est **null**.

Vous devez fournir au moins un nom de colonne dans une instruction SELECT. dans la requête langage SQL (SQL), vous êtes autorisé à utiliser l’astérisque ( \* ) pour spécifier que toutes les colonnes d’une table doivent être retournées. Toutefois, aucun ensemble de propriétés défini et fixe ne s’applique à tous les documents. pour cette raison, le SQL astérisque n’est pas autorisé dans le <columns> spécificateur de l’instruction SELECT.

## <a name="getting-the-top-n-results"></a>Obtention des n premiers résultats

Vous pouvez spécifier le nombre maximal de résultats à renvoyer à l’aide de la syntaxe TOP :


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Conversion de types de données de colonne

Parfois, vous devrez peut-être convertir des données de type chaîne extraites de documents en un autre type de données afin qu’une comparaison appropriée puisse être effectuée. Pour plus d’informations, consultez [cast du type de données d’une colonne](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Exemples

Les exemples suivants retournent le nom et l’URL des documents correspondants.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Conversion du type de données d’une colonne](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



