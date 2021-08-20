---
description: ICE71 vérifie que la table des médias contient une entrée dont le depatinage est égal à 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142513"
---
# <a name="ice71"></a>ICE71

ICE71 vérifie que la [table des médias](media-table.md) contient une entrée dont le depatinage est égal à 1. (Windows Installer suppose que le package .msi est sur le disque 1.)

## <a name="result"></a>Résultat

ICE71 renvoie une erreur si la table de média ne contient pas d’entrée avec un depatinage égal à 1.

## <a name="example"></a>Exemples

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

 

 



