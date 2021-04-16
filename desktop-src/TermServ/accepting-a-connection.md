---
title: Acceptation d’une connexion (Services Bureau à distance)
description: À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104556967"
---
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="b9d06-103">Acceptation d’une connexion (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="b9d06-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="b9d06-104">À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC.</span><span class="sxs-lookup"><span data-stu-id="b9d06-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="b9d06-105">Lorsque cela se produit, l’écouteur peut générer un canal de communication unique vers le client, qui est géré par la méthode [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span><span class="sxs-lookup"><span data-stu-id="b9d06-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="b9d06-106">Pour obtenir un exemple, consultez l’implémentation de **CDVCSamplePlugin :: OnNewChannelConnection** dans l’exemple de code du [plug-in client DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d06-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="b9d06-107">La figure ci-dessous illustre la séquence d’événements permettant d’établir une connexion DVC.</span><span class="sxs-lookup"><span data-stu-id="b9d06-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="b9d06-108">Les objets ombrés sont fournis par l’utilisateur (application/service DVC et [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), tandis que les objets non ombrés font partie de l’infrastructure (Bureau à distance service hôte de session Bureau à distance), écouteur et [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span><span class="sxs-lookup"><span data-stu-id="b9d06-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![séquence d’événements pour l’établissement d’une connexion DVC](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="b9d06-110">Cette figure suppose qu’un objet écouteur a été créé via un appel [**createListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) à [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), et que le plug-in a spécifié [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9d06-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




