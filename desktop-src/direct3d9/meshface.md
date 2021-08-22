---
description: Utilisé par le modèle de maillage pour définir les visages d’un filet. Chaque élément du tableau nFaceVertexIndices fait référence à un vertex de maillage utilisé pour générer le visage.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563529"
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

 

 



