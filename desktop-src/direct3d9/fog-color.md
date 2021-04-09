---
description: La couleur de brouillard pour le brouillard de pixel et de vertex est définie via l' \_ État de rendu D3DRS FOGCOLOR. Les valeurs d’état de rendu peuvent être n’importe quelle couleur RVB, spécifiée comme une couleur RVBA. Le composant alpha est ignoré.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Couleur de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033365"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="5ef57-105">Couleur de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5ef57-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="5ef57-106">La couleur de brouillard pour le brouillard de pixel et de vertex est définie via l' \_ État de rendu D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="5ef57-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="5ef57-107">Les valeurs d’état de rendu peuvent être n’importe quelle couleur RVB, spécifiée comme une couleur RVBA.</span><span class="sxs-lookup"><span data-stu-id="5ef57-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="5ef57-108">Le composant alpha est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5ef57-108">The alpha component is ignored.</span></span>

<span data-ttu-id="5ef57-109">L’exemple C++ suivant définit la couleur de brouillard sur blanc.</span><span class="sxs-lookup"><span data-stu-id="5ef57-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="5ef57-110">Le brouillard est appliqué différemment par le pipeline de fonction fixe et le pipeline programmable.</span><span class="sxs-lookup"><span data-stu-id="5ef57-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="5ef57-111">Si le pilote prend en charge D3DPMISCCAPS \_ FOGANDSPECULARALPHA :</span><span class="sxs-lookup"><span data-stu-id="5ef57-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="5ef57-112">Si le pipeline de fonction fixe est utilisé et que D3DRS \_ FOGCOLOR est défini, v1. w (dans le nuanceur de pixels) est égal à la valeur définie dans le RenderState de brouillard.</span><span class="sxs-lookup"><span data-stu-id="5ef57-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="5ef57-113">Si le pipeline programmable est utilisé, v1. w (dans le nuanceur de pixels) est égal à 0, même si oD1. w est écrit explicitement dans un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="5ef57-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="5ef57-114">Si le pilote ne prend pas en charge D3DPMISCCAPS \_ FOGANDSPECULARALPHA :</span><span class="sxs-lookup"><span data-stu-id="5ef57-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="5ef57-115">Si le pipeline de fonction fixe est utilisé et que D3DRS \_ FOGCOLOR est défini, v1. w (dans le nuanceur de pixels) est égal à la valeur définie dans le RenderState de brouillard.</span><span class="sxs-lookup"><span data-stu-id="5ef57-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="5ef57-116">Si oFog est écrit explicitement dans un nuanceur de sommets, v1. w (dans le nuanceur de pixels) est égal à oFog, placé entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="5ef57-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="5ef57-117">Si aucun des deux cas ci-dessus ne s’applique, v1. w (dans le nuanceur de pixels) est égal à 0, même si oD1. w est écrit explicitement dans un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="5ef57-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="5ef57-118">Pour plus d’informations, consultez [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="5ef57-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ef57-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ef57-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef57-120">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="5ef57-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



