---
description: Windows Sockets (Winsock) et les fonctionnalités de multidiffusion et de multipoint indépendantes des protocoles.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multidiffusion et multipoint dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f6e7176d9b64ac8c7ef339ee82b8252e2a0d466dd8709fa008363ec3ef954e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993619"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multidiffusion et multipoint dans le SPI

tout comme Windows sockets 2 permet d’accéder aux fonctionnalités de transport de données de base de nombreux protocoles de transport de manière générique, il fournit également un moyen générique d’utiliser les fonctionnalités multipoint et de multidiffusion des transports qui implémentent ces fonctionnalités. Pour simplifier, le terme *multipoint* est utilisé ci-après pour faire référence aux communications multidiffusion et multipoint.

Les implémentations multipoint actuelles (par exemple, multidiffusion IP, ST-II, T. 120, ATM UNI) varient largement en ce qui concerne la façon dont les nœuds rejoignent une session multipoint, si un nœud particulier est désigné comme nœud racine ou racine et si les données sont échangées entre tous les nœuds ou uniquement entre un nœud racine et différents nœuds terminaux. Windows la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sockets 2 est utilisée pour déclarer les attributs multipoint d’un protocole. En examinant ces attributs, le programmeur connaîtra les conventions à suivre pour utiliser les fonctions Winsock applicables afin de configurer, d’utiliser et de détruire les sessions multipoint.

les fonctionnalités de Windows sockets 2 qui prennent en charge la multidiffusion peuvent être résumées comme suit :

-   Trois bits d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatre indicateurs définis pour le paramètre *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Une fonction, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint.
-   Deux codes de commande [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) pour le contrôle de bouclage multipoint et l’établissement de l’étendue des transmissions par multidiffusion. (Ce dernier correspond au paramètre de durée de vie et de durée de vie de la multidiffusion IP.)

> [!Note]  
> l’inclusion de ces fonctionnalités multipoint dans Windows sockets 2 n’empêche pas un fournisseur de services de prendre en charge également une interface existante dépendante du protocole, telle que les options de socket Deering pour la multidiffusion IP.

 

 

 
