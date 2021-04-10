---
title: Interface (RRAS)
description: Une interface est une connexion logique à un réseau. Chaque interface est identifiée par un index unique. Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941566"
---
# <a name="interface-rras"></a><span data-ttu-id="2a0a8-105">Interface (RRAS)</span><span class="sxs-lookup"><span data-stu-id="2a0a8-105">Interface (RRAS)</span></span>

<span data-ttu-id="2a0a8-106">Une interface est une connexion logique à un réseau.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="2a0a8-107">Chaque interface est identifiée par un index unique.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="2a0a8-108">Les protocoles de routage de multidiffusion (tels que MOSPF) traitent tous les types d’interfaces de la même façon.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="2a0a8-109">Dans le cas d’une interface LAN, l’interface correspond à un appareil physique réel de l’ordinateur (la carte LAN).</span><span class="sxs-lookup"><span data-stu-id="2a0a8-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="2a0a8-110">Dans le cas d’une interface de réseau étendu (WAN), l’interface est mappée à un port lorsqu’une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="2a0a8-111">Les interfaces WAN peuvent être basées sur des tunnels et le port peut être un port de réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="2a0a8-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="2a0a8-112">Les systèmes d’exploitation Windows 2000 et versions ultérieures prennent en charge une interface point-à-multipoint.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="2a0a8-113">Ce type d’interface peut être affiché sous la forme d’une collection de liens point à point qui partagent un point de terminaison unique.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="2a0a8-114">Pour identifier de façon unique un lien exact dans une interface point à multipoint, l’API MGM utilise l’adresse de tronçon suivant de l’ID d’interface.</span><span class="sxs-lookup"><span data-stu-id="2a0a8-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="2a0a8-115">Pour prendre en charge cette identification, l’API MGM utilise un ID d’interface étendu, qui comprend une adresse de [tronçon suivant](next-hop.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0a8-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




