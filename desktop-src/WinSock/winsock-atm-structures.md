---
description: La liste suivante fournit des descriptions concises de chaque structure Winsock ATM. Pour plus d’informations sur n’importe quelle structure, cliquez sur le nom de la structure.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Structures ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529715"
---
# <a name="winsock-atm-structures"></a>Structures ATM Winsock

La liste suivante fournit des descriptions concises de chaque structure Winsock ATM. Pour plus d’informations sur n’importe quelle structure, cliquez sur le nom de la structure.



| Structure ATM                           | Description                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**\_adresse ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Stocke les données d’adresse ATM pour les sockets ATM.             |
| [**\_BHLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifie les informations B-HLI pour un socket ATM associé. |
| [**\_BLLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifie les informations de B-LLI pour un socket ATM associé. |
| [**sockaddr \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Stocke les informations d’adresse de socket pour les sockets ATM.         |



 

Pour les services ATM natifs, utilisez \_ le DAB AF pour la famille d’adresses et la structure d’adresse de socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) . Pour ouvrir un socket ATM natif, transmettez AF- \_ ATM, chaussette \_ RAW, ATMPROTO \_ AAL5 ou ATMPROTO \_ AALUSER à la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivement.

 

 



