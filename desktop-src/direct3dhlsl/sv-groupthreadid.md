---
title: SV_GroupThreadID
description: Indices pour lesquels un thread individuel dans un groupe de threads est en cours d’exécution dans un nuanceur de calcul.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996986"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Indices pour lesquels un thread individuel dans un groupe de threads est en cours d’exécution dans un nuanceur de calcul. SV \_ GroupThreadID varie dans la plage spécifiée pour le nuanceur de calcul dans l’attribut [numThreads](sm5-attributes-numthreads.md) . Par exemple, si numThreads (3, 2, 1) a été spécifié, les valeurs possibles pour la \_ valeur d’entrée de SV GroupThreadID sont comprises dans cette plage de valeurs (0-2, 0-1, 0).

## <a name="type"></a>Type



|       |
|-------|
| Type  |
| uint3 |



 

## <a name="remarks"></a>Remarques

Cette valeur système est facultative et est toujours dans les limites des valeurs passées à l’attribut [numThreads](sm5-attributes-numthreads.md) .

L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
