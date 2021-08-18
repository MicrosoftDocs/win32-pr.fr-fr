---
title: Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)
description: En savoir plus sur la valeur de référence du stencil dans les graphiques Direct3D 11. L’activation des nuanceurs de pixels pour utiliser la valeur de référence du stencil permet un contrôle précis des opérations du stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d780c7a800f4291b3cce01c6f974cdeedaa8f590fc76fdf8afa8b3fb3c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632309"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)

L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.

La valeur spécifiée du nuanceur remplace la *valeur de référence du stencil* spécifiée par l’API pour cet appel, ce qui signifie que la modification affecte à la fois le test de stencil, et lorsque stencil op d3d11 \_ stencil \_ op \_ remplacer (un membre de [**d3d11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) est utilisé pour écrire la valeur de référence dans la mémoire tampon du stencil.

Dans les versions antérieures de D3D11, la valeur de référence du stencil ne peut être spécifiée que par la méthode [**ID3D11DeviceContext :: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) . Cela signifie que cette valeur ne peut être définie que sur une granularité par dessin. Cette fonctionnalité D3D 11.3 permet aux développeurs de lire et d’utiliser la valeur de référence du stencil ( `SV_StencilRef` ) qui est la sortie d’un nuanceur de pixels, ce qui signifie qu’elle peut être spécifiée sur une granularité par pixel ou par échantillon.

Cette fonctionnalité est facultative dans D3D 11.3. Pour tester sa prise en charge, vérifiez le `PSSpecifiedStencilRefSupported` champ booléen des données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) à l’aide de [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Voici un exemple d’utilisation de `SV_StencilRef` dans un nuanceur de pixels :

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
