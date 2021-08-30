---
title: Acceptation d’une connexion (Services Bureau à distance)
description: À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1747354f540db8b50aff23fa5dc8ad23289b11c7a003e8281b72c8f8c174fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099651"
---
# <a name="accepting-a-connection-remote-desktop-services"></a>Acceptation d’une connexion (Services Bureau à distance)

À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC. Lorsque cela se produit, l’écouteur peut générer un canal de communication unique vers le client, qui est géré par la méthode [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback). Pour obtenir un exemple, consultez l’implémentation de **CDVCSamplePlugin :: OnNewChannelConnection** dans l’exemple de code du [plug-in client DVC](dvc-client-plug-in-example.md) .

La figure ci-dessous illustre la séquence d’événements permettant d’établir une connexion DVC. Les objets ombrés sont fournis par l’utilisateur (application/service DVC et [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), tandis que les objets non ombrés font partie de l’infrastructure (Bureau à distance service hôte de session Bureau à distance), écouteur et [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).

![séquence d’événements pour l’établissement d’une connexion DVC](images/acceptingconnection.png)

> [!Note]  
> Cette figure suppose qu’un objet écouteur a été créé via un appel [**createListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) à [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), et que le plug-in a spécifié [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) comme paramètre.

 

 

 




