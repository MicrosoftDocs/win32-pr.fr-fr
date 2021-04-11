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
# <a name="start-sequence"></a><span data-ttu-id="4a9cb-103">Séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="4a9cb-103">Start Sequence</span></span>

<span data-ttu-id="4a9cb-104">Pour démarrer votre fournisseur de protocole, le service Services Bureau à distance :</span><span class="sxs-lookup"><span data-stu-id="4a9cb-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="4a9cb-105">Récupère le nom de l’écouteur et le CLSID de votre objet de gestionnaire de protocole ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="4a9cb-106">Pour plus d’informations, consultez [inscription du gestionnaire de protocoles](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="4a9cb-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="4a9cb-107">Appelle [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) pour initialiser le gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="4a9cb-108">Crée un objet de gestionnaire de protocole à l’aide du CLSID.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="4a9cb-109">Même s’il existe plusieurs écouteurs inscrits pour le même fournisseur de protocole, le service ne crée qu’un seul objet de gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="4a9cb-110">Appelle [**createListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) pour indiquer à l’objet de gestionnaire de protocole de créer un objet écouteur [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) et le retourner au service.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="4a9cb-111">L’objet de gestionnaire de protocole doit ajouter une référence à l’objet d’écouteur avant de le retourner au service.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="4a9cb-112">Le service libère l’objet lorsque le service s’arrête ou que l’écouteur est supprimé.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="4a9cb-113">Appelle [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) sur l’objet de l’écouteur afin que l’écouteur puisse commencer à écouter les connexions entrantes.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="4a9cb-114">Appelle [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) pour empêcher l’écoute de l’objet de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="4a9cb-115">Appelle [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) pour ne pas initialiser le gestionnaire de protocoles.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="4a9cb-116">L’écouteur crée un objet [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) lorsqu’un client essaie de se connecter.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="4a9cb-117">L’objet écouteur appelle [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) pour notifier au service Services Bureau à distance qu’un nouveau client tente de se connecter ou se reconnecter et passe l’objet **IWRdsProtocolConnection** dans cet appel.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="4a9cb-118">Le service Services Bureau à distance retourne à son tour un objet [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) dans cet appel afin que le protocole puisse communiquer avec le service Services Bureau à distance en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="4a9cb-119">Le service ajoute une référence à l’objet de rappel avant de retourner, et le protocole doit libérer cette référence lorsque la connexion se ferme.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="4a9cb-120">L’illustration suivante montre l’interaction entre les différents objets au démarrage.</span><span class="sxs-lookup"><span data-stu-id="4a9cb-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![séquence de démarrage du RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="4a9cb-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a9cb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a9cb-123">Séquence d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="4a9cb-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="4a9cb-124">Séquence de connexion</span><span class="sxs-lookup"><span data-stu-id="4a9cb-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




