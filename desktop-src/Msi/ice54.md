---
description: ICE54 recherche les composants qui utilisent un fichier compagnon comme chemin d’accès de clé.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865477"
---
# <a name="ice54"></a>ICE54

ICE54 recherche les composants qui utilisent un fichier compagnon comme chemin d’accès de clé.

Le fichier de chemin d’accès de clé d’un composant ne doit pas dériver sa version d’un autre fichier. Cela peut entraîner l’échec de l’installation de certains fichiers. Pour plus d’informations sur les fichiers d’accompagnement, consultez la [table file](file-table.md) .

## <a name="result"></a>Résultats

ICE54 publie un avertissement si un composant a un fichier de chemin d’accès de clé qui dérive sa version d’un autre fichier.

## <a name="example"></a>Exemple

ICE54 retourne l’avertissement suivant pour l’exemple indiqué.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Table des composants](component-table.md) (partielle)



| Composant  | Attribut | KeyPath |
|------------|-----------|---------|
| Composant1 | 0         | Fichier1   |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Version | Language |
|-------|---------|----------|
| Fichier1 | Fichier2   |          |
| Fichier2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



