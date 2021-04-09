---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Utilisation de l’enregistreur du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951615"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="50c1f-103">Utilisation de l’enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="50c1f-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="50c1f-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="50c1f-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="50c1f-105">Types de conteneurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="50c1f-105">File Container Types</span></span>

<span data-ttu-id="50c1f-106">L’enregistreur du récepteur offre une prise en charge intégrée de plusieurs types de conteneurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="50c1f-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="50c1f-107">Pour obtenir une liste complète, consultez la page relative au [ \_ transcodage MF \_ CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="50c1f-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="50c1f-108">Vous pouvez prendre en charge des types de conteneur supplémentaires en écrivant un [récepteur multimédia](media-sinks.md)personnalisé.</span><span class="sxs-lookup"><span data-stu-id="50c1f-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="50c1f-109">Le conteneur de fichiers est spécifié lorsque vous créez une nouvelle instance du writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="50c1f-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="50c1f-110">Formats de flux</span><span class="sxs-lookup"><span data-stu-id="50c1f-110">Stream Formats</span></span>

<span data-ttu-id="50c1f-111">Pour chaque flux, l’application doit spécifier les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="50c1f-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="50c1f-112">Le format *d’entrée* est le format que l’application envoie à l’enregistreur du récepteur.</span><span class="sxs-lookup"><span data-stu-id="50c1f-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="50c1f-113">Le format de *sortie* est le format qui sera écrit dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="50c1f-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="50c1f-114">Les formats d’entrée et de sortie peuvent être compressés ou non compressés.</span><span class="sxs-lookup"><span data-stu-id="50c1f-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="50c1f-115">Le writer du récepteur prend en charge les combinaisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="50c1f-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="50c1f-116">Entrée non compressée avec sortie compressée.</span><span class="sxs-lookup"><span data-stu-id="50c1f-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="50c1f-117">C’est généralement le cas et est utilisé pour l’encodage ou le transcodage de scénarios.</span><span class="sxs-lookup"><span data-stu-id="50c1f-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="50c1f-118">Un encodeur de Microsoft Media Foundation doit être disponible qui accepte le type d’entrée et encode le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="50c1f-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="50c1f-119">Entrée compressée avec une sortie identique.</span><span class="sxs-lookup"><span data-stu-id="50c1f-119">Compressed input with identical output.</span></span> <span data-ttu-id="50c1f-120">Utilisez cette combinaison pour REMUX un fichier sans transcodage.</span><span class="sxs-lookup"><span data-stu-id="50c1f-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="50c1f-121">Entrée non compressée avec une sortie identique.</span><span class="sxs-lookup"><span data-stu-id="50c1f-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="50c1f-122">Utilisez cette combinaison pour écrire du contenu audio ou vidéo non compressé dans un conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="50c1f-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="50c1f-123">L’enregistreur du récepteur ne prend pas en charge le redimensionnement vidéo, la conversion de la fréquence d’images ou le rééchantillonnage audio, sauf si ces fonctions sont fournies par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="50c1f-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="50c1f-124">Dans le cas contraire, l’application peut utiliser des [processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md) pour convertir les données d’entrée avant d’envoyer les données au</span><span class="sxs-lookup"><span data-stu-id="50c1f-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="50c1f-125">Création du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="50c1f-125">Creating the Sink Writer</span></span>

<span data-ttu-id="50c1f-126">Il existe deux fonctions qui créent l’enregistreur du récepteur :</span><span class="sxs-lookup"><span data-stu-id="50c1f-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="50c1f-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) prend l’URL d’un fichier de sortie ou un pointeur vers un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="50c1f-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="50c1f-128">Cette fonction crée le récepteur multimédia en interne.</span><span class="sxs-lookup"><span data-stu-id="50c1f-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="50c1f-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) prend un pointeur vers un récepteur multimédia qui a déjà été créé par l’application.</span><span class="sxs-lookup"><span data-stu-id="50c1f-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="50c1f-130">Si vous utilisez l’un des récepteurs multimédias intégrés, la fonction [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) est préférable, car l’appelant n’a pas besoin de configurer le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="50c1f-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="50c1f-131">La méthode [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fournit plusieurs options pour spécifier le type de conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="50c1f-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="50c1f-132">Dans le cas le plus simple, la fonction utilise l’extension de nom de fichier dans l’URL pour sélectionner le conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="50c1f-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="50c1f-133">Pour plus d’informations, reportez-vous à la page de référence des fonctions.</span><span class="sxs-lookup"><span data-stu-id="50c1f-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="50c1f-134">Par exemple, le code suivant spécifie le nom de fichier « output. wmv » pour l’URL.</span><span class="sxs-lookup"><span data-stu-id="50c1f-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="50c1f-135">En fonction de l’extension de nom de fichier, l’enregistreur du récepteur chargera le [récepteur de média ASF](asf-media-sinks.md) pour créer un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="50c1f-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="50c1f-136">Dans le cas de [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), le type de fichier est déterminé par le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="50c1f-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50c1f-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50c1f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c1f-138">Enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="50c1f-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



