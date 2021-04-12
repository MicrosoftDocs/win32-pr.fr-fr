---
title: Flux d’images
description: Flux d’images
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK, flux d’images
- ASF (Advanced Systems Format), flux d’images
- ASF (format des systèmes avancés), flux d’images
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux d’images, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310845"
---
# <a name="image-streams"></a><span data-ttu-id="82a9f-110">Flux d’images</span><span class="sxs-lookup"><span data-stu-id="82a9f-110">Image Streams</span></span>

<span data-ttu-id="82a9f-111">Un flux d’image est un type spécial de flux qui contient des images fixes affectées aux durées de présentation.</span><span class="sxs-lookup"><span data-stu-id="82a9f-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="82a9f-112">Une application peut afficher les images dans un flux d’image comme vous le souhaitez, mais l’implémentation classique consiste à afficher chaque image jusqu’à ce que l’image suivante soit remise, comme un diaporama.</span><span class="sxs-lookup"><span data-stu-id="82a9f-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="82a9f-113">En règle générale, un flux d’image est encodé dans un fichier avec un flux audio pour produire une présentation simple d’images synchronisées avec de la musique ou de la parole.</span><span class="sxs-lookup"><span data-stu-id="82a9f-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="82a9f-114">Les flux d’images sont semblables aux flux vidéo dans la mesure où ils sont créés à partir d’exemples non compressés qui sont compressés dans le cadre du processus d’écriture de fichier, mais ils sont également des flux arbitraires, car vous devez affecter une vitesse de transmission et une fenêtre de mémoire tampon appropriées au contenu sans utiliser les propriétés affectées par un codec.</span><span class="sxs-lookup"><span data-stu-id="82a9f-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82a9f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82a9f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a9f-116">**Flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="82a9f-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="82a9f-117">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="82a9f-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="82a9f-118">**Flux audio et vidéo**</span><span class="sxs-lookup"><span data-stu-id="82a9f-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="82a9f-119">**Écriture de flux d’images**</span><span class="sxs-lookup"><span data-stu-id="82a9f-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




