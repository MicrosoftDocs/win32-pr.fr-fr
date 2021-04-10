---
title: Objet récepteur push de l’enregistreur
description: Objet récepteur push de l’enregistreur
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK, objets récepteurs push de l’enregistreur
- ASF (Advanced Systems Format), objets récepteurs push de l’enregistreur
- ASF (format des systèmes avancés), objets récepteurs push de l’enregistreur
- objets, rédacteurs, objets récepteurs Push
- objets de récepteur push du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940675"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="ceb4a-108">Objet récepteur push de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="ceb4a-108">Writer Push Sink Object</span></span>

<span data-ttu-id="ceb4a-109">L’objet récepteur push du writer distribue les médias numériques aux points de publication.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="ceb4a-110">Par exemple, un concert en direct peut être encodé par un serveur unique, puis remis, ou *poussé*, à plusieurs autres serveurs qui diffusent en réalité le contenu aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="ceb4a-111">Un objet récepteur push du writer est créé par la fonction [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), qui définit un pointeur vers une interface **IWMWriterPushSink** .</span><span class="sxs-lookup"><span data-stu-id="ceb4a-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="ceb4a-112">Les autres interfaces prises en charge par l’objet, énumérées dans le tableau suivant, peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ceb4a-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="ceb4a-113">Interface</span><span class="sxs-lookup"><span data-stu-id="ceb4a-113">Interface</span></span>                                          | <span data-ttu-id="ceb4a-114">Description</span><span class="sxs-lookup"><span data-stu-id="ceb4a-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb4a-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="ceb4a-116">Permet à l’application d’afficher des messages d’État à partir de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="ceb4a-117">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="ceb4a-118">Gère une session de distribution push.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="ceb4a-119">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="ceb4a-120">Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et expose plusieurs fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="ceb4a-121">L’interface de rappel suivante peut être implémentée par l’application pour suivre la progression d’un objet récepteur push de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="ceb4a-122">Interface</span><span class="sxs-lookup"><span data-stu-id="ceb4a-122">Interface</span></span>                                      | <span data-ttu-id="ceb4a-123">Description</span><span class="sxs-lookup"><span data-stu-id="ceb4a-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb4a-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="ceb4a-125">Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="ceb4a-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ceb4a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ceb4a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb4a-127">**Objets**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="ceb4a-128">**Envoi de données ASF à un point de publication**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="ceb4a-129">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="ceb4a-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




