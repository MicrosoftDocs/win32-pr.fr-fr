---
description: Un correctif qui ne doit plus être utilisé peut être éliminé de la séquence de mise à jour corrective.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Élimination des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521473"
---
# <a name="eliminating-patches"></a>Élimination des correctifs

Un correctif qui ne doit plus être utilisé peut être éliminé de la séquence de mise à jour corrective. Cela empêche l’application du correctif lorsque l’application cible est corrigée. Cela est différent de la suppression d’un correctif qui est déjà appliqué à une application. Pour plus d’informations sur la suppression des correctifs appliqués, consultez [suppression des correctifs](removing-patches.md).

* * Windows Installer 3,0 et versions ultérieures : * *

Les correctifs qui comportent la table [MsiPatchSequence](msipatchsequence-table.md) peuvent utiliser ce tableau pour éliminer les correctifs de la séquence de mise à jour corrective. Un correctif peut éliminer les correctifs qui le précèdent dans la séquence de mise à jour corrective et remplacer les informations de ces correctifs par leurs propres informations. Le correctif qui spécifie les correctifs à éliminer et les correctifs en cours d’élimination doit avoir une table MsiPatchSequence contenant des informations.

Si les correctifs et correctifs logiciels supprimés n’ont pas de tables [MsiPatchSequence](msipatchsequence-table.md) , le package de correctifs peut spécifier une liste de correctifs à supprimer de la séquence de mise à jour de la propriété [**Résumé du numéro de révision**](revision-number-summary.md) . Windows Installer 3,0 ignore cette liste si les correctifs supprimés ou de remplacement ont une table MsiPatchSequence.

Lorsque le package de correctifs contient des correctifs avec les informations de séquence de la table [MsiPatchSequence](msipatchsequence-table.md) et certains correctifs sans ces informations, Windows Installer 3,0 séquence les correctifs dans l’ordre décrit dans la section suivante : mise en séquence des [correctifs](sequencing-patches.md).

Par exemple, Patch1, Patch2 et Patch3 peuvent être trois correctifs qui n’ont pas la table [MsiPatchSequence](msipatchsequence-table.md) . Patch2 peut être un correctif qui s’applique uniquement si Patch1 a déjà été appliqué à l’application. Patch3 peut être un patch ultérieur qui contient toutes les informations dans Patch1 et élimine Patch1 de la séquence de mise à jour corrective. Cela signifie que lorsque Patch3 est appliqué, patch 2 devient également inapplicable, car il nécessite Patch1. Toutes les informations contenues dans Patch2 seul ne sont pas remises à l’application.

**Windows Installer 2,0 :** Non pris en charge. La seule méthode disponible consiste à spécifier la liste des correctifs à supprimer de la séquence de mise à jour corrective dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) .

> [!Note]  
> Les rédacteurs de correctifs doivent utiliser les fonctions [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) et [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) pour déterminer la séquence des correctifs qui sont réellement appliqués au produit, car l’élimination de certains correctifs peut rendre d’autres correctifs non applicables.

 

 

 



