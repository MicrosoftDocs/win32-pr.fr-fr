---
title: SV_GroupIndex
description: Le \ 0034 ; aplati \ 0034 ; index d’un thread de nuanceur de calcul dans un groupe de threads, qui transforme le SV multidimensionnel \_ GroupThreadID en valeur 1D. SV \_ GroupIndex varie de 0 à (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211 ; 1,0.
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508249"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

Index « aplati » d’un thread de nuanceur de calcul dans un groupe de threads, qui convertit le SV multidimensionnel \_ GroupThreadID en valeur 1D. SV \_ GroupIndex varie de 0 à (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Type



| Type |
|------|
| uint |



 

## <a name="remarks"></a>Remarques


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



où dimx et Dimy sont les dimensions spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) pour le point d’entrée.

Cette valeur système est facultative. Toutefois, son utilisation garantit qu’un thread écrit uniquement dans la région de mémoire qui lui est assignée dans la variable groupshared.

L’illustration suivante montre la relation entre les paramètres passés à [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads (SV GroupIndex, SV DispatchThreadID, SV \_ ,[SV \_ GroupID](sv-groupid.md)).[ \_](sv-dispatchthreadid.md)[ \_](sv-groupthreadid.md)

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 