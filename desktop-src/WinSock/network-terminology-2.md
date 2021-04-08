---
description: Les mesures sont utilisées pour mesurer les aspects des performances du réseau et du protocole.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologie réseau (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751420"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="24573-103">Terminologie réseau (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="24573-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="24573-104">Les mesures sont utilisées pour mesurer les aspects des performances du réseau et du protocole.</span><span class="sxs-lookup"><span data-stu-id="24573-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="24573-105">Les valeurs de ces métriques dans différents scénarios indiquent le niveau de performances d’une application réseau.</span><span class="sxs-lookup"><span data-stu-id="24573-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="24573-106">Cette section définit les termes et métriques utilisés à l’ensemble du secteur pour mesurer les performances des applications réseau.</span><span class="sxs-lookup"><span data-stu-id="24573-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="24573-107">Ces termes sont utilisés dans le reste de ce guide.</span><span class="sxs-lookup"><span data-stu-id="24573-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="24573-108">Temps aller-retour (RTT)</span><span class="sxs-lookup"><span data-stu-id="24573-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="24573-109">Durée, en millisecondes, nécessaire à la demande d’effectuer un voyage d’un ordinateur source vers un ordinateur de destination, puis de nouveau.</span><span class="sxs-lookup"><span data-stu-id="24573-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="24573-110">Des valeurs inférieures indiquent de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="24573-110">Lower values indicate better performance.</span></span> <span data-ttu-id="24573-111">Les heures de chemin d’accès direct et de retour ne sont pas nécessairement égales.</span><span class="sxs-lookup"><span data-stu-id="24573-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="24573-112">Les valeurs RTT sont affectées par l’infrastructure réseau, la distance entre les nœuds, les conditions réseau et la taille des paquets.</span><span class="sxs-lookup"><span data-stu-id="24573-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="24573-113">Taille du paquet, congestion et impact de la compressibilité sur la surcharge sur les liaisons lentes, telles que les connexions d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="24573-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="24573-114">D’autres facteurs affectent RTT, y compris la correction des erreurs de transfert et la compression de données, qui introduisent des mémoires tampons et des files d’attente qui augmentent RTT et, par conséquent, réduisent les performances.</span><span class="sxs-lookup"><span data-stu-id="24573-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="24573-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="24573-115">Goodput</span></span>

    <span data-ttu-id="24573-116">Mesure des données d’application utiles traitées avec succès par le destinataire, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="24573-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="24573-117">Goodput permet de mesurer le débit effectif ou utile et comprend uniquement les données d’application. les en-têtes de paquet, de protocole et de média sont considérés comme des surcharges et ne font pas partie de goodput.</span><span class="sxs-lookup"><span data-stu-id="24573-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="24573-118">Surcharge de protocole</span><span class="sxs-lookup"><span data-stu-id="24573-118">Protocol Overhead</span></span>

    <span data-ttu-id="24573-119">Octets qui ne sont pas des applications, y compris les trames de protocole et de support, divisés par le nombre total d’octets transmis.</span><span class="sxs-lookup"><span data-stu-id="24573-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="24573-120">La valeur est exprimée sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="24573-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="24573-121">Des valeurs plus élevées indiquent une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="24573-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="24573-122">La surcharge est calculée pour les deux directions dans ce guide, mais peut être calculée séparément pour chaque direction.</span><span class="sxs-lookup"><span data-stu-id="24573-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="24573-123">Bandwidth-Delay produit</span><span class="sxs-lookup"><span data-stu-id="24573-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="24573-124">Produit de la bande passante bits par seconde du réseau et temps RTT (en secondes).</span><span class="sxs-lookup"><span data-stu-id="24573-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="24573-125">Cette valeur correspond au nombre de bits nécessaires pour remplir la bande passante réseau disponible.</span><span class="sxs-lookup"><span data-stu-id="24573-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="24573-126">Lorsque la valeur de la largeur de bande-délai du produit est élevée, la pile TCP/IP doit gérer de grandes quantités de données non acquittées afin de garder le pipeline complet.</span><span class="sxs-lookup"><span data-stu-id="24573-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="24573-127">La bande passante-délai du produit est une mesure de bout en bout clé pour les applications de streaming.</span><span class="sxs-lookup"><span data-stu-id="24573-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



