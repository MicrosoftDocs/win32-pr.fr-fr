---
description: Les paramètres de brouillard sont contrôlés par le biais d’États de rendu d’appareil.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Paramètres de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846173"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="ac2dc-103">Paramètres de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ac2dc-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="ac2dc-104">Les paramètres de brouillard sont contrôlés par le biais d’États de rendu d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="ac2dc-105">Les types de brouillard de pixel et de vertex prennent en charge toutes les formules de brouillard introduites dans des [formules de brouillard (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="ac2dc-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="ac2dc-106">Le type énuméré [**D3DFOGMODE**](./d3dfogmode.md) définit des constantes que vous pouvez utiliser pour identifier la formule de brouillard que vous souhaitez que Microsoft Direct3D utilise.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="ac2dc-107">L' \_ État de rendu D3DRS FOGTABLEMODE contrôle le mode de brouillard utilisé par Direct3D pour le brouillard de pixel, tandis que l' \_ État de rendu D3DRS FOGVERTEXMODE contrôle le mode du brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="ac2dc-108">Lorsque vous utilisez la formule de brouillard linéaire, vous définissez les distances de début et de fin via les \_ États de rendu D3DRS FOGSTART et D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="ac2dc-109">La façon dont le système interprète ces valeurs dépend du type de brouillard utilisé par votre application : pixel ou brouillard de vertex, et, lors de l’utilisation du brouillard de pixel, si une profondeur z ou w est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="ac2dc-110">Le tableau suivant résume les types de brouillard et leurs unités de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="ac2dc-111">Type de brouillard</span><span class="sxs-lookup"><span data-stu-id="ac2dc-111">Fog type</span></span>  | <span data-ttu-id="ac2dc-112">Unités de début/fin du brouillard</span><span class="sxs-lookup"><span data-stu-id="ac2dc-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="ac2dc-113">Pixel (Z)</span><span class="sxs-lookup"><span data-stu-id="ac2dc-113">Pixel (Z)</span></span> | <span data-ttu-id="ac2dc-114">Espace \[ de périphérique 0.0, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="ac2dc-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="ac2dc-115">Pixel (W)</span><span class="sxs-lookup"><span data-stu-id="ac2dc-115">Pixel (W)</span></span> | <span data-ttu-id="ac2dc-116">Espace de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="ac2dc-116">Camera space</span></span>             |
| <span data-ttu-id="ac2dc-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="ac2dc-117">Vertex</span></span>    | <span data-ttu-id="ac2dc-118">Espace de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="ac2dc-118">Camera space</span></span>             |



 

<span data-ttu-id="ac2dc-119">L' \_ État de rendu D3DRS FOGDENSITY contrôle la densité de brouillard appliquée quand une formule de brouillard exponentiel est activée.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="ac2dc-120">La densité de brouillard est essentiellement un facteur de pondération, allant de 0,0 à 1,0 (inclus), qui met à l’échelle la valeur de distance dans l’exposant.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="ac2dc-121">La couleur utilisée par le système pour la fusion de brouillard est contrôlée par le biais de l’état de rendu de l' \_ appareil D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="ac2dc-122">Pour plus d’informations, consultez [couleur de brouillard (Direct3D 9)](fog-color.md) et [mélange de brouillards (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="ac2dc-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac2dc-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac2dc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2dc-124">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="ac2dc-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
