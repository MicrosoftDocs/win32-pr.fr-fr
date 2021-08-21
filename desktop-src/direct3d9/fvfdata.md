---
description: Spécifie les données de maillage moins les données de position.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec21cf354ed10e7229f1392dd31bf32bc416c27dff90d5d70858aeefc1b5c68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987989"
---
# <a name="fvfdata"></a>FVFData

Spécifie les données de maillage moins les données de position.

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Où :

-   dwFVF : code de la Commission.
-   nDWords-données binaires. Nombre de DWORDs.
-   Data \[ nDWords \] -tableau de DWORDS contenant les données de chaque élément vertex.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



