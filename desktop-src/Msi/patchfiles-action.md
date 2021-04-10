---
description: L’action PatchFiles interroge la table des correctifs pour déterminer les correctifs à appliquer. L’action PatchFiles effectue également la mise à jour corrective basée sur les octets des fichiers.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Action PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865213"
---
# <a name="patchfiles-action"></a>Action PatchFiles

L’action PatchFiles interroge la [table des correctifs](patch-table.md) pour déterminer les correctifs à appliquer. L’action PatchFiles effectue également la mise à jour corrective basée sur les octets des fichiers.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Si le fichier à corriger n’est pas installé, l’action PatchFiles doit venir après l' [action InstallFiles](installfiles-action.md) qui installe le fichier. Les fichiers précédemment installés peuvent être corrigés à tout moment dans la séquence d’action. L' [action DuplicateFiles](duplicatefiles-action.md) doit venir après l’action PatchFiles pour empêcher la duplication de la version non corrigée du fichier.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                    |
|-------|-----------------------------------------------|
| \[1\] | Identificateur du fichier corrigé.                   |
| \[2\] | Identificateur du répertoire contenant le fichier corrigé. |
| \[3\] | Taille du correctif en octets.                       |



 

 

 



