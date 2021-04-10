---
title: Récepteur de fichiers d’auteur, objet
description: Récepteur de fichiers d’auteur, objet
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK, objets récepteur de fichiers du writer
- ASF (Advanced Systems Format), objets de récepteur de fichiers de writer
- ASF (format de systèmes avancés), objets de récepteur de fichiers de writer
- objets, writer file sink, objets
- objets du récepteur de fichiers du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030938"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="ef392-108">Récepteur de fichiers d’auteur, objet</span><span class="sxs-lookup"><span data-stu-id="ef392-108">Writer File Sink Object</span></span>

<span data-ttu-id="ef392-109">L’objet récepteur de fichiers du writer est utilisé lors de l’écriture de la sortie Windows Media dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ef392-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="ef392-110">L’objet récepteur de fichiers du writer est créé par la fonction [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), qui définit un pointeur vers une interface **IWMWriterFileSink** .</span><span class="sxs-lookup"><span data-stu-id="ef392-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="ef392-111">Les autres interfaces de l’objet récepteur de fichiers du writer peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ef392-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="ef392-112">Les interfaces suivantes sont prises en charge par l’objet récepteur de fichiers du writer.</span><span class="sxs-lookup"><span data-stu-id="ef392-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="ef392-113">Interface</span><span class="sxs-lookup"><span data-stu-id="ef392-113">Interface</span></span>                                          | <span data-ttu-id="ef392-114">Description</span><span class="sxs-lookup"><span data-stu-id="ef392-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef392-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="ef392-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="ef392-116">Permet à l’application d’afficher des messages d’État à partir de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef392-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="ef392-117">**IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="ef392-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="ef392-118">Ouvre un fichier dans lequel l’objet Writer peut écrire des données.</span><span class="sxs-lookup"><span data-stu-id="ef392-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="ef392-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="ef392-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="ef392-120">Fournit la gestion étendue d’un objet de récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ef392-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="ef392-121">Hérite de toutes les méthodes de **IWMWriterFileSink**.</span><span class="sxs-lookup"><span data-stu-id="ef392-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="ef392-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="ef392-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="ef392-123">Fournit des options supplémentaires pour l’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ef392-123">Provides additional options for writing files.</span></span> <span data-ttu-id="ef392-124">Hérite de toutes les méthodes de **IWMWriterFileSink** et **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="ef392-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="ef392-125">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="ef392-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="ef392-126">Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et gère plusieurs fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="ef392-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="ef392-127">L’interface de rappel suivante doit être implémentée par l’application pour suivre la progression d’un objet récepteur de fichiers de writer.</span><span class="sxs-lookup"><span data-stu-id="ef392-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="ef392-128">Interface</span><span class="sxs-lookup"><span data-stu-id="ef392-128">Interface</span></span>                                      | <span data-ttu-id="ef392-129">Description</span><span class="sxs-lookup"><span data-stu-id="ef392-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ef392-130">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="ef392-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="ef392-131">Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="ef392-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ef392-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef392-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef392-133">**Objets**</span><span class="sxs-lookup"><span data-stu-id="ef392-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="ef392-134">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="ef392-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




