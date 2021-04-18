---
description: Il existe plusieurs attributs de socket qui peuvent être indiqués par le biais du paramètre flags dans WSPSocket.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Indicateurs et modes d’attribut de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da1a5f621a7d9f489f4e91782462c215659772b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536186"
---
# <a name="socket-attribute-flags-and-modes"></a>Indicateurs et modes d’attribut de socket

Il existe plusieurs attributs de socket qui peuvent être indiqués par le biais du paramètre *Flags* dans [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). L' \_ indicateur de \_ chevauchement d’indicateur WSA indique qu’un socket sera utilisé pour les opérations d’e/s avec chevauchement. La prise en charge de cet attribut est obligatoire pour tous les fournisseurs de services. Pour plus d’informations, consultez [e/s avec chevauchement](overlapped-i-o-2.md) . Notez que la création d’un socket avec l’attribut Overlapped n’a aucun impact sur le fait qu’un socket est actuellement en mode blocage ou non bloquant. Les sockets créés avec l’attribut Overlapped peuvent être utilisés pour effectuer des e/s avec chevauchement, et cela ne modifie pas le mode de blocage d’un Socket. Étant donné que les opérations d’e/s avec chevauchement ne sont pas bloquées, le mode de blocage d’un socket n’est pas pertinent pour ces opérations.

Quatre indicateurs d’attribut supplémentaires sont utilisés lors de la création de sockets à utiliser pour les opérations multipoint et/ou de multidiffusion, et la prise en charge de ces attributs est facultative. Les fournisseurs qui prennent en charge les attributs multipoint l’indiquent par le biais du \_ bit XP1 prise en charge \_ multipoint dans leurs structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) respectives. Pour connaître la définition et l’utilisation de chacun de ces indicateurs, consultez [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) et [multidiffusion indépendante du protocole et multipoint dans l’API](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) . Seuls les sockets créés avec des attributs multipoint peuvent être utilisés dans la fonction [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour la création de sessions multipoint.

Un socket est dans l’un des deux modes, bloquant et non bloquant, à tout moment. Les sockets sont créés en mode blocage par défaut et peuvent être modifiés en mode non bloquant en appelant [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)). Un socket peut être rétabli en mode blocage à l’aide de **WSPIoctl** si aucun **WSPAsyncSelect** ou **WSPEventSelect** n’est actif. Le mode d’un socket affecte uniquement les fonctions qui peuvent se bloquer et n’affecte pas les opérations d’e/s avec chevauchement. Pour plus d’informations, consultez [opérations de blocage](blocking-operations-2.md) .

 

 
