---
title: Vue d’ensemble des interfaces réseau
description: Vue d’ensemble des interfaces réseau
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK, interfaces réseau
- Windows Media Format SDK, interfaces
- ASF (Advanced Systems Format), interfaces réseau
- ASF (format des systèmes avancés), interfaces réseau
- ASF (Advanced Systems Format), liste d’interfaces pour les fonctionnalités de mise en réseau
- ASF (format de systèmes avancés), liste d’interfaces pour les fonctionnalités de mise en réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724130"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="22d3e-109">Vue d’ensemble des interfaces réseau</span><span class="sxs-lookup"><span data-stu-id="22d3e-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="22d3e-110">Les fonctionnalités de mise en réseau de ce kit de développement logiciel (SDK) sont prises en charge par les méthodes des interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="22d3e-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="22d3e-111">Interface</span><span class="sxs-lookup"><span data-stu-id="22d3e-111">Interface</span></span>                                                  | <span data-ttu-id="22d3e-112">Description</span><span class="sxs-lookup"><span data-stu-id="22d3e-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22d3e-113">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="22d3e-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="22d3e-114">Obtient des informations sur les clients connectés à un récepteur réseau.</span><span class="sxs-lookup"><span data-stu-id="22d3e-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="22d3e-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="22d3e-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="22d3e-116">Fournit une méthode pour obtenir des informations sur un client attaché à un récepteur réseau d’écriture.</span><span class="sxs-lookup"><span data-stu-id="22d3e-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="22d3e-117">Cette interface étend l’interface **IWMClientConnections** .</span><span class="sxs-lookup"><span data-stu-id="22d3e-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="22d3e-118">**IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="22d3e-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="22d3e-119">Fournit une méthode de rappel pour obtenir les informations d’identification de l’utilisateur lors de l’accès à un site distant.</span><span class="sxs-lookup"><span data-stu-id="22d3e-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="22d3e-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="22d3e-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="22d3e-121">Fournit des méthodes avancées sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="22d3e-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="22d3e-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="22d3e-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="22d3e-123">Étend l’interface **IWMReaderAdvanced2** .</span><span class="sxs-lookup"><span data-stu-id="22d3e-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="22d3e-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="22d3e-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="22d3e-125">Étend l’interface **IWMReaderAdvanced3** .</span><span class="sxs-lookup"><span data-stu-id="22d3e-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="22d3e-126">**IWMReaderNetworkConfig**</span><span class="sxs-lookup"><span data-stu-id="22d3e-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="22d3e-127">Configure les paramètres réseau sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="22d3e-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="22d3e-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="22d3e-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="22d3e-129">Configure des paramètres réseau supplémentaires sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="22d3e-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="22d3e-130">Cette interface étend l’interface **IWMReaderNetworkConfig** .</span><span class="sxs-lookup"><span data-stu-id="22d3e-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="22d3e-131">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="22d3e-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="22d3e-132">Configure l’objet récepteur réseau, qui est utilisé pour écrire des médias numériques sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="22d3e-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="22d3e-133">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="22d3e-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="22d3e-134">Configure l’objet récepteur push, qui est utilisé pour distribuer des médias numériques aux points de publication.</span><span class="sxs-lookup"><span data-stu-id="22d3e-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="22d3e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22d3e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22d3e-136">**Implémentation des fonctionnalités réseau**</span><span class="sxs-lookup"><span data-stu-id="22d3e-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




