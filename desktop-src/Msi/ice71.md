---
description: ICE71 vérifie que la table des médias contient une entrée dont le depatinage est égal à 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952730"
---
# <a name="ice71"></a>ICE71

ICE71 vérifie que la [table des médias](media-table.md) contient une entrée dont le depatinage est égal à 1. (Windows Installer suppose que le package. msi est sur le disque 1.)

## <a name="result"></a>Résultats

ICE71 renvoie une erreur si la table de média ne contient pas d’entrée avec un depatinage égal à 1.

## <a name="example"></a>Exemple

ICE71 signale l’erreur suivante pour l’exemple indiqué.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 corriger cette erreur, modifiez le depatinage de l’entrée où le package est stocké sur 1.

[Table des médias](media-table.md) (partielle)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



