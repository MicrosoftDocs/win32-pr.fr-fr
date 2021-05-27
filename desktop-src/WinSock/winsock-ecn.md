---
title: Notification de congestion explicite Winsock (ECN)
description: Certaines applications et/ou protocoles basés sur le protocole UDP (User Datagram Protocol) (par exemple, QUIC) cherchent à tirer parti de l’utilisation des points de décomptes ECN (Explicit congestion notification) afin d’améliorer la latence et l’instabilité dans les réseaux encombrés.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559970"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="2256e-103">Notification de congestion explicite Winsock (ECN)</span><span class="sxs-lookup"><span data-stu-id="2256e-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="2256e-104">Introduction</span><span class="sxs-lookup"><span data-stu-id="2256e-104">Introduction</span></span>

<span data-ttu-id="2256e-105">Certaines applications et/ou protocoles basés sur le protocole UDP (User Datagram Protocol) (par exemple, QUIC) cherchent à tirer parti de l’utilisation des points de décomptes ECN (Explicit congestion notification) afin d’améliorer la latence et l’instabilité dans les réseaux encombrés.</span><span class="sxs-lookup"><span data-stu-id="2256e-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="2256e-106">Les API Winsock ECN étendent l' / interface **setsockopt** getsockopt, ainsi &mdash; que l’interface de message de contrôle [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , avec la &mdash; prise en charge de la modification et de la réception des points de ECN dans les en-têtes IP.</span><span class="sxs-lookup"><span data-stu-id="2256e-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="2256e-107">La fonctionnalité fournie vous permet d’obtenir et de définir des points de ECN par paquet.</span><span class="sxs-lookup"><span data-stu-id="2256e-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="2256e-108">Pour plus d’informations sur ECN, consultez [Ajout d’une notification de congestion explicite (ECN) à l’adresse IP](https://tools.ietf.org/html/rfc3168).</span><span class="sxs-lookup"><span data-stu-id="2256e-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="2256e-109">Votre application n’est pas autorisée à spécifier le point de code de congestion rencontrée lors de l’envoi de datagrammes.</span><span class="sxs-lookup"><span data-stu-id="2256e-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="2256e-110">L’envoi est retourné avec l’erreur **WSAEINVAL**.</span><span class="sxs-lookup"><span data-stu-id="2256e-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="2256e-111">Interroger ECN avec WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="2256e-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="2256e-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) est une fonction inline, définie dans `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="2256e-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="2256e-113">Appelez **WSAGetRecvIPEcn** pour interroger l’activation actuelle de la réception du message de contrôle **IP_ECN** (ou **IPV6_ECN**) via [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span><span class="sxs-lookup"><span data-stu-id="2256e-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="2256e-114">Consultez également la structure [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) .</span><span class="sxs-lookup"><span data-stu-id="2256e-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="2256e-115">**Protocole**: IPv4</span><span class="sxs-lookup"><span data-stu-id="2256e-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="2256e-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="2256e-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="2256e-117">**Cmsg_type**: IP_ECN (50 décimal)</span><span class="sxs-lookup"><span data-stu-id="2256e-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="2256e-118">**Description**: spécifie/reçoit le point de ECN dans le champ d’en-tête IPv4 du type de service (TOS).</span><span class="sxs-lookup"><span data-stu-id="2256e-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="2256e-119">**Protocole**: IPv6</span><span class="sxs-lookup"><span data-stu-id="2256e-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="2256e-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="2256e-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="2256e-121">**Cmsg_type**: IPV6_ECN (50 décimal)</span><span class="sxs-lookup"><span data-stu-id="2256e-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="2256e-122">**Description**: spécifie/reçoit le point de ECN dans le champ d’en-tête IPv6 de classe de trafic.</span><span class="sxs-lookup"><span data-stu-id="2256e-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="2256e-123">Spécifier ECN avec WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="2256e-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="2256e-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) est une fonction inline, définie dans `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="2256e-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="2256e-125">Appelez **WSASetRecvIPEcn** pour spécifier si la pile IP doit remplir la mémoire tampon de contrôle avec un message contenant le point de ECN du type de champ d’en-tête IPv4 de service (ou le champ d’en-tête IPv6 de la classe de trafic) sur un datagramme reçu.</span><span class="sxs-lookup"><span data-stu-id="2256e-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="2256e-126">Si la valeur est `TRUE` , la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant le point de ECN du datagramme reçu.</span><span class="sxs-lookup"><span data-stu-id="2256e-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="2256e-127">Le type de message de contrôle retourné sera **IP_ECN** (ou **IPV6_ECN**) avec le niveau **IPPROTO_IP** (ou **IPPROTO_IPV6**).</span><span class="sxs-lookup"><span data-stu-id="2256e-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="2256e-128">Les données de message de contrôle sont retournées en tant que **int**.</span><span class="sxs-lookup"><span data-stu-id="2256e-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="2256e-129">Cette option est valide uniquement sur les sockets de datagrammes (le type de socket doit être **SOCK_DGRAM**).</span><span class="sxs-lookup"><span data-stu-id="2256e-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="2256e-130">Exemple de code 1 &mdash; application de publicité ECN support technique</span><span class="sxs-lookup"><span data-stu-id="2256e-130">Code example 1&mdash;application advertising ECN support</span></span>

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="2256e-131">Exemple de code 2 &mdash; application détectant la congestion</span><span class="sxs-lookup"><span data-stu-id="2256e-131">Code example 2&mdash;application detecting congestion</span></span>

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a><span data-ttu-id="2256e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2256e-132">See also</span></span>

* [<span data-ttu-id="2256e-133">WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="2256e-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="2256e-134">WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="2256e-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
