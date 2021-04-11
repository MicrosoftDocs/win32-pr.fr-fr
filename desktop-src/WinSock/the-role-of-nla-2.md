---
description: Le fournisseur de services NLA (Network Location Awareness) est vital pour les ordinateurs ou périphériques qui peuvent se déplacer entre différents réseaux et pour sélectionner des configurations optimales lorsque plusieurs sont disponibles.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Rôle de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202301"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="f9680-103">Rôle de NLA</span><span class="sxs-lookup"><span data-stu-id="f9680-103">The Role of NLA</span></span>

<span data-ttu-id="f9680-104">Le fournisseur de services NLA (Network Location Awareness) est vital pour les ordinateurs ou périphériques qui peuvent se déplacer entre différents réseaux et pour sélectionner des configurations optimales lorsque plusieurs sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="f9680-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="f9680-105">Par exemple, un ordinateur sans fil itinérant entre des réseaux physiques peut utiliser NLA pour déterminer la configuration appropriée en fonction des informations sur la connexion réseau disponible.</span><span class="sxs-lookup"><span data-stu-id="f9680-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="f9680-106">NLA s’avère également utile lorsqu’un ordinateur multirésident dispose d’une connexion physique à un réseau, tout en étant connecté à un autre réseau par le biais d’une connexion d’accès à distance ou d’un tunnel.</span><span class="sxs-lookup"><span data-stu-id="f9680-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="f9680-107">Par le passé, les développeurs devaient obtenir des informations sur une interface réseau logique et, par conséquent, prendre des décisions sur la connectivité réseau, en se basant sur une multitude d’informations réseau disparates.</span><span class="sxs-lookup"><span data-stu-id="f9680-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="f9680-108">Dans ces circonstances, les développeurs devaient choisir l’interface réseau appropriée en fonction de l’adresse IP, du sous-réseau de l’interface, du nom DNS (Domain Name System) associé à l’interface, de l’adresse MAC d’une carte réseau, d’un nom de réseau sans fil ou d’autres informations réseau.</span><span class="sxs-lookup"><span data-stu-id="f9680-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="f9680-109">NLA évite ce problème en fournissant une interface standard pour énumérer les informations de pièce jointe du réseau logique, en la mettant en corrélation avec les informations de l’interface réseau physique, puis en fournissant une notification lorsque les informations précédemment retournées sont invalidées.</span><span class="sxs-lookup"><span data-stu-id="f9680-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="f9680-110">NLA fournit les informations d’emplacement réseau suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9680-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="f9680-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identité du réseau logique</span><span class="sxs-lookup"><span data-stu-id="f9680-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="f9680-112">NLA tente d’abord d’identifier un réseau logique par son nom de domaine DNS.</span><span class="sxs-lookup"><span data-stu-id="f9680-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="f9680-113">Si un réseau logique n’a pas de nom de domaine, NLA identifie le réseau à partir des informations statiques personnalisées stockées dans le registre, et enfin à partir de son adresse de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="f9680-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="f9680-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces réseau logiques</span><span class="sxs-lookup"><span data-stu-id="f9680-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="f9680-115">Pour chaque réseau auquel un ordinateur est attaché, NLA fournit un *AdapterName* qui identifie de façon unique une interface physique telle qu’une carte réseau, ou une interface logique telle qu’une connexion RAS.</span><span class="sxs-lookup"><span data-stu-id="f9680-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="f9680-116">Le AdapterName peut ensuite être utilisé avec les fonctions disponibles dans l’API d’assistance IP pour obtenir d’autres caractéristiques d’interface.</span><span class="sxs-lookup"><span data-stu-id="f9680-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="f9680-117">NLA implémente le réseau logique en tant que classe de service, avec un GUID et des propriétés de classe associés.</span><span class="sxs-lookup"><span data-stu-id="f9680-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="f9680-118">Chaque réseau logique pour lequel NLA retourne des informations est une instance de cette classe de service.</span><span class="sxs-lookup"><span data-stu-id="f9680-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



