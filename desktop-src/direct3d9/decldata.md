---
description: Décrit une déclaration de vertex.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5686e3344e4642483490c9bd2892cbc92ade290567107b702cc9c56ff351c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803234"
---
# <a name="decldata"></a>DeclData

Décrit une déclaration de vertex.

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Où :

-   nElements : nombre d’éléments de déclaration de vertex.
-   Éléments \[ nElements \] -tableau d’éléments de déclaration de vertex.
-   nDWords : nombre de DWORDs.
-   Data \[ nDWords \] -tableau de DWORDS contenant les données de chaque élément vertex.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



