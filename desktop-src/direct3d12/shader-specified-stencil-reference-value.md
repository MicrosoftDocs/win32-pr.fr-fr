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
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="0da66-103">Valeur de référence du stencil spécifié par le nuanceur (Direct3D 12 Graphics)</span><span class="sxs-lookup"><span data-stu-id="0da66-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="0da66-104">L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.</span><span class="sxs-lookup"><span data-stu-id="0da66-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="0da66-105">La valeur de référence du stencil est normalement spécifiée par la méthode [**ID3D12GraphicsCommandList :: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="0da66-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="0da66-106">Cette méthode définit la valeur de référence du stencil sur une granularité par dessin.</span><span class="sxs-lookup"><span data-stu-id="0da66-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="0da66-107">Toutefois, cette valeur peut être remplacée par le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="0da66-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="0da66-108">Cette fonctionnalité D3D12 (et D3D 11.3) permet aux développeurs de lire et d’utiliser la valeur de référence du stencil (*SV \_ StencilRef*) qui est la sortie d’un nuanceur de pixels, ce qui permet une granularité par pixel ou par échantillon.</span><span class="sxs-lookup"><span data-stu-id="0da66-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="0da66-109">La valeur spécifiée du nuanceur remplace la valeur de référence spécifiée par l’API pour cet appel, ce qui signifie que la modification affecte à la fois le test de stencil, et lorsque l’opération de stencil D3D12 \_ stencil \_ op \_ remplacer (un membre de [**D3D12 \_ stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) est utilisée pour écrire la valeur de référence dans la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="0da66-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="0da66-110">Cette fonctionnalité est facultative dans D3D12 et D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="0da66-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="0da66-111">Pour tester sa prise en charge, consultez le champ *PSSpecifiedStencilRefSupported* Boolean de [**D3D12 \_ Feature \_ Data \_ D3D12 \_ options**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="0da66-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="0da66-112">Voici un exemple d’utilisation de *SV \_ StencilRef* dans un nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="0da66-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="0da66-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0da66-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da66-114">Rendu</span><span class="sxs-lookup"><span data-stu-id="0da66-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="0da66-115">Liaison de ressources en HLSL</span><span class="sxs-lookup"><span data-stu-id="0da66-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="0da66-116">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0da66-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="0da66-117">Spécification de signatures racines en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="0da66-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
