---
description: PatchMesh9 définit une maille définie par les correctifs de Bézier, y compris une liste de vertex et les correctifs pour la maille en indexant dans le tableau de vertex.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20216bcfa33c3e3ef36dea999a6fef10384719254f4874a1da3907aa02551a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798535"
---
# <a name="patchmesh9"></a>PatchMesh9

Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Où :

-   Type-type de maillage des correctifs : rectangle, triangle ou N-patch.
-   Degré-degré des variables dans l’équation de la courbe.
-   Base : type de base d’une surface corrective de poids fort.
-   nVertices-nombre de vertex.
-   vertex \[ nVertices \] -tableau de vertex. Consultez [**Vector**](vector.md).
-   nPatches : nombre de correctifs.
-   patchs \[ nPatches \] -Array of patchs. Consultez [**patch**](patch.md).
-   \[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici. L’architecture est ainsi extensible.

Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



