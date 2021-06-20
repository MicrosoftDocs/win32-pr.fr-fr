---
title: Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)
description: En savoir plus sur la valeur de référence du stencil dans les graphiques Direct3D 11. L’activation des nuanceurs de pixels pour utiliser la valeur de référence du stencil permet un contrôle précis des opérations du stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408102"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="d37ed-104">Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)</span><span class="sxs-lookup"><span data-stu-id="d37ed-104">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="d37ed-105">L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.</span><span class="sxs-lookup"><span data-stu-id="d37ed-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="d37ed-106">La valeur spécifiée du nuanceur remplace la *valeur de référence du stencil* spécifiée par l’API pour cet appel, ce qui signifie que la modification affecte à la fois le test de stencil, et lorsque stencil op d3d11 \_ stencil \_ op \_ remplacer (un membre de [**d3d11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) est utilisé pour écrire la valeur de référence dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="d37ed-106">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="d37ed-107">Dans les versions antérieures de D3D11, la valeur de référence du stencil ne peut être spécifiée que par la méthode [**ID3D11DeviceContext :: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) .</span><span class="sxs-lookup"><span data-stu-id="d37ed-107">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="d37ed-108">Cela signifie que cette valeur ne peut être définie que sur une granularité par dessin.</span><span class="sxs-lookup"><span data-stu-id="d37ed-108">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="d37ed-109">Cette fonctionnalité D3D 11.3 permet aux développeurs de lire et d’utiliser la valeur de référence du stencil ( `SV_StencilRef` ) qui est la sortie d’un nuanceur de pixels, ce qui signifie qu’elle peut être spécifiée sur une granularité par pixel ou par échantillon.</span><span class="sxs-lookup"><span data-stu-id="d37ed-109">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="d37ed-110">Cette fonctionnalité est facultative dans D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="d37ed-110">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="d37ed-111">Pour tester sa prise en charge, vérifiez le `PSSpecifiedStencilRefSupported` champ booléen des données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) à l’aide de [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="d37ed-111">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="d37ed-112">Voici un exemple d’utilisation de `SV_StencilRef` dans un nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="d37ed-112">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="d37ed-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d37ed-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d37ed-114">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="d37ed-114">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="d37ed-115">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="d37ed-115">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
