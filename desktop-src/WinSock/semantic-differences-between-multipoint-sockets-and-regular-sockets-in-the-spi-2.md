---
description: différences entre les sockets point-à-point normaux et \_ les sockets multipoint racine c dans le SPI de Windows sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Différences sémantiques entre les sockets multipoint et les sockets standard dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e585c335d7503d884d58e25b6fc0ad6dd0c0c3356064ebb1504898770d4b7b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740607"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Différences sémantiques entre les sockets multipoint et les sockets standard dans le SPI

Dans le plan de contrôle, il existe des différences sémantiques significatives entre un \_ Socket racine c et un socket point à point standard :

-   Le \_ Socket racine c peut être utilisé dans [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour rejoindre une nouvelle feuille.
-   Le fait de placer un \_ Socket racine c dans le mode d’écoute (en appelant [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) n’empêche pas le \_ Socket racine c d’être utilisé dans un appel à [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour ajouter une nouvelle feuille, ou pour envoyer et recevoir des données multipoint.
-   La fermeture d’un \_ Socket racine c amène tous les \_ sockets de feuille c associés à obtenir la \_ notification FD Close.

Il n’existe aucune différence sémantique entre un \_ Socket feuille c et un socket standard dans le plan de contrôle, sauf que le \_ Socket feuille c peut être utilisé dans [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)et que l’utilisation du \_ Socket feuille c dans [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indique que seules les demandes de connexion multipoint doivent être acceptées.

Dans le plan de données, les différences sémantiques entre le \_ Socket racine d et un socket point à point standard sont

-   Les données envoyées sur le \_ Socket racine d seront remises à tous les feuilles de la même session multipoint.
-   Les données reçues sur le \_ Socket racine d peuvent provenir de n’importe lequel des feuilles.

Le \_ Socket de feuille d dans le plan de données enraciné n’a pas de différence sémantique par rapport au socket normal. Toutefois, dans le plan de données non enraciné, les données envoyées sur le \_ Socket de feuille d sont dirigées vers tous les autres nœuds terminaux, et les données reçues peuvent provenir de l’un des autres nœuds terminaux. Comme nous l’avons vu précédemment, les informations indiquant si le \_ Socket feuille d se trouve dans un plan de données associé ou non dans la racine sont contenues dans la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante pour le Socket.

 

 
