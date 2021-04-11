---
description: La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusion alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111123"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="c586a-103">Fusion alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="c586a-104">La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents.</span><span class="sxs-lookup"><span data-stu-id="c586a-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="c586a-105">Outre un canal de couleur rouge, vert et bleu, chaque pixel d’une bitmap Alpha possède un composant de transparence appelé « canal alpha ».</span><span class="sxs-lookup"><span data-stu-id="c586a-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="c586a-106">Le canal alpha contient généralement autant de bits qu’un canal de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c586a-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="c586a-107">Par exemple, un canal alpha 8 bits peut représenter 256 niveaux de transparence, à partir de 0 (le pixel entier est transparent) à 255 (le pixel entier est opaque).</span><span class="sxs-lookup"><span data-stu-id="c586a-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="c586a-108">La liste ci-dessous présente certains effets spéciaux que vous pouvez créer à l’aide de la fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="c586a-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="c586a-109">La couleur peut être définie avec ou sans valeurs alpha.</span><span class="sxs-lookup"><span data-stu-id="c586a-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="c586a-110">La couleur sans alpha est la couleur RVB avec alpha est stockée en tant que ARGB.</span><span class="sxs-lookup"><span data-stu-id="c586a-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="c586a-111">Les données de vertex, les données de matériau et les données de texture peuvent être utilisées pour fournir la transparence de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c586a-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="c586a-112">La mémoire tampon de trame peut également être utilisée pour générer des effets de transparence.</span><span class="sxs-lookup"><span data-stu-id="c586a-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="c586a-113">Vertex alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="c586a-114">Matériau alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="c586a-115">Texture alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="c586a-116">Mémoire tampon de trame alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="c586a-117">Rendu de la cible Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="c586a-118">Les exemples qui illustrent alpha sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c586a-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="c586a-119">Billboarding (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="c586a-120">Clouds, fumées et traces de vapeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="c586a-121">Incendie, halos et explosions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c586a-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="c586a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c586a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c586a-123">Rendu Direct3D</span><span class="sxs-lookup"><span data-stu-id="c586a-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



