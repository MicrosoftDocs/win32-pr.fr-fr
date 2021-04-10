---
title: API clientes DVC
description: Les API clientes de canal virtuel dynamique (DVC) sont implémentées spécifiquement pour le client Connexion Bureau à distance (RDC) de la connexion.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309782"
---
# <a name="dvc-client-apis"></a>API clientes DVC

Les API clientes de canal virtuel dynamique (DVC) sont implémentées spécifiquement pour le client Connexion Bureau à distance (RDC) de la connexion. Certaines API sont implémentées par l’infrastructure DVC, et certaines sont implémentées par le développeur du plug-in. Certaines API sont utilisées pour prendre en charge le plug-in client Connexion Bureau à distance (RDC) et ne sont pas directement liées au transport de données.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Autorise le chargement du plug-in client Connexion Bureau à distance (RDC) par le client Connexion Bureau à distance (RDC).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Gère les paramètres de configuration pour chaque écouteur de la connexion de canal virtuel dynamique (DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Permet d’informer le plug-in client Connexion Bureau à distance (RDC) des demandes entrantes sur un écouteur particulier.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Gère tous les plug-ins client Connexion Bureau à distance (RDC) et les écouteurs de canal virtuel dynamique (DVC).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Utilisé pour contrôler l’état du canal et écrit sur le canal.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Reçoit des notifications sur les modifications de l’état du canal ou les données reçues.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Cette interface n’est pas prise en charge.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Appelé pour que le plug-in crée une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.

</dd> </dl>

 

 




