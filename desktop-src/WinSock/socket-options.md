---
description: Page de navigation pour les options de socket Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Options de socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540820"
---
# <a name="socket-options"></a><span data-ttu-id="f117b-103">Options de socket</span><span class="sxs-lookup"><span data-stu-id="f117b-103">Socket Options</span></span>

<span data-ttu-id="f117b-104">Cette section décrit les options de socket Winsock pour différentes éditions des systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="f117b-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="f117b-105">Utilisez les fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.</span><span class="sxs-lookup"><span data-stu-id="f117b-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="f117b-106">Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="f117b-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="f117b-107">Certaines options de socket requièrent plus d’explications que celles pouvant être transmises par ces tables. ces options contiennent des liens vers des pages supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f117b-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="f117b-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO \_ IP**</span><span class="sxs-lookup"><span data-stu-id="f117b-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-109">Options de socket applicables au niveau IPv4.</span><span class="sxs-lookup"><span data-stu-id="f117b-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="f117b-110">Pour plus d’informations, consultez [**les \_ options de socket IP IPPROTO**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="f117b-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-112">Options de socket applicables au niveau IPv6.</span><span class="sxs-lookup"><span data-stu-id="f117b-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="f117b-113">Pour plus d’informations, consultez [**les \_ options de socket IPv6 IPPROTO**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**</span><span class="sxs-lookup"><span data-stu-id="f117b-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-115">Options de socket applicables au niveau de la multidiffusion fiable.</span><span class="sxs-lookup"><span data-stu-id="f117b-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="f117b-116">Pour plus d’informations, consultez [**les \_ options de socket RM IPPROTO**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="f117b-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-118">Options de socket applicables au niveau TCP.</span><span class="sxs-lookup"><span data-stu-id="f117b-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="f117b-119">Pour plus d’informations, consultez [**les \_ options de socket TCP IPPROTO**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**\_UDP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="f117b-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-121">Options de socket applicables au niveau du protocole UDP.</span><span class="sxs-lookup"><span data-stu-id="f117b-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="f117b-122">Pour plus d’informations, consultez [**les \_ options de socket UDP IPPROTO**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**\_IPX NSPROTO**</span><span class="sxs-lookup"><span data-stu-id="f117b-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-124">Options de socket applicables au niveau IPX.</span><span class="sxs-lookup"><span data-stu-id="f117b-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="f117b-125">Pour plus d’informations, consultez [**les \_ options de socket IPX NSPROTO**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**\_AppleTalk AppleTalk**</span><span class="sxs-lookup"><span data-stu-id="f117b-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-127">Options de socket applicables au niveau du protocole AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="f117b-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="f117b-128">Pour plus d’informations, consultez [**les \_ options de socket AppleTalk AppleTalk**](sol-appletalk-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**\_IRLMP sol**</span><span class="sxs-lookup"><span data-stu-id="f117b-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-130">Options de socket applicables au niveau du protocole de gestion des liaisons infrarouges.</span><span class="sxs-lookup"><span data-stu-id="f117b-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="f117b-131">Pour plus d’informations, consultez [**les \_ options de socket sol IRLMP**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f117b-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_Socket sol**</span><span class="sxs-lookup"><span data-stu-id="f117b-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f117b-133">Options de socket applicables au niveau du Socket.</span><span class="sxs-lookup"><span data-stu-id="f117b-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="f117b-134">Pour plus d’informations, consultez [**les \_ options de socket de socket sol**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="f117b-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f117b-135">Notes</span><span class="sxs-lookup"><span data-stu-id="f117b-135">Remarks</span></span>

<span data-ttu-id="f117b-136">Toutes les \_ \* options de socket s’appliquent également aux protocoles IPv4 et IPv6 (à l’exception de la \_ diffusion, car la diffusion n’est pas implémentée dans IPv6).</span><span class="sxs-lookup"><span data-stu-id="f117b-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



