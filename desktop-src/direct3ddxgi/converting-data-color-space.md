---
description: Pour composer à l’écran ou effectuer des opérations à virgule flottante, vous devez travailler dans l’espace de couleurs correct.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Conversion de données pour l’espace colorimétrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745933"
---
# <a name="converting-data-for-the-color-space"></a>Conversion de données pour l’espace colorimétrique

Pour composer à l’écran ou effectuer des opérations à virgule flottante, vous devez travailler dans l’espace de couleurs correct. Nous vous recommandons d’effectuer des opérations en virgule flottante dans un espace colorimétrique linéaire. Ensuite, pour présenter vos images à l’écran, convertissez les données en données RVB standard (sRGB, gamma 2,2-corrigé). La présentation de l’espace de couleurs sRVB à l’écran est importante pour la précision des couleurs. Si les images ne sont pas gamma 2,2-corrigées, elles allouent trop de bits ou trop de bande passante pour mettre en évidence que les gens ne peuvent pas différencier, et trop peu de bits ou de bande passante pour les valeurs fantômes auxquelles les personnes sont sensibles, et nécessitent donc plus de bits ou de bande passante pour maintenir la même qualité visuelle. Par conséquent, pour garantir une meilleure précision des couleurs, présentez les images à l’écran correspondant à la valeur gamma 2,2-corrigée.

-   [Précision des couleurs](#color-accuracy)
-   [Rubriques connexes](#related-topics)

## <a name="color-accuracy"></a>Précision des couleurs

Pour la présentation, les formats d’affichage à valeurs entières (tels que [**dxgi \_ format \_ B8G8R8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), etc.) contiennent toujours des données de correction gamma RVB. Les formats d’affichage à valeurs float (actuellement uniquement [**dxgi \_ format \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contiennent des données linéaires.

Le \_ [modificateur de format](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRVB indique au système d’exploitation d’aider l’application à placer des données sRVB à l’écran. L’application doit toujours placer les données sRVB dans des mémoires tampons d’arrière-plan avec des formats à valeurs entières pour présenter les données sRVB à l’écran, même si les données n’ont pas ce modificateur de format dans son nom de format. Pour obtenir la liste complète des formats d’analyse d’affichage :

-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Prise en charge matérielle pour les formats Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Prise en charge du matériel pour les formats Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Prise en charge matérielle pour les formats Direct3D 10](/previous-versions//cc627090(v=vs.85))

Lorsque vous écrivez des valeurs de sortie à virgule flottante à partir du nuanceur de pixels dans des vues de cible de rendu (**RenderTargetView**) avec le \_ [modificateur de format](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRVB lié au [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), vous les convertissez en espace de couleurs corrigé gamma 2,2. De même, lorsque les vues de ressource de nuanceur (**ShaderResourceView**) avec le \_ modificateur de format sRVB sont liées au pipeline, vous convertissez les valeurs de l’espace de couleurs gamma 2,2-corrigé en espace de couleurs linéaire lorsque vous les Lisez à partir de **ShaderResourceView** s. Le nuanceur peut ensuite effectuer des opérations sur ceux-ci.

Par exemple, utilisez un code similaire à celui-ci pour écrire des valeurs de sortie à virgule flottante à partir d’un nuanceur dans un format **RenderTargetView** :


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



Lorsque la routine de est retournée, les valeurs à virgule flottante (1, 0, 0, 1) sont converties au format **RenderTargetView** . Ensuite, si vous assignez le \_ [modificateur de format](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB à **RenderTargetView**, la conversion gamma se produit.

Voici les étapes à suivre pour vous assurer que le contenu affiché sur l’écran présente la meilleure précision en matière de couleurs.

**Pour garantir la précision des couleurs dans le pipeline**

1.  Si une texture contient du contenu sRVB, assurez-vous que le **ShaderResourceView** a le \_ [modificateur de format](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRVB. ainsi, lorsque vous lisez à partir du **ShaderResourceView** dans le nuanceur, vous convertissez le contenu de la texture de l’espace de couleurs gamma 2,2-corrigé en espace colorimétrique linéaire.
2.  Assurez-vous que le **RenderTargetView** a également le \_ [modificateur de format](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB afin que les valeurs de sortie du nuanceur soient converties.

Si vous suivez les étapes précédentes, quand vous appelez la méthode [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , le contenu qui s’affiche sur l’écran présente le meilleur niveau de précision des couleurs.

Vous pouvez utiliser la méthode [**ID3D11Device :: CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) pour créer des vues **\_ \_ \* \_ sRVB au format dxgi** sur les mémoires tampons d’arrière-plan à partir d’une chaîne de permutation que vous créez uniquement avec un format **dxgi \_ \_ \* \_ UNORM** . Il s’agit d’une exception spéciale à la règle pour créer des vues de cible de rendu, ce qui indique que vous pouvez utiliser un format différent avec **ID3D11Device :: CreateRenderTargetView** uniquement si vous avez créé la ressource que vous souhaitez afficher avec le **format dxgi sans \_ \_ \* \_ type**.

Pour plus d’informations sur les règles de conversion des données, consultez [règles de conversion des données](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Pour plus d’informations sur la façon de lire et d’écrire simultanément dans une texture, consultez [décompresser et empaqueter le \_ format DXGI pour la modification d’image In-Place](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration de la présentation avec le modèle de retournement, les rectangles modifiés et les zones défilantes](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
