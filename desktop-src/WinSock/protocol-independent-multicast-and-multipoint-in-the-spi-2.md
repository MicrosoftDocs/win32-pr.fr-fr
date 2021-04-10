---
description: Windows Sockets (Winsock) et les fonctionnalités de transport multipoint et multidiffusion indépendantes des protocoles.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multidiffusion et multipoint dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115059"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multidiffusion et multipoint dans le SPI

Tout comme Windows Sockets 2 permet d’accéder de façon générique aux fonctionnalités de transport de données de base de nombreux protocoles de transport, il offre également un moyen générique d’utiliser les fonctionnalités multipoint et de multidiffusion des transports qui implémentent ces fonctionnalités. Pour simplifier, le terme *multipoint* est utilisé ci-après pour faire référence aux communications multidiffusion et multipoint.

Les implémentations multipoint actuelles (par exemple, multidiffusion IP, ST-II, T. 120, ATM UNI) varient largement en ce qui concerne la façon dont les nœuds rejoignent une session multipoint, si un nœud particulier est désigné comme nœud racine ou racine et si les données sont échangées entre tous les nœuds ou uniquement entre un nœud racine et différents nœuds terminaux. La structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Windows Sockets 2 est utilisée pour déclarer les attributs multipoint d’un protocole. En examinant ces attributs, le programmeur connaîtra les conventions à suivre pour utiliser les fonctions Winsock applicables afin de configurer, d’utiliser et de détruire les sessions multipoint.

Les fonctionnalités de Windows Sockets 2 qui prennent en charge la multidiffusion peuvent être résumées comme suit :

-   Trois bits d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatre indicateurs définis pour le paramètre *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Une fonction, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint.
-   Deux codes de commande [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) pour le contrôle de bouclage multipoint et l’établissement de l’étendue des transmissions par multidiffusion. (Ce dernier correspond au paramètre de durée de vie et de durée de vie de la multidiffusion IP.)

> [!Note]  
> L’inclusion de ces fonctionnalités multipoint dans Windows Sockets 2 n’empêche pas un fournisseur de services de prendre en charge également une interface existante dépendante du protocole, telle que les options de socket Deering pour la multidiffusion IP.

 

 

 
