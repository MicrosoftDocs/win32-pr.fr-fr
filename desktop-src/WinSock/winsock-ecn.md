---
title: Notification de congestion explicite Winsock (ECN)
description: Certaines applications et/ou protocoles basés sur le protocole UDP (User Datagram Protocol) (par exemple, QUIC) cherchent à tirer parti de l’utilisation des points de décomptes ECN (Explicit congestion notification) afin d’améliorer la latence et l’instabilité dans les réseaux encombrés.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 79b38611cd0301d0b5d301592eec02b68c02353246c67a6c94528417623834f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322022"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Notification de congestion explicite Winsock (ECN)

## <a name="introduction"></a>Introduction

Certaines applications et/ou protocoles basés sur le protocole UDP (User Datagram Protocol) (par exemple, QUIC) cherchent à tirer parti de l’utilisation des points de décomptes ECN (Explicit congestion notification) afin d’améliorer la latence et l’instabilité dans les réseaux encombrés.

Les API Winsock ECN étendent l' / interface **setsockopt** getsockopt, ainsi &mdash; que l’interface de message de contrôle [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , avec la &mdash; prise en charge de la modification et de la réception des points de ECN dans les en-têtes IP. La fonctionnalité fournie vous permet d’obtenir et de définir des points de ECN par paquet.

Pour plus d’informations sur ECN, consultez [Ajout d’une notification de congestion explicite (ECN) à l’adresse IP](https://tools.ietf.org/html/rfc3168).

Votre application n’est pas autorisée à spécifier le point de code de congestion rencontrée lors de l’envoi de datagrammes. L’envoi est retourné avec l’erreur **WSAEINVAL**.

## <a name="query-ecn-with-wsagetrecvipecn"></a>Interroger ECN avec WSAGetRecvIPEcn

[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) est une fonction inline, définie dans `ws2tcpip.h` .

Appelez **WSAGetRecvIPEcn** pour interroger l’activation actuelle de la réception du message de contrôle **IP_ECN** (ou **IPV6_ECN**) via [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).

Consultez également la structure [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) .

- **Protocole**: IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type**: IP_ECN (50 décimal)
- **Description**: spécifie/reçoit le point de ECN dans le champ d’en-tête IPv4 du type de service (TOS).

- **Protocole**: IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type**: IPV6_ECN (50 décimal)
- **Description**: spécifie/reçoit le point de ECN dans le champ d’en-tête IPv6 de classe de trafic.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Spécifier ECN avec WSASetRecvIPEcn

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) est une fonction inline, définie dans `ws2tcpip.h` .

Appelez **WSASetRecvIPEcn** pour spécifier si la pile IP doit remplir la mémoire tampon de contrôle avec un message contenant le point de ECN du type de champ d’en-tête IPv4 de service (ou le champ d’en-tête IPv6 de la classe de trafic) sur un datagramme reçu. Si la valeur est `TRUE` , la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant le point de ECN du datagramme reçu. Le type de message de contrôle retourné sera **IP_ECN** (ou **IPV6_ECN**) avec le niveau **IPPROTO_IP** (ou **IPPROTO_IPV6**). Les données de message de contrôle sont retournées en tant que **int**. Cette option est valide uniquement sur les sockets de datagrammes (le type de socket doit être **SOCK_DGRAM**).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Exemple de code 1 &mdash; application de publicité ECN support technique

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Exemple de code 2 &mdash; application détectant la congestion

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

## <a name="see-also"></a>Voir aussi

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
