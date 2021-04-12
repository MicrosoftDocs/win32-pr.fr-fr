---
title: Gestionnaires de fichiers et de flux personnalisés
description: Gestionnaires de fichiers et de flux personnalisés
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Video for Windows (VFW), gestionnaires de fichiers personnalisés
- Video for Windows (VFW), gestionnaires de flux personnalisés
- Video for Windows (VFW), gestionnaires de fichiers
- Video for Windows (VFW), gestionnaires de flux
- VFW (vidéo pour Windows), gestionnaires de fichiers personnalisés
- VFW (vidéo pour Windows), gestionnaires de flux personnalisés
- VFW (vidéo pour Windows), gestionnaires de fichiers
- VFW (vidéo pour Windows), gestionnaires de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462294"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="c4a1d-111">Gestionnaires de fichiers et de flux personnalisés</span><span class="sxs-lookup"><span data-stu-id="c4a1d-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="c4a1d-112">Les gestionnaires de fichiers et de flux sont des pilotes qui fournissent des interfaces cohérentes à une application qui contrôle les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="c4a1d-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="c4a1d-113">Les gestionnaires de fichiers et de flux inclus dans le système d’exploitation utilisent des données vidéo et Waveform-Audio stockées dans des fichiers AVI (Audio-Video entrelacés) et des fichiers audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="c4a1d-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="c4a1d-114">Vous pouvez écrire des gestionnaires pour permettre à votre application d’écrire ou d’accéder à des données multimédias à partir d’une autre source, telle qu’un fichier à l’aide d’un format propriétaire, un fichier AVI développé pour contenir des flux de données supplémentaires ou un gestionnaire qui génère ses propres données multimédias.</span><span class="sxs-lookup"><span data-stu-id="c4a1d-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="c4a1d-115">Si vous disposez d’un format de fichier personnalisé pour les données AVI que vous souhaitez utiliser avec les [fonctions et macros avifile](avifile-functions-and-macros.md), vous devez écrire un gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c4a1d-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="c4a1d-116">À propos des gestionnaires de fichiers et de flux personnalisés</span><span class="sxs-lookup"><span data-stu-id="c4a1d-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="c4a1d-117">Utilisation de gestionnaires de fichiers et de flux personnalisés</span><span class="sxs-lookup"><span data-stu-id="c4a1d-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="c4a1d-118">Informations de référence sur les fichiers et les gestionnaires de flux personnalisés</span><span class="sxs-lookup"><span data-stu-id="c4a1d-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




