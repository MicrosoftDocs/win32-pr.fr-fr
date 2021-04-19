---
description: Le test de ciseaux élimine les pixels qui se trouvent en dehors du rectangle symétrique, une sous-section rectangulaire définie par l’utilisateur de la cible de rendu.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Test de ciseaux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516760"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="b7d07-103">Test de ciseaux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b7d07-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="b7d07-104">Le test de ciseaux élimine les pixels qui se trouvent en dehors du rectangle symétrique, une sous-section rectangulaire définie par l’utilisateur de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b7d07-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="b7d07-105">Le rectangle à ciseaux peut être utilisé pour indiquer la zone de la cible de rendu où le monde du jeu est dessiné.</span><span class="sxs-lookup"><span data-stu-id="b7d07-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="b7d07-106">La zone en dehors du rectangle est Culling et peut être dédiée à l’interface utilisateur graphique d’un jeu.</span><span class="sxs-lookup"><span data-stu-id="b7d07-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="b7d07-107">Le test de ciseaux ne peut pas les zones non rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="b7d07-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="b7d07-108">Les rectangles de ciseaux ne peuvent pas être plus grands que la cible de rendu, mais ils peuvent être plus grands que la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b7d07-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="b7d07-109">Le rectangle de la ciseaux est géré par un état de rendu de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b7d07-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="b7d07-110">Un test de ciseaux est activé ou désactivé en affectant à RenderState la **valeur true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="b7d07-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="b7d07-111">Ce test est effectué après le calcul de la couleur du fragment, mais avant le test alpha.</span><span class="sxs-lookup"><span data-stu-id="b7d07-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="b7d07-112">[**IDirect3DDevice9 :: SetRenderTarget**](/windows/desktop/api) réinitialise le rectangle de la ciseaux sur la cible de rendu complète, similaire à la fenêtre d’affichage réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="b7d07-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="b7d07-113">[**IDirect3DDevice9 :: SetScissorRect**](/windows/desktop/api) est enregistré par Stateblocks et [**IDirect3DDevice9 :: CreateStateBlock**](/windows/desktop/api) avec le paramètre d’État All (D3DSBT \_ toute la valeur dans [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="b7d07-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="b7d07-114">Le test de ciseaux affecte également l’opération [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b7d07-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="b7d07-115">Le rectangle à ciseaux par défaut est la fenêtre d’affichage complète.</span><span class="sxs-lookup"><span data-stu-id="b7d07-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="b7d07-116">Le test de ciseaux est effectué juste après la fin du traitement des pixels par un nuanceur de pixels ou le pipeline de fonction fixe, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b7d07-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![diagramme de l’exécution du test de ciseaux par rapport à d’autres étapes](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="b7d07-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7d07-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7d07-119">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="b7d07-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
