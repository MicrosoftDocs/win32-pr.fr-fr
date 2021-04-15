---
description: Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520892"
---
# <a name="patchmesh"></a>PatchMesh

Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Où :

-   nVertices-nombre de vertex.
-   vertex \[ nVertices \] -tableau de vertex. Consultez [**Vector**](vector.md).
-   nPatches : nombre de correctifs.
-   patchs \[ nPatches \] -Array of patchs. Consultez [**patch**](patch.md).
-   \[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici. L’architecture est ainsi extensible.

Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif. Il s’agit d’un modèle hérité. Le dernier modèle de maillage des correctifs est [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



