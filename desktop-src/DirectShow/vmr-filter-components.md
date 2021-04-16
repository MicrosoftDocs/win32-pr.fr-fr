---
description: Composants de filtre VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Composants de filtre VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529511"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="84f1c-103">Composants de filtre VMR</span><span class="sxs-lookup"><span data-stu-id="84f1c-103">VMR Filter Components</span></span>

<span data-ttu-id="84f1c-104">VMR utilise une conception modulaire qui permet aux applications de les configurer pour de nombreux scénarios de rendu différents.</span><span class="sxs-lookup"><span data-stu-id="84f1c-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="84f1c-105">En fonction de sa configuration, VMR contient de deux à cinq sous-composants (en plus de ses broches d’entrée).</span><span class="sxs-lookup"><span data-stu-id="84f1c-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR en mode fenêtre avec plusieurs flux](images/vmr-multiple-streams.png)

<span data-ttu-id="84f1c-107">**Mélangeur :** Le mélangeur est un objet COM chargé de mélanger plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="84f1c-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="84f1c-108">La désentrelacement se produit également dans le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="84f1c-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="84f1c-109">Le mélangeur est chargé par le VMR lorsque plusieurs flux d’entrée sont détectés, ou lorsque la vidéo d’entrée est entrelacée.</span><span class="sxs-lookup"><span data-stu-id="84f1c-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="84f1c-110">Le mélangeur collecte des informations sur chaque flux d’entrée et trie les flux dans l’ordre de plan correct.</span><span class="sxs-lookup"><span data-stu-id="84f1c-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="84f1c-111">Il est chargé de déterminer à quel moment chaque broche d’entrée reçoit un échantillon et de demander au compositeur d’image de s’exécuter au bon moment pour effectuer la fusion réelle.</span><span class="sxs-lookup"><span data-stu-id="84f1c-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="84f1c-112">Le mélangeur calcule également l’horodatage à appliquer à chaque image de sortie.</span><span class="sxs-lookup"><span data-stu-id="84f1c-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="84f1c-113">Lorsque l’application fournit une image bitmap à afficher en haut de l’image composite, le mélangeur est chargé de s’assurer que la bitmap est affichée en haut, même si l’ordre de plan des flux d’entrée est modifié.</span><span class="sxs-lookup"><span data-stu-id="84f1c-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="84f1c-114">**Compositeur d’image :** Le compositeur d’image est un objet COM qui effectue la fusion réelle des flux d’entrée sur une surface DirectDraw ou Direct3D unique fournie par l’Allocator-presenter.</span><span class="sxs-lookup"><span data-stu-id="84f1c-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="84f1c-115">VMR fournit un compositeur d’image par défaut qui permet aux applications d’effectuer des effets de fusion alpha 2D.</span><span class="sxs-lookup"><span data-stu-id="84f1c-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="84f1c-116">Les applications peuvent fournir un compositeur d’image personnalisé pour permettre d’autres effets 2D et 3D, tels que l’application de textures à des portions de l’image, la fusion alpha par pixel, le mappage de l’image à des objets 3D stationnaires ou mobiles, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="84f1c-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="84f1c-117">**Allocator-présentateur :** L’Allocator-Presenter est un objet COM qui alloue l’objet DirectDraw ou Direct3D et gère la communication avec la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="84f1c-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="84f1c-118">Le dessin peut être exécuté comme un flip ou un blit.</span><span class="sxs-lookup"><span data-stu-id="84f1c-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="84f1c-119">Vous pouvez brancher votre propre allocateur-présentateur pour créer et contrôler l’objet DirectDraw ou Direct3D, et/ou pour obtenir l’accès aux bits vidéo au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="84f1c-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="84f1c-120">**Gestionnaire de fenêtres :** Le gestionnaire de fenêtres est utilisé uniquement en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84f1c-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="84f1c-121">Le gestionnaire de fenêtres prend en charge les interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) héritées pour assurer la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="84f1c-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84f1c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84f1c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f1c-123">À propos du rendu de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="84f1c-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



