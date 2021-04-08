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
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web

La procédure et les exemples de code suivants illustrent les étapes permettant d’implémenter des canaux virtuels scriptables avec Connexion Bureau à distance par le Web. Les exemples ont été écrits en Visual Basic Scripting Edition et supposent que le contrôle ActiveX Bureau à distance est nommé « MsRdpClient ».

**Pour créer et déployer des canaux virtuels scriptables**

1.  Déployez le côté serveur de l’application et assurez-vous qu’il s’exécute sur le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance). Pour plus d’informations sur le déploiement d’applications de canaux virtuels sur le serveur, consultez [application de serveur de canal virtuel](virtual-channel-server-application.md).
2.  Dans votre script client, appelez [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md), en passant une chaîne qui contient une liste séparée par des virgules de noms de canaux virtuels.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Pour plus d’informations sur les restrictions de nom de canal virtuel, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md).

3.  Appelez [**IMsTscAx :: Connect**](imstscax-connect.md) pour créer votre connexion services Bureau à distance.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Utilisez la méthode [**IMsTscAx :: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) pour envoyer des données au serveur, en passant une chaîne qui contient le nom du canal virtuel et une deuxième chaîne qui contient les données à passer.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Recevoir des données du serveur sur l’événement [**IMsTscAxEvents :: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




