---
description: Cette rubrique décrit des considérations de programmation spécifiques lors de l’utilisation de l’infrastructure homologue.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considérations relatives à la programmation (peer-to-peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534271"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="c4cb0-103">Considérations relatives à la programmation (peer-to-peer)</span><span class="sxs-lookup"><span data-stu-id="c4cb0-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="c4cb0-104">Cette rubrique décrit des considérations de programmation spécifiques lors de l’utilisation de l’infrastructure homologue.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="c4cb0-105">Lorsque vous utilisez l’infrastructure homologue pour développer des applications homologues, vous devez prendre en compte les considérations de programmation suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4cb0-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="c4cb0-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="c4cb0-106">IPv6</span></span>

    <span data-ttu-id="c4cb0-107">L’infrastructure homologue requiert l’installation et le démarrage D’ipv6 pour permettre aux applications réseau homologues de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="c4cb0-108">Ports du pare-feu</span><span class="sxs-lookup"><span data-stu-id="c4cb0-108">Firewall Ports</span></span>

    <span data-ttu-id="c4cb0-109">Lorsqu’un pare-feu est utilisé sur un réseau (tel que le pare-feu de connexion Internet IPv6), des ports spécifiques doivent être ouverts pour permettre à l’infrastructure homologue de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="c4cb0-110">Les ports suivants doivent être ouverts :</span><span class="sxs-lookup"><span data-stu-id="c4cb0-110">The following ports must be open:</span></span>

    <span data-ttu-id="c4cb0-111">Port TCP 3587 pour l’infrastructure de regroupement de pairs.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="c4cb0-112">Port UDP 3540 pour l’infrastructure de représentation graphique des homologues.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="c4cb0-113">Les applications qui utilisent l’infrastructure de représentation graphique des pairs sur TCP choisissent leur propre port TCP lors de l’appel de [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span><span class="sxs-lookup"><span data-stu-id="c4cb0-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="c4cb0-114">Option de socket</span><span class="sxs-lookup"><span data-stu-id="c4cb0-114">Socket Option</span></span>

    <span data-ttu-id="c4cb0-115">Lorsque vous tentez de vous connecter à d’autres nœuds homologues IPv6 directement (sans utiliser l’infrastructure homologue), assurez-vous que l’option \_ \_ de socket niveau de protection IPv6 est définie sur **niveau de protection non \_ \_ restreint**.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="c4cb0-116">Bande passante</span><span class="sxs-lookup"><span data-stu-id="c4cb0-116">Bandwidth</span></span>

    <span data-ttu-id="c4cb0-117">Quand vous utilisez PNRP, une application peut publier un ou plusieurs [noms d’homologues](peer-names.md) qui peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="c4cb0-118">Pour chaque nom d’homologue inscrit avec PNRP, il y a une augmentation de la bande passante réseau utilisée par PNRP pour publier le nom de l’homologue et le maintenir à la disposition des autres nœuds.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="c4cb0-119">Pour empêcher l’utilisation d’une bande passante trop importante, les applications doivent éviter d’inscrire un grand nombre de noms d’homologues sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="c4cb0-120">Par exemple, une application qui publie des images ne doit pas créer de nom d’homologue pour chaque image, mais doit créer un nom d’homologue pour le service qui publie des images et utiliser un protocole différent pour les clients afin d’interroger le service à la recherche d’images spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="c4cb0-121">Inscription du nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="c4cb0-121">Peer Name Registration</span></span>

    <span data-ttu-id="c4cb0-122">Certaines applications peuvent être nécessaires pour inscrire le même [nom d’homologue](peer-names.md) sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="c4cb0-123">En général, cela se produit si un nom d’homologue est associé à une personne qui utilise plus d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="c4cb0-124">Une méthode que vous pouvez utiliser pour enregistrer le même nom d’homologue sur plusieurs ordinateurs consiste à créer un groupe homologue pour la personne et à se connecter à ce groupe à partir de tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="c4cb0-125">Une autre méthode consiste à créer une identité d’homologue et un nom d’homologue sur un ordinateur, à exporter l’identité d’homologue à partir de cet ordinateur et à l’importer sur d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="c4cb0-126">Cela permet de créer le même nom d’homologue sécurisé sur tous les ordinateurs qui ont importé l’identité d’homologue.</span><span class="sxs-lookup"><span data-stu-id="c4cb0-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



