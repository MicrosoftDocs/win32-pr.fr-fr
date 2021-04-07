---
title: Utilisation des récepteurs d’écriture
description: Utilisation des récepteurs d’écriture
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), récepteurs d’écriture
- ASF (format de systèmes avancés), récepteurs d’écriture
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs d’écriture
- récepteurs d’écriture, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723370"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="10c0d-109">Utilisation des récepteurs d’écriture</span><span class="sxs-lookup"><span data-stu-id="10c0d-109">Working with Writer Sinks</span></span>

<span data-ttu-id="10c0d-110">L’objet Writer du kit de développement logiciel (SDK) de format Windows Media traite les données de média d’entrée dans un flux de bits.</span><span class="sxs-lookup"><span data-stu-id="10c0d-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="10c0d-111">Toutefois, l’objet Writer ne remet pas le flux binaire à sa destination finale (dans un fichier ou un emplacement réseau).</span><span class="sxs-lookup"><span data-stu-id="10c0d-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="10c0d-112">Pour écrire le contenu ASF dans un format utilisable, vous devez utiliser des récepteurs d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="10c0d-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="10c0d-113">L’objet Writer prend en charge trois types de récepteurs : les récepteurs de fichiers, les récepteurs réseau et les récepteurs push.</span><span class="sxs-lookup"><span data-stu-id="10c0d-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="10c0d-114">Un récepteur de fichiers écrit du contenu ASF dans un fichier ASF sur le disque.</span><span class="sxs-lookup"><span data-stu-id="10c0d-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="10c0d-115">Un récepteur réseau diffuse du contenu ASF à partir d’une adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="10c0d-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="10c0d-116">Un récepteur de notifications push transmet des données à un serveur exécutant Windows Media Services afin que le serveur puisse mettre le contenu à la disposition de son public visé.</span><span class="sxs-lookup"><span data-stu-id="10c0d-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="10c0d-117">Vous pouvez également créer vos propres récepteurs pour fournir des données ASF de la manière requise par votre application.</span><span class="sxs-lookup"><span data-stu-id="10c0d-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="10c0d-118">Pour plus d’informations sur les récepteurs réseau et les récepteurs de notifications push, consultez [envoi de données ASF sur un réseau](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="10c0d-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="10c0d-119">Le reste de cette section traite des récepteurs d’écriture.</span><span class="sxs-lookup"><span data-stu-id="10c0d-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="10c0d-120">Vous pouvez configurer un ou plusieurs récepteurs pour chaque instance du writer que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="10c0d-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="10c0d-121">Chaque récepteur ne gère qu’une seule destination.</span><span class="sxs-lookup"><span data-stu-id="10c0d-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="10c0d-122">Par exemple, si vous souhaitez écrire trois fichiers à la fois, vous devez créer et configurer un récepteur de fichiers distinct pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="10c0d-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="10c0d-123">Les sections suivantes décrivent l’utilisation des récepteurs de Writers.</span><span class="sxs-lookup"><span data-stu-id="10c0d-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="10c0d-124">Section</span><span class="sxs-lookup"><span data-stu-id="10c0d-124">Section</span></span>                                                                      | <span data-ttu-id="10c0d-125">Description</span><span class="sxs-lookup"><span data-stu-id="10c0d-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="10c0d-126">Ajout de récepteurs à l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="10c0d-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="10c0d-127">Décrit comment ajouter des récepteurs au writer.</span><span class="sxs-lookup"><span data-stu-id="10c0d-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="10c0d-128">Énumération des récepteurs</span><span class="sxs-lookup"><span data-stu-id="10c0d-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="10c0d-129">Décrit comment énumérer les récepteurs qui ont été ajoutés au writer.</span><span class="sxs-lookup"><span data-stu-id="10c0d-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="10c0d-130">Obtention de messages d’erreur à partir d’un récepteur</span><span class="sxs-lookup"><span data-stu-id="10c0d-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="10c0d-131">Décrit comment configurer des récepteurs pour remettre des messages d’État à votre application.</span><span class="sxs-lookup"><span data-stu-id="10c0d-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="10c0d-132">Utilisation de récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="10c0d-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="10c0d-133">Décrit comment utiliser un récepteur de fichiers de Writer pour créer un fichier ASF sur le disque.</span><span class="sxs-lookup"><span data-stu-id="10c0d-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="10c0d-134">Utilisation de récepteurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="10c0d-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="10c0d-135">Décrit comment créer et utiliser vos propres récepteurs personnalisés pour fournir des données ASF.</span><span class="sxs-lookup"><span data-stu-id="10c0d-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="10c0d-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10c0d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10c0d-137">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="10c0d-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="10c0d-138">**Interface IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="10c0d-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="10c0d-139">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="10c0d-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




