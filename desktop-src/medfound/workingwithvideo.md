---
description: Utilisation de la vidéo
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Utilisation de la vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320466"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="11b60-103">Utilisation de la vidéo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="11b60-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="11b60-104">Bien que les différents codecs vidéo aient leurs propres particularités, ils utilisent tous les mêmes procédures de base.</span><span class="sxs-lookup"><span data-stu-id="11b60-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="11b60-105">Cette section explique comment encoder et décoder la vidéo avec les codecs Windows Media Video, et traite les fonctionnalités particulières de chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="11b60-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="11b60-106">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="11b60-106">This section contains the following topics.</span></span>



| <span data-ttu-id="11b60-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="11b60-107">Topic</span></span>                                                                                                        | <span data-ttu-id="11b60-108">Description</span><span class="sxs-lookup"><span data-stu-id="11b60-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11b60-109">Choix d’un codec vidéo</span><span class="sxs-lookup"><span data-stu-id="11b60-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="11b60-110">Décrit les types de contenu qui conviennent le mieux à la compression avec chacun des codecs de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="11b60-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="11b60-111">Configuration de l’encodage vidéo</span><span class="sxs-lookup"><span data-stu-id="11b60-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="11b60-112">Décrit comment configurer l’encodeur vidéo DMOs.</span><span class="sxs-lookup"><span data-stu-id="11b60-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="11b60-113">Configuration du décodage vidéo</span><span class="sxs-lookup"><span data-stu-id="11b60-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="11b60-114">Décrit comment configurer le décodeur vidéo DMOs.</span><span class="sxs-lookup"><span data-stu-id="11b60-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="11b60-115">Insertion d’une image clé forcée</span><span class="sxs-lookup"><span data-stu-id="11b60-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="11b60-116">Décrit comment demander l’encodage d’un échantillon sous la forme d’une image clé.</span><span class="sxs-lookup"><span data-stu-id="11b60-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="11b60-117">Encodage vidéo entrelacé</span><span class="sxs-lookup"><span data-stu-id="11b60-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="11b60-118">Décrit comment maintenir l’entrelacement dans les flux de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="11b60-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="11b60-119">Utilisation du codec de profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="11b60-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="11b60-120">Décrit comment utiliser le codec de profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="11b60-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="11b60-121">Utilisation du codec d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="11b60-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="11b60-122">Décrit comment utiliser le codec d’écran Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="11b60-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="11b60-123">Utilisation du codec d’image Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="11b60-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="11b60-124">Décrit comment utiliser le codec d’image Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="11b60-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="11b60-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11b60-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11b60-126">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="11b60-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



