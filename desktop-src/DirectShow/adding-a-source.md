---
description: Ajout d’une source
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Ajout d’une source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515328"
---
# <a name="adding-a-source"></a><span data-ttu-id="c066d-103">Ajout d’une source</span><span class="sxs-lookup"><span data-stu-id="c066d-103">Adding a Source</span></span>

<span data-ttu-id="c066d-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="c066d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c066d-105">Créez un objet source de la même façon que vous créez d’autres objets Timeline.</span><span class="sxs-lookup"><span data-stu-id="c066d-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="c066d-106">Toutefois, avant de l’insérer dans la chronologie, vous devez spécifier au moins les propriétés suivantes sur la source.</span><span class="sxs-lookup"><span data-stu-id="c066d-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="c066d-107">Heures de début et de fin, par rapport à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="c066d-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="c066d-108">Appelez la méthode [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="c066d-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="c066d-109">Fichier multimédia à utiliser comme source.</span><span class="sxs-lookup"><span data-stu-id="c066d-109">The media file to use as a source.</span></span> <span data-ttu-id="c066d-110">Appelez la méthode [**IAMTimelineSrc :: SetMediaName**](iamtimelinesrc-setmedianame.md) avec une chaîne de caractères larges représentant le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="c066d-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="c066d-111">Les heures de début et de fin des médias, qui sont relatives au fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="c066d-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="c066d-112">Appelez la méthode [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="c066d-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="c066d-113">Pour plus d’informations sur les temps de support, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="c066d-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="c066d-114">Dans l’exemple suivant, l’élément source démarre quatre secondes dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c066d-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="c066d-115">La durée du média est de 10 secondes, soit deux fois plus longue que la durée de la chronologie, ce qui signifie que la source est lue à deux fois la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="c066d-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="c066d-116">Les unités constantes sont définies comme 10 millions (10 ^ 7) et sont égales à une seconde.</span><span class="sxs-lookup"><span data-stu-id="c066d-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="c066d-117">Actuellement, les ne peuvent pas afficher simultanément plus de 75 sources compressées avec des codecs VCM (Video Compression Manager).</span><span class="sxs-lookup"><span data-stu-id="c066d-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="c066d-118">En outre, si le projet dans son ensemble contient plus de 75 de telles sources, vous devez utiliser la reconnexion dynamique ou DES ne peuvent pas afficher un aperçu du projet.</span><span class="sxs-lookup"><span data-stu-id="c066d-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="c066d-119">Pour plus d’informations, consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="c066d-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="c066d-120">Pour plus d’informations sur les sources, consultez [utilisation des sources](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c066d-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c066d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c066d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c066d-122">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="c066d-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



