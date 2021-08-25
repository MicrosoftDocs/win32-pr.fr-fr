---
title: Sync (SM5-ASM)
description: Synchronisation de groupe de threads ou barrière de mémoire.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c64532669fc94d7d2109c39e501af0825e56434f66b79e20e1641c787a1a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852859"
---
# <a name="sync-sm5---asm"></a>Sync (SM5-ASM)

Synchronisation de groupe de threads ou barrière de mémoire.



| synchroniser \[ \_ Uglobal \|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Remarques

La **synchronisation** possède \_ les options Uglobal, \_ ugroup, \_ g et \_ t.

Dans le nuanceur de pixels, seul **\_ Uglobal de synchronisation** est autorisé.

Dans le nuanceur de calcul, vous \_ devez spécifier (Uglobal ou \_ ugroup \* ) et/ou \_ g. \_t est facultatif en plus.

### <a name="_uglobal"></a>\_uglobal

\#Limite de mémoire globale u (UAV).

Toutes les opérations de \# lecture/écriture de la mémoire u précédentes par ce thread dans l’ordre du programme sont rendues visibles à tous les threads de l’ensemble du GPU avant tout \# accès à la mémoire u ultérieur par ce thread. La partie GPU entière de la définition est remplacée par une portée « inférieur à » dans un cas, décrite ci-dessous.

Cela s’applique à toutes les mémoires UAV liées à l’étape de nuanceur actuelle.

\_Uglobal est disponible dans le nuanceur de calcul ou le nuanceur de pixels.

Pour tout UAV lié qui n’a pas été déclaré par le nuanceur comme cohérent globalement, la \_ barrière de mémoire Uglobal u \# dispose uniquement de la visibilité dans le groupe de threads du nuanceur de calcul actuel pour ce UAV, comme s’il s’agissait \_ de ugroup au lieu de \_ Uglobal. Ce problème s’applique uniquement au nuanceur de calcul, étant donné que le nuanceur de pixels doit déclarer tous les UAVs comme cohérents globalement.

### <a name="_ugroup"></a>\_ugroup

\#Limite de mémoire de l’étendue de groupe de threads u (UAV).

Toutes les opérations de \# lecture ou d’écriture de la mémoire en u antérieures par ce thread dans l’ordre du programme sont rendues visibles à tous les threads dans le groupe de threads avant que la mémoire u suivante n' \# accède à ce thread.

Cela s’applique à toutes les mémoires UAV liées à l’étape de nuanceur actuelle.

\_ugroup est disponible uniquement dans le nuanceur de calcul.

Si \_ ugroup est exposé, pour certaines implémentations. L’avantage de spécifier \_ ugroup au lieu de \_ Uglobal est que l’opération de **synchronisation** peut s’effectuer plus rapidement.

D’autres implémentations ne distinguent pas \_ ugroup de \_ Uglobal, donc les deux opérations sont équivalentes et se comportent comme \_ Uglobal. Les applications peuvent spécifier leur intention en demandant l’étendue de **synchronisation** la plus étroite nécessaire.

Même si un UAV particulier est déclaré comme cohérent globalement, une \_ opération de **synchronisation** ugroup fonctionnera plus efficacement sur ce UAV si un cloisonnement global n’est pas requis.

### <a name="_g"></a>\_activée

\#limite g (thread de groupe de threads partagés).

Toutes les opérations de \# lecture ou d’écriture de la mémoire antérieure à g par ce thread dans l’ordre du programme sont rendues visibles à tous les threads dans le groupe de threads avant les \# accès à la mémoire g suivants par ce thread.

Cela s’applique à l’ensemble de la mémoire partagée du groupe de threads actuel \# .

\_g est disponible uniquement dans le nuanceur de calcul.

### <a name="_t"></a>\_t

Synchronisation du groupe de threads. Tous les threads d’un groupe de threads unique (ceux qui peuvent partager l’accès à un ensemble commun d’espace de Registre partagé) sont exécutés jusqu’à ce qu’ils atteignent cette instruction avant que tout thread puisse continuer.

\_t ne peut pas être placé dans un contrôle de flux dynamique, (branches pouvant varier au sein d’un groupe de threads), mais peut être présent dans un contrôle de flux uniforme, où tous les threads du groupe sélectionnent le même chemin d’accès.

\_t est disponible uniquement dans le nuanceur de calcul.

La liste suivante répertorie les variantes de « Sync » du nuanceur de calcul.

-   synchronisation \_ g
-   synchroniser \_ ugroup\*
-   synchroniser \_ Uglobal
-   synchronisation \_ g \_ t
-   synchroniser \_ ugroup \_ t\*
-   synchroniser \_ Uglobal \_ t
-   synchroniser \_ ugroup \_ g\*
-   synchroniser \_ Uglobal \_ g
-   synchroniser \_ ugroup \_ g \_ t\*
-   synchroniser \_ Uglobal \_ g \_ t

\*Les variantes avec \_ ugroup peuvent ne pas être ciblées par le compilateur HLSL, conformément à la discussion précédente de la \_ section ugroup ci-dessus.

La liste des variantes de synchronisation de nuanceur de pixels inclut Sync \_ Uglobal uniquement.

Les limites de mémoire empêchent la réorganisation des instructions affectées par les compilateurs ou le matériel sur la clôture.

Plusieurs lectures à partir de la même adresse par un appel de nuanceur qui ne sont pas séparées par des barrières de mémoire ou des écritures vers l’adresse peuvent être réduites ensemble. Il en va de même pour les écritures. Les accès séparés par un cloisonnement ne peuvent pas être fusionnés ou déplacés sur le cloisonnement.

Les limites de mémoire ne sont pas nécessaires pour que les opérations atomiques sur une adresse donnée par différents threads fonctionnent correctement. Les délimitations sont nécessaires lorsque les opérations atomiques et/ou de charge/stockage doivent être synchronisées les unes par rapport aux autres, dans la mesure où elles apparaissent dans des threads individuels du point de vue d’autres threads.

Dans le nuanceur de pixels, les instructions [ignorent](discard--sm4---asm-.md) une \_ clôture de Uglobal de synchronisation, dans le sens où les instructions ne peuvent pas être réorganisées à travers la **suppression**. synchroniser les \_ Uglobal dans les pixels d’assistance (qui s’exécutent uniquement pour prendre en charge les dérivés) ou les pixels ignorés peuvent avoir un impact quelconque. Elle n’est pas autorisée pour les pixels d’assistance ou ignorés à écrire dans UAVs si, dans le cas d’un rejet, les écritures sont émises après la suppression. Les valeurs retournées à partir de UAVs ne sont pas autorisées à contribuer aux calculs dérivés. Par conséquent, si \_ la synchronisation u est respectée ou non pour les pixels d’assistance ou lorsqu’elle est émise après la discutable de la suppression.

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, la variante **Sync \_ Uglobal** de cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




