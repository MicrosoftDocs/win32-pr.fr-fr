---
description: Un processus peut surveiller un ensemble d’événements qui se produisent dans une ressource de communication. Par exemple, une application peut utiliser la surveillance des événements pour déterminer à quel moment les signaux CTS (Clear-to-Send) et DSR (Data-Set-Ready) signalent la modification de l’État.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Événements de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bcb257652723a2464ff66c862f574f6aeae621bc6459b55d250f785d0b0895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815489"
---
# <a name="communications-events"></a>Événements de communication

Un processus peut surveiller un ensemble d’événements qui se produisent dans une ressource de communication. Par exemple, une application peut utiliser la surveillance des événements pour déterminer à quel moment les signaux CTS (Clear-to-Send) et DSR (Data-Set-Ready) signalent la modification de l’État.

Un processus peut surveiller des événements sur une ressource de communication donnée à l’aide de la fonction [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) pour créer un masque d’événement. Pour déterminer le masque d’événement actuel d’une ressource de communication, un processus peut utiliser la fonction [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) . Les valeurs suivantes spécifient les événements qui peuvent être analysés.



| Valeur           | Signification                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_interruption ev**   | Un arrêt a été détecté sur l'entrée.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | Le signal CTS (Clear-to-Send) a changé d’État.                                                                                                                                                                                                     |
| **\_DSR ev**     | L’état du signal DSR (Data-Set-Ready) a changé.                                                                                                                                                                                                    |
| **EV \_ Err**     | Une erreur d’état de ligne s’est produite. Les erreurs d’état de ligne sont les **\_ trames ce**, le **\_ dépassement ce** et le **\_ RXPARITY ce**.                                                                                                                                        |
| **\_anneau ev**    | Un indicateur de tonalité a été détecté.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | Le signal RLSD (Receive-Line-signal-Detect) a changé d’État.                                                                                                                                                                                       |
| **\_RXCHAR ev**  | Un caractère a été reçu et placé dans la mémoire tampon d’entrée.                                                                                                                                                                                          |
| **\_RXFLAG ev**  | Le caractère d’événement a été reçu et placé dans la mémoire tampon d’entrée. Le caractère d’événement est spécifié dans la structure [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) de l’appareil, qui est appliquée à un port série à l’aide de la fonction [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) . |
| **\_TXEMPTY ev** | Le dernier caractère de la mémoire tampon de sortie a été envoyé.                                                                                                                                                                                                 |



 

Une fois qu’un ensemble d’événements est spécifié, un processus utilise la fonction [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) pour attendre que l’un des événements se produise. **WaitCommEvent** peut être utilisé de façon synchrone ou en tant qu’opération avec chevauchement. Pour plus d’informations sur l’exécution d’une fonction sous la forme d’une opération avec chevauchement, consultez [Synchronization](/windows/desktop/Sync/synchronization).

Lorsque l’un des événements spécifiés dans le masque d’événement se produit, le processus termine l’opération d’attente et définit une variable de masque d’événement pour indiquer le type d’événement détecté. Si le [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) est appelé pour une ressource de communication alors qu’une attente est en attente pour cette ressource, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) retourne une erreur.

La fonction [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) détecte les événements qui se sont produits depuis le dernier appel à [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) ou **WaitCommEvent**. Par exemple, si vous spécifiez l’événement **ev \_ RXCHAR** comme un événement Wait-condition_recherche, un appel à **WaitCommEvent** est satisfait si la mémoire tampon d’entrée du pilote contient des caractères qui sont arrivés depuis le dernier appel à **WaitCommEvent** ou **SetCommMask**. Par conséquent, étant donné le pseudocode suivant, tous les caractères reçus entre T1 et T2 satisferont l’appel suivant à **WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Lors de la surveillance d’un événement qui se produit lorsqu’un signal (CTS, DSR, etc.) change d’État, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) signale la modification, mais pas l’état actuel. Pour interroger l’état actuel des signaux CTS (Clear-to-Send), DSR (Data-Set prêt), RLSD (Receive-Line-signal-Detect) et Ring Indicator, un processus peut utiliser la fonction [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) .

 

 
