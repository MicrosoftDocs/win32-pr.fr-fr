---
title: Flux de données arbitraires personnalisés
description: Flux de données arbitraires personnalisés
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, flux de données arbitraires personnalisés
- ASF (Advanced Systems Format), flux de données arbitraires personnalisés
- ASF (format de systèmes avancés), flux de données arbitraires personnalisés
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux de données arbitraires personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509621"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="7aaca-110">Flux de données arbitraires personnalisés</span><span class="sxs-lookup"><span data-stu-id="7aaca-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="7aaca-111">Vous pouvez créer un flux dans un fichier ASF pour contenir n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="7aaca-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="7aaca-112">Si aucun des types de flux pris en charge ne répond à vos besoins, vous devez utiliser un flux de données arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7aaca-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="7aaca-113">L’objet writer gère un flux de données arbitraire de la même manière qu’un flux non compressé. les exemples sont paquets et combinés avec les exemples d’autres flux dans la section de données du fichier.</span><span class="sxs-lookup"><span data-stu-id="7aaca-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="7aaca-114">Bien entendu, seule une application de lecture qui a été spécifiquement programmée pour gérer votre type arbitraire sera en mesure de gérer les données une fois qu’elles sont fournies par l’objet de lecture.</span><span class="sxs-lookup"><span data-stu-id="7aaca-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="7aaca-115">Une utilisation courante des flux de données arbitraires concerne les données multimédias encodées à l’aide d’un codec tiers.</span><span class="sxs-lookup"><span data-stu-id="7aaca-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="7aaca-116">Étant donné que les objets de ce kit de développement logiciel (SDK) n’interagissent pas directement avec les codecs tiers, votre application d’écriture doit traiter les exemples avec la partie encodage du codec et transmettre les exemples compressés au writer.</span><span class="sxs-lookup"><span data-stu-id="7aaca-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aaca-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7aaca-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aaca-118">**Flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="7aaca-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="7aaca-119">**Configuration de flux arbitraires personnalisés**</span><span class="sxs-lookup"><span data-stu-id="7aaca-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




