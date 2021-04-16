---
description: Le lecteur source est une alternative à l’utilisation de la session de média et du pipeline Microsoft Media Foundation pour traiter les données multimédias.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lecteur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527831"
---
# <a name="source-reader"></a><span data-ttu-id="a7079-103">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="a7079-103">Source Reader</span></span>

<span data-ttu-id="a7079-104">Le lecteur source est une alternative à l’utilisation de la [session de média](media-session.md) et du pipeline Microsoft Media Foundation pour traiter les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="a7079-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="a7079-105">Pourquoi utiliser le lecteur source ?</span><span class="sxs-lookup"><span data-stu-id="a7079-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="a7079-106">Media Foundation fournit un pipeline optimisé pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="a7079-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="a7079-107">Le pipeline est de bout en bout, ce qui signifie qu’il gère le workflow de la source (par exemple, un fichier vidéo) jusqu’à la destination (telle que l’affichage graphique).</span><span class="sxs-lookup"><span data-stu-id="a7079-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="a7079-108">Toutefois, si vous souhaitez lire ou modifier les données au fur et à mesure de leur passage dans le pipeline, vous devez écrire un plug-in personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a7079-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="a7079-109">Cela nécessite une connaissance assez profonde du pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a7079-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="a7079-110">Pour certaines tâches, la création d’un nouveau plug-in est trop importante.</span><span class="sxs-lookup"><span data-stu-id="a7079-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="a7079-111">Le lecteur source est conçu pour ce type de situation, lorsque vous souhaitez obtenir les données brutes d’une source sans la surcharge de l’ensemble du pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7079-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="a7079-112">En interne, le lecteur source contient un pointeur vers une source de média.</span><span class="sxs-lookup"><span data-stu-id="a7079-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="a7079-113">Une *source de média* est un objet Media Foundation qui génère des données multimédias à partir d’une source externe, telle qu’un fichier multimédia ou un périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="a7079-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="a7079-114">Le lecteur source gère tous les appels de méthode à la source du média.</span><span class="sxs-lookup"><span data-stu-id="a7079-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="a7079-115">(Pour plus d’informations sur les sources multimédias, consultez [sources multimédias](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="a7079-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="a7079-116">Si la source du média fournit des données compressées, vous pouvez utiliser le lecteur source pour décoder les données.</span><span class="sxs-lookup"><span data-stu-id="a7079-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="a7079-117">Dans ce cas, le lecteur source chargera le décodeur approprié et gérera le workflow entre la source du média et le décodeur.</span><span class="sxs-lookup"><span data-stu-id="a7079-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="a7079-118">Le lecteur source peut également effectuer un traitement vidéo limité : conversion des couleurs YUV en RVB-32 et désentrelacement de logiciels, bien que ces opérations ne soient pas recommandées pour le rendu vidéo en temps réel.</span><span class="sxs-lookup"><span data-stu-id="a7079-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="a7079-119">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="a7079-119">The following image illustrates this process.</span></span>

![diagramme du lecteur source](images/sourcereader.png)

<span data-ttu-id="a7079-121">Le lecteur source n’envoie pas les données à une destination ; C’est à l’application d’utiliser les données.</span><span class="sxs-lookup"><span data-stu-id="a7079-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="a7079-122">Par exemple, le lecteur source peut lire un fichier vidéo, mais il n’affiche pas la vidéo à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a7079-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="a7079-123">En outre, le lecteur source ne gère pas une horloge de présentation, ne gère pas les problèmes de minutage ou ne synchronise pas les vidéos avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="a7079-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="a7079-124">Envisagez d’utiliser le lecteur source dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="a7079-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="a7079-125">Vous souhaitez obtenir des données à partir d’un fichier multimédia sans vous soucier de la structure de fichiers sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="a7079-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="a7079-126">Vous souhaitez obtenir des données à partir d’un périphérique de capture audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="a7079-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="a7079-127">Vos tâches de traitement de données ne sont pas sensibles au temps ou vous n’avez pas besoin d’une horloge de présentation.</span><span class="sxs-lookup"><span data-stu-id="a7079-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="a7079-128">Vous avez déjà un pipeline multimédia qui n’est pas basé sur Media Foundation et vous souhaitez incorporer les sources de média Media Foundation dans votre propre Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7079-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="a7079-129">Le lecteur source n’est pas recommandé dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="a7079-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="a7079-130">Pour le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="a7079-130">For protected content.</span></span> <span data-ttu-id="a7079-131">Le lecteur source ne prend pas en charge la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="a7079-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="a7079-132">Si vous vous souciez des détails de la structure de fichier sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="a7079-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="a7079-133">Le lecteur source masque ce type de détail.</span><span class="sxs-lookup"><span data-stu-id="a7079-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a7079-134">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a7079-134">In this section</span></span>



| <span data-ttu-id="a7079-135">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a7079-135">Topic</span></span>                                                                                                        | <span data-ttu-id="a7079-136">Description</span><span class="sxs-lookup"><span data-stu-id="a7079-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7079-137">Utilisation du lecteur source pour traiter les données multimédias</span><span class="sxs-lookup"><span data-stu-id="a7079-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="a7079-138">Cette rubrique explique comment utiliser le lecteur source pour traiter les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="a7079-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="a7079-139">Utilisation du lecteur source en mode asynchrone</span><span class="sxs-lookup"><span data-stu-id="a7079-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="a7079-140">Cette rubrique explique comment utiliser le lecteur source en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a7079-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="a7079-141">Didacticiel : décodage de l’audio</span><span class="sxs-lookup"><span data-stu-id="a7079-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="a7079-142">Ce didacticiel montre comment utiliser le lecteur source pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier WAVE.</span><span class="sxs-lookup"><span data-stu-id="a7079-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a7079-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7079-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7079-144">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7079-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="a7079-145">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7079-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a7079-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="a7079-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




