---
title: Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)
description: L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316978"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="413c9-103">Valeur de référence du stencil spécifié par le nuanceur (Direct3D 11 Graphics)</span><span class="sxs-lookup"><span data-stu-id="413c9-103">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="413c9-104">L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.</span><span class="sxs-lookup"><span data-stu-id="413c9-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="413c9-105">La valeur spécifiée du nuanceur remplace la *valeur de référence du stencil* spécifiée par l’API pour cet appel, ce qui signifie que la modification affecte à la fois le test de stencil, et lorsque stencil op d3d11 \_ stencil \_ op \_ remplacer (un membre de [**d3d11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) est utilisé pour écrire la valeur de référence dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="413c9-105">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="413c9-106">Dans les versions antérieures de D3D11, la valeur de référence du stencil ne peut être spécifiée que par la méthode [**ID3D11DeviceContext :: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) .</span><span class="sxs-lookup"><span data-stu-id="413c9-106">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="413c9-107">Cela signifie que cette valeur ne peut être définie que sur une granularité par dessin.</span><span class="sxs-lookup"><span data-stu-id="413c9-107">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="413c9-108">Cette fonctionnalité D3D 11.3 permet aux développeurs de lire et d’utiliser la valeur de référence du stencil ( `SV_StencilRef` ) qui est la sortie d’un nuanceur de pixels, ce qui signifie qu’elle peut être spécifiée sur une granularité par pixel ou par échantillon.</span><span class="sxs-lookup"><span data-stu-id="413c9-108">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="413c9-109">Cette fonctionnalité est facultative dans D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="413c9-109">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="413c9-110">Pour tester sa prise en charge, vérifiez le `PSSpecifiedStencilRefSupported` champ booléen des données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) à l’aide de [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="413c9-110">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="413c9-111">Voici un exemple d’utilisation de `SV_StencilRef` dans un nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="413c9-111">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="413c9-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="413c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="413c9-113">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="413c9-113">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="413c9-114">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="413c9-114">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
