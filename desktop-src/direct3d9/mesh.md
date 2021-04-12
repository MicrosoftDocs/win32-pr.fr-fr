---
description: Définit un maillage simple. Le premier tableau est une liste de vertex, tandis que le deuxième tableau définit les visages de la maille en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Maillage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480697"
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

 

 



