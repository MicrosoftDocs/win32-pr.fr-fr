---
title: Démarrage d’un écouteur DVC
description: Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311320"
---
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="6336d-103">Démarrage d’un écouteur DVC</span><span class="sxs-lookup"><span data-stu-id="6336d-103">Starting a DVC Listener</span></span>

<span data-ttu-id="6336d-104">Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.</span><span class="sxs-lookup"><span data-stu-id="6336d-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="6336d-105">L’instanciation d’un écouteur se produit généralement dans la méthode [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) du plug-in DVC.</span><span class="sxs-lookup"><span data-stu-id="6336d-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="6336d-106">Toutefois, l’instanciation n’est pas limitée à la méthode **Initialize** et peut être démarrée à tout moment de l’exécution du plug-in.</span><span class="sxs-lookup"><span data-stu-id="6336d-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="6336d-107">L’écouteur est décrit par l’interface [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) qui est instanciée par le [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="6336d-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="6336d-108">Une instance du gestionnaire de canaux est passée au plug-in au point d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="6336d-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="6336d-109">Le plug-in peut conserver une référence interne à l’instance aussi longtemps qu’elle en a besoin.</span><span class="sxs-lookup"><span data-stu-id="6336d-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="6336d-110">Un plug-in peut instancier autant d’écouteurs que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6336d-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="6336d-111">Toute connexion entrante sera gérée par [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), qui est fourni dans la méthode [**createListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="6336d-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="6336d-112">Pour obtenir un exemple, consultez l’implémentation de **CDVCSamplePlugin :: Initialize** dans l’exemple de code du [plug-in du client DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="6336d-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




