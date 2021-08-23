---
description: Connecter et communiquer avec une carte à puce spécifique.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Fonctions d’accès aux lecteurs et aux cartes à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b571764ae2d31865082e823996e8cc1ecde9d9d3e2dd618f28e528fd465a567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917954"
---
# <a name="smart-card-and-reader-access-functions"></a>Fonctions d’accès aux lecteurs et aux cartes à puce

Les fonctions suivantes se connectent à une carte à [*puce*](../secgloss/s-gly.md)spécifique et la communiquent avec celle-ci. Les opérations d’e/s vers la carte utilisent une mémoire tampon pour l’envoi ou la réception de données et une structure qui contient des informations de contrôle de protocole. La structure des informations de contrôle de protocole commence toujours par une structure de [**\_ \_ demande d’e/s**](scard-io-request.md) inactive.



| Rubrique                                                  | Description                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Connecter à une carte.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Rétablissez une connexion.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Mettre fin à une connexion.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Démarrer une [*transaction*](../secgloss/t-gly.md), empêchant les autres applications d’accéder à une carte.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Mettre fin à une transaction, ce qui permet à d’autres applications d’accéder à une carte.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Indiquez l’état actuel du lecteur.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Demande le service et reçoit des données à partir d’une carte à l’aide de [*t = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)et des protocoles bruts. |



 

 

 
