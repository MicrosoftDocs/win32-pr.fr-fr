---
description: Cette section décrit comment utiliser l’API de transcodage pour recoder des fichiers multimédias. L’API de transcodage a été introduite dans Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863942"
---
# <a name="transcode-api"></a><span data-ttu-id="86735-104">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="86735-104">Transcode API</span></span>

<span data-ttu-id="86735-105">Cette section décrit comment utiliser l’API de transcodage pour recoder des fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="86735-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="86735-106">L’API de transcodage a été introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="86735-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="86735-107">Le *transcodage* est la conversion d’un fichier multimédia numérique d’un format à un autre.</span><span class="sxs-lookup"><span data-stu-id="86735-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="86735-108">L’API de transcodage est conçue pour être utilisée avec la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="86735-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="86735-109">Il simplifie l’utilisation de la session multimédia pour certains types d’applications de transcodage :</span><span class="sxs-lookup"><span data-stu-id="86735-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="86735-110">Encodage à vitesse de transmission constante (CBR), où la vitesse de transmission cible est connue à l’avance.</span><span class="sxs-lookup"><span data-stu-id="86735-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="86735-111">Au plus un flux audio et un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="86735-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="86735-112">Encodage à partir de et vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="86735-112">Encoding from and to a file.</span></span>

<span data-ttu-id="86735-113">L’API de transcodage ne prend pas en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="86735-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="86735-114">Débit binaire variable (VBR) ou encodage à plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="86735-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="86735-115">Plusieurs flux audio ou plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="86735-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="86735-116">Contenu protégé par DRM autre que les fichiers ASF protégés par WMDRM.</span><span class="sxs-lookup"><span data-stu-id="86735-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="86735-117">La diffusion en continu en direct, telle que la diffusion en continu en direct ou en direct.</span><span class="sxs-lookup"><span data-stu-id="86735-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="86735-118">Si votre application d’encodage respecte ces contraintes, l’API de transcodage est un modèle de programmation plus simple que l’utilisation de la session de média seule.</span><span class="sxs-lookup"><span data-stu-id="86735-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="86735-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="86735-119">In this section</span></span>



| <span data-ttu-id="86735-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="86735-120">Topic</span></span>                                                                                          | <span data-ttu-id="86735-121">Description</span><span class="sxs-lookup"><span data-stu-id="86735-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86735-122">À propos de l’API de transcodage</span><span class="sxs-lookup"><span data-stu-id="86735-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="86735-123">Fournit une vue d’ensemble générale de l’API de transcodage.</span><span class="sxs-lookup"><span data-stu-id="86735-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="86735-124">Utilisation de l’API de transcodage</span><span class="sxs-lookup"><span data-stu-id="86735-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="86735-125">Décrit comment une application utilise l’API de transcodage.</span><span class="sxs-lookup"><span data-stu-id="86735-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="86735-126">Didacticiel : encodage d’un fichier MP4</span><span class="sxs-lookup"><span data-stu-id="86735-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="86735-127">Didacticiel pas à pas qui montre comment utiliser l’API de transcodage pour encoder un fichier MP4.</span><span class="sxs-lookup"><span data-stu-id="86735-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="86735-128">Didacticiel : encodage d’un fichier WMA</span><span class="sxs-lookup"><span data-stu-id="86735-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="86735-129">Montre comment utiliser l’API de transcodage pour encoder un fichier WMA.</span><span class="sxs-lookup"><span data-stu-id="86735-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="86735-130">Ce didacticiel modifie le code affiché dans le [Didacticiel : codage d’un fichier MP4](tutorial--encoding-an-mp4-file-.md). vous devez d’abord lire ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="86735-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="86735-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86735-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86735-132">Codage et création de fichier</span><span class="sxs-lookup"><span data-stu-id="86735-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="86735-133">Media Foundation : notions essentielles</span><span class="sxs-lookup"><span data-stu-id="86735-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="86735-134">Vue d’ensemble de l’encodage dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86735-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




