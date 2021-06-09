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
ms.openlocfilehash: 8e2713aaa50206660f7672688a43e644873b1c13
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827058"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Index pour lesquels un nuanceur de calcul et un groupe de threads combinés sont en cours d’exécution. SV \_ DispatchThreadID est la somme de SV \_ GroupID \* numThreads et GroupThreadID. Elle varie selon la plage spécifiée dans [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) et [numThreads](sm5-attributes-numthreads.md). Par exemple, si Dispatch (2, 2, 2) est appelé sur un nuanceur de calcul avec numThreads (3, 3, 3) SV \_ DispatchThreadID aura une plage de 0.. 5 pour chaque dimension.

## <a name="type"></a>Type



| Type      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Remarques

Cette valeur système est facultative.

L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
