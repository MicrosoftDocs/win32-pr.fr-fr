---
title: Redimensionnement vidéo
description: Redimensionnement vidéo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK, redimensionnement vidéo
- Windows Media Format SDK, redimensionnement de la vidéo
- Format de systèmes avancés (ASF), redimensionnement vidéo
- ASF (format des systèmes avancés), redimensionnement vidéo
- Format de systèmes avancés (ASF), redimensionnement vidéo
- ASF (format des systèmes avancés), redimensionnement de la vidéo
- redimensionnement vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196552"
---
# <a name="video-resizing"></a><span data-ttu-id="bf7ef-110">Redimensionnement vidéo</span><span class="sxs-lookup"><span data-stu-id="bf7ef-110">Video Resizing</span></span>

<span data-ttu-id="bf7ef-111">Lorsque vous définissez les paramètres d’un flux vidéo, vous devez spécifier une largeur et une hauteur pour les images vidéo.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="bf7ef-112">Cette taille vidéo détermine la taille des images vidéo encodées dans la section de données du fichier.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="bf7ef-113">Toutefois, la taille de la vidéo dans un profil ne détermine pas, ou limite, la taille du média d’entrée que vous fournissez au rédacteur, ou la taille du média de sortie que vous recevez du lecteur.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="bf7ef-114">L’enregistreur peut redimensionner les images vidéo en fonction des besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="bf7ef-115">La taille de l’image vidéo peut être considérée comme allant jusqu’à trois étapes : la taille de la vidéo d’entrée, la taille de la vidéo du flux et la taille de la vidéo de sortie.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="bf7ef-116">La taille de la vidéo d’entrée correspond à la taille des frames que vous transmettez comme exemples à l’objet enregistreur.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="bf7ef-117">Vous définissez cette taille comme l’une des propriétés d’entrée vidéo requises.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="bf7ef-118">Pour plus d’informations sur les propriétés d’entrée, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bf7ef-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="bf7ef-119">La taille vidéo de la diffusion en continu correspond à la taille des frames dans la section des données du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="bf7ef-120">Vous définissez cette taille en tant qu’un des paramètres de configuration de flux requis dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="bf7ef-121">Si vous écrivez un fichier et que la taille de la vidéo d’entrée est différente de la taille de la vidéo du flux, l’enregistreur redimensionne les frames pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="bf7ef-122">Pour plus d’informations sur les propriétés du flux vidéo, consultez [Configuration des flux vidéo](configuring-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="bf7ef-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="bf7ef-123">La taille de la vidéo de sortie est la taille des trames fournies par le lecteur ou le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="bf7ef-124">Vous définissez cette taille comme l’une des propriétés de sortie vidéo requises.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="bf7ef-125">Si vous lisez un fichier et que la taille de la vidéo de sortie est différente de celle de la vidéo de diffusion en continu, le lecteur redimensionne les frames lors du décodage.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="bf7ef-126">Vous ne pouvez pas définir une taille vidéo de flux sur un nombre impair de pixels de largeur.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="bf7ef-127">Si vous définissez la largeur d’un flux vidéo sur une valeur impaire, soit le profil n’est pas accepté par le writer, soit la vidéo obtenue est encodée avec une ligne noire d’un côté pour commettre la différence.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="bf7ef-128">Vous devez veiller à redimensionner la vidéo.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-128">You should take care when resizing video.</span></span> <span data-ttu-id="bf7ef-129">Les images ont tendance à être plus adaptées à leur résolution d’origine.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="bf7ef-130">Le redimensionnement des images peut souvent provoquer une distorsion et rendre le texte illisible.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="bf7ef-131">Si vous compressez la vidéo à une vitesse de transmission faible, vous constaterez également que les distorsions de redimensionnement peuvent entraîner des artefacts de compression graves.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="bf7ef-132">Le codec d’écran Windows Media Video 9 ne prend pas en charge le redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf7ef-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf7ef-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7ef-134">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="bf7ef-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="bf7ef-135">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="bf7ef-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="bf7ef-136">**Utilisation des sorties**</span><span class="sxs-lookup"><span data-stu-id="bf7ef-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




