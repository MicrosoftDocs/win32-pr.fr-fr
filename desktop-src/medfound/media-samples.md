---
description: Exemples de supports
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Exemples de supports (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953417"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="fe80f-103">Exemples de supports (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="fe80f-103">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="fe80f-104">Un exemple de média est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="fe80f-104">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="fe80f-105">Les exemples de supports exposent l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="fe80f-105">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="fe80f-106">La quantité de données contenues dans un échantillon dépend du composant qui crée l’échantillon et du type de données dans les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="fe80f-106">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="fe80f-107">Pour une vidéo non compressée, un échantillon contient généralement une seule image vidéo.</span><span class="sxs-lookup"><span data-stu-id="fe80f-107">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="fe80f-108">Pour le son non compressé, la quantité de données peut varier, mais généralement une trame audio ne couvre pas deux échantillons.</span><span class="sxs-lookup"><span data-stu-id="fe80f-108">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="fe80f-109">Pour les données compressées, ces instructions peuvent ne pas s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="fe80f-109">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="fe80f-110">Un seul échantillon peut contenir plusieurs mémoires tampons pour des raisons d’efficacité.</span><span class="sxs-lookup"><span data-stu-id="fe80f-110">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="fe80f-111">Par exemple, dans un fichier ASF, une image vidéo est souvent répartie entre plusieurs paquets ASF.</span><span class="sxs-lookup"><span data-stu-id="fe80f-111">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="fe80f-112">La source du média peut lire les paquets dans plusieurs mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="fe80f-112">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="fe80f-113">Au lieu de copier chaque fragment dans une mémoire tampon, la source place simplement toutes les mémoires tampon dans un seul échantillon.</span><span class="sxs-lookup"><span data-stu-id="fe80f-113">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="fe80f-114">Les composants en aval peuvent ensuite décider s’il faut copier les mémoires tampons plus petites dans une seule mémoire tampon contiguë.</span><span class="sxs-lookup"><span data-stu-id="fe80f-114">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="fe80f-115">En règle générale, si vous écrivez un composant de pipeline, vous devez supposer que tout exemple peut contenir plusieurs mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="fe80f-115">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="fe80f-116">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe80f-116">This section contains the following topics.</span></span>



| <span data-ttu-id="fe80f-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="fe80f-117">Topic</span></span>                                                        | <span data-ttu-id="fe80f-118">Description</span><span class="sxs-lookup"><span data-stu-id="fe80f-118">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe80f-119">Utilisation des exemples de supports</span><span class="sxs-lookup"><span data-stu-id="fe80f-119">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="fe80f-120">Décrit le comportement général des exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="fe80f-120">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="fe80f-121">Exemples vidéo</span><span class="sxs-lookup"><span data-stu-id="fe80f-121">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="fe80f-122">Décrit une implémentation spécialisée de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) conçue pour contenir des images vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="fe80f-122">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fe80f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe80f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe80f-124">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="fe80f-124">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="fe80f-125">Primitives de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe80f-125">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



