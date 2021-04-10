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
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="6e4f4-103">Protocol-Independent multidiffusion et multipoint dans le SPI</span><span class="sxs-lookup"><span data-stu-id="6e4f4-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="6e4f4-104">Tout comme Windows Sockets 2 permet d’accéder de façon générique aux fonctionnalités de transport de données de base de nombreux protocoles de transport, il offre également un moyen générique d’utiliser les fonctionnalités multipoint et de multidiffusion des transports qui implémentent ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="6e4f4-105">Pour simplifier, le terme *multipoint* est utilisé ci-après pour faire référence aux communications multidiffusion et multipoint.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="6e4f4-106">Les implémentations multipoint actuelles (par exemple, multidiffusion IP, ST-II, T. 120, ATM UNI) varient largement en ce qui concerne la façon dont les nœuds rejoignent une session multipoint, si un nœud particulier est désigné comme nœud racine ou racine et si les données sont échangées entre tous les nœuds ou uniquement entre un nœud racine et différents nœuds terminaux.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="6e4f4-107">La structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Windows Sockets 2 est utilisée pour déclarer les attributs multipoint d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="6e4f4-108">En examinant ces attributs, le programmeur connaîtra les conventions à suivre pour utiliser les fonctions Winsock applicables afin de configurer, d’utiliser et de détruire les sessions multipoint.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="6e4f4-109">Les fonctionnalités de Windows Sockets 2 qui prennent en charge la multidiffusion peuvent être résumées comme suit :</span><span class="sxs-lookup"><span data-stu-id="6e4f4-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="6e4f4-110">Trois bits d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="6e4f4-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="6e4f4-111">Quatre indicateurs définis pour le paramètre *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span><span class="sxs-lookup"><span data-stu-id="6e4f4-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="6e4f4-112">Une fonction, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="6e4f4-113">Deux codes de commande [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) pour le contrôle de bouclage multipoint et l’établissement de l’étendue des transmissions par multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="6e4f4-114">(Ce dernier correspond au paramètre de durée de vie et de durée de vie de la multidiffusion IP.)</span><span class="sxs-lookup"><span data-stu-id="6e4f4-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="6e4f4-115">L’inclusion de ces fonctionnalités multipoint dans Windows Sockets 2 n’empêche pas un fournisseur de services de prendre en charge également une interface existante dépendante du protocole, telle que les options de socket Deering pour la multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="6e4f4-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
