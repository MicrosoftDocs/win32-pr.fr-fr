---
title: Écriture de données à l’aide d’un canal DVC
description: L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011016"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Écriture de données à l’aide d’un canal DVC

L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client. L’écriture des données de canal est implémentée par la méthode [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) de l’interface [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .

L’illustration suivante montre l’envoi et la réception du paquet de données entre le client et le serveur DVC (plug-in DVC).

![envoi et réception d’un paquet de données entre le client et le serveur DVC](images/writedvcchannel.png)

 

 




