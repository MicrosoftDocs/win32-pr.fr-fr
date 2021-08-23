---
description: Spécifie des couleurs de vertex pour un maillage, au lieu d’appliquer un matériau par visage ou par maillage.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035f8d51ae692b0edd20f7b06b5ab8e756ff73d9cd8265d64700ce5374f9a15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628329"
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

 

 



