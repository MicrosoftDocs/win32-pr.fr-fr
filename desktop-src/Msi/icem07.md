---
description: ICEM07 vérifie que l’ordre des fichiers dans la table de séquences correspond à l’ordre des fichiers dans MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef29ffc26658660e9acd09ba108779bf6902d1d0326963765f13b29c99b845ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894519"
---
# <a name="icem07"></a>ICEM07

ICEM07 vérifie que l’ordre des fichiers dans la table de séquences correspond à l’ordre des fichiers dans [MergeModule.CABinet](mergemodule-cabinet.md).

Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.

## <a name="result"></a>Résultat

ICEM07 publie une erreur si l’ordre des fichiers dans la table de fichiers ne correspond pas à l’ordre dans le fichier CAB.

## <a name="example"></a>Exemple

IC0M07 publie le message d’erreur suivant pour l’exemple indiqué.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Table de fichier](file-table.md)



| Fichier          | Séquence |
|---------------|----------|
| Filea. *Guid1* | 1        |
| FileB. *Guid1* | 8        |
| FileC. *Guid1* | 52       |



 

Intégration [MergeModule.CABinet](mergemodule-cabinet.md)



| Fichier          |
|---------------|
| Filea. *Guid1* |
| FileC. *Guid1* |
| Classer. *Guid1* |
| FileB. *Guid1* |



 

Bien qu’il ne soit pas nécessaire que les numéros de séquence de fichier de la table de fichiers soient consécutifs, et que des fichiers supplémentaires puissent exister dans le fichier CAB, la séquence relative de tous les fichiers de la table de fichiers doit correspondre à l’ordre dans [MergeModule.CABinet](mergemodule-cabinet.md). Pour corriger cette erreur, modifiez le numéro de séquence de FileB à venir après FileC pour qu’il corresponde à l’ordre des fichiers dans le CAB, ou régénérez le fichier CAB avec les fichiers dans l’ordre approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



