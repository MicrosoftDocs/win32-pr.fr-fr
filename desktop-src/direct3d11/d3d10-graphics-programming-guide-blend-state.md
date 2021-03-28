---
title: Configuration de la fonctionnalité de fusion
description: Les opérations de fusion sont effectuées sur chaque sortie de nuanceur de pixels (valeur RVBA) avant que la valeur de sortie ne soit écrite dans une cible de rendu. Si l’échantillonnage multiple est activé, la fusion est effectuée sur chaque échantillon multiple ; dans le cas contraire, la fusion est effectuée sur chaque pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990920"
---
# <a name="configuring-blending-functionality"></a>Configuration de la fonctionnalité de fusion

Les opérations de fusion sont effectuées sur chaque sortie de nuanceur de pixels (valeur RVBA) avant que la valeur de sortie ne soit écrite dans une cible de rendu. Si l’échantillonnage multiple est activé, la fusion est effectuée sur chaque échantillon multiple ; dans le cas contraire, la fusion est effectuée sur chaque pixel.

-   [Créer l’état de fusion](#create-the-blend-state)
-   [Lier l’état de fusion](#bind-the-blend-state)
-   [Rubriques avancées sur la fusion](#advanced-blending-topics)
    -   [Alpha-à-couverture](#alpha-to-coverage)
    -   [Fusion des sorties de nuanceur de pixels](#blending-pixel-shader-outputs)
-   [Rubriques connexes](#related-topics)

## <a name="create-the-blend-state"></a>Créer l’état de fusion

L’État Blend est une collection d’États utilisée pour contrôler la fusion. Ces États (définis dans [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) sont utilisés pour créer l’objet d’État Blend en appelant [**ID3D11Device1 :: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).

Par exemple, voici un exemple très simple de création d’état de fusion qui désactive la fusion alpha et n’utilise pas de masquage de pixel par composant.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Cet exemple est similaire à l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="bind-the-blend-state"></a>Lier l’état de fusion

Après avoir créé l’objet d’état de fusion, liez l’objet d’état de fusion à l’étape de fusion de sortie en appelant [**ID3D11DeviceContext :: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Cette API prend trois paramètres : l’objet d’état de fusion, un facteur de mélange à quatre composants et un exemple de masque. Vous pouvez transmettre **null** pour l’objet d’état de fusion pour spécifier l’état de fusion par défaut ou passer un objet d’état de fusion. Si vous avez créé l’objet d’état de fusion avec [**d3d11 \_ Blend Blend \_ \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) ou [**d3d11 Blend Blend Blend \_ \_ \_ \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), vous pouvez passer un facteur de fusion pour moduler les valeurs du nuanceur de pixels, de la cible de rendu ou des deux. Si vous n’avez pas créé l’objet d’état de fusion avec le facteur de fusion **\_ Blend d3d11 \_ \_** ou le **\_ \_ \_ \_ facteur de fusion d3d11 Blend**, vous pouvez toujours passer un facteur de fusion non null, mais la phase de fusion n’utilise pas le facteur de fusion ; le runtime stocke le facteur de fusion et vous pouvez ensuite appeler [**ID3D11DeviceContext :: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) pour récupérer le facteur de fusion. Si vous transmettez la **valeur null**, le runtime utilise ou stocke un facteur de fusion égal à {1, 1, 1, 1}. L’exemple de masque est un masque défini par l’utilisateur qui détermine comment échantillonner la cible de rendu existante avant de la mettre à jour. Le masque d’échantillonnage par défaut est 0xFFFFFFFF qui désigne l’échantillonnage des points.

Dans la plupart des schémas de mise en mémoire tampon de profondeur, le pixel le plus proche de l’appareil photo est celui qui est dessiné. Lors de [la configuration de l’état du stencil de profondeur](d3d10-graphics-programming-guide-depth-stencil.md), le membre **DepthFunc** de la [**\_ \_ \_ Description du stencil de profondeur d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) peut être n’importe quelle fonction de [**\_ comparaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func). Normalement, vous souhaitez que **DepthFunc** soit **d3d11 une \_ comparaison \_ inférieure**, afin que les pixels les plus proches de l’appareil photo remplacent les pixels situés derrière eux. Toutefois, selon les besoins de votre application, toutes les autres fonctions de comparaison peuvent être utilisées pour effectuer le test de profondeur.

## <a name="advanced-blending-topics"></a>Rubriques avancées sur la fusion

-   [Alpha-à-couverture](#alpha-to-coverage)
-   [Fusion des sorties de nuanceur de pixels](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Alpha-à-couverture

L’alpha-to-Coverage est une technique d’échantillonnage multiple qui est très utile dans des situations telles que des feuillages denses où il existe plusieurs polygones qui utilisent la transparence alpha pour définir des bords dans la surface.

Vous pouvez utiliser le membre **AlphaToCoverageEnable** de [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) ou [**d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) pour déterminer si le Runtime convertit le. un composant (alpha) du registre de sortie [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 du nuanceur de pixels vers un masque de couverture n-STEP (à partir d’un exemple de **renderTarget** n-Sample). Le Runtime effectue une opération **and** de ce masque avec la couverture d’exemple classique du pixel dans la primitive (en plus de l’exemple de masque) pour déterminer les exemples à mettre à jour dans tous les **renderTarget** actifs.

Si le nuanceur de pixels génère une [ \_ couverture de SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), le runtime désactive alpha-to-coverage.

> [!Note]  
> Dans l’échantillonnage multiple, le Runtime partage une seule couverture pour tous les **renderTarget** s. Le fait que le runtime lit et convertit. a de la sortie [VP \_ cible](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 à la couverture quand **AlphaToCoverageEnable** a la valeur true ne change pas. valeur qui accède au Blender à **renderTarget** 0 (si un **renderTarget** est défini ici). En général, si vous activez l’alpha-à-couverture, vous n’affectez pas la manière dont toutes les sorties de couleur des nuanceurs de pixels interagissent avec **renderTarget** dans l' [étape de fusion de sortie](d3d10-graphics-programming-guide-output-merger-stage.md) , à ceci près que le runtime effectue une opération **and** du masque de couverture avec le masque Alpha-à-couverture. Alpha-to-cover fonctionne indépendamment si le runtime peut mélanger **renderTarget** ou si vous utilisez la fusion sur **renderTarget**.

 

Le matériel graphique ne spécifie pas précisément comment il convertit le nuanceur de pixels de la [ \_ cible](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (alpha) en masque de couverture, sauf que la valeur alpha de 0 (ou moins) doit correspondre à aucune couverture et alpha (ou plus) doit correspondre à une couverture complète (avant que le runtime effectue une opération **and** avec la couverture primitive réelle). Comme alpha passe de 0 à 1, la couverture résultante doit généralement augmenter de façon monotone. Toutefois, le matériel peut effectuer le tramage de zone pour fournir une meilleure quantification des valeurs alpha au détriment de la résolution spatiale et du bruit. Une valeur alpha NaN (pas un nombre) entraîne un masque aucun (zéro) de couverture.

La couverture alpha-à-couverture est également traditionnellement utilisée pour la transparence de la porte d’écran ou pour la définition d’silhouettes détaillées pour les sprites autrement opaques.

### <a name="blending-pixel-shader-outputs"></a>Fusion des sorties de nuanceur de pixels

Cette fonctionnalité permet à la fusion de sortie d’utiliser les sorties de nuanceur de pixels simultanément en tant que sources d’entrée pour une opération de fusion avec la cible de rendu unique à l’emplacement 0.

Cet exemple prend deux résultats et les combine en une seule passe, en fusionnant un dans la destination avec une multiplication et l’autre avec un Add :


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



Cet exemple configure la sortie du premier nuanceur de pixels comme couleur source et la deuxième sortie en tant que facteur de mélange de composant par couleur.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



Cet exemple montre comment les facteurs de fusion doivent correspondre au Swizzles du nuanceur :


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Ensemble, les facteurs de mélange et le code du nuanceur impliquent que le nuanceur de pixels est requis pour la sortie au moins de o0. r et O1. a. Les composants de sortie supplémentaires peuvent être générés par le nuanceur, mais ils sont ignorés, mais moins de composants produirait des résultats indéfinis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sortie-étape de fusion](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 