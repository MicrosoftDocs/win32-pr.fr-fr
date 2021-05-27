---
title: Horodatage Winsock
description: Les horodateurs de paquets sont une fonctionnalité essentielle pour de nombreuses applications de synchronisation d’horloges &mdash; , par exemple, le protocole de précision. Plus la génération d’horodatage est proche de la réception ou de l’envoi d’un paquet par le matériel de carte réseau, plus l’application de synchronisation peut être précise.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559956"
---
# <a name="winsock-timestamping"></a><span data-ttu-id="41a9a-104">Horodatage Winsock</span><span class="sxs-lookup"><span data-stu-id="41a9a-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="41a9a-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="41a9a-105">Introduction</span></span>

<span data-ttu-id="41a9a-106">Les horodateurs de paquets sont une fonctionnalité essentielle pour de nombreuses applications de synchronisation d’horloges &mdash; , par exemple, le protocole de précision.</span><span class="sxs-lookup"><span data-stu-id="41a9a-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="41a9a-107">Plus la génération d’horodatage est proche de la réception ou de l’envoi d’un paquet par le matériel de carte réseau, plus l’application de synchronisation peut être précise.</span><span class="sxs-lookup"><span data-stu-id="41a9a-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="41a9a-108">Par conséquent, les API d’horodatage décrites dans cette rubrique fournissent à votre application un mécanisme pour signaler les horodateurs qui sont générés bien au-dessous de la couche application.</span><span class="sxs-lookup"><span data-stu-id="41a9a-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="41a9a-109">Plus précisément, un horodateur logiciel au niveau de l’interface entre le miniport et NDIS et un horodateur matériel dans le matériel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="41a9a-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="41a9a-110">L’API d’horodatage peut améliorer la précision de la synchronisation de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="41a9a-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="41a9a-111">Actuellement, la prise en charge est limitée aux sockets UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="41a9a-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="41a9a-112">Recevoir les horodateurs</span><span class="sxs-lookup"><span data-stu-id="41a9a-112">Receive timestamps</span></span>

<span data-ttu-id="41a9a-113">Vous configurez la réception des horodateurs de réception via le [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) ioctl.</span><span class="sxs-lookup"><span data-stu-id="41a9a-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="41a9a-114">Utilisez cette IOCTL pour activer la réception des horodateurs de réception.</span><span class="sxs-lookup"><span data-stu-id="41a9a-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="41a9a-115">Lorsque vous recevez un datagramme à l’aide de la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , son horodateur (s’il est disponible) est contenu dans le message de contrôle **SO_TIMESTAMP** .</span><span class="sxs-lookup"><span data-stu-id="41a9a-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="41a9a-116">**SO_TIMESTAMP** (0x300A) est défini dans `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="41a9a-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="41a9a-117">Les données de message de contrôle sont retournées en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="41a9a-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="41a9a-118">Transmettre les horodateurs</span><span class="sxs-lookup"><span data-stu-id="41a9a-118">Transmit timestamps</span></span>

<span data-ttu-id="41a9a-119">La réception des horodateurs de transmission est également configurée via l’IOCTL [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) .</span><span class="sxs-lookup"><span data-stu-id="41a9a-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="41a9a-120">Utilisez cette IOCTL pour activer la réception des horodateurs de transmission et spécifiez le nombre d’horodateurs de transmission que le système mettra en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="41a9a-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="41a9a-121">À mesure que les horodateurs de transmission sont générés, ils sont ajoutés à la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="41a9a-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="41a9a-122">Si la mémoire tampon est saturée, les nouveaux horodateurs de transmission sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="41a9a-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="41a9a-123">Lors de l’envoi d’un datagramme, associez le datagramme à un message de contrôle **SO_TIMESTAMP_ID** .</span><span class="sxs-lookup"><span data-stu-id="41a9a-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="41a9a-124">Il doit contenir un identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="41a9a-124">This should contain a unique identifier.</span></span> <span data-ttu-id="41a9a-125">Envoyer le datagramme, ainsi que son **SO_TIMESTAMP_ID** message de contrôle, à l’aide de [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span><span class="sxs-lookup"><span data-stu-id="41a9a-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="41a9a-126">Les horodateurs de transmission peuvent ne pas être immédiatement disponibles après le retour de **WSASendMsg** .</span><span class="sxs-lookup"><span data-stu-id="41a9a-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="41a9a-127">À mesure que les horodateurs de transmission deviennent disponibles, ils sont placés dans une mémoire tampon par socket.</span><span class="sxs-lookup"><span data-stu-id="41a9a-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="41a9a-128">Utilisez le [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) ioctl pour interroger l’horodateur par son ID.</span><span class="sxs-lookup"><span data-stu-id="41a9a-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="41a9a-129">Si l’horodatage est disponible, il est supprimé de la mémoire tampon et retourné.</span><span class="sxs-lookup"><span data-stu-id="41a9a-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="41a9a-130">Si l’horodatage n’est pas disponible, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retourne **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="41a9a-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="41a9a-131">Si un horodateur de transmission est généré alors que la mémoire tampon est saturée, le nouvel horodatage est ignoré.</span><span class="sxs-lookup"><span data-stu-id="41a9a-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="41a9a-132">**SO_TIMESTAMP_ID** (0x300B) est défini dans `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="41a9a-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="41a9a-133">Vous devez fournir les données du message de contrôle sous la forme d’un **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="41a9a-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="41a9a-134">Les horodateurs sont représentés sous la forme d’une valeur de compteur de bits 64.</span><span class="sxs-lookup"><span data-stu-id="41a9a-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="41a9a-135">La fréquence du compteur dépend de la source de l’horodateur.</span><span class="sxs-lookup"><span data-stu-id="41a9a-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="41a9a-136">Pour les horodateurs de logiciel, le compteur est une valeur [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) et vous pouvez déterminer sa fréquence via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span><span class="sxs-lookup"><span data-stu-id="41a9a-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="41a9a-137">Pour les horodateurs de matériel de carte réseau, la fréquence des compteurs dépend du matériel de la carte réseau et vous pouvez la déterminer avec des informations supplémentaires fournies par [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span><span class="sxs-lookup"><span data-stu-id="41a9a-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="41a9a-138">Pour déterminer la source des horodateurs, utilisez les fonctions [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) et [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="41a9a-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="41a9a-139">En plus de la configuration au niveau du socket à l’aide de l’option de socket [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) pour activer la réception des horodateurs pour un socket, une configuration au niveau du système est également nécessaire.</span><span class="sxs-lookup"><span data-stu-id="41a9a-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="41a9a-140">Estimation de la latence du chemin d’envoi du socket</span><span class="sxs-lookup"><span data-stu-id="41a9a-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="41a9a-141">Dans cette section, nous allons utiliser des horodateurs de transmission pour estimer la latence du chemin d’envoi du Socket.</span><span class="sxs-lookup"><span data-stu-id="41a9a-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="41a9a-142">Si vous disposez d’une application existante qui utilise des horodateurs d’e/s au niveau de &mdash; l’application où l’horodateur doit être aussi proche que possible du point de transmission réel &mdash; , cet exemple fournit une description quantitative de la façon dont les API d’horodatage Winsock peuvent améliorer la précision de votre application.</span><span class="sxs-lookup"><span data-stu-id="41a9a-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="41a9a-143">L’exemple suppose qu’il n’y a qu’une seule carte d’interface réseau (NIC) dans le système, et que *interfaceLuid* est le LUID de cet adaptateur.</span><span class="sxs-lookup"><span data-stu-id="41a9a-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="41a9a-144">Estimation de la latence du chemin de réception du socket</span><span class="sxs-lookup"><span data-stu-id="41a9a-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="41a9a-145">Voici un exemple similaire pour le chemin de réception.</span><span class="sxs-lookup"><span data-stu-id="41a9a-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="41a9a-146">L’exemple suppose qu’il n’y a qu’une seule carte d’interface réseau (NIC) dans le système, et que *interfaceLuid* est le LUID de cet adaptateur.</span><span class="sxs-lookup"><span data-stu-id="41a9a-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="a-limitation"></a><span data-ttu-id="41a9a-147">Une limitation</span><span class="sxs-lookup"><span data-stu-id="41a9a-147">A limitation</span></span>

<span data-ttu-id="41a9a-148">L’une des limitations des API d’horodatage Winsock est que l’appel de [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) est toujours une opération sans blocage.</span><span class="sxs-lookup"><span data-stu-id="41a9a-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="41a9a-149">Même l’appel de l’IOCTL en mode CHEVAUCHement entraîne un retour immédiat de **WSAEWOULDBLOCK** s’il n’existe actuellement aucun horodatage de transmission disponible.</span><span class="sxs-lookup"><span data-stu-id="41a9a-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="41a9a-150">Étant donné que les horodateurs de transmission peuvent ne pas être immédiatement disponibles après le retour de [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) , votre application doit interroger l’IOCTL jusqu’à ce que l’horodatage soit disponible.</span><span class="sxs-lookup"><span data-stu-id="41a9a-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="41a9a-151">Un horodatage de transmission est garanti être disponible après un appel **WSASendMsg** réussi, étant donné que la mémoire tampon d’horodatage de transmission n’est pas saturée.</span><span class="sxs-lookup"><span data-stu-id="41a9a-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
