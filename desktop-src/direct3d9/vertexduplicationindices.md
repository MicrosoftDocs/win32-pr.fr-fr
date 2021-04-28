---
description: 'VertexDuplicationIndices : ce modèle est instancié par maillage, en contenant des informations sur les vertex de la maille qui sont des doublons.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090176"
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

 

 



