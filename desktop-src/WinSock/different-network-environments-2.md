---
description: Plusieurs environnements réseau affectent le comportement réseau d’une application.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Différents environnements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211199"
---
# <a name="different-network-environments"></a><span data-ttu-id="05e42-103">Différents environnements réseau</span><span class="sxs-lookup"><span data-stu-id="05e42-103">Different Network Environments</span></span>

<span data-ttu-id="05e42-104">Plusieurs environnements réseau affectent le comportement réseau d’une application.</span><span class="sxs-lookup"><span data-stu-id="05e42-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="05e42-105">Les propriétés qui différencient les environnements réseau incluent une bande passante faible ou élevée, et un temps RTT faible ou élevé.</span><span class="sxs-lookup"><span data-stu-id="05e42-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="05e42-106">Les environnements réseau affectent les applications transactionnelles et de streaming de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="05e42-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="05e42-107">Les applications transactionnelles sont plus sensibles au temps RTT. les applications de streaming sont plus sensibles aux produits de délai de bande passante.</span><span class="sxs-lookup"><span data-stu-id="05e42-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![Diagramme montrant comment différents environnements réseau affectent le comportement en réseau d’une application.](images/hperf-1.png)

<span data-ttu-id="05e42-109">Les réseaux d’accès à distance et certains réseaux sans fil ont une variable RTT.</span><span class="sxs-lookup"><span data-stu-id="05e42-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="05e42-110">En règle générale, les réseaux satellites ont une bande passante asymétrique entre en amont et en aval.</span><span class="sxs-lookup"><span data-stu-id="05e42-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="05e42-111">Les réseaux locaux sans fil et xDSL sont de bons exemples de réseaux avec des produits avec un délai de bande passante similaire à celui de Fast Ethernet.</span><span class="sxs-lookup"><span data-stu-id="05e42-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05e42-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05e42-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05e42-113">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="05e42-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="05e42-114">Dimensions de performances</span><span class="sxs-lookup"><span data-stu-id="05e42-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



