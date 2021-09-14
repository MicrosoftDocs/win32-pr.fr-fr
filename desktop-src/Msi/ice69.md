---
description: ICE69 vérifie que toutes les sous-chaînes de la forme \[ $componentkey \] dans une chaîne mise en forme ne font pas référence à des composants.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021504"
---
# <a name="ice69"></a>ICE69

ICE69 vérifie que toutes les sous-chaînes de la forme \[ $componentkey \] dans une chaîne [mise en forme](formatted.md) ne font pas référence à des composants. Une référence entre composants se produit lorsque la \[ \] propriété $componentkey d’une chaîne mise en forme fait référence à un composant autre que le composant stocké dans la \_ colonne composant de vos tables.

Les problèmes de référencement entre composants proviennent de la façon dont les chaînes [mises en forme](formatted.md) sont évaluées. Si le composant référencé avec la \[ propriété $componentkey \] est déjà installé et n’est pas modifié pendant l’installation actuelle (par exemple, s’il est réinstallé, déplacé vers la source, etc.), l’expression \[ $componentkey \] prend la valeur null, car l’état d’action du composant dans \[ $componentkey \] est null. Des problèmes similaires peuvent se produire pendant les opérations de mise à niveau et de réparation.

## <a name="result"></a>Résultats

ICE69 retourne une erreur si un \[ $componentkey \] sous-chaîne d’une chaîne [mise en forme](formatted.md) fait référence à un composant d’une autre fonctionnalité. ICE69 retourne un avertissement si un \[ $componentkey \] sous-chaîne d’une chaîne mise en forme fait référence à un composant dans la même fonctionnalité. (La table [FeatureComponents](featurecomponents-table.md) est utilisée pour déterminer ce mappage. Elle doit être mappée à la même fonctionnalité pour l’avertissement. Le fait de référencer des composants dans des fonctionnalités parentes ou de référencer des composants dans des fonctionnalités enfants est considéré comme une erreur.)

ICE69 signale une erreur si la \[ \# \] sous-chaîne FileKey dans une chaîne [mise en forme](formatted.md) fait référence à un fichier qui n’est pas spécifié dans la table de [fichiers](file-table.md) comme appartenant au même composant.

## <a name="example"></a>Exemple

ICE69 signale les éléments suivants pour les exemples indiqués.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Pour corriger cette erreur, ne faites pas référence à des composants. Modifiez le \[ $componentkey \] pour qu’il corresponde au composant du raccourci.

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Composant\_ | Argument     |
|-----------|-------------|--------------|
| Test      | QuickTest   | $Test-v \[\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

Les tables de [verbes](verb-table.md) et d' [Extensions](extension-table.md) sont des cas spéciaux dans le cas où la table de verbes fait référence à une extension qui appartient à un composant. Toutefois, une extension peut appartenir à plusieurs composants, car la clé primaire de la table d’extension est constituée des colonnes d’extension et de composant \_ . Vous pouvez logiquement avoir la situation suivante.

[Table de verbes](verb-table.md) (partielle)



| Extension | Verbe\_ | Argument                |
|-----------|--------|-------------------------|
| TST       | ouvert   | -v \[ $COMP 1 \] \[ $COMP 2\] |



 

[Table d’extension](extension-table.md) (partielle)



| Extension | Composant\_ |
|-----------|-------------|
| TST       | COMP1       |
| TST       | COMP2       |



 

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_ | Composant\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Test        |
| Feature2  | Test 2       |



 

Dans ce cas, vous devez vous assurer qu’au moins une des \[ Propriétés de $componentkey \] correspond à une valeur non null. Toutefois, chaque \[ \] propriété $componentkey dans la colonne argument de la table de verbes ( \[ $comp 1 \] et \[ $COMP 2 \] dans l’exemple ci-dessus) doit référencer un composant possible inclus avec l’extension associée au verbe. Une référence comme \[ $COMP 3 \] génère un avertissement à partir de ICE69.

La [table AppID](appid-table.md) présente une situation similaire à celle de la table de verbes. Elle utilise la [table de classe](class-table.md) pour sa référence de composant. Dans ce cas, la table AppId est validée de la même façon que la validation Verb-Extension (désormais AppId-Class).

La colonne argument de la table de classes est validée comme le [raccourci](shortcut-table.md), le [registre](registry-table.md)et les tables similaires.

## <a name="table-used-during-execution-only-if-found"></a>Table utilisée lors de l’exécution (uniquement si elle est trouvée)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registre](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Raccourci](shortcut-table.md)

[Verb](verb-table.md)

[Extension](extension-table.md)

[Classe](class-table.md)

[AppId](appid-table.md)

[Environment](environment-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



