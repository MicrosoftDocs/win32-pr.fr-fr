---
title: Écriture d’un module DVC client
description: Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513673"
---
# <a name="writing-a-client-dvc-module"></a>Écriture d’un module DVC client

Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC). Le plug-in DVC est une implémentation de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), inscrite en tant qu’objet COM (Component Object Model).

> [!Note]  
> Le plug-in doit être implémenté dans un modèle de thread libre. L’implémentation du modèle cloisonné n’est pas prise en charge.

 

Voici une liste des interfaces implémentées par des objets instanciés par le plug-in.



| Interface                                                        | Description                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Autorise le chargement du plug-in client Connexion Bureau à distance (RDC) par le client Connexion Bureau à distance (RDC).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Avertit le plug-in client Connexion Bureau à distance (RDC) des demandes entrantes sur un écouteur particulier.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Reçoit des notifications sur les modifications de l’état du canal ou les données reçues. Chaque instance de cette interface est associée à une instance de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).<br/> |



 

Voici une liste des interfaces implémentées par des objets instanciés par le client Connexion Bureau à distance (RDC) et faisant partie de l’infrastructure.



| Interface                                                      | Description                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Gère tous les plug-ins client Connexion Bureau à distance (RDC), les écouteurs DVC ou les canaux virtuels statiques.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Gère les paramètres de configuration pour chaque écouteur de la connexion DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Contrôle l’état du canal, ainsi que les écritures sur le canal.<br/>                                           |



 

L’illustration suivante montre la relation entre le client Connexion Bureau à distance (RDC) et le plug-in client Connexion Bureau à distance (RDC).

![relation entre le client et le plug-in](images/tsclient.png)

 

 





