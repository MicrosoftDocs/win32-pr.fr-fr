---
title: SV_DispatchThreadID
description: Index pour lesquels un nuanceur de calcul et un groupe de threads combinés sont en cours d’exécution.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104557950"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Index pour lesquels un nuanceur de calcul et un groupe de threads combinés sont en cours d’exécution. SV \_ DispatchThreadID est la somme de SV \_ GroupID \* numThreads et GroupThreadID. Elle varie selon la plage spécifiée dans [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) et [numThreads](sm5-attributes-numthreads.md). Par exemple, si Dispatch (2, 2, 2) est appelé sur un nuanceur de calcul avec numThreads (3, 3, 3) SV \_ DispatchThreadID aura une plage de 0.. 5 pour chaque dimension.

## <a name="type"></a>Type



|       |
|-------|
| Type  |
| uint3 |



 

## <a name="remarks"></a>Notes

Cette valeur système est facultative.

L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

Cette fonction est prise en charge dans les types de nuanceurs suivants :



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 