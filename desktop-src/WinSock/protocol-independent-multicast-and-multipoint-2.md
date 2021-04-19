---
description: Windows Sockets 2 fournit une méthode générique pour l’utilisation des fonctionnalités multipoint et de multidiffusion des transports.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multidiffusion et multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527813"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="3fe6c-103">Protocol-Independent multidiffusion et multipoint</span><span class="sxs-lookup"><span data-stu-id="3fe6c-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="3fe6c-104">Windows Sockets 2 fournit une méthode générique pour l’utilisation des fonctionnalités multipoint et de multidiffusion des transports.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="3fe6c-105">Cette méthode générique implémente ces fonctionnalités de la même manière qu’elle permet d’accéder aux fonctionnalités de transport de données de base de nombreux protocoles de transport.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="3fe6c-106">Le terme multipoint, est utilisé ci-après pour faire référence aux communications multidiffusion et multipoint.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="3fe6c-107">Les implémentations multipoint actuelles (par exemple, multidiffusion IP, ST-II, T. 120 et ATM UNI) varient considérablement.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="3fe6c-108">Comment les nœuds rejoignent une session multipoint, si un nœud particulier est désigné comme nœud central ou racine, et si les données sont échangées entre tous les nœuds ou uniquement entre un nœud racine et les différents nœuds terminaux diffèrent entre les implémentations.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="3fe6c-109">La structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour Windows Sockets 2 est utilisée pour déclarer les différents attributs multipoint d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="3fe6c-110">En examinant ces attributs, le programmeur sait quelles conventions suivre avec les fonctions Windows Sockets 2 applicables pour configurer, utiliser et détruire les sessions multipoint.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="3fe6c-111">Voici un résumé des fonctionnalités Winsock qui prennent en charge multipoint :</span><span class="sxs-lookup"><span data-stu-id="3fe6c-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="3fe6c-112">Bits à deux attributs dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="3fe6c-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="3fe6c-113">Quatre indicateurs définis pour le paramètre *dwFlags* de la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="3fe6c-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="3fe6c-114">Une fonction, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint</span><span class="sxs-lookup"><span data-stu-id="3fe6c-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="3fe6c-115">Deux codes de commande [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour le contrôle du bouclage multipoint et l’établissement de l’étendue des transmissions par multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="3fe6c-116">(Ce dernier correspond au paramètre de durée de vie et de durée de vie de la multidiffusion IP.)</span><span class="sxs-lookup"><span data-stu-id="3fe6c-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="3fe6c-117">L’inclusion de ces fonctionnalités multipoint dans Windows Sockets 2 n’empêche pas une application d’utiliser une interface existante dépendante du protocole, telle que les options de socket Deering pour la multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="3fe6c-118">Pour plus d’informations sur la façon dont les différents schémas multipoint sont caractérisés et sur la façon dont les fonctionnalités applicables de Windows Sockets 2 sont utilisées, consultez [sémantique multipoint et multicast](multipoint-and-multicast-semantics-2.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe6c-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
