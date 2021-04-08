---
description: La fonction DATEADD effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date. Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Fonction DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112434"
---
# <a name="dateadd-function"></a>Fonction DATEADD

La fonction DATEADD effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date. Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.

## <a name="syntax"></a>Syntaxe


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Arguments

*DateTimeUnits*

Spécifie les unités du paramètre *DateTime* : année, trimestre, mois, semaine, jour, heure, minute ou seconde. Cette valeur respecte la casse et les guillemets ne sont pas requis autour du paramètre.

*OffsetValue*

Spécifie l’offset de temps, dans les unités spécifiées par le paramètre *DateTimeUnits* . **OffsetValue** doit être un entier négatif. Les valeurs positives ne sont pas prises en charge.

*DateTime*

Spécifie un horodatage à partir duquel calculer le décalage. Il ne peut pas s’agir d’un littéral de date. Il doit s’agir de GETGMTDATE ou du résultat d’une autre fonction DATEADD.

## <a name="remarks"></a>Notes

La fonction DATEADD ne peut être utilisée que dans les comparaisons de valeurs littérales et uniquement à droite de l’opérateur de comparaison.

La fonction GETGMTDATE retourne la date et l’heure actuelles en heure GMT (Greenwich Mean Time). N’oubliez pas que cette valeur peut ne pas être la même que l’heure locale de votre ordinateur.

N’utilisez pas l’opérateur de comparaison égal à (=), car la représentation temporelle interne peut produire des erreurs d’arrondi qui aboutissent à des résultats de correspondance inattendus.

Vous pouvez utiliser plusieurs fonctions DATEADD pour combiner des unités de décalage.

### <a name="examples"></a>Exemples

L’exemple suivant de clause WHERE correspond à des documents qui ont été modifiés au cours des cinq derniers jours :


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



L’exemple suivant de clause WHERE correspond à des documents qui ont été modifiés au cours des deux derniers jours et quatre heures :


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



