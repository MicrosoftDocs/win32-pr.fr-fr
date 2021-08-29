---
description: ICE70 vérifie que les valeurs entières pour les entrées de Registre sont spécifiées correctement.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd76d38b796650346a8651fe5a3817edfaa412dfe7772f2dba9c0295f7eebdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649269"
---
# <a name="ice70"></a>ICE70

ICE70 vérifie que les valeurs entières pour les entrées de Registre sont spécifiées correctement. Les valeurs de la forme \# \# Str, \# % non développé Str ne sont pas validées. Les valeurs de la forme \# xhex, \# xhex, \# Integer et \# \[ Property \] sont validées. Le tableau suivant fournit une brève vue d’ensemble.



| Valeur                 | Validation                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#Str               | valide                                                                         |
| \#% non développé     | valide                                                                         |
| \#xHex, \# xHex         | Validez les caractères hexadécimaux valides (0-9, a-f, A-F). Les propriétés sont autorisées ici. |
| \#+ int, \# -int, \# int | Validez les caractères numériques valides (0-9). Les propriétés sont autorisées ici.     |



 

La syntaxe d’une valeur entière à entrer dans le Registre est un \# entier où entier est numérique.

## <a name="result"></a>Résultat

ICE70 signale une erreur si les valeurs entières pour les entrées de registre ne sont pas spécifiées correctement.

## <a name="example"></a>Exemples

ICE70 signale les erreurs suivantes pour l’exemple donné.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

Pour corriger cette erreur : Si vous souhaitez que la valeur soit numérique, modifiez la valeur pour utiliser tous les caractères numériques. Si vous souhaitez que la valeur soit une chaîne, elle doit être précédée de deux' \# ' ( \# \# ) au lieu d’un seul.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

Pour corriger cette erreur : les caractères hexadécimaux valides sont 0-9, A-F et a-f. Seuls ces caractères peuvent être suivis de \# x (ou \# x).

[Table du Registre](registry-table.md) (partielle)



| Registre | Valeur    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Remarques

-   \#\[MyProperty \] est valide.
-   \#\[MyProperty n’est pas valide (crochet de fin manquant).
-   \#\[myprop1 \] \[ myprop2 est valide. (Même si la dernière parenthèse fermante ne contient pas le crochet de fin, myprop1 peut avoir la valeur \# Str, ce qui signifie que \# \# Str \[ myprop2, qui est valide
-   \#\]MyProperty \[ n’est pas valide
-   Toute propriété incorporée dans une chaîne de valeur ne peut pas être dans le \[ \] formulaire $compkey, \[ \# filekey \] ou \[ ! filekey, \] car ces propriétés ne sont pas numériques. Toutefois, il existe une exception, \# \[ MyProperty \] \[ $compkey \] (ou \[ \# filekey \] ou \[ ! filekey \] ) est valide, car, comme avec le précédent, \[ MyProperty \] peut évaluer en \# Str.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



