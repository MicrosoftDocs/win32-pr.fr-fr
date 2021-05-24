---
description: Dans Direct3D 10, l’état de l’appareil est regroupé en objets d’État, ce qui réduit de manière considérable le coût des changements d’État.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objets d’État (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335423"
---
# <a name="state-objects-direct3d-10"></a>Objets d’État (Direct3D 10)

Dans Direct3D 10, l’état de l’appareil est regroupé en objets d’État, ce qui réduit de manière considérable le coût des changements d’État. Il existe plusieurs objets d’État et chacun d’eux est conçu pour initialiser un ensemble d’États pour une étape de pipeline particulière. Vous pouvez créer jusqu’à 4096 pour chaque type d’objet d’État.

-   [État de la disposition d’entrée](#input-layout-state)
-   [État du rastériseur](#rasterizer-state)
-   [État du stencil de profondeur](#depth-stencil-state)
-   [État de fusion](#blend-state)
-   [État de l’échantillonneur](#sampler-state)
-   [Considérations relatives aux performances](#performance-considerations)
-   [Rubriques connexes](#related-topics)

## <a name="input-layout-state"></a>État de l' Input-Layout

Ce groupe d’État (voir la description de l' [**\_ \_ \_ élément d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dicte comment l' [étape assembleur d’entrée](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) lit les données en dehors des mémoires tampons d’entrée et les assemble pour une utilisation par le nuanceur de sommets. Cela comprend l’État, tel que le nombre d’éléments dans la mémoire tampon d’entrée et la signature des données d’entrée. L’étape assembleur d’entrée est une nouvelle étape dans le pipeline dont la tâche consiste à diffuser en continu des primitives de la mémoire dans le pipeline.

Pour créer un objet d’état de disposition d’entrée, consultez [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>État du rastériseur

Ce groupe d’États (voir [**D3D10 \_ rastériseur \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) Initialise l’étape de [rastérisation](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Cet objet comprend un état tel que les modes de remplissage ou d’élimination, l’activation d’un rectangle de ciseaux pour le découpage et la définition des paramètres d’échantillonnages. Cette étape pixellise les primitives en pixels, en effectuant des opérations telles que le découpage et le mappage des primitives à la fenêtre d’affichage.

Pour créer un objet d’État rastériseur, consultez [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).

## <a name="depth-stencil-state"></a>État de l' Depth-Stencil

Ce groupe d’États (voir [**D3D10 de \_ profondeur du \_ stencil \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) Initialise la partie profondeur du gabarit de l' [étape de fusion de sortie](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md). Plus spécifiquement, cet objet Initialise le test de profondeur et de stencil.

Pour créer un objet d’état de stencil-profondeur, consultez [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).

## <a name="blend-state"></a>État de fusion

Ce groupe d’États (voir [**D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) Initialise la partie de fusion de l' [étape de fusion de sortie](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).

Pour créer un objet d’état de fusion, consultez [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>État de l’échantillonneur

Ce groupe d’État (voir [**l' \_ exemple D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Initialise un objet échantillonneur. Un objet échantillonneur est utilisé par les étapes du nuanceur pour filtrer les textures en mémoire.



Différences entre Direct3D 9 et Direct3D 10 :

- Dans Direct3D 10, l’objet échantillonneur n’est plus lié à une texture spécifique, mais il décrit simplement comment effectuer un filtrage en fonction d’une ressource attachée.



 

Pour créer un objet d’état d’échantillonnage, consultez [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).

## <a name="performance-considerations"></a>Considérations relatives aux performances

La conception de l’API pour utiliser les objets d’État crée plusieurs avantages en matière de performances. Cela inclut la validation de l’État au moment de la création de l’objet, l’activation de la mise en cache des objets d’État dans le matériel et la réduction considérable de la quantité d’État qui est passée pendant un appel d’API de paramétrage d’État (en passant un handle à l’objet d’État au lieu de l’État).

Pour améliorer ces performances, vous devez créer vos objets d’État au démarrage de votre application, bien avant votre boucle de rendu. Les objets d’État sont immuables, autrement dit, une fois qu’ils sont créés, vous ne pouvez pas les modifier. Au lieu de cela, vous devez les détruire et les recréer. Pour faire face à cette restriction, vous pouvez créer jusqu’à 4096 pour chaque type d’objets d’État. Par exemple, vous pouvez créer plusieurs objets échantillonner avec différentes combinaisons d’États d’échantillonnage. La modification de l’état de l’échantillonneur est ensuite effectuée en appelant l’API Set appropriée qui passe un handle à l’objet (par opposition à l’état de l’échantillonneur). Cela réduit considérablement la quantité de surcharge au cours de chaque trame de rendu pour la modification de l’État, car le nombre d’appels et la quantité de données sont considérablement réduits.

Vous pouvez également choisir d’utiliser le système d’effet qui gère automatiquement la création et la destruction efficaces des objets d’État pour votre application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités de l’API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
