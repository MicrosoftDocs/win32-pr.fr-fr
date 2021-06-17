---
description: En savoir plus sur la fusion alpha. La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusion alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262001"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="58323-104">Fusion alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="58323-105">La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents.</span><span class="sxs-lookup"><span data-stu-id="58323-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="58323-106">Outre un canal de couleur rouge, vert et bleu, chaque pixel d’une bitmap Alpha possède un composant de transparence appelé « canal alpha ».</span><span class="sxs-lookup"><span data-stu-id="58323-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="58323-107">Le canal alpha contient généralement autant de bits qu’un canal de couleurs.</span><span class="sxs-lookup"><span data-stu-id="58323-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="58323-108">Par exemple, un canal alpha 8 bits peut représenter 256 niveaux de transparence, à partir de 0 (le pixel entier est transparent) à 255 (le pixel entier est opaque).</span><span class="sxs-lookup"><span data-stu-id="58323-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="58323-109">La liste ci-dessous présente certains effets spéciaux que vous pouvez créer à l’aide de la fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="58323-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="58323-110">La couleur peut être définie avec ou sans valeurs alpha.</span><span class="sxs-lookup"><span data-stu-id="58323-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="58323-111">La couleur sans alpha est la couleur RVB avec alpha est stockée en tant que ARGB.</span><span class="sxs-lookup"><span data-stu-id="58323-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="58323-112">Les données de vertex, les données de matériau et les données de texture peuvent être utilisées pour fournir la transparence de l’objet.</span><span class="sxs-lookup"><span data-stu-id="58323-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="58323-113">La mémoire tampon de trame peut également être utilisée pour générer des effets de transparence.</span><span class="sxs-lookup"><span data-stu-id="58323-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="58323-114">Vertex alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="58323-115">Matériau alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="58323-116">Texture alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="58323-117">Mémoire tampon de trame alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="58323-118">Rendu de la cible Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="58323-119">Les exemples qui illustrent alpha sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="58323-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="58323-120">Billboarding (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="58323-121">Clouds, fumées et traces de vapeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="58323-122">Incendie, halos et explosions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58323-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="58323-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58323-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58323-124">Rendu Direct3D</span><span class="sxs-lookup"><span data-stu-id="58323-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



