---
title: SV_GroupID
description: Index pour le groupe de threads dans lequel un nuanceur de calcul s’exécute.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bce2623141329b4d750ab5add7957a7674662d7c21de9ff03e1165d341f98576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118159"
---
# <a name="sv_groupid"></a>\_GROUPID vs

Index pour le groupe de threads dans lequel un nuanceur de calcul s’exécute. Les index concernent l’ensemble du groupe et non un thread individuel. Les valeurs possibles varient au sein de la plage passée comme paramètres à la [**distribution**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Par exemple, l’appel de dispatch (2, 1, 1) donne les valeurs possibles 0, 0, 0 et 1, 0, 0.

Définit l’offset de groupe dans un appel de [**distribution**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , par dimension de l’appel de répartition.

## <a name="type"></a>Type



| Type      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Remarques

Cette valeur système est facultative.

L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupId).

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

 

 
