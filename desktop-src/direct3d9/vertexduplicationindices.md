---
description: Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515299"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons. Le résultat est dupliqué lorsqu’un sommet se trouve sur un groupe de lissage ou une limite de matériau. L’objectif de ce modèle est de permettre au chargeur de déterminer quels vertex qui présentent des paramètres de périphérique différents sont en fait les mêmes sommets dans le modèle. Certaines applications (telles que la simplification du maillage, par exemple) peuvent utiliser ces informations.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Où :

-   nIndices : nombre d’index de vertex. Il s’agit du nombre de vertex dans la maille.
-   nOriginalVertices : nombre de vertex dans la maille avant l’exécution d’une duplication.
-   La valeur indices \[ n \] contient l’index de vertex que le vertex \[ n \] dans le tableau de vertex pour le maillage aurait eu si aucune duplication n’avait eu lieu. Les index de ce tableau sont identiques, par conséquent, indiquent des vertex dupliqués.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



