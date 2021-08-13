---
description: Définit un maillage simple. Le premier tableau est une liste de vertex, tandis que le deuxième tableau définit les visages de la maille en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Maillage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240739"
---
# <a name="mesh"></a>Maillage

Définit un maillage simple. Le premier tableau est une liste de vertex, tandis que le deuxième tableau définit les visages de la maille en indexant dans le tableau de vertex.

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

Où :

-   nVertices-nombre de vertex.
-   sommets de vecteurs \[ de tableau nVertices \] -tableau de vertex, chacun de type Vector. Consultez [**Vector**](vector.md).
-   nFaces-nombre de visages.
-   le tableau MeshFace \[ face \] à nFaces-Array of faces, chacun de type MeshFace. Consultez [**MeshFace**](meshface.md).
-   \[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici. L’architecture est ainsi extensible. Les modèles [**Material**](material.md) et [**TextureFilename**](texturefilename.md) sont généralement utilisés.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



