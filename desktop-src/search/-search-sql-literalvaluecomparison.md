---
description: La comparaison de valeurs littérales utilise des opérateurs de comparaison standard pour faire correspondre une colonne à valeur unique à une valeur littérale.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparaison de valeurs littérales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e311c6f98c1114b63a1bf650d6e7be004e1e8e4cf5848b962a7cbf8049bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227174"
---
# <a name="literal-value-comparison"></a>Comparaison de valeurs littérales

La comparaison de valeurs littérales utilise des opérateurs de comparaison standard pour faire correspondre une colonne à valeur unique à une valeur [littérale](-search-sql-literals.md) . Pour plus d’informations sur la comparaison de colonnes à valeurs multiples, consultez [comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md).

Le prédicat de comparaison de valeur littérale a la syntaxe suivante :


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> La partie droite de la comparaison doit être un littéral. Vous ne pouvez pas comparer une colonne à une valeur calculée et vous ne pouvez pas comparer une colonne à une autre colonne.

 

La partie colonne est une colonne de propriété valide et peut être convertie en un autre type si nécessaire. Si vous le souhaitez, vous pouvez placer le nom de colonne entre guillemets doubles pour une meilleure lisibilité sans affecter les fonctionnalités. Pour plus d’informations, consultez [cast du type de données d’une colonne](-search-sql-castingdatacolumntype.md).

Le littéral peut être n’importe quel littéral de chaîne, numérique, hexadécimal, booléen ou de date, placé entre guillemets simples. Seules les correspondances exactes sont reconnues, et les caractères génériques sont ignorés. Le littéral peut également être converti en un autre type.

## <a name="comparison-operators"></a>Opérateurs de comparaison

Le tableau suivant décrit les opérateurs de comparaison pris en charge.



| Opérateur de comparaison | Description              |
|---------------------|--------------------------|
| =                   | Égal à                 |
| ! = ou <>      | Différent de             |
| >                | Supérieur à             |
| >=               | Supérieur ou égal à |
| <                | Inférieur à                |
| <=               | Inférieur ou égal à    |



 

 

conjointement avec l’opérateur « = », Windows langage SQL de recherche (SQL) prend en charge l’utilisation de mots clés before et after, qui spécifient si la requête doit comparer des valeurs de colonne avant ou après une valeur spécifiée, dans un ordre de tri du dictionnaire.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Exemples

Voici des exemples de prédicats de comparaison de valeurs littérales.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat LIKE](-search-sql-like.md)
</dt> <dt>

[DATEADD, fonction](-search-sql-dateadd.md)
</dt> <dt>

[Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Prédicat NULL](-search-sql-null.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



