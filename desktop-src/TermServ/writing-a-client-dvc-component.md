---
title: Écriture d’un module DVC client
description: Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008262"
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

 

 





