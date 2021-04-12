---
description: Le protocole Kerberos est composé de trois sous-protocoles.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Sous-protocoles Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203179"
---
# <a name="kerberos-subprotocols"></a>Sous-protocoles Kerberos

Le [*protocole Kerberos*](../secgloss/k-gly.md) est composé de trois sous-protocoles.



| Sous-protocole                                                                         | Signification                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Échange de service d'authentification](authentication-service-exchange.md)<br/>   | Dans ce sous-protocole, le [*Centre de distribution de clés*](../secgloss/k-gly.md) (KDC) donne au client une [*clé de session*](../secgloss/s-gly.md) de connexion et un ticket TGT (Ticket-Granting Ticket).<br/> |
| [Échange de service TG (ticket-granting)](ticket-granting-service-exchange.md)<br/> | Dans ce sous-protocole, le centre de distribution de clés distribue une clé de session de service et un ticket pour le service.<br/>                                                                                                                                                                                                            |
| [Échange client/serveur](client-server-exchange.md)<br/>                     | Dans ce sous-protocole, le client présente le ticket d’admission à un service.<br/>                                                                                                                                                                                                                         |



 

 

 
