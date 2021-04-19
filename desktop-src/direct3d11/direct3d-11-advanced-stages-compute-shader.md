---
title: Vue d’ensemble du nuanceur de calcul
description: Un nuanceur de calcul est une étape de nuanceur programmable qui développe Microsoft Direct3D 11 au-delà de la programmation graphique. La technologie de nuanceur de calcul est également appelée technologie DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485e83ab965f14342d235a07810f210e18aadc53
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222867"
---
# <a name="compute-shader-overview"></a>Vue d’ensemble du nuanceur de calcul

Un nuanceur de calcul est une étape de nuanceur programmable qui développe Microsoft Direct3D 11 au-delà de la programmation graphique. La technologie de nuanceur de calcul est également appelée technologie DirectCompute.

Comme d’autres nuanceurs programmables (nuanceurs vertex et Geometry, par exemple), un nuanceur de calcul est conçu et implémenté avec le [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) , mais il s’agit juste de savoir où se termine la similarité. Un nuanceur de calcul fournit un calcul universel à grande vitesse et tire parti du grand nombre de processeurs parallèles sur l’unité de traitement graphique (GPU). Le nuanceur de calcul fournit des fonctionnalités de partage de mémoire et de synchronisation de threads pour permettre des méthodes de programmation parallèles plus efficaces. Vous appelez la méthode [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) ou [**ID3D11DeviceContext ::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) pour exécuter des commandes dans un nuanceur de calcul. Un nuanceur de calcul peut s’exécuter sur un grand nombre de threads en parallèle.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Utilisation du nuanceur de calcul sur du matériel Direct3D 10. x

Un nuanceur de calcul sur Microsoft Direct3D 10 est également connu sous le nom de DirectCompute 4. x.

Si vous utilisez l’API Direct3D 11 et les pilotes mis à jour, le matériel Direct3D de [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10 et 10,1 peut éventuellement prendre en charge une forme limitée de DirectCompute qui utilise les \_ profils CS 4 \_ 0 et CS \_ 4 \_ 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Lorsque vous utilisez DirectCompute sur ce matériel, gardez à l’esprit les limitations suivantes :

-   Le nombre maximal de threads est limité au nombre maximal de threads de \_ \_ groupe de threads d3d11 CS 4 \_ X par groupe \_ \_ \_ \_ \_ \_ (768) par groupe.
-   La dimension X et Y de **numThreads** est limitée à d3d11 \_ cs \_ 4 \_ x \_ thread \_ Group \_ Max \_ x (768) et D3D11 \_ cs \_ 4 \_ x \_ thread \_ Group \_ Max \_ Y (768).
-   La dimension Z de **numThreads** est limitée à 1.
-   La dimension Z de dispatch est limitée aux \_ groupes de \_ \_ \_ Threads Max Dispatch d3d11 CS 4 X dans la \_ \_ \_ \_ \_ \_ dimension z (1).
-   Un seul affichage d’accès non ordonné peut être lié au nuanceur (le \_ nombre de registres d3d11 cs \_ 4 \_ X \_ UAV \_ \_ est 1).
-   Seuls [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s et [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s sont disponibles en tant que vues d’accès non ordonnées.
-   Un thread peut uniquement accéder à sa propre région dans la mémoire groupshared pour l’écriture, bien qu’il puisse lire à partir de n’importe quel emplacement.
-   [SV \_ GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) ou [SV \_ GroupThreadID](/windows/desktop/direct3dhlsl/sv-groupthreadid) doivent être utilisés lors de l’accès à la mémoire **groupshared** pour l’écriture.
-   La mémoire **Groupshared** est limitée à 16 Ko par groupe.
-   Un seul thread est limité à une région de 256 octets de mémoire **groupshared** pour l’écriture.
-   Aucune instruction atomique n’est disponible.
-   Aucune valeur à double précision n’est disponible.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Utilisation du nuanceur de calcul sur du matériel Direct3D 11. x

Un nuanceur de calcul sur Direct3D 11 est également connu sous le nom de DirectCompute 5,0.

Quand vous utilisez DirectCompute avec des \_ \_ [profils](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)CS 5 0, gardez les éléments suivants à l’esprit :

-   Le nombre maximal de threads est limité au nombre maximal de threads de \_ \_ groupe de threads d3d11 cs par groupe \_ \_ \_ \_ \_ (1024) par groupe.
-   Les dimensions X et Y de **numThreads** sont limitées aux groupes \_ de \_ Threads d3d11 cs \_ \_ Max \_ X (1024) et D3D11 \_ cs \_ thread \_ Group \_ Max \_ Y (1024).
-   La dimension Z de **numThreads** est limitée à d3d11 \_ cs \_ thread \_ Group \_ Max \_ Z (64).
-   La dimension maximale de la répartition est limitée aux \_ \_ groupes de \_ Threads Max Dispatch d3d11 cs \_ \_ \_ par \_ dimension (65535).
-   Le nombre maximal de vues d’accès non ordonnées qui peuvent être liées à un nuanceur est D3D11 \_ PS \_ cs \_ UAV \_ Register \_ Count (8).
-   Prend en charge [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s et les vues d’accès non ordonnées typées ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d), etc.).
-   Des instructions atomiques sont disponibles.
-   Une prise en charge de la double précision peut être disponible. Pour plus d’informations sur la façon de déterminer si la double précision est disponible, consultez la rubrique relative aux [**\_ fonctionnalités d3d11 \_ double**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                              | Description                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveaux types de ressources](direct3d-11-advanced-stages-cs-resources.md)<br/>      | Plusieurs nouveaux types de ressources ont été ajoutés dans Direct3D 11.<br/>                                                                                                                                                                                                 |
| [Accès aux ressources](direct3d-11-advanced-stages-cs-access.md)<br/>        | Il existe plusieurs façons d’accéder aux [ressources](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Atomic, fonctions](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Pour accéder à un nouveau type de ressource ou à une mémoire partagée, utilisez une fonction intrinsèque verrouillée. Il est garanti que les fonctions interverrouillées fonctionnent de manière atomique. Autrement dit, il est garanti qu’ils se produisent dans l’ordre programmé. Cette section répertorie les fonctions atomiques.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Comment : créer un nuanceur de calcul](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

