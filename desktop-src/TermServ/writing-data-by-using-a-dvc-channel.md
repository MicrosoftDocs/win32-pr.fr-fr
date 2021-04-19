---
title: Écriture de données à l’aide d’un canal DVC
description: L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511025"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="a6e44-103">Écriture de données à l’aide d’un canal DVC</span><span class="sxs-lookup"><span data-stu-id="a6e44-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="a6e44-104">L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client.</span><span class="sxs-lookup"><span data-stu-id="a6e44-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="a6e44-105">L’écriture des données de canal est implémentée par la méthode [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) de l’interface [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .</span><span class="sxs-lookup"><span data-stu-id="a6e44-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="a6e44-106">L’illustration suivante montre l’envoi et la réception du paquet de données entre le client et le serveur DVC (plug-in DVC).</span><span class="sxs-lookup"><span data-stu-id="a6e44-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![envoi et réception d’un paquet de données entre le client et le serveur DVC](images/writedvcchannel.png)

 

 




