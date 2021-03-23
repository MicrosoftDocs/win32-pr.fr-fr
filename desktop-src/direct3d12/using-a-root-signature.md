---
title: Utilisation d’une signature racine
description: La signature racine est la définition d’une collection de tables de descripteurs réorganisée arbitrairement (y compris leur disposition), de constantes racine et de descripteurs racine.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104045"
---
# <a name="using-a-root-signature"></a>Utilisation d’une signature racine

La signature racine est la définition d’une collection de tables de descripteurs réorganisée arbitrairement (y compris leur disposition), de constantes racine et de descripteurs racine. Chaque entrée a un coût pour une limite maximale. par conséquent, l’application peut effectuer un compromis entre le nombre de chaque type d’entrée que la signature racine contiendra.

-   [Sémantique de liste de commandes](#command-list-semantic)
-   [Sémantique de Bundle](#bundle-semantics)
-   [Rubriques connexes](#related-topics)

La signature racine est un objet qui peut être créé par une spécification manuelle au niveau de l’API. Tous les nuanceurs d’un PSO doivent être compatibles avec la disposition racine spécifiée avec l’PSO, sinon les nuanceurs individuels doivent inclure des dispositions de racine incorporées qui correspondent les unes aux autres. dans le cas contraire, la création d’PSO échouera. L’une des propriétés de la signature racine est que les nuanceurs n’ont pas besoin de les connaître lors de leur création, bien que les signatures racines puissent également être créées directement dans les nuanceurs si vous le souhaitez. Les ressources de nuanceur existantes ne nécessitent aucune modification pour être compatibles avec les signatures racines. Le modèle de nuanceur 5,1 est introduit pour offrir une plus grande flexibilité (indexation dynamique des descripteurs dans les nuanceurs) et peut être adopté de manière incrémentielle à partir des ressources de nuanceur existantes, comme vous le souhaitez.

## <a name="command-list-semantic"></a>Sémantique de liste de commandes

Au début d’une liste de commandes, la signature racine n’est pas définie. Les nuanceurs graphiques ont une signature racine distincte du nuanceur de calcul, chacun étant affecté indépendamment à une liste de commandes. La signature racine définie sur une liste de commandes ou un bundle doit également correspondre au PSO actuellement défini au niveau du dessin/Dispatch ; dans le cas contraire, le comportement n’est pas défini. Les incompatibilités de signature racine temporaires avant le dessin/dispatch sont correctes, par exemple la définition d’un PSO incompatible avant le basculement vers une signature racine compatible (à condition qu’elles soient compatibles avec l’appel de la méthode Draw/Dispatch). La définition d’un PSO ne modifie pas la signature racine. L’application doit appeler une API dédiée pour définir la signature racine.

Une fois qu’une signature racine a été définie sur une liste de commandes, la disposition définit l’ensemble des liaisons que l’application est censée fournir et les objets psoables qui peuvent être utilisés (ceux qui sont compilés avec la même disposition) pour les appels de dessin/distribution suivants. Par exemple, une signature racine peut être définie par l’application pour avoir les entrées suivantes. Chaque entrée est appelée « emplacement ».

-   \[0 un descripteur \] CBV en ligne (descripteurs racine)
-   \[1 \] table de descripteur contenant 2 SRVs, 1 CBVS et 1 UAV
-   \[2 \] table de descripteur contenant 1 échantillonneur
-   \[3 \] une collection 4x32 bits de constantes racine
-   \[4 \] une table de descripteur contenant un nombre non spécifié de SRVs

Dans ce cas, avant de pouvoir émettre un dessin/Dispatch, l’application est censée définir la liaison appropriée à chacun des emplacements \[ 0.. 4 \] que l’application a définie avec sa signature racine actuelle. Par exemple, à \[ l’emplacement 1 \] , une table de descripteur doit être liée, qui est une région contiguë dans un tas de descripteur qui contient (ou contiendra au moment de l’exécution) 2 SRVs, 1 CBVS et 1 UAV. De même, les tables de descripteurs doivent être définies aux emplacements \[ 2 \] et \[ 4 \] .

L’application peut modifier une partie des liaisons de signature racine à la fois (le reste reste inchangé). Par exemple, si la seule chose qui doit être modifiée entre draws est l’une des constantes à l’emplacement \[ 2 \] , c’est que toutes les applications doivent se relier. Comme nous l’avons vu précédemment, les versions de pilote/matériel de tous les États de liaison de signature racine sont modifiées automatiquement. Si une signature racine est modifiée sur une liste de commandes, toutes les liaisons de signature racine précédentes deviennent obsolètes et toutes les liaisons qui viennent d’être attendues doivent être définies avant le dessin/Dispatch ; dans le cas contraire, le comportement n’est pas défini. Si la signature racine est définie de façon redondante sur la même que celle actuellement définie, les liaisons de signature racine existantes ne deviennent pas obsolètes.

## <a name="bundle-semantics"></a>Sémantique de Bundle

Les offres groupées héritent des liaisons de signature racine de la liste de commandes (liaisons aux différents emplacements dans l’exemple de liste de commandes ci-dessus). Si un bundle doit modifier certaines des liaisons de signature racine héritées, il doit d’abord définir la signature racine de manière à ce qu’elle soit identique à la liste de commandes appelante (les liaisons héritées ne deviennent pas obsolètes). Si le bundle définit la signature racine sur une autre valeur que la liste de commandes appelante, qui a le même effet que la modification de la signature racine sur la liste de commandes décrite ci-dessus : toutes les liaisons de signature racine précédentes sont obsolètes et les liaisons nouvellement attendues doivent être définies avant le dessin/Dispatch ; dans le cas contraire, le comportement n’est pas défini. Si un bundle n’a pas besoin de modifier des liaisons de signature racine, il n’a pas besoin de définir la signature racine.

Le code suivant montre un exemple de déroulement d’appel dans un bundle.

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

À partir d’un bundle, les modifications de disposition racine et/ou les modifications de liaison apportées par un bundle sont héritées de la liste de commandes appelante à la fin de l’exécution d’un bundle.

Pour plus d’informations sur l’héritage, reportez-vous à la section héritage de l' **État du pipeline Graphics** de gestion de l' [État des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Signatures racines](root-signatures.md)
</dt> </dl>

 

 




