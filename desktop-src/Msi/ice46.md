---
description: ICE46 recherche des propriétés personnalisées dans les conditions, le texte mis en forme et d’autres emplacements qui diffèrent d’une propriété définie par le système uniquement par la casse d’un ou plusieurs caractères.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021548"
---
# <a name="ice46"></a>ICE46

ICE46 recherche des propriétés personnalisées dans les conditions, le texte mis en forme et d’autres emplacements qui diffèrent d’une propriété définie par le système uniquement par la casse d’un ou plusieurs caractères.

## <a name="result"></a>Résultats

ICE46 publie un message d’information s’il existe une propriété personnalisée dans une condition, du texte mis en forme et d’autres emplacements qui diffèrent des propriétés définies par le système uniquement dans le cas d’un ou plusieurs caractères.

## <a name="example"></a>Exemple

ICE46 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE46                                                                                                                                            | Description                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La propriété ReinstallMode définie dans la table de propriétés diffère d’une autre propriété définie uniquement par la casse.                                                   | Le nom de la propriété définie par le système **REINSTALLMODE** diffère de la propriété personnalisée par la casse uniquement. Les propriétés respectent la casse, de sorte que la propriété personnalisée n’est pas la même que la propriété système. Il s’agit d’une cause courante d’erreurs. |
| Propriété « MyProperty » référencée dans la colonne « InstallExecuteSequence ». La condition’de la ligne’InstallFinalize’diffère d’une propriété définie par la casse uniquement. | La table de propriétés définit la table MyProperty, mais la propriété référencée est MyProperty. Les propriétés étant sensibles à la casse, les deux propriétés ne sont pas les mêmes. Il s’agit d’une cause courante d’erreurs.                          |



 

[Table de propriétés](property-table.md)



| Propriété      | Valeur   |
|---------------|---------|
| ReinstallMode | omus    |
| MyProperty    | une valeur |



 

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action          | Condition  |
|-----------------|------------|
| InstallFinalize | MyProperty |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



