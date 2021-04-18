---
description: Certaines cartes accélérateur 3D plus anciennes ne prennent pas en charge la fusion de texture à l’aide de la valeur alpha du pixel de destination.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Cartes de lumière monochromes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516337"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="23b9c-103">Cartes de lumière monochromes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23b9c-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="23b9c-104">Certaines cartes accélérateur 3D plus anciennes ne prennent pas en charge la fusion de texture à l’aide de la valeur alpha du pixel de destination.</span><span class="sxs-lookup"><span data-stu-id="23b9c-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="23b9c-105">Pour plus d’informations, consultez [fusion de texture alpha (Direct3D 9)](alpha-texture-blending.md) .</span><span class="sxs-lookup"><span data-stu-id="23b9c-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="23b9c-106">En général, ces adaptateurs ne prennent pas en charge la fusion de texture multiple.</span><span class="sxs-lookup"><span data-stu-id="23b9c-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="23b9c-107">Si votre application s’exécute sur un adaptateur tel que celui-ci, elle peut utiliser la fusion de texture multipasse pour effectuer un mappage de lumière monochrome.</span><span class="sxs-lookup"><span data-stu-id="23b9c-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="23b9c-108">Pour effectuer un mappage de lumière monochrome, une application stocke les informations d’éclairage dans les données alpha de ses textures de carte de lumière.</span><span class="sxs-lookup"><span data-stu-id="23b9c-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="23b9c-109">L’application utilise les fonctionnalités de filtrage de texture de Direct3D pour effectuer un mappage de chaque pixel de l’image de la primitive à un Texel correspondant dans la carte de lumière.</span><span class="sxs-lookup"><span data-stu-id="23b9c-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="23b9c-110">Elle définit le facteur de fusion source sur la valeur alpha du Texel correspondant.</span><span class="sxs-lookup"><span data-stu-id="23b9c-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="23b9c-111">L’exemple suivant montre comment une application peut utiliser une texture comme une carte d’éclairage monochrome :</span><span class="sxs-lookup"><span data-stu-id="23b9c-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



<span data-ttu-id="23b9c-112">Étant donné que les adaptateurs d’affichage qui ne prennent pas en charge la fusion alpha de destination ne prennent généralement pas en charge la fusion de texture multiple, cet exemple définit la carte de lumière comme première texture, qui est disponible sur toutes les cartes d’accélération 3D.</span><span class="sxs-lookup"><span data-stu-id="23b9c-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="23b9c-113">L’exemple de code définit l’opération de couleur pour la phase de fusion de la texture afin de fusionner les données de texture avec la couleur existante de la primitive.</span><span class="sxs-lookup"><span data-stu-id="23b9c-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="23b9c-114">Il sélectionne ensuite la première texture et la couleur existante de la primitive comme données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="23b9c-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23b9c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23b9c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b9c-116">Placage de lumière avec des textures</span><span class="sxs-lookup"><span data-stu-id="23b9c-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



