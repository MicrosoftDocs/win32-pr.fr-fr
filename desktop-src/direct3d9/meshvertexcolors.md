---
description: Spécifie des couleurs de vertex pour un maillage, au lieu d’appliquer un matériau par visage ou par maillage.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392475"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Spécifie des couleurs de vertex pour un maillage, au lieu d’appliquer un matériau par visage ou par maillage.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Où :

-   nVertexColors : nombre de couleurs. Cela correspond au nombre de vertex dans la maille.
-   Tableau IndexColor vertexColors \[ nVertexColors \] -tableau de couleurs indexées. Consultez [**IndexedColor**](indexedcolor.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



