---
title: Flux audio
description: Flux audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online stores, flux audio
- magasins en ligne, flux audio
- types 1 magasins en ligne, flux audio
- Windows Media Player Online stores, flux de serveurs musicaux
- magasins en ligne, flux de serveurs musicaux
- types 1 magasins en ligne, flux de serveurs musicaux
- Magasins en ligne du lecteur Windows Media, flux de serveur de musique
- magasins en ligne, flux de serveurs de musique
- types 1 magasins en ligne, flux de serveur de musique
- flux audio
- flux de serveur de musique
- flux de serveurs musicaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030829"
---
# <a name="audio-streams"></a><span data-ttu-id="87537-115">Flux audio</span><span class="sxs-lookup"><span data-stu-id="87537-115">Audio Streams</span></span>

<span data-ttu-id="87537-116">Les magasins en ligne peuvent fournir de la musique sous forme de flux à partir d’un serveur de musique.</span><span class="sxs-lookup"><span data-stu-id="87537-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="87537-117">Cela est utile pour fournir des exemples, des éléments promotionnels spéciaux ou pour permettre aux utilisateurs d’abonnements de profiter de la musique sans avoir à télécharger le contenu.</span><span class="sxs-lookup"><span data-stu-id="87537-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="87537-118">Il est courant de ne pas stocker l’URL du flux en tant que partie du catalogue musical, mais de résoudre l’URL juste avant la lecture en fonction de l’ID de piste.</span><span class="sxs-lookup"><span data-stu-id="87537-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="87537-119">Pour activer cette fonction, le lecteur Windows Media appelle [IWMPContentPartner :: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) et fournit le type de diffusion en continu (en tant que valeur d’énumération [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) et l’ID du flux.</span><span class="sxs-lookup"><span data-stu-id="87537-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="87537-120">Le plug-in retourne l’URL du flux via le paramètre *pbstrURL* .</span><span class="sxs-lookup"><span data-stu-id="87537-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87537-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87537-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87537-122">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="87537-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




