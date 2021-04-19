---
title: Audio Low-Delay
description: Audio Low-Delay
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio à faible délai
- Kit de développement logiciel (SDK) Windows Media format, prise en charge audio
- codecs, audio à faible délai
- codecs, prise en charge audio
- audio à faible retards
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510226"
---
# <a name="low-delay-audio"></a><span data-ttu-id="94d2d-108">Audio Low-Delay</span><span class="sxs-lookup"><span data-stu-id="94d2d-108">Low-Delay Audio</span></span>

<span data-ttu-id="94d2d-109">L’audio à faible délai est un mode d’encodage qui produit un contenu audio compressé avec un paramètre de fenêtre de mémoire tampon plus petit que les autres modes.</span><span class="sxs-lookup"><span data-stu-id="94d2d-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="94d2d-110">Cela est utile pour les flux qui doivent être basculés rapidement pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="94d2d-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="94d2d-111">Le scénario classique de cette fonctionnalité est une présentation diffusée en continu qui comprend la possibilité de changer arbitrairement le contenu, par exemple en modifiant le canal d’une télévision.</span><span class="sxs-lookup"><span data-stu-id="94d2d-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="94d2d-112">Lorsque vous utilisez un format audio à faible retards, la latence du changement de contenu est considérablement réduite par rapport à d’autres formats audio.</span><span class="sxs-lookup"><span data-stu-id="94d2d-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="94d2d-113">La latence est également réduite pour les diffusions en direct lorsque vous utilisez des formats à faible délai.</span><span class="sxs-lookup"><span data-stu-id="94d2d-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="94d2d-114">Cette fonctionnalité est prise en charge par les codecs Windows Media Audio 9,1 et Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="94d2d-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="94d2d-115">Les formats à faible délai sont disponibles uniquement pour l’encodage à vitesse binaire constante (à la fois en un passage et en deux passes).</span><span class="sxs-lookup"><span data-stu-id="94d2d-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94d2d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94d2d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94d2d-117">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="94d2d-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




