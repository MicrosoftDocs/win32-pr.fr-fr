---
title: Source de l’image pour le TrackBar désactivé
description: Source de l’image pour le TrackBar désactivé
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les apparences, source d’image
- source de l’image pour les apparences, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517955"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="715a4-108">Source de l’image pour le TrackBar désactivé</span><span class="sxs-lookup"><span data-stu-id="715a4-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="715a4-109">Vous devez définir la source de l’image que vous souhaitez afficher lorsqu’un TrackBar est désactivé, à l’aide du type de bitmap à partir duquel vous souhaitez dessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="715a4-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="715a4-110">L’image que vous affichez se trouve généralement dans le fichier super ou si vous créez une apparence pour Windows Media Player 10 mobile, l’image se trouve dans le fichier SeekThumb.</span><span class="sxs-lookup"><span data-stu-id="715a4-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="715a4-111">Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="715a4-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="715a4-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.</span><span class="sxs-lookup"><span data-stu-id="715a4-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="715a4-113">Par exemple, pour utiliser une image de la bitmap SeekThumb qui a une position supérieure et gauche de 50, 60 pixels, tapez :</span><span class="sxs-lookup"><span data-stu-id="715a4-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="715a4-114">Vous devez définir un emplacement d’image pour une image TrackBar désactivée.</span><span class="sxs-lookup"><span data-stu-id="715a4-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="715a4-115">Si vous ne souhaitez pas afficher une nouvelle image, vous pouvez définir l’image d’arrière-plan en tant qu’image désactivée avec un décalage de 0, 0 :</span><span class="sxs-lookup"><span data-stu-id="715a4-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="715a4-116">Dans l’exemple précédent, 50, 60 représente l’emplacement du bouton que vous utilisez dans le fichier SeekThumb (dans ce cas, le même emplacement que le bouton sur la bitmap d’arrière-plan).</span><span class="sxs-lookup"><span data-stu-id="715a4-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="715a4-117">Toutefois, il est fortement recommandé d’afficher une image désactivée pour tous les trackbars afin de permettre à votre utilisateur d’indiquer visuellement, car trackbars ne sera pas utilisable dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="715a4-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="715a4-118">Par exemple, la recherche trackbars peut être désactivée lorsque la sélection actuelle est vide.</span><span class="sxs-lookup"><span data-stu-id="715a4-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="715a4-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="715a4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="715a4-120">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="715a4-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




