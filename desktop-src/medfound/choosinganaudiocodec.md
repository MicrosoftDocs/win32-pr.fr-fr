---
description: Choix d’un codec audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Choix d’un codec audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201178"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="62a3d-103">Choix d’un codec audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="62a3d-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="62a3d-104">L' [**Encodeur Windows Media Audio**](windowsmediaaudioencoder.md) fournit trois catégories d’encodage audio, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="62a3d-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="62a3d-105">Category</span><span class="sxs-lookup"><span data-stu-id="62a3d-105">Category</span></span>                         | <span data-ttu-id="62a3d-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="62a3d-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="62a3d-107">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="62a3d-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="62a3d-108">Compression de l’audio à usage général.</span><span class="sxs-lookup"><span data-stu-id="62a3d-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="62a3d-109">Windows Media Audio professionnel</span><span class="sxs-lookup"><span data-stu-id="62a3d-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="62a3d-110">Compression des données audio multicanaux et haute définition.</span><span class="sxs-lookup"><span data-stu-id="62a3d-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="62a3d-111">Windows Media Audio sans perte</span><span class="sxs-lookup"><span data-stu-id="62a3d-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="62a3d-112">Compression de l’audio sans perdre les données d’origine.</span><span class="sxs-lookup"><span data-stu-id="62a3d-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="62a3d-113">La catégorie standard fournit un codage audio à usage général adapté à un large éventail de scénarios de lecture.</span><span class="sxs-lookup"><span data-stu-id="62a3d-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="62a3d-114">Par exemple, il peut compresser l’audio sur un faible taux de diffusion en continu sur un réseau avec une bande passante limitée, ou pour le rendu sur des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="62a3d-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="62a3d-115">À l’autre extrémité de l’échelle, elle peut produire du contenu audio compressé pour une lecture de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="62a3d-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="62a3d-116">L’accent est mis sur la musique des algorithmes d’encodage standard, mais ils conviennent également à d’autres contenus audio complexes.</span><span class="sxs-lookup"><span data-stu-id="62a3d-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="62a3d-117">La catégorie standard doit être votre valeur par défaut pour le contenu audio.</span><span class="sxs-lookup"><span data-stu-id="62a3d-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="62a3d-118">Les catégories professionnel et sans perte doivent être utilisées pour répondre à des besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="62a3d-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="62a3d-119">Un encodeur distinct, l' [**encodeur Windows Media Voice**](windowsmediaaudiovoiceencoder.md), permet la compression de la parole.</span><span class="sxs-lookup"><span data-stu-id="62a3d-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62a3d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62a3d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62a3d-121">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="62a3d-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



