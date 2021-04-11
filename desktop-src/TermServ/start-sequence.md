---
title: Séquence de démarrage
description: Étapes de démarrage de votre protocole personnalisé.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190845"
---
# <a name="start-sequence"></a>Séquence de démarrage

Pour démarrer votre fournisseur de protocole, le service Services Bureau à distance :

-   Récupère le nom de l’écouteur et le CLSID de votre objet de gestionnaire de protocole ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) à partir du Registre. Pour plus d’informations, consultez [inscription du gestionnaire de protocoles](registering-the-custom-protocol.md).
-   Appelle [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) pour initialiser le gestionnaire de protocole.
-   Crée un objet de gestionnaire de protocole à l’aide du CLSID. Même s’il existe plusieurs écouteurs inscrits pour le même fournisseur de protocole, le service ne crée qu’un seul objet de gestionnaire de protocole.
-   Appelle [**createListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) pour indiquer à l’objet de gestionnaire de protocole de créer un objet écouteur [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) et le retourner au service. L’objet de gestionnaire de protocole doit ajouter une référence à l’objet d’écouteur avant de le retourner au service. Le service libère l’objet lorsque le service s’arrête ou que l’écouteur est supprimé.
-   Appelle [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) sur l’objet de l’écouteur afin que l’écouteur puisse commencer à écouter les connexions entrantes.
-   Appelle [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) pour empêcher l’écoute de l’objet de l’écouteur.
-   Appelle [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) pour ne pas initialiser le gestionnaire de protocoles.

L’écouteur crée un objet [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) lorsqu’un client essaie de se connecter. L’objet écouteur appelle [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) pour notifier au service Services Bureau à distance qu’un nouveau client tente de se connecter ou se reconnecter et passe l’objet **IWRdsProtocolConnection** dans cet appel. Le service Services Bureau à distance retourne à son tour un objet [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) dans cet appel afin que le protocole puisse communiquer avec le service Services Bureau à distance en fonction des besoins. Le service ajoute une référence à l’objet de rappel avant de retourner, et le protocole doit libérer cette référence lorsque la connexion se ferme.

L’illustration suivante montre l’interaction entre les différents objets au démarrage.

![séquence de démarrage du RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquence d’appel de méthode](method-call-sequence.md)
</dt> <dt>

[Séquence de connexion](connection-sequence.md)
</dt> </dl>

 

 




