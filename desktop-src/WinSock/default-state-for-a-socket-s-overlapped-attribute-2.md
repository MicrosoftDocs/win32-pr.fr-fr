---
description: La fonction Socket a créé des sockets avec l’attribut Overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: État par défaut de l’attribut Overlapped d’un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113087"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>État par défaut de l’attribut Overlapped d’un socket

La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) a créé des sockets avec l’attribut Overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows sockets 1,1. Pour garantir la compatibilité descendante avec les implémentations de Wsock32.dll actuellement déployées, cela continuera d’être le cas pour Windows Sockets 2 également. Autrement dit, dans Windows Sockets 2, les sockets créés avec la fonction **Socket** auront l’attribut Overlapped. Toutefois, pour être plus compatible avec le reste de l’API Windows, les sockets créés avec [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ne sont pas, par défaut, dotés de l’attribut Overlapped. Cet attribut sera appliqué uniquement si le bit de \_ chevauchement de l’indicateur WSA \_ est défini.

 

 



