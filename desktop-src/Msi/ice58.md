---
description: ICE58 vérifie que votre table des médias ne contient pas plus de 80 lignes.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528229"
---
# <a name="ice58"></a>ICE58

ICE58 vérifie que votre [table des médias](media-table.md) ne contient pas plus de 80 lignes.

## <a name="result"></a>Résultat

les avertissements signalés par ICE58 provoquent l’échec de l’installation, à moins que le package ne soit installé avec Windows Installer 2,0 ou une version ultérieure. à partir de Windows Installer 2,0, la restriction à plus de 80 entrées de table multimédia est supprimée. Aucun avertissement n’est émis si la propriété de [**Résumé du nombre de pages**](page-count-summary.md) du package est supérieure ou égale à 150. les Packages de schéma 200 ou version ultérieure peuvent uniquement être installés par Windows Installer 2,0 ou version ultérieure.

## <a name="example"></a>Exemples

ICE58 signale les erreurs et avertissements suivants pour l’exemple indiqué.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Pour corriger cette erreur, supprimez toutes les entrées de table de média inutilisées, consolidez les entrées de table de média qui font référence au même support et reconditionnez votre application pour réduire le support requis.

[Table des médias](media-table.md) (partielle)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



