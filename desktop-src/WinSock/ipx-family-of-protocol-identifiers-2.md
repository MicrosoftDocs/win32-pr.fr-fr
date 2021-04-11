---
description: Le paramètre Protocol dans socket et WSASocket est un identificateur qui établit un type de réseau et une méthode pour identifier les différents protocoles de transport qui s’exécutent sur le réseau.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Famille IPX d’identificateurs de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113050"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="def7a-103">Famille IPX d’identificateurs de protocole</span><span class="sxs-lookup"><span data-stu-id="def7a-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="def7a-104">Le paramètre *Protocol* dans [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) est un identificateur qui établit un type de réseau et une méthode pour identifier les différents protocoles de transport qui s’exécutent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="def7a-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="def7a-105">Contrairement à IP, IPX n’utilise pas une seule valeur de protocole pour sélectionner une pile de transport.</span><span class="sxs-lookup"><span data-stu-id="def7a-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="def7a-106">Étant donné qu’il n’est pas nécessaire d’utiliser une valeur spécifique pour chaque protocole de transport, nous sommes libres de les affecter de manière pratique pour les applications Winsock.</span><span class="sxs-lookup"><span data-stu-id="def7a-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="def7a-107">Nous évitons les valeurs comprises entre 0 et 255 afin d’éviter les collisions avec les valeurs de protocole inet de PF correspondantes \_ .</span><span class="sxs-lookup"><span data-stu-id="def7a-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="def7a-108">Nom</span><span class="sxs-lookup"><span data-stu-id="def7a-108">Name</span></span>         | <span data-ttu-id="def7a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="def7a-109">Value</span></span>       | <span data-ttu-id="def7a-110">Types de Sockets</span><span class="sxs-lookup"><span data-stu-id="def7a-110">Socket types</span></span>              | <span data-ttu-id="def7a-111">Description</span><span class="sxs-lookup"><span data-stu-id="def7a-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="def7a-112">Réservé</span><span class="sxs-lookup"><span data-stu-id="def7a-112">Reserved</span></span>     | <span data-ttu-id="def7a-113">0-255</span><span class="sxs-lookup"><span data-stu-id="def7a-113">0-255</span></span>       |                           | <span data-ttu-id="def7a-114">Réservé aux valeurs de protocole de PF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="def7a-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="def7a-115">\_IPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="def7a-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="def7a-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="def7a-116">1000 - 1255</span></span> | <span data-ttu-id="def7a-117">\_DGRAM chaussette \_ brute</span><span class="sxs-lookup"><span data-stu-id="def7a-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="def7a-118">Service de datagramme pour IPX.</span><span class="sxs-lookup"><span data-stu-id="def7a-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="def7a-119">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="def7a-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="def7a-120">1256</span><span class="sxs-lookup"><span data-stu-id="def7a-120">1256</span></span>        | <span data-ttu-id="def7a-121">\_flux de chaussette \_ SEQPKT</span><span class="sxs-lookup"><span data-stu-id="def7a-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="def7a-122">Échange de paquets fiable utilisant des paquets de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="def7a-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="def7a-123">Quand NSPROTO \_ SPX est spécifié, le protocole SPX II est utilisé automatiquement si les deux points de terminaison sont en mesure de le faire.</span><span class="sxs-lookup"><span data-stu-id="def7a-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



