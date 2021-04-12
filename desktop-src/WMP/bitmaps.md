---
title: Bitmaps (kit de développement logiciel Windows Media Player)
description: Images bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Apparences mobiles du lecteur Windows Media, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464006"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="7a849-107">Bitmaps (kit de développement logiciel Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="7a849-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="7a849-108">Vous devez utiliser une ou plusieurs images dans votre apparence, et chaque image doit être définie dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="7a849-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="7a849-109">Si vous ne définissez pas d’image dans cette section, votre apparence ne sera pas en mesure de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="7a849-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="7a849-110">Le terme « bitmap » est utilisé tout au long de la référence, et fait référence aux images bitmap avec une extension. bmp, aux images GIF avec une extension. gif, aux images JPEG avec une extension. jpg et aux images PNG avec une extension. png.</span><span class="sxs-lookup"><span data-stu-id="7a849-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="7a849-111">La section bitmaps du fichier de définition d’apparence commence par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="7a849-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="7a849-112">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des images de votre apparence.</span><span class="sxs-lookup"><span data-stu-id="7a849-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="7a849-113">Une ligne classique peut être :</span><span class="sxs-lookup"><span data-stu-id="7a849-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="7a849-114">Vous pouvez utiliser le modèle suivant pour la section bitmaps de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="7a849-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="7a849-115">Vous devez utiliser l’ordre suivant pour les informations de bitmap pour chaque ligne dans la section bitmap.</span><span class="sxs-lookup"><span data-stu-id="7a849-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="7a849-116">Chaque partie de la ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="7a849-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="7a849-117">Type de bitmap</span><span class="sxs-lookup"><span data-stu-id="7a849-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="7a849-118">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="7a849-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="7a849-119">Coordinates</span><span class="sxs-lookup"><span data-stu-id="7a849-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="7a849-120">Pour obtenir un exemple de code bitmap, consultez la [section exemple de bitmap](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="7a849-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a849-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a849-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a849-122">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="7a849-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




