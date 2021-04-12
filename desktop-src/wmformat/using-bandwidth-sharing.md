---
title: Utilisation du partage de bande passante
description: Utilisation du partage de bande passante
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK, partage de bande passante
- partage de bande passante, à propos de
- profils, partage de bande passante
- flux, partage de bande passante
- partage de bande passante, interface IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381699"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="a1c45-108">Utilisation du partage de bande passante</span><span class="sxs-lookup"><span data-stu-id="a1c45-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="a1c45-109">Vous pouvez utiliser des objets de partage de bande passante pour spécifier que certains flux, lorsqu’ils sont combinés, n’utilisent pas plus de bande passante que ce qui est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a1c45-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="a1c45-110">Les informations contenues dans un objet de partage de bande passante ne sont pas générées ou vérifiées par le writer et ne sont utilisées par le lecteur pour rien.</span><span class="sxs-lookup"><span data-stu-id="a1c45-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="a1c45-111">Lorsqu’un fichier écrit qui possède des informations de partage de bande passante dans son profil, les données sont stockées dans sa section d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="a1c45-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="a1c45-112">Vous pouvez utiliser l’interface [**IWMProfile**](iwmprofile.md) dans le lecteur pour vérifier les informations de partage de bande passante lors de la lecture du fichier.</span><span class="sxs-lookup"><span data-stu-id="a1c45-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="a1c45-113">Chaque objet de partage de bande passante est défini par deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="a1c45-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="a1c45-114">Tout d’abord, la bande passante, telle que définie par une bande passante et une fenêtre de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a1c45-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="a1c45-115">Le deuxième paramètre est un type de partage de bande passante, qui peut être exclusif ou partiel.</span><span class="sxs-lookup"><span data-stu-id="a1c45-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="a1c45-116">Le partage de bande passante exclusive signifie que les flux constitutifs sont lus l’un après l’autre, tandis que partial signifie que les flux sont remis simultanément.</span><span class="sxs-lookup"><span data-stu-id="a1c45-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c45-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1c45-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c45-118">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="a1c45-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="a1c45-119">**IWMProfile3::AddBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="a1c45-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="a1c45-120">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="a1c45-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="a1c45-121">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="a1c45-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="a1c45-122">**IWMProfile3::GetBandwidthSharingCount**</span><span class="sxs-lookup"><span data-stu-id="a1c45-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="a1c45-123">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="a1c45-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




