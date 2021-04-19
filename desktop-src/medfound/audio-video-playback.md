---
description: Cette section décrit comment implémenter la lecture audio/vidéo dans votre application à l’aide de Microsoft Media Foundation.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Lecture audio/vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516597"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="b6c54-103">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="b6c54-103">Audio/Video Playback</span></span>

<span data-ttu-id="b6c54-104">Cette section décrit comment implémenter la lecture audio/vidéo dans votre application à l’aide de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b6c54-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6c54-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b6c54-105">In this section</span></span>



| <span data-ttu-id="b6c54-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b6c54-106">Topic</span></span>                                                                                               | <span data-ttu-id="b6c54-107">Description</span><span class="sxs-lookup"><span data-stu-id="b6c54-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6c54-108">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6c54-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="b6c54-109">Ce didacticiel montre comment lire des fichiers multimédias à l’aide de l’objet [Media session](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c54-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="b6c54-110">Comment lire des fichiers multimédias protégés</span><span class="sxs-lookup"><span data-stu-id="b6c54-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="b6c54-111">Comment lire des fichiers qui contiennent des médias protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="b6c54-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="b6c54-112">Recherche de la durée d’un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="b6c54-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="b6c54-113">Comment rechercher la durée d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="b6c54-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="b6c54-114">Recherche, avance rapide et lecture inversée</span><span class="sxs-lookup"><span data-stu-id="b6c54-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="b6c54-115">Cette rubrique montre un exemple de code pour gérer la recherche et les modifications de taux, lors de l’utilisation de la [session multimédia](media-session.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="b6c54-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="b6c54-116">Comment définir l’heure d’arrêt de la lecture</span><span class="sxs-lookup"><span data-stu-id="b6c54-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="b6c54-117">Cette rubrique explique comment définir une heure d’arrêt pour la lecture lors de l’utilisation de la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="b6c54-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="b6c54-118">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="b6c54-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="b6c54-119">Le convertisseur vidéo amélioré (EVR) est un composant qui affiche la vidéo sur l’écran de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6c54-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="b6c54-120">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="b6c54-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="b6c54-121">Le convertisseur audio de streaming (SAR) est un récepteur multimédia qui restitue l’audio.</span><span class="sxs-lookup"><span data-stu-id="b6c54-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="b6c54-122">MFPlay</span><span class="sxs-lookup"><span data-stu-id="b6c54-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="b6c54-123">L’API MFPlay est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b6c54-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="b6c54-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6c54-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6c54-125">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6c54-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="b6c54-126">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6c54-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="b6c54-127">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6c54-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




