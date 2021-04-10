---
description: L’assistance IP fournit des fonctionnalités de récupération des informations qui sont utiles pour l’administration réseau de l’ordinateur local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Récupération d’informations sur le protocole Internet et le protocole de message de contrôle Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950929"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="2decb-103">Récupération d’informations sur le protocole Internet et le protocole de message de contrôle Internet</span><span class="sxs-lookup"><span data-stu-id="2decb-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="2decb-104">L’assistance IP fournit des fonctionnalités de récupération des informations qui sont utiles pour l’administration réseau de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2decb-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="2decb-105">Les fonctions suivantes récupèrent les statistiques pour le protocole IP (Internet Protocol) et le protocole ICMP (Internet Control Message Protocol).</span><span class="sxs-lookup"><span data-stu-id="2decb-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="2decb-106">Vous pouvez également utiliser ces fonctions pour définir certains paramètres de configuration pour l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="2decb-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="2decb-107">La fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) récupère les statistiques IP actuelles pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2decb-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="2decb-108">Pour obtenir des exemples de code impliquant des **GetIpStatistics** , consultez [extraction d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="2decb-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="2decb-109">La fonction [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) récupère les statistiques ICMP actuelles.</span><span class="sxs-lookup"><span data-stu-id="2decb-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="2decb-110">Utilisez la fonction [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) pour activer ou désactiver le transfert IP.</span><span class="sxs-lookup"><span data-stu-id="2decb-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="2decb-111">Cette fonction vous permet également de définir la durée de vie (TTL) par défaut des datagrammes IP.</span><span class="sxs-lookup"><span data-stu-id="2decb-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="2decb-112">Vous pouvez également définir la durée de vie à l’aide de la fonction [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .</span><span class="sxs-lookup"><span data-stu-id="2decb-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



