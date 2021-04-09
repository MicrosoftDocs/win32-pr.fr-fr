---
description: Utilisé par le modèle de maillage pour définir les visages d’un filet. Chaque élément du tableau nFaceVertexIndices fait référence à un vertex de maillage utilisé pour générer le visage.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108463"
---
# <a name="meshface"></a>MeshFace

Utilisé par le modèle de [**maillage**](mesh.md) pour définir les visages d’un filet. Chaque élément du tableau nFaceVertexIndices fait référence à un vertex de maillage utilisé pour générer le visage.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Où :

-   nFaceVertexIndices-nombre d’index.
-   Tableau DWORD faceVertexIndices \[ nFaceVertexIndices \] -tableau d’index.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



