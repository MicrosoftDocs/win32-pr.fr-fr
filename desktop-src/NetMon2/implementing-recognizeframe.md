---
description: Les analyses réseau appellent la fonction RecognizeFrame d’un analyseur pour déterminer que l’analyseur reconnaît les données non réclamées d’une trame.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implémentation de RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890493"
---
# <a name="implementing-recognizeframe"></a>Implémentation de RecognizeFrame

Les analyses réseau appellent la fonction [**RecognizeFrame**](recognizeframe.md) d’un analyseur pour déterminer que l’analyseur reconnaît les données non réclamées d’une trame. Les données non réclamées peuvent se trouver au début d’une image, mais en général, les données non réclamées se trouvent au milieu d’une trame. L’illustration suivante montre les données inutilisées situées au milieu d’une trame.

![données libérées situées au milieu d’une trame](images/recognizeframe1.png)

Moniteur réseau fournit les informations suivantes quand il appelle la fonction [**RecognizeFrame**](recognizeframe.md) :

-   Handle du frame.
-   Pointeur vers le début du frame.
-   Pointeur vers le début des données inrécupérées.
-   Valeur MAC du premier protocole dans le frame.
-   Nombre d’octets dans les données inrécupérées ; autrement dit, les octets restants dans le frame.
-   Handle du protocole précédent.
-   Offset du protocole précédent.

Lorsque la DLL de l’analyseur détermine que les données non réclamées commencent par le protocole de l’analyseur, la DLL de l’analyseur détermine l’emplacement de démarrage du protocole suivant et le protocole qui suit. La DLL de l’analyseur fonctionne de la façon suivante :

-   Si la DLL de l’analyseur reconnaît des données non réclamées, la DLL de l’analyseur définit le paramètre *pProtocolStatus* et retourne un pointeur vers le protocole suivant dans le frame ou la **valeur null**. La **valeur null** est retournée si le protocole actuel est le dernier protocole dans le frame.
-   Si la DLL de l’analyseur reconnaît les données non réclamées et identifie le protocole qui suit (à partir des informations fournies dans le protocole), la DLL de l’analyseur retourne un pointeur vers le descripteur du protocole suivant dans le paramètre *phNextProtocol* de la fonction.
-   Si la DLL de l’analyseur ne reconnaît pas les données non réclamées, la DLL de l’analyseur retourne le pointeur au début des données non réclamées et Moniteur réseau continue d’analyser les données non réclamées.

**Pour implémenter RecognizeFrame**

1.  Testez pour déterminer que vous avez reconnu le protocole.
2.  Si vous reconnaissez des données non réclamées et que vous connaissez le protocole qui suit, définissez *pProtocolStatus* sur protocole \_ Status \_ Next \_ Protocol, définissez *phNextProtocol* sur un pointeur qui pointe vers le handle pour le protocole suivant, puis renvoyez un pointeur vers le protocole suivant.

    –ou–

    Si vous reconnaissez des données non réclamées et que vous ne connaissez pas le protocole qui suit, affectez à *pProtocolStatus* la valeur État de protocole \_ \_ reconnu, puis renvoyez un pointeur au protocole suivant.

    –ou–

    Si vous reconnaissez des données non réclamées et que votre protocole est le dernier protocole d’une trame, définissez *pProtocolStatus* sur l’état du protocole \_ \_ revendiqué, puis retournez la **valeur null**.

    –ou–

    Si vous ne reconnaissez pas les données non réclamées, affectez à *pProtocolStatus* la valeur État du protocole \_ \_ non \_ reconnu, puis renvoyez le pointeur qui vous est transmis dans *pProtocol*.

Voici une implémentation de base de [**RecognizeFrame**](recognizeframe.md).

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



