---
description: PatchMesh définit une maille définie par les correctifs de Bézier, y compris une liste de vertex et les correctifs pour la maille en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918223"
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

 

 



