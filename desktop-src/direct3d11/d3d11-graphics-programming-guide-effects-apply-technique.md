---
title: Appliquer une technique (Direct3D 11)
description: Découvrez comment définir l’état de l’effet dans l’appareil pour Direct3D 11 après que les constantes, les textures et l’état du nuanceur sont déclarés et initialisés.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118944"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="83864-103">Appliquer une technique (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="83864-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="83864-104">Avec les constantes, les textures et l’état du nuanceur déclarés et initialisés, la seule chose à faire est de définir l’état de l’effet dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="83864-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="83864-105">Définir un état de non-nuanceur dans l’appareil</span><span class="sxs-lookup"><span data-stu-id="83864-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="83864-106">Un état de pipeline n’est pas défini par un effet.</span><span class="sxs-lookup"><span data-stu-id="83864-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="83864-107">Par exemple, la suppression d’une cible de rendu prépare la cible de rendu pour les données.</span><span class="sxs-lookup"><span data-stu-id="83864-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="83864-108">Avant de définir l’état de l’effet dans l’appareil, voici un exemple d’effacement des tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="83864-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="83864-109">Définir l’état de l’effet dans l’appareil</span><span class="sxs-lookup"><span data-stu-id="83864-109">Set Effect State in the Device</span></span>

<span data-ttu-id="83864-110">La définition de l’état d’effet s’effectue en appliquant l’état d’effet dans la boucle de rendu.</span><span class="sxs-lookup"><span data-stu-id="83864-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="83864-111">Cette opération s’effectue à partir de l’extérieur de.</span><span class="sxs-lookup"><span data-stu-id="83864-111">This is done from the outside in.</span></span> <span data-ttu-id="83864-112">Autrement dit, sélectionnez une technique, puis définissez l’État pour chacune des passes (selon le résultat souhaité).</span><span class="sxs-lookup"><span data-stu-id="83864-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="83864-113">Un effet n’affiche rien, il définit simplement l’état de l’effet sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="83864-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="83864-114">Le code de rendu est appelé après que l’état de l’effet a mis à jour l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="83864-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="83864-115">Dans cet exemple, l’appel DrawIndexed effectue le rendu.</span><span class="sxs-lookup"><span data-stu-id="83864-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83864-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83864-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83864-117">Rendu d’un effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="83864-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




