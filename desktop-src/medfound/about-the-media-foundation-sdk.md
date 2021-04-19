---
description: Microsoft Media Foundation est la plateforme multimédia nouvelle génération pour Windows qui permet aux développeurs, aux consommateurs et aux fournisseurs de contenu d’adopter la nouvelle vague de contenus Premium avec une robustesse améliorée, une qualité inégalée et une interopérabilité transparente.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: À propos de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539377"
---
# <a name="about-media-foundation"></a><span data-ttu-id="f1d0d-103">À propos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1d0d-103">About Media Foundation</span></span>

<span data-ttu-id="f1d0d-104">Microsoft Media Foundation est la plateforme multimédia nouvelle génération pour Windows qui permet aux développeurs, aux consommateurs et aux fournisseurs de contenu d’adopter la nouvelle vague de contenus Premium avec une robustesse améliorée, une qualité inégalée et une interopérabilité transparente.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="f1d0d-105">Media Foundation nécessite Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="f1d0d-106">Elle utilise le modèle COM (Component Object Model) et requiert C/C++.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="f1d0d-107">Microsoft ne fournit pas d’API gérée pour Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="f1d0d-108">Les API Media Foundation font partie du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1d0d-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1d0d-109">Pour développer une application Media Foundation, installez la version la plus récente du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="f1d0d-110">Qualité audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="f1d0d-110">Audio and Video Quality</span></span>

<span data-ttu-id="f1d0d-111">Media Foundation a été conçu pour répondre aux défis posés par le contenu haute définition.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="f1d0d-112">Les améliorations apportées à la qualité audio et vidéo dans l’ensemble de la plate-forme vous permettent désormais de bénéficier d’une expérience remarquable pour le contenu haute définition de la prochaine génération.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="f1d0d-113">DirectX Video Acceleration (DXVA) 2,0 offre une accélération vidéo plus efficace, par rapport à DXVA 1,0, avec un décodage vidéo plus robuste et rationalisé et une utilisation étendue du matériel dans le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="f1d0d-114">Avec DXVA 2,0, Windows peut gérer certains des contenus haute définition les plus exigeants, avec une haute qualité et une meilleure résilience des problèmes.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="f1d0d-115">Les informations sur l’espace colorimétrique sont conservées dans l’ensemble du pipeline vidéo.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="f1d0d-116">Les utilisateurs peuvent profiter d’un contenu vidéo avec une fidélité complète.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="f1d0d-117">Les informations de couleur et les images entrelacées sont désormais transmises au matériel pour les compositions à passage unique.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="f1d0d-118">La préservation des informations sur l’espace colorimétrique réduit également les conversions d’espace colorimétrique inutiles, ce qui libère davantage de cycles pour traiter le contenu HD exigeant.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="f1d0d-119">Le convertisseur vidéo amélioré (EVR) offre une meilleure prise en charge de la synchronisation, un traitement vidéo amélioré et une meilleure résilience des problèmes.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="f1d0d-120">La prise en charge de la lecture plein écran a été améliorée et la suppression de vidéo en mode fenêtre a été réduite.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="f1d0d-121">Media Foundation utilise le service Planificateur de classes multimédias (MMCSS), un nouveau service système dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="f1d0d-122">MMCSS permet aux applications multimédias de s’assurer que leur traitement qui respecte le temps reçoit un accès prioritaire aux ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="f1d0d-123">Accès au contenu</span><span class="sxs-lookup"><span data-stu-id="f1d0d-123">Content Access</span></span>

<span data-ttu-id="f1d0d-124">Étant donné que le divertissement numérique passe dans l’ère haute définition et que le contenu devient plus portable et omniprésent, la protection du contenu devient partie intégrante des produits multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="f1d0d-125">L’extensibilité de Media Foundation s’assure qu’elle peut prendre en charge ces tendances.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="f1d0d-126">En outre, Media Foundation extensibilité permet à différents systèmes de protection de contenu de fonctionner ensemble.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="f1d0d-127">À propos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1d0d-127">About Media Foundation</span></span>

<span data-ttu-id="f1d0d-128">Cette section contient des informations générales sur les API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="f1d0d-129">Vous trouverez des informations de programmation détaillées dans le [Guide de programmation Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="f1d0d-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="f1d0d-130">Section</span><span class="sxs-lookup"><span data-stu-id="f1d0d-130">Section</span></span>                                                                              | <span data-ttu-id="f1d0d-131">Description</span><span class="sxs-lookup"><span data-stu-id="f1d0d-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="f1d0d-132">Nouveautés de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1d0d-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="f1d0d-133">Décrit les nouvelles fonctionnalités de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="f1d0d-134">Media Foundation en-têtes et bibliothèques</span><span class="sxs-lookup"><span data-stu-id="f1d0d-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="f1d0d-135">Répertorie les fichiers d’en-tête et de bibliothèque qui définissent les API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="f1d0d-136">Outils de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1d0d-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="f1d0d-137">Décrit les outils de développement disponibles pour Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="f1d0d-138">Media Foundation n’est pas inclus dans les éditions N et KN de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1d0d-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="f1d0d-139">Pour plus d’informations, consultez [Microsoft Windows Media Feature Pack pour N et kN versions de toutes les éditions de Windows 8](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="f1d0d-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d0d-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1d0d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d0d-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1d0d-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



