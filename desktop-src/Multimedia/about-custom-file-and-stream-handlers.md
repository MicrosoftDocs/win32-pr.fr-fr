---
title: À propos des gestionnaires de fichiers et de flux personnalisés
description: À propos des gestionnaires de fichiers et de flux personnalisés
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
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
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840801"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="cbd51-111">À propos des gestionnaires de fichiers et de flux personnalisés</span><span class="sxs-lookup"><span data-stu-id="cbd51-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="cbd51-112">Votre application peut utiliser un gestionnaire de fichiers personnalisé pour lire un fichier ou écrire dans un fichier dont le format n’est pas standard.</span><span class="sxs-lookup"><span data-stu-id="cbd51-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="cbd51-113">Pour ce faire, votre application utilise simplement le nom de votre gestionnaire de fichiers lors de l’ouverture du fichier ou de l’allocation de l’interface de fichier.</span><span class="sxs-lookup"><span data-stu-id="cbd51-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="cbd51-114">La bibliothèque AVIFile utilise ensuite les fonctions de votre gestionnaire de fichiers au lieu de celles d’un autre gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbd51-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="cbd51-115">Le format non standard apparaît sous forme de données AVI standard pour votre application ou toute autre application à l’aide de votre gestionnaire de fichiers personnalisé.</span><span class="sxs-lookup"><span data-stu-id="cbd51-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="cbd51-116">De même, votre application peut utiliser un gestionnaire de flux personnalisé pour lire un flux dans un format non standard.</span><span class="sxs-lookup"><span data-stu-id="cbd51-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="cbd51-117">Un flux, qu’il s’agisse de données audio, vidéo, MIDI, de texte ou de données personnalisées, est un composant d’un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="cbd51-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="cbd51-118">Par exemple, un fichier AVI qui contient une séquence vidéo, une bande son anglaise et une bande son française sont constitués de trois flux.</span><span class="sxs-lookup"><span data-stu-id="cbd51-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="cbd51-119">Votre application peut spécifier les flux dans un fichier AVI pour traiter et diriger chacun de ces flux vers un gestionnaire qui peut traiter de façon optimale le type approprié de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="cbd51-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="cbd51-120">Vous devez placer des gestionnaires de fichiers et de flux personnalisés dans une ou plusieurs dll, séparés des fichiers d’application principaux.</span><span class="sxs-lookup"><span data-stu-id="cbd51-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




