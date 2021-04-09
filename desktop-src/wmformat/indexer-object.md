---
title: Indexeur (objet)
description: Indexeur (objet)
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK, objets indexer
- ASF (Advanced Systems Format), objets indexer
- ASF (format des systèmes avancés), objets indexer
- objets, indexeurs, objets
- objets indexer
- index, objets indexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104030917"
---
# <a name="indexer-object"></a><span data-ttu-id="690eb-109">Indexeur (objet)</span><span class="sxs-lookup"><span data-stu-id="690eb-109">Indexer Object</span></span>

<span data-ttu-id="690eb-110">L’objet indexeur crée un index dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="690eb-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="690eb-111">Un index est une partie standard d’un fichier ASF qui correspond à des échantillons de vidéos avec des heures, des numéros de trames ou (le cas échéant) de la société des horodatages standard d’image et de télévision (SMPTE).</span><span class="sxs-lookup"><span data-stu-id="690eb-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="690eb-112">Sans index, l’objet lecteur et l’objet lecteur synchrone ne peuvent pas Rechercher un point au milieu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="690eb-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="690eb-113">Les index créés par cet objet ne sont nécessaires que si le fichier contient un ou plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="690eb-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="690eb-114">Cela est dû au fait que les données audio ne sont pas compressées temporellement, ce qui permet de trouver facilement un moment donné dans un flux audio.</span><span class="sxs-lookup"><span data-stu-id="690eb-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="690eb-115">L’objet indexeur est créé par la fonction [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , qui définit un pointeur vers une interface **IWMIndexer** .</span><span class="sxs-lookup"><span data-stu-id="690eb-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="690eb-116">Les autres interfaces de l’objet indexeur peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="690eb-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="690eb-117">Les interfaces suivantes sont prises en charge par l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="690eb-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="690eb-118">Interface</span><span class="sxs-lookup"><span data-stu-id="690eb-118">Interface</span></span>                          | <span data-ttu-id="690eb-119">Description</span><span class="sxs-lookup"><span data-stu-id="690eb-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="690eb-120">**IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="690eb-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="690eb-121">Démarre et arrête le processus d’indexation.</span><span class="sxs-lookup"><span data-stu-id="690eb-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="690eb-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="690eb-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="690eb-123">Configure l’indexeur, en activant l’indexation par Frame, par heure ou par code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="690eb-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="690eb-124">L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="690eb-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="690eb-125">Interface</span><span class="sxs-lookup"><span data-stu-id="690eb-125">Interface</span></span>                                      | <span data-ttu-id="690eb-126">Description</span><span class="sxs-lookup"><span data-stu-id="690eb-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="690eb-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="690eb-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="690eb-128">Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="690eb-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="690eb-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="690eb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="690eb-130">**Objets**</span><span class="sxs-lookup"><span data-stu-id="690eb-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="690eb-131">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="690eb-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




