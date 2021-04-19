---
description: Le récepteur multimédia ASF est le composant final dans le pipeline d’encodage qui permet à une application d’écrire un fichier ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Récepteurs de média ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531456"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="d5485-103">Récepteurs de média ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-103">ASF Media Sinks</span></span>

<span data-ttu-id="d5485-104">Le récepteur multimédia ASF est le composant final dans le pipeline d’encodage qui permet à une application d’écrire un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d5485-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="d5485-105">Media Foundation fournit deux types de récepteurs de média ASF :</span><span class="sxs-lookup"><span data-stu-id="d5485-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="d5485-106">Le *récepteur de fichiers ASF* est utilisé pour archiver des données de support ASF dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d5485-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="d5485-107">Le *récepteur de streaming ASF* est utilisé pour écrire du contenu ASF dans un flux d’octets pouvant être diffusé en continu sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="d5485-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="d5485-108">Les récepteurs de média ASF contiennent un ou plusieurs récepteurs de flux, qui représentent les données à écrire pour chaque flux dans le fichier ASF de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5485-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="d5485-109">Pour l’encodage des applications qui s’exécutent sous Windows Vista, vous devez configurer manuellement la topologie d’encodage en créant et en configurant le récepteur multimédia ASF, puis en l’ajoutant à la topologie.</span><span class="sxs-lookup"><span data-stu-id="d5485-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="d5485-110">Dans Windows 7, si vous utilisez les objets de transcodage rapide pour créer la topologie, vous n’avez pas à créer directement le récepteur multimédia et l’application n’appelle aucune méthode sur le récepteur multimédia ou sur l’un des récepteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="d5485-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="d5485-111">Les objets de transcodage rapide instancient les récepteurs multimédia requis et l’ajoutent à la topologie avant de retourner une référence à l’application appelant.</span><span class="sxs-lookup"><span data-stu-id="d5485-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="d5485-112">Toutefois, pour les objets de transcodage rapides, certaines restrictions s’appliquent selon le type d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d5485-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="d5485-113">Modèle objet du récepteur multimédia ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="d5485-114">Récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="d5485-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5485-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="d5485-116">Modèle objet du récepteur multimédia ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="d5485-117">Les récepteurs de média ASF implémentent l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) et exposent les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="d5485-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="d5485-118">Une application peut obtenir une référence à ces interfaces en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le récepteur multimédia ASF qu’elle utilise pour générer des exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5485-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="d5485-119">Interface</span><span class="sxs-lookup"><span data-stu-id="d5485-119">Interface</span></span>                                                  | <span data-ttu-id="d5485-120">Description</span><span class="sxs-lookup"><span data-stu-id="d5485-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5485-121">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="d5485-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="d5485-122">Requis pour tous les récepteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="d5485-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="d5485-123">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="d5485-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="d5485-124">Implémenté par le récepteur de fichiers ASF qui écrit le contenu multimédia généré dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d5485-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="d5485-125">Vous pouvez utiliser les méthodes sur cette interface pour vider les données et mettre à jour l’objet d’en-tête ASF du fichier de sortie final.</span><span class="sxs-lookup"><span data-stu-id="d5485-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="d5485-126">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="d5485-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="d5485-127">Reçoit des notifications de modification d’État à partir de l’horloge de présentation.</span><span class="sxs-lookup"><span data-stu-id="d5485-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="d5485-128">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="d5485-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="d5485-129">L’objet ASF ContentInfo est un objet de niveau WMContainer qui stocke principalement les informations d’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="d5485-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="d5485-130">Cette valeur est utilisée pour créer des récepteurs de média ASF.</span><span class="sxs-lookup"><span data-stu-id="d5485-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="d5485-131">**IMFMetadata**</span><span class="sxs-lookup"><span data-stu-id="d5485-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="d5485-132">Utilisé pour décrire les métadonnées du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d5485-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="d5485-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="d5485-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="d5485-134">Récupère une collection de métadonnées, soit pour une présentation complète, soit pour un flux de la présentation.</span><span class="sxs-lookup"><span data-stu-id="d5485-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="d5485-135">Récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-135">ASF File Sink</span></span>

<span data-ttu-id="d5485-136">Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d5485-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="d5485-137">Vous devez créer, configurer et appeler des méthodes sur le récepteur de fichiers ou l’un de ses récepteurs de flux si vous utilisez les objets de couche de pipeline pour écrire un nouveau fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d5485-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="d5485-138">Après avoir configuré le récepteur de fichiers, vous pouvez l’ajouter au pipeline d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d5485-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="d5485-139">Voici les étapes générales à suivre pour utiliser le récepteur de fichiers ASF :</span><span class="sxs-lookup"><span data-stu-id="d5485-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="d5485-140">Créez le récepteur de fichiers in-process ou out-of-process.</span><span class="sxs-lookup"><span data-stu-id="d5485-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="d5485-141">Configurez le récepteur de fichiers avec tous les flux, les propriétés d’encodage et les informations de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d5485-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="d5485-142">Associez le récepteur de fichiers au nœud de topologie de sortie en énumérant les récepteurs de flux ou en effectuant le suivi des numéros de flux avec dans le récepteur.</span><span class="sxs-lookup"><span data-stu-id="d5485-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="d5485-143">Les rubriques suivantes contiennent des informations détaillées sur l’utilisation du récepteur de fichiers ASF :</span><span class="sxs-lookup"><span data-stu-id="d5485-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="d5485-144">Création du récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="d5485-145">Ajout d’informations de flux au récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="d5485-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="d5485-146">Définition des propriétés dans le récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="d5485-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="d5485-147">Ajout de métadonnées au récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="d5485-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="d5485-148">Modèle de mémoire tampon de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="d5485-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="d5485-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5485-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5485-150">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="d5485-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="d5485-151">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5485-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
