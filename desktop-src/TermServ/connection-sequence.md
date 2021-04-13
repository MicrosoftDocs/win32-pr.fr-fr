---
title: Séquence de connexion
description: Illustration qui montre les appels de méthode effectués entre le service Services Bureau à distance et votre protocole au cours de la séquence de connexion du client.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380289"
---
# <a name="connection-sequence"></a><span data-ttu-id="1974c-103">Séquence de connexion</span><span class="sxs-lookup"><span data-stu-id="1974c-103">Connection Sequence</span></span>

<span data-ttu-id="1974c-104">L’illustration suivante montre les appels de méthode effectués entre le service Services Bureau à distance et votre protocole au cours de la séquence de connexion du client.</span><span class="sxs-lookup"><span data-stu-id="1974c-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="1974c-105">Les actions présentées ici suivent la [séquence de démarrage](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="1974c-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="1974c-106">L’interaction entre le service et l’objet [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) représente le protocole de transfert de licences pour le client.</span><span class="sxs-lookup"><span data-stu-id="1974c-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![séquence de connexion du client](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="1974c-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1974c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1974c-109">Séquence d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="1974c-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="1974c-110">Séquence de reconnexion</span><span class="sxs-lookup"><span data-stu-id="1974c-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="1974c-111">Séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="1974c-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




