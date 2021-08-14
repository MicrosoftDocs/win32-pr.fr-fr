---
description: l’exemple suivant montre comment Windows Installer 3,0 et versions ultérieures peuvent être utilisés pour appliquer des correctifs dans l’ordre dans lequel ils sont créés.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Exemple de mise à jour corrective multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8d33d103bb27fde3b7fdc4ee46a0c5d946e73b6948513ea1b8fffb7bab30bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943366"
---
# <a name="multiple-patching-example"></a>Exemple de mise à jour corrective multiple

l’exemple suivant montre comment Windows Installer 3,0 et versions ultérieures peuvent être utilisés pour appliquer des correctifs dans l’ordre dans lequel ils sont créés.

## <a name="example"></a> Exemple

Dans cet exemple, il existe trois correctifs, QFE1, QFE2 et ServicePack1, et chacun d’eux a une table [MsiPatchSequence](msipatchsequence-table.md) . Ces correctifs ont été créés pour être appliqués à la version 1,0 de l’application.



| Nom du correctif   | Type de correctif    | Numéro de séquence |
|--------------|---------------|-----------------|
| QFE1         | Petite mise à jour  | 1.1.0           |
| QFE2         | Petite mise à jour  | 1.2.0           |
| ServicePack1 | Mise à niveau mineure | 1.3.0           |



 

La table [MsiPatchSequence](msipatchsequence-table.md) de chaque correctif n’a qu’un seul enregistrement qui contient la famille des correctifs, le code du produit et le numéro de séquence. Les trois correctifs sont tous appliqués au même produit et appartiennent à la même famille de correctifs, nommée AppPatch. Aucun des correctifs n’a l’attribut **msidbPatchSequenceSupersedeEarlier** .

[Table MsiPatchSequence](msipatchsequence-table.md) pour la [petite mise à jour](small-updates.md)qfe1. 

| PatchFamily | ProductCode                            | Séquence | Attributs |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Table MsiPatchSequence](msipatchsequence-table.md) pour la [petite mise à jour](small-updates.md)QFE2. 

| PatchFamily | ProductCode                            | Séquence | Attributs |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[Table MsiPatchSequence](msipatchsequence-table.md) pour la [mise à niveau mineure](minor-upgrades.md)ServicePack1. 

| PatchFamily | ProductCode                            | Séquence | Attributs |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

si un utilisateur installe la version 1,0 du produit, puis applique QFE2, puis qu’à une date ultérieure décide d’appliquer QFE1, Windows Installer garantit que la séquence effective de l’application de correctifs au produit est QFE1 appliquée avant QFE2. si l’utilisateur applique ServicePack1, puis applique QFE2 et QFE1 à une date ultérieure, Windows Installer garantit que la séquence effective de l’application de correctifs au produit est QFE1 en avance de QFE2 et en avance sur ServicePack1.

Si ServicePack1 a **msidbPatchSequenceSupersedeEarlier** défini dans la colonne attributs de sa table [MsiPatchSequence](msipatchsequence-table.md) , cela signifie que l’Service Pack contient toutes les modifications apportées à qfe1 et QFE2. Dans ce cas, QFE1 et QFE2 ne sont pas appliqués lorsque ServicePack1 est appliqué.

**Windows Installer 2,0 :** Non pris en charge. les Versions antérieures à Windows Installer 3,0 peuvent installer un seul correctif par transaction et les correctifs sont appliqués dans l’ordre dans lequel ils sont fournis. Pour l’exemple précédent, si QFE2 est appliqué en premier, puis QFE1 est appliqué, il s’agit de deux transactions et les correctifs sont appliqués à la version 1,0 de l’application dans la séquence QFE2 suivie de QFE1. Si ServicePack1 est appliqué en premier, QFE1 ou QFE2 ne peut pas être appliqué dans une transaction ultérieure, car ServicePack1 est une mise à niveau mineure qui modifie la version de l’application. QFE1 et QFE2 peuvent être appliqués uniquement à la version 1,0 de l’application.

 

 



