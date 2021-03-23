---
title: Valeur de référence du stencil spécifié par le nuanceur (Direct3D 12 Graphics)
description: L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548555"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Valeur de référence du stencil spécifié par le nuanceur (Direct3D 12 Graphics)

L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.

La valeur de référence du stencil est normalement spécifiée par la méthode [**ID3D12GraphicsCommandList :: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) . Cette méthode définit la valeur de référence du stencil sur une granularité par dessin. Toutefois, cette valeur peut être remplacée par le nuanceur de pixels.

Cette fonctionnalité D3D12 (et D3D 11.3) permet aux développeurs de lire et d’utiliser la valeur de référence du stencil (*SV \_ StencilRef*) qui est la sortie d’un nuanceur de pixels, ce qui permet une granularité par pixel ou par échantillon.

La valeur spécifiée du nuanceur remplace la valeur de référence spécifiée par l’API pour cet appel, ce qui signifie que la modification affecte à la fois le test de stencil, et lorsque l’opération de stencil D3D12 \_ stencil \_ op \_ remplacer (un membre de [**D3D12 \_ stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) est utilisée pour écrire la valeur de référence dans la mémoire tampon de stencil.

Cette fonctionnalité est facultative dans D3D12 et D3D 11.3. Pour tester sa prise en charge, consultez le champ *PSSpecifiedStencilRefSupported* Boolean de [**D3D12 \_ Feature \_ Data \_ D3D12 \_ options**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Voici un exemple d’utilisation de *SV \_ StencilRef* dans un nuanceur de pixels :

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu](rendering.md)
</dt> <dt>

[Liaison de ressources en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Spécification de signatures racines en langage HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
