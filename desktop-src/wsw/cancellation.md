---
title: Annulation
description: La plupart des opérations dans WWSAPI peuvent être annulées pendant l’exécution.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Annuler les services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841779"
---
# <a name="cancellation"></a>Annulation

La plupart des opérations dans WWSAPI peuvent être annulées pendant l’exécution.

La fonction que vous utilisez pour annuler une opération dépend de l’objet affecté.

| Fonction                                           | Description                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Annule toutes les entrées et sorties en attente sur un canal spécifié et définit l’état du canal sur WS \_ Channel \_ State \_ Faulted. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Annule toutes les entrées et sorties en attente sur un écouteur spécifié.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Annule toutes les entrées et sorties en attente sur un proxy de service spécifié.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrompt et interrompt les opérations en cours sur l’hôte de service.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandonne un appel, un appel spécifié sur un proxy de service spécifié.                                                        |



 

Pour plus d’informations sur les annulations qui affectent les [opérations de service côté serveur](server-side-service-operations.md) et les rappels de modèle de service, consultez [appel d’annulation](call-cancellation.md).


 

 




