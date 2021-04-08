---
description: Cette section contient des informations sur l’organisation interne des formats de texture compressés.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formats de texture compressés (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748797"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="2d358-103">Formats de texture compressés (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d358-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="2d358-104">Cette section contient des informations sur l’organisation interne des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="2d358-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="2d358-105">Vous n’avez pas besoin de ces détails pour utiliser des textures compressées, car vous pouvez utiliser des fonctions D3DX pour la conversion vers et depuis des formats compressés.</span><span class="sxs-lookup"><span data-stu-id="2d358-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="2d358-106">Toutefois, ces informations sont utiles si vous souhaitez utiliser les données de surface compressées directement.</span><span class="sxs-lookup"><span data-stu-id="2d358-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="2d358-107">Direct3D utilise un format de compression qui divise les cartes de texture en blocs Texel 4x4.</span><span class="sxs-lookup"><span data-stu-id="2d358-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="2d358-108">Si la texture ne contient pas de transparence-est opaque-ou si la transparence est spécifiée par une alpha de 1 bit, un bloc de 8 octets représente le bloc de la carte de texture.</span><span class="sxs-lookup"><span data-stu-id="2d358-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="2d358-109">Si la carte de texture contient des texels transparents, à l’aide d’un canal alpha, un bloc de 16 octets le représente.</span><span class="sxs-lookup"><span data-stu-id="2d358-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="2d358-110">Textures opaques et alpha 1 bits (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d358-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="2d358-111">Textures avec canaux alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d358-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="2d358-112">Toute texture unique doit spécifier que ses données sont stockées sous la forme de 64 ou 128 bits par groupe de 16 texels.</span><span class="sxs-lookup"><span data-stu-id="2d358-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="2d358-113">Si les blocs 64 bits, c’est-à-dire le format DXT1, sont utilisés pour la texture, il est possible de mélanger les formats alpha opaque et 1 bits sur la base de chaque bloc au sein de la même texture.</span><span class="sxs-lookup"><span data-stu-id="2d358-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="2d358-114">En d’autres termes, la comparaison de l’amplitude de l’entier non signé de la couleur \_ 0 et de la couleur \_ 1 est effectuée de manière unique pour chaque bloc de 16 texels.</span><span class="sxs-lookup"><span data-stu-id="2d358-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="2d358-115">Quand des blocs 128 bits sont utilisés, le canal alpha doit être spécifié dans explicite (format DXT2 ou DXT3) ou en mode interpolé (format DXT4 ou DXT5) pour la texture entière.</span><span class="sxs-lookup"><span data-stu-id="2d358-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="2d358-116">Comme pour la couleur, lorsque le mode interpolé est sélectionné, huit alpha interpolés ou six modes alphabétiques interpolés peuvent être utilisés bloc par bloc.</span><span class="sxs-lookup"><span data-stu-id="2d358-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="2d358-117">Là encore, la comparaison de magnitude des alpha \_ 0 et alpha \_ 1 est effectuée de manière unique sur une base bloc par bloc.</span><span class="sxs-lookup"><span data-stu-id="2d358-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="2d358-118">Le pas pour les formats DXTn est différent de ce qui a été retourné dans DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="2d358-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="2d358-119">Le tangage est maintenant mesuré en octets (et non pas en blocs).</span><span class="sxs-lookup"><span data-stu-id="2d358-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="2d358-120">Par exemple, si vous avez une largeur de 16, vous obtiendrez un pas de quatre blocs (4 \* 8 pour DXT1, 4 \* pour DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="2d358-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d358-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d358-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d358-122">Ressources de texture compressées</span><span class="sxs-lookup"><span data-stu-id="2d358-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



