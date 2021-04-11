---
title: Lecture des métadonnées lors de la lecture
description: Lecture des métadonnées lors de la lecture
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media Format SDK, lecture des métadonnées
- Windows Media Format SDK, lecteurs asynchrones
- Windows Media Format SDK, lecteurs synchrones
- ASF (Advanced Systems Format), lecture des métadonnées
- ASF (format des systèmes avancés), lecture des métadonnées
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs asynchrones, lecture des métadonnées
- lecteurs synchrones, lecture des métadonnées
- métadonnées, lire lors de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030922"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="7911f-115">Lecture des métadonnées lors de la lecture</span><span class="sxs-lookup"><span data-stu-id="7911f-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="7911f-116">L’objet lecteur asynchrone et l’objet lecteur synchrone peuvent lire les métadonnées à partir de l’en-tête d’un fichier ASF chargé.</span><span class="sxs-lookup"><span data-stu-id="7911f-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="7911f-117">Lors de la lecture de fichiers, les attributs de métadonnées sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7911f-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="7911f-118">Les deux objets Reader peuvent être interrogés pour les interfaces [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) et [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="7911f-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="7911f-119">Pour plus d’informations sur l’accès aux métadonnées, consultez [utilisation des métadonnées](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="7911f-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7911f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7911f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7911f-121">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="7911f-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




