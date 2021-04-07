---
title: Source de l’image Thumb
description: Source de l’image Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les apparences, source d’image
- trackbars dans les habillages, source d’image Thumb
- source de l’image pour les apparences, trackbars
- Thumb, source de l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028872"
---
# <a name="thumb-image-source"></a><span data-ttu-id="7a2d5-110">Source de l’image Thumb</span><span class="sxs-lookup"><span data-stu-id="7a2d5-110">Thumb Image Source</span></span>

<span data-ttu-id="7a2d5-111">Vous devez définir le nom du fichier qui contient l’image Thumb.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="7a2d5-112">Il doit s’agir d’un nom de fichier valide avec l’extension. bmp,. gif,. jpg ou. png.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="7a2d5-113">Le fichier doit contenir trois images côte à côte de taille identique.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="7a2d5-114">Ils doivent être adjacents les uns aux autres sans espace.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="7a2d5-115">La position supérieure gauche de l’image de gauche doit être située dans l’angle supérieur gauche du fichier.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="7a2d5-116">L’image sur le côté gauche est l’image normale de l’image Thumb, tandis que l’image du milieu représente l’état de l’envoi et l’image à droite illustre l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="7a2d5-117">Vous pouvez faire en sorte que certaines zones de l’image Thumb soient transparentes.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="7a2d5-118">Cela vous permettra de créer des images Thumb dans des formes autres que rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="7a2d5-119">Toute région de l’image Thumb que vous remplissez avec la couleur spécifiée par la valeur RVB 255, 0, 255 apparaîtra transparente dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="7a2d5-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2d5-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a2d5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2d5-121">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="7a2d5-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




