---
description: ICE48 recherche des répertoires qui sont codés en dur sur des chemins d’accès locaux dans la table de propriétés.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521032"
---
# <a name="ice48"></a>ICE48

ICE48 recherche des répertoires qui sont codés en dur sur des chemins d’accès locaux dans la [table de propriétés](property-table.md).

Ne codez pas en dur les chemins d’accès aux lecteurs locaux, car les ordinateurs diffèrent au cours de l’installation du lecteur local. Cette pratique peut être acceptable si vous déployez une application sur un grand nombre d’ordinateurs sur lesquels les portions appropriées des lecteurs sont identiques.

## <a name="result"></a>Résultats

ICE48 publie un message d’erreur s’il existe un répertoire codé en dur vers un chemin d’accès local dans la table de propriétés.

## <a name="example"></a>Exemple

ICE48 signale l’avertissement suivant pour l’exemple indiqué.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Table de répertoires](directory-table.md) (partielle)



| Répertoire | Répertoire \_ parent | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Table de propriétés](property-table.md) (partielle)



| Propriété | Valeur      |
|----------|------------|
| Dir1     | d : \\ source |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



