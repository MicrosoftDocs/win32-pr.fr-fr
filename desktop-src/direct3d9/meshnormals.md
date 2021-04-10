---
description: Définit les normales d’une maille.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200767"
---
# <a name="meshnormals"></a>MeshNormals

Définit les normales d’une maille. Le premier tableau de vecteurs est les vecteurs normaux eux-mêmes, et le deuxième tableau est un tableau d’index spécifiant les normales qui doivent être appliquées à une face donnée. La valeur du membre nFaceNormals doit être égale au nombre de faces dans une maille.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Où :

-   nNormals-nombre de normales.
-   Normals de vecteurs \[ de tableau nNormals \] -tableau de normales. Consultez [**Vector**](vector.md).
-   nFaceNormals-nombre de normales de visage.
-   Tableau MeshFace faceNormals \[ nFaceNormals \] -tableau de la face normale de la maille. Consultez [**MeshFace**](meshface.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



