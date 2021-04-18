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
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="1a013-103">Différences sémantiques entre les sockets multipoint et les sockets standard</span><span class="sxs-lookup"><span data-stu-id="1a013-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="1a013-104">Dans le plan de contrôle, il existe des différences sémantiques significatives entre un \_ Socket racine c et un socket point à point standard :</span><span class="sxs-lookup"><span data-stu-id="1a013-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="1a013-105">Le \_ Socket racine c peut être utilisé dans [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour joindre une nouvelle feuille.</span><span class="sxs-lookup"><span data-stu-id="1a013-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="1a013-106">Le fait de placer un \_ Socket racine c en mode d’écoute (en appelant [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) n’empêche pas le \_ Socket racine c d’être utilisé dans un appel à [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter une nouvelle feuille, ou pour envoyer et recevoir des données multipoint.</span><span class="sxs-lookup"><span data-stu-id="1a013-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="1a013-107">La fermeture d’un \_ Socket racine c amène tous les \_ sockets de feuille c associés à obtenir une \_ notification FD Close.</span><span class="sxs-lookup"><span data-stu-id="1a013-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="1a013-108">Il n’existe aucune différence sémantique entre un \_ Socket feuille c et un socket standard dans le plan de contrôle, sauf que le \_ Socket feuille c peut être utilisé dans [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)et que l’utilisation du \_ Socket feuille c dans [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indique que seules les demandes de connexion multipoint doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="1a013-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="1a013-109">Dans le plan de données, les différences sémantiques entre le \_ Socket racine d et un socket point à point standard sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a013-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="1a013-110">Les données envoyées sur le \_ Socket racine d sont remises à tous les feuilles de la même session multipoint.</span><span class="sxs-lookup"><span data-stu-id="1a013-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="1a013-111">Les données reçues sur le \_ Socket racine d peuvent provenir de n’importe lequel des feuilles.</span><span class="sxs-lookup"><span data-stu-id="1a013-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="1a013-112">Le \_ Socket de feuille d dans le plan de données enraciné n’a pas de différence sémantique par rapport au socket normal. Toutefois, dans le plan de données non enraciné, les données envoyées sur le \_ Socket feuille d sont envoyées à tous les autres nœuds terminaux, et les données reçues peuvent provenir de n’importe quel autre nœud feuille.</span><span class="sxs-lookup"><span data-stu-id="1a013-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="1a013-113">Comme nous l’avons vu précédemment, les informations indiquant si le \_ Socket feuille d se trouve dans un plan de données associé ou non dans la racine sont contenues dans la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante pour le Socket.</span><span class="sxs-lookup"><span data-stu-id="1a013-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
