---
title: Objet récepteur réseau de l’enregistreur
description: Objet récepteur réseau de l’enregistreur
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK, objets récepteur réseau du scripteur
- ASF (Advanced Systems Format), objets récepteur réseau du writer
- ASF (format des systèmes avancés), objets du récepteur réseau de l’enregistreur
- objets, enregistreur réseau du récepteur
- objets du récepteur réseau du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101352"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="12f6e-108">Objet récepteur réseau de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="12f6e-108">Writer Network Sink Object</span></span>

<span data-ttu-id="12f6e-109">L’objet récepteur réseau du writer est utilisé pour écrire des médias numériques sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="12f6e-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="12f6e-110">L’objet récepteur réseau du writer est créé par la fonction [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), qui définit un pointeur vers une interface **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="12f6e-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="12f6e-111">Les autres interfaces de l’objet récepteur réseau du writer peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="12f6e-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="12f6e-112">Interface</span><span class="sxs-lookup"><span data-stu-id="12f6e-112">Interface</span></span>                                              | <span data-ttu-id="12f6e-113">Description</span><span class="sxs-lookup"><span data-stu-id="12f6e-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12f6e-114">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="12f6e-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="12f6e-115">Collecte des informations sur les clients connectés.</span><span class="sxs-lookup"><span data-stu-id="12f6e-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="12f6e-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="12f6e-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="12f6e-117">Récupère des informations sur le client avancé.</span><span class="sxs-lookup"><span data-stu-id="12f6e-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="12f6e-118">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="12f6e-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="12f6e-119">Permet à l’application d’afficher des messages d’État à partir de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12f6e-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="12f6e-120">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="12f6e-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="12f6e-121">Ouvre et ferme les ports, définit et récupère le nombre maximal de clients qui peuvent se connecter à l’objet récepteur, définit le protocole réseau à utiliser par l’objet Writer et effectue d’autres fonctions avancées.</span><span class="sxs-lookup"><span data-stu-id="12f6e-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="12f6e-122">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="12f6e-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="12f6e-123">Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et gère plusieurs fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="12f6e-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="12f6e-124">L’interface de rappel suivante peut être implémentée par l’application pour suivre la progression d’un objet récepteur réseau du writer.</span><span class="sxs-lookup"><span data-stu-id="12f6e-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="12f6e-125">Interface</span><span class="sxs-lookup"><span data-stu-id="12f6e-125">Interface</span></span>                                      | <span data-ttu-id="12f6e-126">Description</span><span class="sxs-lookup"><span data-stu-id="12f6e-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="12f6e-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="12f6e-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="12f6e-128">Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="12f6e-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12f6e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12f6e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f6e-130">**Diffusion de données ASF**</span><span class="sxs-lookup"><span data-stu-id="12f6e-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="12f6e-131">**Objets**</span><span class="sxs-lookup"><span data-stu-id="12f6e-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="12f6e-132">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="12f6e-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




