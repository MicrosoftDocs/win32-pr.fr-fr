---
description: Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513909"
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

 

 



