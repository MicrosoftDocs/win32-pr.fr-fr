---
description: ICE65 vérifie que la table d’environnement ne possède pas de valeurs de préfixe ou d’ajout non valides.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021511"
---
# <a name="ice65"></a>ICE65

ICE65 vérifie que la [table d’environnement](environment-table.md) ne possède pas de valeurs de préfixe ou d’ajout non valides.

L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICE65 provoque généralement des problèmes d’installation, de désinstallation ou de réparation de la variable d’environnement. Par exemple, seules certaines valeurs d’une variable particulière peuvent être supprimées si une ou plusieurs des valeurs de cette variable ont un séparateur de fin.

## <a name="result"></a>Résultats

ICE65 publie un avertissement ou une erreur si la table d’environnement contient des valeurs de préfixe ou d’ajout non valides.

## <a name="example"></a>Exemple

ICE65 signale l’erreur et l’avertissement suivants pour l’exemple indiqué.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

La valeur null de fin à la fin de la valeur ( \[ ~ \] ) marque cette valeur comme étant ajoutée à toute valeur existante. Le caractère situé juste avant la valeur null (point-virgule) devient le séparateur de cette valeur. Cette valeur comporte également un point-virgule au début de la chaîne.

Pour corriger cette erreur, supprimez simplement le point-virgule de début.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

La valeur null de début dans la valeur ( \[ ~ \] ) marque cette valeur à ajouter à toute valeur existante. Le caractère situé juste après la valeur null devient le séparateur de cette valeur. Dans ce cas, ce caractère est la lettre « e », qui se produit également au milieu de la chaîne à ajouter. Cette condition (avec un séparateur identique à un caractère dans la chaîne à ajouter) peut provoquer des résultats imprévisibles.

La lettre « e », en tant que lettre courante, est susceptible d’être trouvée dans la valeur. Un meilleur choix serait « ; » ou un autre caractère non alphanumérique. (Toutefois, si la valeur est un chemin d’accès, «  : » et « \\ » et «» sont des choix risqués.)

Pour résoudre cet avertissement, utilisez un autre caractère de séparation.

[Table d’environnement](environment-table.md)



| Composant | Répertoire | Attributs         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



