---
description: La famille d’adresses IPX définit la structure d’adressage pour les protocoles qui utilisent l’adressage de socket IPX standard. Pour ces transports, une adresse de point de terminaison se compose d’un numéro de réseau, d’une adresse de nœud et d’un numéro de Socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Famille d’adresses AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113111"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="ba006-104">\_Famille d’adresses IPX AF</span><span class="sxs-lookup"><span data-stu-id="ba006-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="ba006-105">La famille d’adresses IPX définit la structure d’adressage pour les protocoles qui utilisent l’adressage de socket IPX standard.</span><span class="sxs-lookup"><span data-stu-id="ba006-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="ba006-106">Pour ces transports, une adresse de point de terminaison se compose d’un numéro de réseau, d’une adresse de nœud et d’un numéro de Socket.</span><span class="sxs-lookup"><span data-stu-id="ba006-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="ba006-107">Le numéro de réseau est un domaine d’administration et nomme généralement un segment Ethernet ou Token Ring unique.</span><span class="sxs-lookup"><span data-stu-id="ba006-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="ba006-108">Le numéro de nœud est l’adresse physique d’une station.</span><span class="sxs-lookup"><span data-stu-id="ba006-108">The node number is a station's physical address.</span></span> <span data-ttu-id="ba006-109">La combinaison du filet et du nœud constitue une adresse de station unique supposée être unique dans le monde.</span><span class="sxs-lookup"><span data-stu-id="ba006-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="ba006-110">Les numéros de nœud net et de nœud sont représentés en texte ASCII, en notation de bloc ou en pointillés, comme suit : ' 0101a040, 00001b498765 'ou' 01-01-a0-40, 00-00-1b-49-87-65 '.</span><span class="sxs-lookup"><span data-stu-id="ba006-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="ba006-111">Les zéros non significatifs ne doivent pas être présents.</span><span class="sxs-lookup"><span data-stu-id="ba006-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="ba006-112">Le numéro de socket IPX est un numéro de service de réseau/transport similaire à un numéro de port TCP. il ne doit pas être confondu avec le descripteur de socket Winsock.</span><span class="sxs-lookup"><span data-stu-id="ba006-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="ba006-113">Les numéros de socket IPX sont globaux pour la station finale et ne peuvent pas être liés à des adresses net/node spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ba006-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="ba006-114">Par exemple, si la station finale a deux cartes d’interface réseau, un socket lié peut envoyer et recevoir sur les deux cartes.</span><span class="sxs-lookup"><span data-stu-id="ba006-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="ba006-115">En particulier, les sockets de datagrammes recevaient des datagrammes de diffusion sur les deux cartes.</span><span class="sxs-lookup"><span data-stu-id="ba006-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="ba006-116">SOCKADDR \_ IPX a une longueur de 14 octets et est plus petite que la structure de référence [**sockaddr**](sockaddr-2.md) de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="ba006-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="ba006-117">Les implémentations IPX/SPX peuvent accepter la longueur de 16 octets, ainsi que la longueur réelle.</span><span class="sxs-lookup"><span data-stu-id="ba006-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="ba006-118">Si vous utilisez SOCKADDR \_ IPX et une longueur codée en dur de 16 octets, l’implémentation peut supposer qu’elle a accès aux 2 octets qui suivent votre structure.</span><span class="sxs-lookup"><span data-stu-id="ba006-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="ba006-119">Champ</span><span class="sxs-lookup"><span data-stu-id="ba006-119">Field</span></span>           | <span data-ttu-id="ba006-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba006-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="ba006-121">**\_famille sa**</span><span class="sxs-lookup"><span data-stu-id="ba006-121">**sa\_family**</span></span>  | <span data-ttu-id="ba006-122">Famille d’adresses AF \_ IPX dans l’ordre de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="ba006-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="ba006-123">**Sa \_ netnum**</span><span class="sxs-lookup"><span data-stu-id="ba006-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="ba006-124">Identificateur du réseau IPX dans l’ordre du réseau.</span><span class="sxs-lookup"><span data-stu-id="ba006-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="ba006-125">**Sa \_ nodeNum**</span><span class="sxs-lookup"><span data-stu-id="ba006-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="ba006-126">Adresse du nœud de station, vidée de droite.</span><span class="sxs-lookup"><span data-stu-id="ba006-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="ba006-127">**\_Socket sa**</span><span class="sxs-lookup"><span data-stu-id="ba006-127">**Sa\_socket**</span></span>  | <span data-ttu-id="ba006-128">Numéro de socket IPX dans l’ordre des réseaux.</span><span class="sxs-lookup"><span data-stu-id="ba006-128">IPX socket number in network order.</span></span>      |



 

 

 



