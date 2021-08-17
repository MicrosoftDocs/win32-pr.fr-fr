---
title: Prise en main avec l’étape de rastérisation
description: Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- échantillonnage multiple, état de rastériseur (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e819dd92dd9c07a71f3830d3b67e371bc3d0e0c98f62fa36fdcf8ee3550ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914000"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Prise en main avec l’étape de rastérisation

Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.

## <a name="set-the-viewport"></a>Définir la fenêtre d’affichage

Une fenêtre d’affichage mappe les positions de vertex (dans l’espace de l’élément) aux positions des cibles de rendu. Cette étape met à l’échelle les positions 3D dans l’espace 2D. Une cible de rendu est orientée avec les axes Y pointant vers le dessous ; Cela nécessite que les coordonnées Y soient retournées lors de l’échelle de la fenêtre d’affichage. En outre, les étendues x et y (plage des valeurs x et y) sont mises à l’échelle pour s’ajuster à la taille de la fenêtre d’affichage en fonction des formules suivantes :


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



Le didacticiel 1 crée une fenêtre d’affichage 640 × 480 à l’aide de [**d3d11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) et en appelant [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



La description de la fenêtre d’affichage spécifie la taille de la fenêtre d’affichage, la plage de la profondeur de la carte (à l’aide de *mindepth* et *maxdepth*) et le placement de l’angle supérieur gauche de la fenêtre d’affichage. *Mindepth* doit être inférieur ou égal à *maxdepth*; la plage pour *mindepth* et *maxdepth* est comprise entre 0,0 et 1,0 inclus. Il est courant que la fenêtre d’affichage soit mappée à une cible de rendu, mais ce n’est pas nécessaire. en outre, la fenêtre d’affichage n’a pas besoin d’avoir la même taille ou position que la cible de rendu.

Vous pouvez créer un tableau de Viewports, mais un seul peut être appliqué à une sortie primitive à partir du nuanceur Geometry. Une seule fenêtre d’affichage peut être activée à la fois. Le pipeline utilise une fenêtre d’affichage par défaut (et un rectangle à ciseaux, présenté dans la section suivante) pendant la pixellisation. La valeur par défaut est toujours le premier Viewport (ou rectangle à ciseaux) dans le tableau. Pour effectuer une sélection par primitive de la fenêtre d’affichage dans le nuanceur Geometry, spécifiez la sémantique ViewportArrayIndex sur le composant de sortie GS approprié dans la déclaration de signature de sortie GS.

Le nombre maximal d’Viewports (et de rectangles ciseaux) qui peuvent être liés à l’étape de rastérisation à un moment donné est 16 (spécifié par **d3d11 \_ VIEWPORT \_ et \_ SCISSORRECT \_ Object \_ Count \_ per \_ pipeline**).

## <a name="set-the-scissor-rectangle"></a>Définir le rectangle de la ciseaux

Un rectangle à ciseaux vous donne une autre possibilité de réduire le nombre de pixels qui seront envoyés à l’étape de fusion de sortie. Les pixels en dehors du rectangle de la ciseaux sont ignorés. La taille du rectangle de la ciseaux est spécifiée dans des entiers. Un seul rectangle symétrique (basé sur *ViewportArrayIndex* dans la [sémantique de valeur système](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) peut être appliqué à un triangle au cours de la pixellisation.

Pour activer le rectangle de la ciseaux, utilisez le membre *ScissorEnable* (dans [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). Le rectangle de la ciseaux par défaut est un rectangle vide. autrement dit, toutes les valeurs Rect sont 0. En d’autres termes, si vous ne configurez pas le rectangle de la ciseaux et que la ciseaux est activée, vous n’allez pas envoyer de pixels à l’étape de fusion de sortie. Le programme d’installation le plus courant consiste à initialiser le rectangle à ciseaux à la taille de la fenêtre d’affichage.

Pour définir un tableau de rectangles de ciseaux sur l’appareil, appelez [**ID3D11DeviceContext :: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) avec [**d3d11 \_ Rect**](d3d11-rect.md).


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Cette méthode prend deux paramètres : (1) le nombre de rectangles dans le tableau et (2) un tableau de rectangles.

Le pipeline utilise un index de rectangles de ciseaux par défaut lors de la pixellisation (la valeur par défaut est un rectangle de taille zéro avec le découpage désactivé). Pour ce faire, spécifiez la \_ sémantique SV ViewportArrayIndex sur un composant de sortie GS dans la déclaration de signature de sortie GS. Ainsi, l’étape GS marque ce composant GS output comme un composant généré par le système avec cette sémantique. L’étape de rastérisation reconnaît cette sémantique et utilise le paramètre auquel elle est attachée en tant qu’index de rectangles de ciseaux pour accéder au tableau de rectangles de ciseaux. N’oubliez pas d’indiquer à l’étape du rastériseur d’utiliser le rectangle de la ciseaux que vous définissez en activant la valeur *ScissorEnable* dans la description du rastériseur avant de créer l’objet rastériseur.

## <a name="set-rasterizer-state"></a>Définir l’état du rastériseur

À partir de Direct3D 10, l’état de rastériseur est encapsulé dans un objet d’État rastériseur. Vous pouvez créer jusqu’à 4096 objets d’État rastériseur qui peuvent ensuite être définis sur l’appareil en passant un handle à l’objet d’État.

Utilisez [**ID3D11Device1 :: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) pour créer un objet d’état de rastériseur à partir d’une description de rastériseur (consultez [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



Cet exemple de jeu d’état effectue peut-être l’installation du rastériseur le plus basique :

-   Mode de remplissage plein
-   Élimination ou suppression des faces arrière ; supposer le sens inverse des aiguilles d’une montre pour les primitives
-   Désactiver le décalage de profondeur, mais activer la mise en mémoire tampon de profondeur et activer le rectangle de la ciseaux
-   Désactiver l’échantillonnage multiple et l’anticrénelage de ligne

En outre, les opérations de rastérisation de base incluent toujours les éléments suivants : découpage (vers la vue frustum), Division de perspective et échelle de la fenêtre d’affichage. Après avoir créé l’objet d’état de rastériseur, définissez-le sur l’appareil comme suit :


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Échantillonnage multiple

L’échantillonnage multiple échantillonne une partie ou la totalité des composants d’une image à une résolution supérieure (suivie d’un sous-échantillonnage à la résolution d’origine) pour réduire la forme d’alias la plus visible provoquée par le dessin des bords de polygones. Même si l’échantillonnage multiple nécessite des exemples de sous-pixels, les GPU modernes implémentent l’échantillonnage multiple afin qu’un nuanceur de pixels s’exécute une fois par pixel. Cela fournit un compromis acceptable entre les performances (surtout dans une application liée au GPU) et l’anticrénelage de l’image finale.

Pour utiliser l’échantillonnage multiple, définissez le champ activer dans la [**Description de pixellisation**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), créez une cible de rendu à échantillonnage multiple et lisez la cible de rendu avec un nuanceur pour résoudre les exemples en une couleur de pixel unique ou appelez [**ID3D11DeviceContext :: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) pour résoudre les exemples à l’aide de la carte vidéo. Le scénario le plus courant consiste à dessiner sur une ou plusieurs cibles de rendu à échantillonnage unique.

L’échantillonnage multiple est indépendant du fait qu’un exemple de masque est utilisé, qu’il soit activé ou non, ou que les opérations [du](d3d10-graphics-programming-guide-blend-state.md) stencil (qui sont toujours effectuées par exemple).

Le test de profondeur est affecté par l’échantillonnage multiple :

-   Lorsque l’échantillonnage multiple est activé, la profondeur est interpolée par échantillon et le test de profondeur/stencil est effectué par échantillon. la couleur de sortie du nuanceur de pixels est dupliquée pour tous les exemples de passage. Si le nuanceur de pixels génère une profondeur, la valeur de profondeur est dupliquée pour tous les échantillons (même si ce scénario perd l’avantage de l’échantillonnage multiple).
-   Lorsque l’échantillonnage multiple est désactivé, le test de profondeur/gabarit est toujours effectué par échantillon, mais la profondeur n’est pas interpolée par échantillon.

Il n’existe aucune restriction pour mélanger un rendu à échantillonnage et non multiéchantillonnés dans une cible de rendu unique. Si vous activez l’échantillonnage multiple et que vous dessinez sur une cible de rendu non multiéchantillonnée, vous obtenez le même résultat que si l’échantillonnage multiple n’était pas activé. l’échantillonnage s’effectue avec un seul échantillon par pixel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape du rastériseur](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 