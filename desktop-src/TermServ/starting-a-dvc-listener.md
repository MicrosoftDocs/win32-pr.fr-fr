---
title: Démarrage d’un écouteur DVC
description: Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000449"
---
# <a name="starting-a-dvc-listener"></a>Démarrage d’un écouteur DVC

Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.

L’instanciation d’un écouteur se produit généralement dans la méthode [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) du plug-in DVC. Toutefois, l’instanciation n’est pas limitée à la méthode **Initialize** et peut être démarrée à tout moment de l’exécution du plug-in. L’écouteur est décrit par l’interface [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) qui est instanciée par le [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Une instance du gestionnaire de canaux est passée au plug-in au point d’initialisation. Le plug-in peut conserver une référence interne à l’instance aussi longtemps qu’elle en a besoin.

Un plug-in peut instancier autant d’écouteurs que nécessaire. Toute connexion entrante sera gérée par [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), qui est fourni dans la méthode [**createListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Pour obtenir un exemple, consultez l’implémentation de **CDVCSamplePlugin :: Initialize** dans l’exemple de code du [plug-in du client DVC](dvc-client-plug-in-example.md) .

 

 




