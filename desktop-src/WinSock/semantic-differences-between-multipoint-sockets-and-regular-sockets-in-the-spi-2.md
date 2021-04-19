---
description: Différences entre les sockets point à point standard et \_ les sockets multipoint racine c dans le SPI de Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Différences sémantiques entre les sockets multipoint et les sockets standard dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517613"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="38b23-103">Différences sémantiques entre les sockets multipoint et les sockets standard dans le SPI</span><span class="sxs-lookup"><span data-stu-id="38b23-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="38b23-104">Dans le plan de contrôle, il existe des différences sémantiques significatives entre un \_ Socket racine c et un socket point à point standard :</span><span class="sxs-lookup"><span data-stu-id="38b23-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="38b23-105">Le \_ Socket racine c peut être utilisé dans [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour rejoindre une nouvelle feuille.</span><span class="sxs-lookup"><span data-stu-id="38b23-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="38b23-106">Le fait de placer un \_ Socket racine c dans le mode d’écoute (en appelant [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) n’empêche pas le \_ Socket racine c d’être utilisé dans un appel à [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour ajouter une nouvelle feuille, ou pour envoyer et recevoir des données multipoint.</span><span class="sxs-lookup"><span data-stu-id="38b23-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="38b23-107">La fermeture d’un \_ Socket racine c amène tous les \_ sockets de feuille c associés à obtenir la \_ notification FD Close.</span><span class="sxs-lookup"><span data-stu-id="38b23-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="38b23-108">Il n’existe aucune différence sémantique entre un \_ Socket feuille c et un socket standard dans le plan de contrôle, sauf que le \_ Socket feuille c peut être utilisé dans [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)et que l’utilisation du \_ Socket feuille c dans [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indique que seules les demandes de connexion multipoint doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="38b23-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="38b23-109">Dans le plan de données, les différences sémantiques entre le \_ Socket racine d et un socket point à point standard sont</span><span class="sxs-lookup"><span data-stu-id="38b23-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="38b23-110">Les données envoyées sur le \_ Socket racine d seront remises à tous les feuilles de la même session multipoint.</span><span class="sxs-lookup"><span data-stu-id="38b23-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="38b23-111">Les données reçues sur le \_ Socket racine d peuvent provenir de n’importe lequel des feuilles.</span><span class="sxs-lookup"><span data-stu-id="38b23-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="38b23-112">Le \_ Socket de feuille d dans le plan de données enraciné n’a pas de différence sémantique par rapport au socket normal. Toutefois, dans le plan de données non enraciné, les données envoyées sur le \_ Socket de feuille d sont dirigées vers tous les autres nœuds terminaux, et les données reçues peuvent provenir de l’un des autres nœuds terminaux.</span><span class="sxs-lookup"><span data-stu-id="38b23-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="38b23-113">Comme nous l’avons vu précédemment, les informations indiquant si le \_ Socket feuille d se trouve dans un plan de données associé ou non dans la racine sont contenues dans la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante pour le Socket.</span><span class="sxs-lookup"><span data-stu-id="38b23-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
