---
description: La valeur alpha d’une couleur contrôle sa transparence. L’activation de la fusion alpha permet de fusionner les couleurs, les matériaux et les textures sur une surface avec une transparence sur une autre surface.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: État de fusion alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393123"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="07d4d-104">État de fusion alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07d4d-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="07d4d-105">La valeur alpha d’une couleur contrôle sa transparence.</span><span class="sxs-lookup"><span data-stu-id="07d4d-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="07d4d-106">L’activation de la fusion alpha permet de fusionner les couleurs, les matériaux et les textures sur une surface avec une transparence sur une autre surface.</span><span class="sxs-lookup"><span data-stu-id="07d4d-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="07d4d-107">Pour plus d’informations, consultez [fusion de texture alpha (Direct3D 9)](alpha-texture-blending.md) et [fusion de texture (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="07d4d-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="07d4d-108">Les applications écrites en C++ utilisent l’état de rendu [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) pour activer la fusion de la transparence alpha.</span><span class="sxs-lookup"><span data-stu-id="07d4d-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="07d4d-109">L’API Direct3D autorise un grand nombre de types de fusions alpha.</span><span class="sxs-lookup"><span data-stu-id="07d4d-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="07d4d-110">Toutefois, il est important de noter que le matériel 3D de l’utilisateur peut ne pas prendre en charge tous les États de fusion autorisés par Direct3D.</span><span class="sxs-lookup"><span data-stu-id="07d4d-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="07d4d-111">Le type de fusion alpha effectué dépend des États de rendu [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) et **D3DRS \_ DESTBLEND** .</span><span class="sxs-lookup"><span data-stu-id="07d4d-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="07d4d-112">Les États de fusion de source et de destination sont utilisés par paires.</span><span class="sxs-lookup"><span data-stu-id="07d4d-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="07d4d-113">L’exemple de code suivant montre comment l’état de fusion source est défini sur D3DBLEND \_ SRCCOLOR et que l’état de fusion de destination est défini sur D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="07d4d-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="07d4d-114">La modification des États de fusion source et de destination peut entraîner l’apparition d’objets émissif dans une atmosphère à la buée ou poussiéreuse.</span><span class="sxs-lookup"><span data-stu-id="07d4d-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="07d4d-115">Par exemple, si votre application modélise des flammes, des champs de force, des faisceaux plasma ou des objets rayonnants de la même manière, définissez les États de fusion source et destination sur D3DBLEND \_ .</span><span class="sxs-lookup"><span data-stu-id="07d4d-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="07d4d-116">Une autre application de la fusion alpha consiste à contrôler l’éclairage dans une scène 3D, également appelée « mappage de lumière ».</span><span class="sxs-lookup"><span data-stu-id="07d4d-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="07d4d-117">La définition de l’état de fusion source sur D3DBLEND \_ zéro et l’état de fusion de destination sur D3DBLEND \_ SRCALPHA assombrit une scène en fonction des informations alpha de la source.</span><span class="sxs-lookup"><span data-stu-id="07d4d-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="07d4d-118">La primitive source est utilisée comme une carte légère qui met à l’échelle le contenu de la mémoire tampon de trame pour l’assombrir quand cela est approprié.</span><span class="sxs-lookup"><span data-stu-id="07d4d-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="07d4d-119">Cela produit un mappage de lumière monochrome.</span><span class="sxs-lookup"><span data-stu-id="07d4d-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="07d4d-120">Vous pouvez obtenir le mappage de la lumière en couleur en définissant l’état de fusion alpha source sur D3DBLEND \_ zéro et l’état de fusion de destination sur D3DBLEND \_ SRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="07d4d-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07d4d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07d4d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d4d-122">États de rendu</span><span class="sxs-lookup"><span data-stu-id="07d4d-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
