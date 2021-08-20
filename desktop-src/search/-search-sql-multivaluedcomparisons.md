---
description: Les colonnes stockées dans l’index de contenu peuvent avoir plusieurs valeurs, et ces colonnes à valeurs multiples peuvent être comparées à l’aide du prédicat de comparaison de tableau.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparaisons à valeurs multiples (tableau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043ed6744717ac3156d9dd64f2f6806f2ffc509107f5bcdc8a66980e5cdd0012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863368"
---
# <a name="multi-valued-array-comparisons"></a>Comparaisons à valeurs multiples (tableau)

Les colonnes stockées dans l’index de contenu peuvent avoir plusieurs valeurs, et ces colonnes à valeurs multiples peuvent être comparées à l’aide du prédicat de comparaison de tableau.

Le prédicat de comparaison de tableau a la syntaxe suivante :


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Une erreur est retournée si la référence de colonne n’est pas une colonne à valeurs multiples. Le type de données de la colonne doit être compatible avec les éléments de la liste de comparaison. Si nécessaire, la référence de colonne peut être [convertie](-search-sql-castingdatacolumntype.md) en un autre type de données.

L’opérateur de comparaison (COMP \_ op) peut être l’un des opérateurs de comparaison normaux. Dans une comparaison à valeurs multiples, les opérateurs de comparaison ont des significations légèrement différentes selon qu’un quantificateur est utilisé ou non. Les quantificateurs identifient si une comparaison doit être effectuée sur l’ensemble ou une partie des valeurs de la liste de comparaison. Les fonctions des opérateurs de comparaison sont indiquées dans les tableaux décrivant chaque quantificateur (tout ou partie) plus loin dans ce document.

La valeur après l’opérateur spécifie une valeur littérale unique qui est comparée à tous les éléments de la colonne à valeurs multiples. Si un élément correspond à la valeur, le prédicat a la valeur true.

La liste de comparaison spécifie un tableau de valeurs littérales comparées à la colonne à valeurs multiples. La syntaxe de la liste de comparaison est la suivante :


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Tenez compte de la syntaxe de la liste de comparaison. Le groupe de littéraux qui composent la liste de comparaison doit être entouré de crochets. N’entourez pas les éléments individuels de la liste de comparaison par des crochets. Par conséquent, le tableau \[ 1 \] et le tableau \[ 1, 2, 3 \] sont valides, mais le tableau \[ 1 \[ , 2 \] \[ , 3 \] \] n’est pas.

 

La méthode utilisée pour déterminer si la comparaison à valeurs multiples retourne la valeur true ou false est spécifiée par le quantificateur facultatif. Les sections suivantes décrivent chaque quantificateur et le fonctionnement de chaque opérateur de comparaison lorsque le quantificateur est utilisé.

## <a name="absent-quantifier"></a>Quantificateur absent

Si aucun quantificateur n’est spécifié, chaque élément du côté gauche de la comparaison est comparé à l’élément situé à la même position sur le côté droit. La comparaison commence par le premier élément des tableaux et progresse jusqu’au dernier élément. Si tous les éléments du côté gauche sont équivalents aux éléments correspondants sur le côté droit, le nombre d’éléments de tableau est utilisé pour déterminer le tableau qui est plus grand.

Le tableau suivant montre l’opération des opérateurs de comparaison quand aucun quantificateur n’est spécifié et fournit une brève description de chacun d’eux.



| Opérateur       | Description                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Égal à’retourne la valeur true lorsque chaque élément de gauche a la même valeur que l’élément de droite correspondant, et que les deux tableaux ont le même nombre d’éléments.                                                                                                                                                                                                                     |
| ! = ou <> | 'Différent de’retourne la valeur true lorsqu’un ou plusieurs éléments côté gauche ont des valeurs qui diffèrent des éléments côté droit correspondants, ou lorsque les tableaux de gauche et de droite n’ont pas le même nombre d’éléments.                                                                                                                                                              |
| >           | « Supérieur à » retourne la valeur true lorsque la valeur de chaque élément de gauche est supérieure à la valeur de l’élément de droite correspondant. Si toutes les valeurs d’élément de gauche correspondent exactement aux éléments de droite correspondants et que le tableau de gauche a plus d’éléments que le tableau de droite, « supérieur à » retourne la valeur true.                                                     |
| >=          | 'Supérieur ou égal à’retourne la valeur true lorsque la valeur de chaque élément de gauche est supérieure ou égale à la valeur de l’élément de droite correspondant. Si toutes les valeurs d’élément de gauche sont égales ou supérieures aux éléments de droite correspondants et que le tableau de gauche a le même élément ou plus que le tableau de droite, 'supérieur à’retourne la valeur true. |
| <           | 'Inférieur à’retourne la valeur true lorsque la valeur de chaque élément de gauche est inférieure à la valeur de l’élément de droite correspondant. 'Inférieur à’retourne également true lorsque le côté gauche a moins d’éléments que le côté droit.                                                                                                                                                  |
| <=          | 'Inférieur ou égal à’retourne la valeur true lorsque la valeur de chaque élément de gauche est inférieure ou égale à la valeur de l’élément de droite correspondant. Si toutes les valeurs d’élément de gauche sont égales ou inférieures aux éléments de droite correspondants et que le tableau de gauche a le même ou un moins grand nombre d’éléments que le tableau de droite, 'supérieur à’retourne la valeur true.         |



 

## <a name="all-quantifier"></a>TOUT quantificateur

Le quantificateur ALL spécifie que chaque élément du côté gauche est comparé à chaque élément situé à droite. Pour retourner true, la comparaison doit avoir la valeur true pour chaque élément du côté gauche par rapport à chaque élément situé à droite. Le nombre d’éléments dans les côtés gauche et droit n’a aucun effet sur le résultat.

Le tableau suivant montre comment chaque opérateur de comparaison fonctionne avec le quantificateur ALL.



| Opérateur       | Description                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | « Égal à » retourne la valeur true lorsque chaque valeur d’élément de gauche est la même que chaque valeur d’élément côté droit.                              |
| ! = ou <> | 'Différent de’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est différente de l’une des valeurs d’élément côté droit. |
| >           | « Supérieur à » retourne la valeur true lorsque chaque valeur d’élément de gauche est supérieure à chaque valeur d’élément de droite.                         |
| >=          | 'Supérieur ou égal à’retourne la valeur true lorsque chaque valeur d’élément de gauche est supérieure ou égale à chaque valeur d’élément de droite. |
| <           | 'Inférieur à’retourne la valeur true lorsque chaque valeur d’élément de gauche est inférieure à toutes les valeurs d’élément côté droit.                               |
| <=          | 'Inférieur ou égal à’retourne la valeur true lorsque chaque valeur d’élément de gauche est inférieure ou égale à chaque valeur d’élément de droite.       |



 

## <a name="some-or-any-quantifier"></a>TOUT (ou un) quantificateur

Le quantificateur et le quantificateur ANY peuvent être utilisés indifféremment. À l’instar du quantificateur ALL, le quantificateur SOME spécifie que chaque élément du côté gauche est comparé à chaque élément du côté droit. Pour retourner true, la comparaison doit avoir la valeur true pour au moins l’un des éléments du côté gauche par rapport à tout élément situé à droite. Le nombre d’éléments sur les tableaux à gauche et à droite n’a aucun effet sur le résultat.

Le tableau suivant montre comment chaque opérateur de comparaison fonctionne avec le quantificateur SOME.



| Opérateur       | Description                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est identique à l’une des valeurs d’élément côté droit.                                  |
| ! = ou <> | 'Différent de’retourne la valeur true si aucune des valeurs de l’élément de gauche n’est identique à l’une des valeurs d’élément côté droit.                                      |
| >           | « Supérieur à » retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est supérieure à l’une des valeurs d’élément côté droit.                         |
| >=          | 'Supérieur ou égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est supérieure ou égale à l’une des valeurs d’élément côté droit. |
| <           | 'Inférieur à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est inférieure à l’une des valeurs d’élément côté droit.                               |
| <=          | 'Inférieur ou égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est inférieure ou égale à l’une des valeurs d’élément de droite.       |



 

## <a name="examples"></a>Exemples

L’exemple suivant vérifie si les documents sont dans les catégories « finance » ou « Planning » :


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Les comparaisons suivantes évaluent toutes la valeur true. N’oubliez pas que, dans l’utilisation réelle, la syntaxe de requête de recherche requiert que le côté gauche soit une propriété, et non une valeur littérale.


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat LIKE](-search-sql-like.md)
</dt> <dt>

[Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Prédicat NULL](-search-sql-null.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



