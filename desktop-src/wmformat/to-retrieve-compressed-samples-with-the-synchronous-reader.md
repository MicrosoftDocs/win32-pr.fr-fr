---
title: Pour récupérer des exemples compressés avec le lecteur synchrone
description: Pour récupérer des exemples compressés avec le lecteur synchrone
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- ASF (Advanced Systems Format), récupération des exemples compressés
- ASF (format des systèmes avancés), récupération des exemples compressés
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- ASF (Advanced Systems Format), exemples compressés
- ASF (Advanced Systems Format), exemples compressés
- lecteurs synchrones, récupération des exemples compressés
- lecteurs synchrones, exemples compressés
- exemples compressés, récupération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101257"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="86315-112">Pour récupérer des exemples compressés avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="86315-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="86315-113">À l’instar du lecteur asynchrone, le lecteur synchrone peut également récupérer des exemples compressés.</span><span class="sxs-lookup"><span data-stu-id="86315-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="86315-114">Les exemples compressés doivent être utilisés lors de la copie de flux d’un fichier vers un autre.</span><span class="sxs-lookup"><span data-stu-id="86315-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="86315-115">Le kit de développement logiciel (SDK) Windows Media format ne fournit aucune méthode pour décoder les données après leur extraction à partir d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="86315-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="86315-116">Si vous recevez des exemples compressés et que vous souhaitez les décompresser ultérieurement, vous devrez fournir votre propre code pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="86315-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="86315-117">Une façon de contourner cette limitation consiste à écrire les exemples compressés dans un nouveau fichier ASF, puis à les relire dans des exemples normaux et non compressés.</span><span class="sxs-lookup"><span data-stu-id="86315-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="86315-118">Pour recevoir des exemples compressés avec le lecteur synchrone, appelez [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) avant ou pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="86315-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="86315-119">Pass true pour *fCompressed*.</span><span class="sxs-lookup"><span data-stu-id="86315-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="86315-120">Les flux d’images ne sont pas valides pour la remise du flux compressé.</span><span class="sxs-lookup"><span data-stu-id="86315-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="86315-121">Si vous copiez un flux d’image d’un fichier vers un autre, il ne fonctionnera pas dans le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="86315-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="86315-122">Pour copier un flux d’image à partir d’un fichier vers un fichier, récupérez les exemples de flux d’image par numéro de sortie et incluez-les dans le nouveau fichier comme si vous incluiez un nouveau flux d’image.</span><span class="sxs-lookup"><span data-stu-id="86315-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="86315-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86315-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86315-124">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="86315-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




