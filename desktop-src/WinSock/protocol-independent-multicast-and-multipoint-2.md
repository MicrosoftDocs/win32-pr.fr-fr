---
description: Windows Sockets 2 fournit une méthode générique pour l’utilisation des fonctionnalités multipoint et de multidiffusion des transports.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multidiffusion et multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238949f017c2ecb910b533d12a809aa1c04af02e64d08aa0ef4e8d4f3d39b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857901"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent multidiffusion et multipoint

Windows Sockets 2 fournit une méthode générique pour l’utilisation des fonctionnalités multipoint et de multidiffusion des transports. Cette méthode générique implémente ces fonctionnalités de la même manière qu’elle permet d’accéder aux fonctionnalités de transport de données de base de nombreux protocoles de transport. Le terme multipoint, est utilisé ci-après pour faire référence aux communications multidiffusion et multipoint.

Les implémentations multipoint actuelles (par exemple, multidiffusion IP, ST-II, T. 120 et ATM UNI) varient considérablement. Comment les nœuds rejoignent une session multipoint, si un nœud particulier est désigné comme nœud central ou racine, et si les données sont échangées entre tous les nœuds ou uniquement entre un nœud racine et les différents nœuds terminaux diffèrent entre les implémentations. la structure [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour Windows sockets 2 est utilisée pour déclarer les différents attributs multipoint d’un protocole. en examinant ces attributs, le programmeur sait quelles conventions suivre avec les fonctions Windows sockets 2 applicables pour configurer, utiliser et détruire les sessions multipoint.

Voici un résumé des fonctionnalités Winsock qui prennent en charge multipoint :

-   Bits à deux attributs dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatre indicateurs définis pour le paramètre *dwFlags* de la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Une fonction, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint
-   Deux codes de commande [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour le contrôle du bouclage multipoint et l’établissement de l’étendue des transmissions par multidiffusion. (Ce dernier correspond au paramètre de durée de vie et de durée de vie de la multidiffusion IP.)

> [!Note]  
> l’inclusion de ces fonctionnalités multipoint dans Windows sockets 2 n’empêche pas une application d’utiliser une interface existante dépendante du protocole, telle que les options de socket Deering pour la multidiffusion IP.

 

pour plus d’informations sur la façon dont les différents schémas multipoint sont caractérisés et sur la façon dont les fonctionnalités applicables de Windows sockets 2 sont utilisées, consultez [sémantique multipoint et Multicast](multipoint-and-multicast-semantics-2.md) .

 

 
