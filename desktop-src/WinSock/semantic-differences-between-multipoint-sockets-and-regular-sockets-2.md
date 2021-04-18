---
title: Différences sémantiques entre les sockets multipoint et les sockets standard
description: Différences entre \_ les sockets multipoint racine c et les sockets point à point standard.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533626"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Différences sémantiques entre les sockets multipoint et les sockets standard

Dans le plan de contrôle, il existe des différences sémantiques significatives entre un \_ Socket racine c et un socket point à point standard :

-   Le \_ Socket racine c peut être utilisé dans [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour joindre une nouvelle feuille.
-   Le fait de placer un \_ Socket racine c en mode d’écoute (en appelant [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) n’empêche pas le \_ Socket racine c d’être utilisé dans un appel à [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter une nouvelle feuille, ou pour envoyer et recevoir des données multipoint.
-   La fermeture d’un \_ Socket racine c amène tous les \_ sockets de feuille c associés à obtenir une \_ notification FD Close.

Il n’existe aucune différence sémantique entre un \_ Socket feuille c et un socket standard dans le plan de contrôle, sauf que le \_ Socket feuille c peut être utilisé dans [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)et que l’utilisation du \_ Socket feuille c dans [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indique que seules les demandes de connexion multipoint doivent être acceptées.

Dans le plan de données, les différences sémantiques entre le \_ Socket racine d et un socket point à point standard sont les suivantes :

-   Les données envoyées sur le \_ Socket racine d sont remises à tous les feuilles de la même session multipoint.
-   Les données reçues sur le \_ Socket racine d peuvent provenir de n’importe lequel des feuilles.

Le \_ Socket de feuille d dans le plan de données enraciné n’a pas de différence sémantique par rapport au socket normal. Toutefois, dans le plan de données non enraciné, les données envoyées sur le \_ Socket feuille d sont envoyées à tous les autres nœuds terminaux, et les données reçues peuvent provenir de n’importe quel autre nœud feuille. Comme nous l’avons vu précédemment, les informations indiquant si le \_ Socket feuille d se trouve dans un plan de données associé ou non dans la racine sont contenues dans la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante pour le Socket.

 

 
