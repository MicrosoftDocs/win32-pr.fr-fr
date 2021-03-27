---
title: Configuration de la fonctionnalité Depth-Stencil
description: Cette section décrit les étapes de configuration de la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur pour l’étape de fusion de sortie.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728741"
---
# <a name="configuring-depth-stencil-functionality"></a>Configuration de la fonctionnalité Depth-Stencil

Cette section décrit les étapes de configuration de la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur pour l’étape de fusion de sortie.

-   [Créer une ressource Depth-Stencil](#create-a-depth-stencil-resource)
-   [Créer un état de Depth-Stencil](#create-depth-stencil-state)
-   [Lier Depth-Stencil données à l’étape OM](#bind-depth-stencil-data-to-the-om-stage)

Une fois que vous savez comment utiliser la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur correspondant, reportez-vous à [techniques de stencil avancées](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Créer une ressource Depth-Stencil

Créez la mémoire tampon du stencil de profondeur à l’aide d’une ressource de texture.


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>Créer un état de Depth-Stencil

L’état de gabarit de profondeur indique à l’étape de fusion de sortie comment effectuer le [test de stencil de profondeur](d3d10-graphics-programming-guide-output-merger-stage.md). Le test de stencil de profondeur détermine si un pixel donné doit être dessiné ou non.


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable et StencilEnable activent (et désactivent) le test de profondeur et de stencil. Affectez à DepthEnable la **valeur false** pour désactiver le test de profondeur et empêcher l’écriture dans le tampon de profondeur. Définissez StencilEnable sur **false** pour désactiver le test stencil et empêcher l’écriture dans la mémoire tampon du stencil (lorsque DepthEnable a la **valeur false** et que StencilEnable a la **valeur true**, le test de profondeur passe toujours dans l’opération de stencil).

DepthEnable affecte uniquement l’étape de fusion de sortie. il n’affecte pas le découpage, le décalage de profondeur ou le verrouillage des valeurs avant que les données ne soient entrées dans un nuanceur de pixels.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Lier Depth-Stencil données à l’étape OM

Liez l’état de gabarit de profondeur.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Liez la ressource de stencil de profondeur à l’aide d’une vue.


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



Un tableau de vues de cible de rendu peut être passé dans [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), mais toutes ces vues de cible de rendu correspondent à une vue de stencil de profondeur unique. Le tableau de la cible de rendu dans Direct3D 11 est une fonctionnalité qui permet à une application d’effectuer un rendu sur plusieurs cibles de rendu simultanément au niveau de la primitive. Les tableaux cibles de rendu offrent des performances accrues par rapport à la définition individuelle des cibles de rendu avec plusieurs appels à **ID3D11DeviceContext :: OMSetRenderTargets** (essentiellement la méthode utilisée dans Direct3D 9).

Les cibles de rendu doivent toutes être du même type de ressource. Si l’anticrénelage est utilisé, toutes les cibles de rendu liées et les tampons de profondeur doivent avoir le même nombre d’échantillons.

Quand une mémoire tampon est utilisée comme cible de rendu, le test du stencil de profondeur et les cibles de rendu multiples ne sont pas pris en charge.

-   Jusqu’à 8 cibles de rendu peuvent être liées simultanément.
-   Toutes les cibles de rendu doivent avoir la même taille dans toutes les dimensions (largeur et hauteur, et profondeur pour la taille 3D ou de tableau pour les \* types tableau).
-   Chaque cible de rendu peut avoir un format de données différent.
-   Les masques d’écriture contrôlent les données qui sont écrites dans une cible de rendu. L’écriture de sortie masque le contrôle sur une cible par rendu, au niveau de chaque composant, quelles données sont écrites dans la ou les cibles de rendu.

## <a name="advanced-stencil-techniques"></a>Techniques avancées de stencil

La partie stencil de la mémoire tampon du stencil de profondeur peut être utilisée pour créer des effets de rendu tels que la composition, le décalque et le mode plan.

-   [Composition](#compositing)
-   [Décalque](#decaling)
-   [Plans et silhouettes](#outlines-and-silhouettes)
-   [Stencil recto-verso](#two-sided-stencil)
-   [Lecture de la mémoire tampon de Depth-Stencil sous forme de texture](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Composition

Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D. Un masque dans le tampon de stencil est utilisé pour occultait une zone de la surface cible de rendu. Des informations 2D stockées, telles que du texte ou des bitmaps, peuvent ensuite être écrites dans la zone bloqués. Votre application peut également restituer des primitives 3D supplémentaires dans la région masquée du stencil de la surface cible de rendu. Il peut même rendre une scène entière.

Les jeux composent souvent plusieurs scènes 3D ensemble. Par exemple, la conduite des jeux affiche généralement un miroir en mode arrière. Le miroir contient la vue de la scène 3D derrière le pilote. Il s’agit essentiellement d’une deuxième scène 3D composite avec la vue d’avance du pilote.

### <a name="decaling"></a>Décalque

Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu. Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.

Par exemple, lorsque vous appliquez des marques de pneu et des lignes jaunes à une chaussée, les marquages doivent apparaître directement en haut de la route. Toutefois, les valeurs z des marquages et de la route sont les mêmes. Par conséquent, il se peut que la mémoire tampon de profondeur ne produise pas une séparation nette entre les deux. Certains pixels de la primitive arrière peuvent être rendus au-dessus de la primitive avant et vice versa. L’image résultante semble en scintillement du cadre au frame. Cet effet est appelé z-combat ou flimmering.

Pour résoudre ce problème, utilisez un gabarit pour masquer la section de la primitive de retour où le décalcomanie s’affichera. Désactivez la mise en mémoire tampon z et affichez l’image de la primitive avant dans la zone masquée de la surface de rendu-cible.

Plusieurs fusions de texture peuvent être utilisées pour résoudre ce problème.

### <a name="outlines-and-silhouettes"></a>Plans et silhouettes

Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.

Si votre application effectue deux passes de rendu, une pour générer le masque de stencil et la seconde pour appliquer le masque de stencil à l’image, mais avec les primitives légèrement plus petites sur la deuxième passe, l’image résultante contient uniquement le contour de la primitive. L’application peut ensuite remplir la zone masquée du gabarit de l’image avec une couleur unie, ce qui donne à la primitive un aspect en relief.

Si la taille et la forme du masque du gabarit sont identiques à celles de la primitive que vous affichez, l’image résultante contient un trou où la primitive doit être. Votre application peut alors remplir le trou avec du noir pour produire une silhouette de la primitive.

### <a name="two-sided-stencil"></a>Two-Sided le stencil

Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil. L’application calcule les volumes de clichés instantanés convertis par la géométrie de la Boucher, en calculant les bords silhouettes et en les séparant de la lumière dans un ensemble de volumes 3D. Ces volumes sont ensuite restitués deux fois dans la mémoire tampon du stencil.

Le premier rendu dessine des polygones vers l’avant et incrémente les valeurs de mémoire tampon de stencil. Le deuxième rendu dessine les polygones de l’arrière-plan du volume de cliché instantané et décrémente les valeurs de la mémoire tampon du stencil. Normalement, toutes les valeurs incrémentées et décrémentées s’annulent les unes des autres. Toutefois, la scène était déjà rendue avec une géométrie normale provoquant l’échec du test de la mémoire tampon z pour certains pixels, car le volume de cliché instantané est rendu. Les valeurs laissées dans la mémoire tampon du stencil correspondent aux pixels qui se trouvent dans l’ombre. Ces contenus de tampons de stencil restants sont utilisés comme masque, afin de mélanger en 3D un grand nombre de cœurs noirs englobant tous dans la scène. Avec la mémoire tampon de stencil jouant le rôle de masque, le résultat est d’assombrir les pixels qui se trouvent dans les ombres.

Cela signifie que la géométrie de l’ombre est dessinée deux fois par source de lumière, ce qui entraîne une pression sur le débit du vertex du GPU. La fonctionnalité de stencil à deux côtés a été conçue pour atténuer cette situation. Dans cette approche, il existe deux ensembles de l’état du gabarit (nommés ci-dessous), un jeu pour les triangles frontaux et l’autre pour les triangles de face arrière. De cette façon, une seule passe est dessinée par volume de cliché instantané, par lumière.

Vous trouverez un exemple d’implémentation de stencil à deux côtés dans l' [exemple ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Lecture de la mémoire tampon de Depth-Stencil sous forme de texture

Une mémoire tampon de stencil de profondeur inactive peut être lue par un nuanceur comme une texture. Une application qui lit une mémoire tampon de stencil de profondeur comme une texture est rendue en deux passes, la première passe écrit dans la mémoire tampon de stencil de profondeur et la deuxième passe lit à partir de la mémoire tampon. Cela permet à un nuanceur de comparer les valeurs de la profondeur ou du gabarit précédemment écrites dans la mémoire tampon par rapport à la valeur du Notez pixel qui est affiché. Le résultat de la comparaison peut être utilisé pour créer des effets tels que le mappage de clichés instantanés ou les particules souples dans un système de particules.

Pour créer une mémoire tampon de stencil de profondeur qui peut être utilisée à la fois comme ressource de stencil de profondeur et comme ressource de nuanceur, quelques modifications doivent être apportées à l’exemple de code dans la section [créer une ressource de Depth-Stencil](#create-a-depth-stencil-resource) .

-   La ressource de stencil de profondeur doit avoir un format non typé tel que DXGI \_ format \_ R32 type non \_ .
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   La ressource de stencil de profondeur doit utiliser à la fois le \_ stencil de profondeur de liaison D3D10 et les \_ \_ indicateurs de liaison de ressource de \_ nuanceur de liaison D3D10 \_ \_ .
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

En outre, une vue de ressource de nuanceur doit être créée pour la mémoire tampon de profondeur à l’aide d’une structure de [**\_ vue de \_ ressource \_ \_ d3d11 Shader**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) et de [**ID3D11Device :: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview). La vue de ressource de nuanceur utilise un format typé tel que **dxgi \_ format \_ R32 \_ float** , qui est l’équivalent au format de type non spécifié lors de la création de la ressource de stencil de profondeur.

Dans la première passe de rendu, le tampon de profondeur est lié comme décrit dans la section [lier les données Depth-Stencil à la phase OM](#bind-depth-stencil-data-to-the-om-stage) . Notez que le format est passé à la [**\_ vue du stencil de profondeur d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Le format utilise un format typé tel que **dxgi \_ format \_ d32 \_ float**. Après la première passe de rendu, la mémoire tampon de profondeur contient les valeurs de profondeur pour la scène.

Dans la deuxième étape de rendu, la fonction [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) est utilisée pour définir la vue de stencil de profondeur sur **null** ou une ressource de stencil de profondeur différente, et la vue de ressource de nuanceur est transmise au nuanceur à l’aide de [**ID3D11EffectShaderResourceVariable :: SetResource**](id3dx11effectshaderresourcevariable-setresource.md). Cela permet au nuanceur de rechercher les valeurs de profondeur calculées dans la première passe de rendu. Notez qu’une transformation devra être appliquée pour récupérer les valeurs de profondeur si le point de vue de la première passe de rendu est différent de la deuxième passe de rendu. Par exemple, si une technique de mappage des clichés instantanés est utilisée, la première passe de rendu sera du point de vue d’une source de lumière, tandis que la deuxième passe de rendu va du point de vue de la visionneuse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sortie-étape de fusion](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 