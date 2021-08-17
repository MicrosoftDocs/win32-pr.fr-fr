---
title: numThreads
description: Définit le nombre de threads à exécuter dans un groupe de threads unique lorsqu’un nuanceur de calcul est distribué (consultez ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f790548fb8ab629b7f6e7af345fa535d28a0d2216f570d02e851ce18618bbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510118"
---
# <a name="numthreads"></a>numThreads

Définit le nombre de threads à exécuter dans un groupe de threads unique lorsqu’un nuanceur de calcul est distribué (consultez [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Les valeurs X, Y et Z indiquent la taille du groupe de threads dans une direction particulière et le total de X \* Y \* Z indique le nombre de threads dans le groupe. La possibilité de spécifier la taille du groupe de threads sur trois dimensions permet d’accéder à des threads individuels d’une manière logique pour les structures de données 2D et 3D.

Par exemple, si un nuanceur de calcul effectue une addition de matrice 4x4, numThreads peut être défini sur numThreads (4, 4, 1) et l’indexation dans les threads individuels correspond automatiquement aux entrées de la matrice. Le nuanceur de calcul peut également déclarer un groupe de threads avec le même nombre de threads (16) à l’aide de numThreads (16, 1, 1), mais il doit alors calculer l’entrée de la matrice actuelle en fonction du numéro de thread actuel.

Les valeurs de paramètre autorisées pour **numThreads** dépendent de la version du nuanceur de calcul.



| Nuanceur de calcul | Z maximal | Nombre maximal de threads (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| CS \_ 4 \_ x       | 1         | 768                       |
| CS \_ 5 \_ 0       | 64        | 1 024                      |



 

L’illustration suivante montre la relation entre les paramètres passés à [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut numThreads, numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système associées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_](sv-dispatchthreadid.md)DispatchThreadID, VP [ \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

Cet attribut est pris en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 