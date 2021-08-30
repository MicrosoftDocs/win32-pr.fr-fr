---
description: la fonction socket a créé des sockets avec l’attribut overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: État par défaut de l’attribut Overlapped d’un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae64f5ba1481c62faf0798fa45aafdd98dde0696dfde68f79132d533ec3abce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860929"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>État par défaut de l’attribut Overlapped d’un socket

la fonction [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) a créé des sockets avec l’attribut overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows sockets 1,1. pour garantir la compatibilité descendante avec les implémentations de Wsock32.dll actuellement déployées, cela restera le cas pour Windows sockets 2 également. autrement dit, dans Windows sockets 2, les sockets créés avec la fonction **socket** auront l’attribut overlapped. toutefois, afin d’être plus compatible avec le reste de l’API Windows, les sockets créés avec [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ne sont pas, par défaut, dotés de l’attribut overlapped. Cet attribut sera appliqué uniquement si le bit de \_ chevauchement de l’indicateur WSA \_ est défini.

 

 



