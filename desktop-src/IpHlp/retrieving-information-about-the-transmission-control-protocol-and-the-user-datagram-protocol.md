---
description: L’assistance IP permet d’accéder aux informations sur les protocoles réseau utilisés sur l’ordinateur local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Récupération d’informations sur le protocole de contrôle de transmission et le protocole de datagramme utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760845"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="5dc03-103">Récupération d’informations sur le protocole de contrôle de transmission et le protocole de datagramme utilisateur</span><span class="sxs-lookup"><span data-stu-id="5dc03-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="5dc03-104">L’assistance IP permet d’accéder aux informations sur les protocoles réseau utilisés sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5dc03-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="5dc03-105">Utilisez les fonctions décrites dans les paragraphes suivants pour récupérer des informations sur le protocole TCP (Transmission Control Protocol) et le protocole UDP (User Datagram Protocol) sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5dc03-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="5dc03-106">La fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) récupère les statistiques actuelles pour TCP.</span><span class="sxs-lookup"><span data-stu-id="5dc03-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="5dc03-107">Pour obtenir des exemples de code impliquant des **GetTcpStatistics** , consultez [extraction d’informations à l’aide de GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="5dc03-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="5dc03-108">La fonction [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) récupère les statistiques actuelles pour UDP.</span><span class="sxs-lookup"><span data-stu-id="5dc03-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="5dc03-109">La fonction [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) récupère la table de connexion TCP.</span><span class="sxs-lookup"><span data-stu-id="5dc03-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="5dc03-110">Le [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) récupère la table d’écouteurs UDP.</span><span class="sxs-lookup"><span data-stu-id="5dc03-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="5dc03-111">La fonction [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permet à un développeur de définir l’état d’une connexion TCP spécifiée sur le TCB d’État TCP de la MIB \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5dc03-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



