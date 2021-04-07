---
description: La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) est une API pour le traitement vidéo accéléré par le matériel.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749253"
---
# <a name="dxva-hd"></a><span data-ttu-id="3a863-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="3a863-103">DXVA-HD</span></span>

<span data-ttu-id="3a863-104">La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) est une API pour le traitement vidéo accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="3a863-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="3a863-105">DXVA-HD utilise le GPU pour exécuter des fonctions telles que l’entrelacement, la composition et la conversion de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="3a863-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="3a863-106">DXVA-HD est similaire au [traitement vidéo DXVA](dxva-video-processing.md) (DXVA-VP), mais offre des fonctionnalités améliorées et un modèle de traitement plus simple.</span><span class="sxs-lookup"><span data-stu-id="3a863-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="3a863-107">En fournissant un modèle de composition plus flexible, DXVA-HD est conçu pour prendre en charge la prochaine génération de formats optiques HD et de normes de diffusion.</span><span class="sxs-lookup"><span data-stu-id="3a863-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="3a863-108">L’API DXVA-HD requiert un pilote d’affichage WDDM qui prend en charge l’interface DDI (Device Driver Interface) DXVA-HD ou un processeur logiciel de plug-in.</span><span class="sxs-lookup"><span data-stu-id="3a863-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="3a863-109">Améliorations apportées à DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="3a863-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="3a863-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a863-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="3a863-111">Améliorations apportées à DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="3a863-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="3a863-112">DXVA-HD étend l’ensemble des fonctionnalités fournies par DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="3a863-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="3a863-113">Les améliorations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a863-113">Enhancements include:</span></span>

-   <span data-ttu-id="3a863-114">Mixage RGB et YUV.</span><span class="sxs-lookup"><span data-stu-id="3a863-114">RGB and YUV mixing.</span></span> <span data-ttu-id="3a863-115">Tout flux peut avoir la valeur RVB ou YUV.</span><span class="sxs-lookup"><span data-stu-id="3a863-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="3a863-116">Il n’existe plus de distinction entre le flux principal et les sous-flux.</span><span class="sxs-lookup"><span data-stu-id="3a863-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="3a863-117">Désentrelacement de plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="3a863-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="3a863-118">Tout flux peut être progressif ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="3a863-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="3a863-119">En outre, la cadence et la fréquence d’images peuvent varier d’un flux d’entrée à l’autre.</span><span class="sxs-lookup"><span data-stu-id="3a863-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="3a863-120">Couleurs d’arrière-plan RVB.</span><span class="sxs-lookup"><span data-stu-id="3a863-120">RGB background colors.</span></span> <span data-ttu-id="3a863-121">Auparavant, seules les couleurs d’arrière-plan YUV étaient prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3a863-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="3a863-122">Incrustation de luminance.</span><span class="sxs-lookup"><span data-stu-id="3a863-122">Luma keying.</span></span> <span data-ttu-id="3a863-123">Lorsque la incrustation de luminance est activée, les valeurs de luminance qui se trouvent dans une plage désignée deviennent transparentes.</span><span class="sxs-lookup"><span data-stu-id="3a863-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="3a863-124">Basculement dynamique entre les modes de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="3a863-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="3a863-125">DXVA-HD définit également certaines fonctionnalités avancées que les pilotes peuvent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="3a863-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="3a863-126">Toutefois, les applications ne doivent pas supposer que tous les pilotes prendront en charge ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3a863-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="3a863-127">Les fonctionnalités avancées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a863-127">The advanced features include:</span></span>

-   <span data-ttu-id="3a863-128">Inverse telecine (par exemple, 60i à 24p).</span><span class="sxs-lookup"><span data-stu-id="3a863-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="3a863-129">Conversion de la fréquence des images (par exemple, 24p à 120P).</span><span class="sxs-lookup"><span data-stu-id="3a863-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="3a863-130">Modes de remplissage alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="3a863-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="3a863-131">Réduction du bruit et filtrage d’amélioration des bords.</span><span class="sxs-lookup"><span data-stu-id="3a863-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="3a863-132">Mise à l’échelle non linéaire anamorphique.</span><span class="sxs-lookup"><span data-stu-id="3a863-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="3a863-133">YCbCr étendu (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="3a863-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="3a863-134">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a863-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="3a863-135">Création d’un processeur vidéo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="3a863-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="3a863-136">Vérification des formats DXVA-HD pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a863-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="3a863-137">Création de surfaces vidéo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="3a863-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="3a863-138">Définition des États DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="3a863-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="3a863-139">Exécution du blit DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="3a863-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="3a863-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a863-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a863-141">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="3a863-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="3a863-142">DXVA-HD, exemple</span><span class="sxs-lookup"><span data-stu-id="3a863-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



