---
title: Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web
description: Exemples de code qui illustrent les étapes d’implémentation de canaux virtuels scriptables avec Connexion Bureau à distance par le Web.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674345"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="f4137-103">Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="f4137-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="f4137-104">La procédure et les exemples de code suivants illustrent les étapes permettant d’implémenter des canaux virtuels scriptables avec Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="f4137-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="f4137-105">Les exemples ont été écrits en Visual Basic Scripting Edition et supposent que le contrôle ActiveX Bureau à distance est nommé « MsRdpClient ».</span><span class="sxs-lookup"><span data-stu-id="f4137-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="f4137-106">**Pour créer et déployer des canaux virtuels scriptables**</span><span class="sxs-lookup"><span data-stu-id="f4137-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="f4137-107">Déployez le côté serveur de l’application et assurez-vous qu’il s’exécute sur le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="f4137-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="f4137-108">Pour plus d’informations sur le déploiement d’applications de canaux virtuels sur le serveur, consultez [application de serveur de canal virtuel](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="f4137-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="f4137-109">Dans votre script client, appelez [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md), en passant une chaîne qui contient une liste séparée par des virgules de noms de canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f4137-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="f4137-110">Pour plus d’informations sur les restrictions de nom de canal virtuel, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="f4137-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="f4137-111">Appelez [**IMsTscAx :: Connect**](imstscax-connect.md) pour créer votre connexion services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4137-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="f4137-112">Utilisez la méthode [**IMsTscAx :: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) pour envoyer des données au serveur, en passant une chaîne qui contient le nom du canal virtuel et une deuxième chaîne qui contient les données à passer.</span><span class="sxs-lookup"><span data-stu-id="f4137-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="f4137-113">Recevoir des données du serveur sur l’événement [**IMsTscAxEvents :: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .</span><span class="sxs-lookup"><span data-stu-id="f4137-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




