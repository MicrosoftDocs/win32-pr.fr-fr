---
title: Nuanceurs de calcul sur du matériel de niveau inférieur
description: Cette rubrique explique comment utiliser les nuanceurs de calcul dans une application Direct3D 11 sur un matériel Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095349"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Nuanceurs de calcul sur du matériel de niveau inférieur

Direct3D 11 offre la possibilité d’utiliser des [nuanceurs de calcul](direct3d-11-advanced-stages-compute-shader.md) qui fonctionnent sur la plupart du matériel Direct3D 10. x, avec quelques limitations au fonctionnement. La technologie de nuanceur de calcul est également appelée technologie DirectCompute. Cette rubrique explique comment utiliser les [nuanceurs de calcul](direct3d-11-advanced-stages-compute-shader.md) dans une application Direct3D 11 sur un matériel Direct3D 10.

La prise en charge des nuanceurs de calcul sur du matériel de niveau inférieur concerne uniquement les appareils compatibles avec Direct3D 10. x. Les nuanceurs de calcul ne peuvent pas être utilisés sur du matériel Direct3D 9. x.

Pour vérifier si le matériel Direct3D 10. x prend en charge les nuanceurs de calcul, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Dans l’appel **CheckFeatureSupport** , transmettez la \_ \_ \_ valeur de l' \_ option d’options matérielles de la fonctionnalité d3d11 D3D10 x \_ au paramètre *Feature* , transmettez un pointeur désignant la [**\_ fonction d3d11 \_ Data \_ D3D10 \_ x \_ \_ Data**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) options structure au paramètre *pFeatureSupportData* , puis transmettez la taille de la **fonction d3d11 \_ \_ Data \_ \_ \_ \_ options Hardware** dans le paramètre *D3D10* . **CheckFeatureSupport** retourne la **valeur true** dans le **ComputeShaders \_ plus \_ RawAndStructuredBuffers \_ via le \_ Shader \_ 4 \_ x** du membre de la **fonctionnalité d3d11 de données de la \_ fonctionnalité \_ \_ D3D10 \_ x \_ \_** si le matériel Direct3D 10. x prend en charge les nuanceurs de calcul.

La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.

-   [Vues d’accès non ordonnées (UAVs)](#unordered-access-views-uavs)
-   [Vues des ressources de nuanceur (SRVs)](#shader-resource-views-srvs)
-   [Groupes de threads](#thread-groups)
    -   [Dimensions de groupe de threads](#thread-group-dimensions)
    -   [Index de thread à deux dimensions](#two-dimensional-thread-indices)
    -   [Mémoire partagée de groupe de threads (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile avec D3DCOMPILE \_ Skip \_ Optimization](/windows)
-   [Rubriques connexes](#related-topics)

## <a name="unordered-access-views-uavs"></a>Vues d’accès non ordonnées (UAVs)

Les vues d’accès non ordonnées brutes ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) et structurées ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) sont prises en charge sur le matériel de niveau inférieur, avec les limitations suivantes :

-   Un seul UAV peut être lié à un pipeline à la fois via [**ID3D11DeviceContext :: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   Le décalage de base pour un UAV brut doit être aligné sur une limite de 256 octets (au lieu de l’alignement sur 16 octets requis pour le matériel Direct3D 11).

Les UAVs typés ne sont pas pris en charge sur le matériel de niveau inférieur. Cela comprend [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)et [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs.

Les nuanceurs de pixels sur du matériel de niveau inférieur ne prennent pas en charge l’accès non ordonné.

## <a name="shader-resource-views-srvs"></a>Vues des ressources de nuanceur (SRVs)

Les tampons bruts et structurés en tant que vues de ressources de nuanceur sont pris en charge sur le matériel de bas niveau pour l’accès en lecture seule, comme c’est le cas sur le matériel Direct3D 11. Ces types de ressources sont pris en charge pour les nuanceurs vertex, les nuanceurs de géométrie, les nuanceurs de pixels et les nuanceurs de calcul.

## <a name="thread-groups"></a>Groupes de threads

Un nuanceur de calcul peut s’exécuter sur un grand nombre de threads en parallèle, au sein d’un groupe de threads.

Les groupes de threads sont pris en charge sur le matériel de niveau inférieur, avec les limitations suivantes :

### <a name="thread-group-dimensions"></a>Dimensions de groupe de threads

Les groupes de threads définis pour le matériel de niveau inférieur sont limités aux dimensions X et Y de 768. Cette valeur est inférieure aux valeurs maximales de 1024 pour le matériel Direct3D 11. La dimension Z maximale de 64 est inchangée.

Le nombre total de threads dans le groupe (X × Y × Z) est limité à 768. Ce nombre est inférieur à la limite de 1024 pour le matériel Direct3D 11.

Si ces nombres sont dépassés, la compilation du nuanceur échoue.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional les index de thread

Un thread particulier dans un groupe de threads est indexé à l’aide d’un vecteur 3D donné par (x, y, z).

Pour les nuanceurs de calcul opérant sur du matériel de niveau inférieur, les groupes de threads prennent uniquement en charge deux dimensions. Cela signifie que la valeur Z dans le vecteur 3D doit toujours être 1.

Cette limitation s’applique spécifiquement aux éléments suivants :

-   [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch): l’argument *ThreadGroupCountZ* doit être 1.
-   [**ID3D11DeviceContext ::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect): cette fonction n’est pas prise en charge sur le matériel de niveau inférieur.
-   [numThreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads): la valeur Z doit être 1.

### <a name="thread-group-shared-memory-tgsm"></a>Mémoire partagée de groupe de threads (TGSM)

La mémoire partagée de groupe de threads est limitée à 16 Ko sur du matériel de niveau inférieur. Cette valeur est inférieure aux 32 Ko disponibles pour le matériel Direct3D 11.

Un thread de nuanceur de calcul peut uniquement écrire dans sa propre région de TGSM. Cette région en écriture seule a une taille maximale de 256 octets ou moins, avec une diminution maximale du nombre de threads déclarés pour le groupe.

Le tableau suivant définit la taille maximale par thread d’une région TGSM pour le nombre de threads dans le groupe :



| Nombre de threads dans le groupe | Taille de TGSM maximale par thread |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

Un thread de nuanceur de calcul peut lire le TGSM à partir de n’importe quel emplacement.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile avec D3DCOMPILE \_ Skip \_ Optimization

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) retourne **E \_ NOTIMPL** lorsque vous transmettez cs \_ 4 \_ 0 comme cible du nuanceur avec l’option de compilation [**D3DCompile \_ Skip \_ Optimization**](/windows/desktop/direct3dhlsl/d3dcompile-constants) . La \_ \_ cible de nuanceur CS 5 0 fonctionne avec l' **\_ \_ optimisation de D3DCOMPILE Skip**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Direct3D 11 sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 