---
description: Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745572"
---
# <a name="faceadjacency"></a>FaceAdjacency

Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons. Le résultat est dupliqué lorsqu’un sommet se trouve sur un groupe de lissage ou une limite de matériau. L’objectif de ce modèle est de permettre au chargeur de déterminer quels vertex qui présentent des paramètres de périphérique différents sont en fait les mêmes sommets dans le modèle. Certaines applications (telles que la simplification du maillage, par exemple) peuvent utiliser ces informations.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Où :

-   nIndices : nombre d’index dans la maille.
-   index \[ nIndices \] -tableau d’index.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



