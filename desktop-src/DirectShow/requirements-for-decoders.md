---
description: Conditions requises pour les décodeurs
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Conditions requises pour les décodeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481449"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="73d17-103">Conditions requises pour les décodeurs</span><span class="sxs-lookup"><span data-stu-id="73d17-103">Requirements for Decoders</span></span>

<span data-ttu-id="73d17-104">Les décodeurs qui fournissent des exemples au VMR doivent respecter les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="73d17-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="73d17-105">Un cadre de sous-image doit être remis à VMR pour chaque image vidéo.</span><span class="sxs-lookup"><span data-stu-id="73d17-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="73d17-106">Les deux frames doivent avoir le même horodatage.</span><span class="sxs-lookup"><span data-stu-id="73d17-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="73d17-107">Si la sous-image n’a pas changé, utilisez \_ l' \_ indicateur AM GBF NOTASYNCPOINT dans la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) pour forcer l’allocateur à retourner une mémoire tampon contenant la dernière trame remise à VMR.</span><span class="sxs-lookup"><span data-stu-id="73d17-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="73d17-108">Il vous suffit de placer un nouvel horodatage sur l’échantillon et de le remettre dans le VMR.</span><span class="sxs-lookup"><span data-stu-id="73d17-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="73d17-109">Si la représentation sous-image est vide, vous devez toujours la remettre.</span><span class="sxs-lookup"><span data-stu-id="73d17-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="73d17-110">VMR détecte le frame vide et ne le fusionne pas avec la vidéo.</span><span class="sxs-lookup"><span data-stu-id="73d17-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="73d17-111">Ce test est effectué par la puce VGA et n’affecte pas les performances de lecture.</span><span class="sxs-lookup"><span data-stu-id="73d17-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="73d17-112">Tous les exemples, à l’exception des flux Live, doivent avoir des horodatages de début et de fin valides attachés.</span><span class="sxs-lookup"><span data-stu-id="73d17-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="73d17-113">(Le DVD n’est pas un flux en direct.)</span><span class="sxs-lookup"><span data-stu-id="73d17-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="73d17-114">Les horodatages de l’échantillon de support doivent être contigus</span><span class="sxs-lookup"><span data-stu-id="73d17-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="73d17-115">Le décodeur doit s’identifier comme étant conforme à VMR pour une utilisation par les générateurs de graphiques.</span><span class="sxs-lookup"><span data-stu-id="73d17-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="73d17-116">Le flux de sous-image doit maintenant contenir des valeurs alpha par pixel incorporées.</span><span class="sxs-lookup"><span data-stu-id="73d17-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="73d17-117">Le type de surface ARGB4444 est idéal pour les sous-images.</span><span class="sxs-lookup"><span data-stu-id="73d17-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="73d17-118">Ne supposez pas que le Stride de la sous-image est identique à la largeur de la surface.</span><span class="sxs-lookup"><span data-stu-id="73d17-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="73d17-119">Ce n’est pas toujours le cas avec VMR.</span><span class="sxs-lookup"><span data-stu-id="73d17-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d17-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73d17-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d17-121">À propos de l’accélération vidéo DirectX</span><span class="sxs-lookup"><span data-stu-id="73d17-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



