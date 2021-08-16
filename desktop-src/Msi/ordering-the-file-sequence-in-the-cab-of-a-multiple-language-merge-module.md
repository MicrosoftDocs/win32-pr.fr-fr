---
description: Les modules de fusion multilingues, les transformations de langage et les fichiers CAB doivent être créés de telle sorte que l’ordre des fichiers corresponde à l’ordre spécifié dans la table de fichiers.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Classement de la séquence de fichiers dans le fichier CAB d’un module de fusion à plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942806"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Classement de la séquence de fichiers dans le fichier CAB d’un module de fusion à plusieurs langues

Les modules de fusion multilingues, les transformations de langage et les fichiers CAB doivent être créés de telle sorte que l’ordre des fichiers dans le .cab corresponde à l’ordre d’installation des fichiers spécifiés dans la [table file](file-table.md), même après l’application de la transformation de langue. Si l’ordre dans le module et dans le .cab ne correspond pas, le module de fusion ne peut pas être utilisé.

Assignez à chaque fichier dans le module, un numéro de séquence unique qui est indépendant de sa langue, puis utilisez toujours ce numéro de séquence pour le fichier. Utilisez la même séquence lors de la génération du fichier CAB et de la création d’une transformation de langue.

Étant donné que le programme d’installation installe uniquement les fichiers répertoriés dans la [table de fichiers](file-table.md), l’utilisation d’une séquence de fichiers globale dans le fichier CAB, la [table de fichiers](file-table.md)et la transformation de langue permet à l’outil de fusion d’ignorer tous les fichiers supplémentaires stockés dans le fichier CAB qui ne sont pas répertoriés dans la table de [fichiers](file-table.md). D’autres fichiers peuvent exister dans le fichier CAB, mais ils ne doivent pas être listés dans la [table file](file-table.md). Par exemple, un module qui installe Code.dll, anglais. dat, allemand. dat et français. dat peut utiliser l’ordre de séquence de fichiers Global suivant.



| Fichier        | Séquence |
|-------------|----------|
| Code.Dll    | 1        |
| Anglais. dat | 2        |
| Allemand. dat  | 3        |
| Français. dat  | 4        |



 

Les transformations de langage peuvent ensuite être créées pour modifier la [table de fichiers](file-table.md) du module pour l’anglais, l’allemand ou le français.

[Table de fichiers](file-table.md) (partielle pour l’anglais)



| Fichier        | Séquence |
|-------------|----------|
| Code.Dll    | 1        |
| Anglais. dat | 2        |



 

[Table de fichiers](file-table.md) (partielle pour l’allemand)



| Fichier       | Séquence |
|------------|----------|
| Code.Dll   | 1        |
| Allemand. dat | 3        |



 

[Table de fichiers](file-table.md) (partielle pour le français)



| Fichier       | Séquence |
|------------|----------|
| Code.Dll   | 1        |
| Français. dat | 4        |



 

Pour plus d’informations, consultez [création d’une transformation de langage pour un module de fusion multilingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md) et [tables de fichiers de module de fusion de création](authoring-merge-module-file-tables.md).

 

 



