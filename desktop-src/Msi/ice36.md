---
description: ICE36 valide que chaque icône de la table des icônes figure au moins une fois dans la propriété ARPPRODUCTICON ou dans la classe, ProgId ou Shortcut tables.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021567"
---
# <a name="ice36"></a>ICE36

ICE36 valide que chaque icône de la table des icônes figure au moins une fois dans la propriété [**ARPPRODUCTICON**](arpproducticon.md) ou dans la [classe](class-table.md), [ProgID](progid-table.md)ou [Shortcut](shortcut-table.md) tables.

Pendant la publication, le programme d’installation installe toutes les icônes listées dans la [table icône](icon-table.md) sur l’ordinateur de l’utilisateur. Le fait d’avoir des icônes inutilisées dans la table d’icônes n’empêche pas l’exécution de l’installation, mais elle augmente inutilement la taille du fichier .msi et le temps et l’espace requis pour publier une fonctionnalité.

Si aucune icône n’est référencée dans la propriété ou la table et qu’aucune interface utilisateur n’est fournie pour créer une référence au moment de l’exécution, vous devez supprimer l’icône pour obtenir de meilleures performances.

## <a name="result"></a>Résultats

ICE36 publie un message si une icône de la table d’icônes n’est pas référencée dans la [classe](class-table.md), le [ProgID](progid-table.md)ou les tables de [raccourcis](shortcut-table.md) et si aucune interface utilisateur n’est fournie pour créer une telle référence au moment de l’exécution.

## <a name="example"></a>Exemple

ICE36 signale l’erreur suivante pour l’exemple indiqué.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Table d’icônes](icon-table.md) (partielle)



| Nom  | Données     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[Table ProgID](progid-table.md) (partielle)



| ProgID    |
|-----------|
| Property1 |



 

[Table de classe](class-table.md) (partielle)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Icône\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



