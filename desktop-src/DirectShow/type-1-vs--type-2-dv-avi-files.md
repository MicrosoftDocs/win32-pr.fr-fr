---
description: Type-1 et
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Types-1 et fichiers AVI DV type-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952187"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="971db-103">Types-1 et fichiers AVI DV type-2</span><span class="sxs-lookup"><span data-stu-id="971db-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="971db-104">Les caméras DV produisent une vidéo audio entrelacée ; chaque image de la vidéo contient également les informations audio.</span><span class="sxs-lookup"><span data-stu-id="971db-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="971db-105">Si vous enregistrez des données DV dans un fichier AVI, vous avez le choix entre les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="971db-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="971db-106">Stockez les données entrelacées sous la forme d’un flux dans le fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="971db-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="971db-107">C’est ce qu’on appelle un fichier de type 1.</span><span class="sxs-lookup"><span data-stu-id="971db-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="971db-108">Fractionner les données entrelacées en flux audio et vidéo distincts.</span><span class="sxs-lookup"><span data-stu-id="971db-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="971db-109">C’est ce qu’on appelle un fichier de type 2.</span><span class="sxs-lookup"><span data-stu-id="971db-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="971db-110">Pour la capture vidéo, où le débit maximal est essentiel, il est préférable d’utiliser un fichier de type 1, car les fichiers de type 2 transmettent des données audio redondantes.</span><span class="sxs-lookup"><span data-stu-id="971db-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="971db-111">(Le flux vidéo contient toujours les données audio.</span><span class="sxs-lookup"><span data-stu-id="971db-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="971db-112">L’audio est simplement masqué en étiquetant le flux en tant que vidéo.) En outre, l’écriture d’un fichier de type 2 nécessite du temps processeur supplémentaire pour fractionner le flux entrelacé.</span><span class="sxs-lookup"><span data-stu-id="971db-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="971db-113">En revanche, les fichiers de type 1 sont moins efficaces pour la modification en temps réel.</span><span class="sxs-lookup"><span data-stu-id="971db-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="971db-114">L’application doit extraire le contenu audio du flux entrelacé, effectuer les modifications et entrelacer à nouveau les données.</span><span class="sxs-lookup"><span data-stu-id="971db-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="971db-115">En outre, le format type-1 n’est pas compatible avec Microsoft® Video pour Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="971db-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="971db-116">DirectShow peut gérer les deux types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="971db-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="971db-117">Un fichier de type 2 peut être converti en type-1 à l’aide du filtre [DV du multiplexeur](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="971db-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="971db-118">Un fichier de type 1 peut être converti en type-2 à l’aide du filtre de [séparateur DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="971db-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="971db-119">Le diagramme suivant illustre la différence entre les deux formats.</span><span class="sxs-lookup"><span data-stu-id="971db-119">The following diagram illustrates the difference between the two formats.</span></span>

![conversion entre type-1 et DV de type 2](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="971db-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="971db-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="971db-122">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="971db-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="971db-123">Données DV au format de fichier AVI</span><span class="sxs-lookup"><span data-stu-id="971db-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



