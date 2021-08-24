---
title: Horodatage Winsock
description: Les horodateurs de paquets sont une fonctionnalité essentielle pour de nombreuses applications de synchronisation d’horloges &mdash; , par exemple, le protocole de précision. Plus la génération d’horodatage est proche de la réception ou de l’envoi d’un paquet par le matériel de carte réseau, plus l’application de synchronisation peut être précise.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: 329c13d76fc0c4ce0d87550623e7419af14bfdd268bf359a8f50729e0b0596e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568989"
---
# <a name="winsock-timestamping"></a>Horodatage Winsock

## <a name="introduction"></a>Introduction

Les horodateurs de paquets sont une fonctionnalité essentielle pour de nombreuses applications de synchronisation d’horloges &mdash; , par exemple, le protocole de précision. Plus la génération d’horodatage est proche de la réception ou de l’envoi d’un paquet par le matériel de carte réseau, plus l’application de synchronisation peut être précise.

Par conséquent, les API d’horodatage décrites dans cette rubrique fournissent à votre application un mécanisme pour signaler les horodateurs qui sont générés bien au-dessous de la couche application. Plus précisément, un horodateur logiciel au niveau de l’interface entre le miniport et NDIS et un horodateur matériel dans le matériel de la carte réseau. L’API d’horodatage peut améliorer la précision de la synchronisation de l’horloge. Actuellement, la prise en charge est limitée aux sockets UDP (User Datagram Protocol).

## <a name="receive-timestamps"></a>Recevoir les horodateurs

Vous configurez la réception des horodateurs de réception via le [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) ioctl. Utilisez cette IOCTL pour activer la réception des horodateurs de réception. Lorsque vous recevez un datagramme à l’aide de la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , son horodateur (s’il est disponible) est contenu dans le message de contrôle **SO_TIMESTAMP** .

**SO_TIMESTAMP** (0x300A) est défini dans `mstcpip.h` . Les données de message de contrôle sont retournées en tant que **UINT64**.

## <a name="transmit-timestamps"></a>Transmettre les horodateurs

La réception des horodateurs de transmission est également configurée via l’IOCTL [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) . Utilisez cette IOCTL pour activer la réception des horodateurs de transmission et spécifiez le nombre d’horodateurs de transmission que le système mettra en mémoire tampon. À mesure que les horodateurs de transmission sont générés, ils sont ajoutés à la mémoire tampon. Si la mémoire tampon est saturée, les nouveaux horodateurs de transmission sont ignorés.

Lors de l’envoi d’un datagramme, associez le datagramme à un message de contrôle **SO_TIMESTAMP_ID** . Il doit contenir un identificateur unique. Envoyer le datagramme, ainsi que son **SO_TIMESTAMP_ID** message de contrôle, à l’aide de [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg). Les horodateurs de transmission peuvent ne pas être immédiatement disponibles après le retour de **WSASendMsg** . À mesure que les horodateurs de transmission deviennent disponibles, ils sont placés dans une mémoire tampon par socket. Utilisez le [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) ioctl pour interroger l’horodateur par son ID. Si l’horodatage est disponible, il est supprimé de la mémoire tampon et retourné. Si l’horodatage n’est pas disponible, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retourne **WSAEWOULDBLOCK**. Si un horodateur de transmission est généré alors que la mémoire tampon est saturée, le nouvel horodatage est ignoré.

**SO_TIMESTAMP_ID** (0x300B) est défini dans `mstcpip.h` . Vous devez fournir les données du message de contrôle sous la forme d’un **UInt32**.

Les horodateurs sont représentés sous la forme d’une valeur de compteur de bits 64. La fréquence du compteur dépend de la source de l’horodateur. Pour les horodateurs de logiciel, le compteur est une valeur [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) et vous pouvez déterminer sa fréquence via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency). Pour les horodateurs de matériel de carte réseau, la fréquence des compteurs dépend du matériel de la carte réseau et vous pouvez la déterminer avec des informations supplémentaires fournies par [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp). Pour déterminer la source des horodateurs, utilisez les fonctions [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) et [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .

En plus de la configuration au niveau du socket à l’aide de l’option de socket [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) pour activer la réception des horodateurs pour un socket, une configuration au niveau du système est également nécessaire.

## <a name="estimating-latency-of-socket-send-path"></a>Estimation de la latence du chemin d’envoi du socket

Dans cette section, nous allons utiliser des horodateurs de transmission pour estimer la latence du chemin d’envoi du Socket. Si vous disposez d’une application existante qui utilise des horodateurs d’e/s au niveau de &mdash; l’application où l’horodateur doit être aussi proche que possible du point de transmission réel &mdash; , cet exemple fournit une description quantitative de la façon dont les API d’horodatage Winsock peuvent améliorer la précision de votre application.

L’exemple suppose qu’il n’y a qu’une seule carte d’interface réseau (NIC) dans le système, et que *interfaceLuid* est le LUID de cet adaptateur.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

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
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a>Estimation de la latence du chemin de réception du socket

Voici un exemple similaire pour le chemin de réception. L’exemple suppose qu’il n’y a qu’une seule carte d’interface réseau (NIC) dans le système, et que *interfaceLuid* est le LUID de cet adaptateur.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a>Une limitation

L’une des limitations des API d’horodatage Winsock est que l’appel de [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) est toujours une opération sans blocage. Même l’appel de l’IOCTL en mode CHEVAUCHement entraîne un retour immédiat de **WSAEWOULDBLOCK** s’il n’existe actuellement aucun horodatage de transmission disponible. Étant donné que les horodateurs de transmission peuvent ne pas être immédiatement disponibles après le retour de [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) , votre application doit interroger l’IOCTL jusqu’à ce que l’horodatage soit disponible. Un horodatage de transmission est garanti être disponible après un appel **WSASendMsg** réussi, étant donné que la mémoire tampon d’horodatage de transmission n’est pas saturée.
