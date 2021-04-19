---
description: Top-Down et
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down et Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517903"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="7ab11-103">Top-Down et Bottom-Up DIB</span><span class="sxs-lookup"><span data-stu-id="7ab11-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="7ab11-104">Si vous ne connaissez pas la programmation graphique, vous pouvez vous attendre à ce qu’une bitmap soit organisée en mémoire afin que la ligne supérieure de l’image apparaisse au début de la mémoire tampon, suivie de la ligne suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7ab11-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="7ab11-105">Toutefois, cela n’est pas nécessairement le cas.</span><span class="sxs-lookup"><span data-stu-id="7ab11-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="7ab11-106">Dans Windows, les images bitmap indépendantes du périphérique (DIB) peuvent être placées en mémoire dans deux orientations différentes, de bas en haut et de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="7ab11-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="7ab11-107">Dans un DIB de bas en haut, la mémoire tampon d’image commence par la ligne inférieure des pixels, suivie de la ligne suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7ab11-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="7ab11-108">La ligne supérieure de l’image est la dernière ligne de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ab11-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="7ab11-109">Par conséquent, le premier octet en mémoire est le pixel inférieur gauche de l’image.</span><span class="sxs-lookup"><span data-stu-id="7ab11-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="7ab11-110">Dans GDI, tous les DIB sont ascendants.</span><span class="sxs-lookup"><span data-stu-id="7ab11-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="7ab11-111">Le diagramme suivant montre la disposition physique d’un DIB ascendant.</span><span class="sxs-lookup"><span data-stu-id="7ab11-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![DIB ascendant](images/pixel-layout-bottomup.png)

<span data-ttu-id="7ab11-113">Dans un DIB descendant, l’ordre des lignes est inversé.</span><span class="sxs-lookup"><span data-stu-id="7ab11-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="7ab11-114">La ligne supérieure de l’image est la première ligne en mémoire, suivie de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="7ab11-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="7ab11-115">La ligne inférieure de l’image est la dernière ligne de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ab11-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="7ab11-116">Avec un DIB descendant, le premier octet en mémoire est le pixel supérieur gauche de l’image.</span><span class="sxs-lookup"><span data-stu-id="7ab11-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="7ab11-117">DirectDraw utilise des DIB descendants.</span><span class="sxs-lookup"><span data-stu-id="7ab11-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="7ab11-118">Le diagramme suivant montre la disposition physique d’un DIB descendant :</span><span class="sxs-lookup"><span data-stu-id="7ab11-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![DIB descendant](images/pixel-layout-topdown.png)

<span data-ttu-id="7ab11-120">Pour les DIB RGB, l’orientation de l’image est indiquée par le membre **biheight** de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="7ab11-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="7ab11-121">Si la **bihauteur** est positive, l’image est en bas.</span><span class="sxs-lookup"><span data-stu-id="7ab11-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="7ab11-122">Si la **bihauteur** est négative, l’image est de haut en haut.</span><span class="sxs-lookup"><span data-stu-id="7ab11-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="7ab11-123">Les DIB dans les formats YUV sont toujours de haut en haut et le signe du membre **biheight** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7ab11-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="7ab11-124">Les décodeurs doivent offrir des formats YUV avec une **bihauteur** positive, mais ils doivent également accepter les formats YUV avec une **bihauteur** négative et ignorer le signe.</span><span class="sxs-lookup"><span data-stu-id="7ab11-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="7ab11-125">En outre, tout type DIB qui utilise un **FourCC** dans le membre de **bicompression** doit exprimer sa **bihauteur** sous la forme d’un nombre positif, quelle que soit son orientation, puisque le **FourCC** lui-même identifie un schéma de compression dont l’orientation d’image doit être comprise par n’importe quel filtre compatible.</span><span class="sxs-lookup"><span data-stu-id="7ab11-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ab11-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ab11-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ab11-127">Utilisation des images vidéo</span><span class="sxs-lookup"><span data-stu-id="7ab11-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



