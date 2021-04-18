---
description: Calcul de la surcharge avec netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcul de la surcharge avec netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516248"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="e1f69-103">Calcul de la surcharge avec netstat</span><span class="sxs-lookup"><span data-stu-id="e1f69-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="e1f69-104">Le calcul de la surcharge avec netstat doit être effectué sur un réseau silencieux pour éviter que d’autres trafics réseau n’inclinent les données, telles que le trafic de diffusion ou de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e1f69-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="e1f69-105">**Pour calculer la surcharge réseau d’une application à l’aide de netstat**</span><span class="sxs-lookup"><span data-stu-id="e1f69-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="e1f69-106">Récupérez les statistiques d’interface actuelles à l’aide de netstat.</span><span class="sxs-lookup"><span data-stu-id="e1f69-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="e1f69-107">Exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="e1f69-107">Execute the application.</span></span>
3.  <span data-ttu-id="e1f69-108">Récupérez les statistiques de l’interface, à nouveau à l’aide de netstat.</span><span class="sxs-lookup"><span data-stu-id="e1f69-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="e1f69-109">Calculez le nombre d’octets reçus entre les deux mesures netstat.</span><span class="sxs-lookup"><span data-stu-id="e1f69-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="e1f69-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1f69-110">Example</span></span>

<span data-ttu-id="e1f69-111">L’exemple suivant illustre ces étapes, à l’aide de TTCP, pour envoyer 10 octets de données, un octet à la fois.</span><span class="sxs-lookup"><span data-stu-id="e1f69-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="e1f69-112">Tout d’abord, une surcharge théorique pour l’application est calculée.</span><span class="sxs-lookup"><span data-stu-id="e1f69-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="e1f69-113">Pour ce test, tous les paquets sont de 60 octets (la valeur Ethernet minimale).</span><span class="sxs-lookup"><span data-stu-id="e1f69-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="e1f69-114">Ce transfert requiert trois paquets pour configurer la connexion, 10 paquets de données, 10 paquets d’accusés de réception (ACK retardé est déclenché presque à tout moment) et quatre paquets pour fermer la connexion correctement.</span><span class="sxs-lookup"><span data-stu-id="e1f69-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="e1f69-115">Cela équivaut à 27 paquets de 60 octets chacun, ou à 1620 octets (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="e1f69-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="e1f69-116">Étant donné que seuls 10 octets de données sont transférés, la charge est de 1610 octets, ce qui correspond à plus de 99% de la charge de protocole.</span><span class="sxs-lookup"><span data-stu-id="e1f69-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="e1f69-117">Commandes</span><span class="sxs-lookup"><span data-stu-id="e1f69-117">Commands</span></span>

<span data-ttu-id="e1f69-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="e1f69-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="e1f69-119">**TTCP-t-H0-D-L1-n10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="e1f69-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="e1f69-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="e1f69-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="e1f69-121">Calculs</span><span class="sxs-lookup"><span data-stu-id="e1f69-121">Calculations</span></span>

<span data-ttu-id="e1f69-122">**Envoyé :** 816 octets</span><span class="sxs-lookup"><span data-stu-id="e1f69-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="e1f69-123">**Reçu :** 674 octets</span><span class="sxs-lookup"><span data-stu-id="e1f69-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="e1f69-124">**Nombre total d’octets :** 1490</span><span class="sxs-lookup"><span data-stu-id="e1f69-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="e1f69-125">**Octets utilisateur :** 10</span><span class="sxs-lookup"><span data-stu-id="e1f69-125">**User bytes:** 10</span></span>

<span data-ttu-id="e1f69-126">**Surcharge :** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="e1f69-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="e1f69-127">\* \* Goodput : \* \* = 5 octets/seconde (ou 40 bits/s)</span><span class="sxs-lookup"><span data-stu-id="e1f69-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="e1f69-128">Les octets réels transférés ne correspondent pas aux valeurs théoriques en raison des octets de remplissage non pris en compte pour les valeurs netstat.</span><span class="sxs-lookup"><span data-stu-id="e1f69-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e1f69-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1f69-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f69-130">Comportement de l’application</span><span class="sxs-lookup"><span data-stu-id="e1f69-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="e1f69-131">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="e1f69-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



