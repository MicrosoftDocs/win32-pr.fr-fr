---
title: Notifications de l’état du socket Winsock
description: Les API de notifications de l’état du socket vous offrent un moyen évolutif et efficace d’obtenir des notifications sur les modifications de l’état du Socket. Cela comprend les notifications relatives à des éléments tels que les lectures non bloquantes, les écritures non bloquantes, les conditions d’erreur et d’autres informations.
ms.topic: article
ms.date: 11/18/2020
ms.openlocfilehash: 9ad7f7afcb3dda223b4d54af293bc9a4dd019758
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559963"
---
# <a name="winsock-socket-state-notifications"></a><span data-ttu-id="a3581-104">Notifications de l’état du socket Winsock</span><span class="sxs-lookup"><span data-stu-id="a3581-104">Winsock socket state notifications</span></span>

## <a name="introduction"></a><span data-ttu-id="a3581-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="a3581-105">Introduction</span></span>

<span data-ttu-id="a3581-106">Les API de notifications de l’état du socket dans le tableau ci-dessous vous offrent un moyen évolutif et efficace d’obtenir des notifications sur les modifications de l’état du socket (efficacement en termes d’UC et de mémoire).</span><span class="sxs-lookup"><span data-stu-id="a3581-106">The socket state notifications APIs in the table below provide you with a scalable and efficient way to obtain notifications about socket state changes (efficient in terms of both CPU and memory).</span></span> <span data-ttu-id="a3581-107">Cela comprend les notifications relatives à des éléments tels que les lectures non bloquantes, les écritures non bloquantes, les conditions d’erreur et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="a3581-107">This includes notifications about things such as non-blocking read, non-blocking write, error conditions, and other info.</span></span>

|<span data-ttu-id="a3581-108">API</span><span class="sxs-lookup"><span data-stu-id="a3581-108">API</span></span>|<span data-ttu-id="a3581-109">Description</span><span class="sxs-lookup"><span data-stu-id="a3581-109">Description</span></span>|
|-|-|
|<span data-ttu-id="a3581-110">[**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) fonction)</span><span class="sxs-lookup"><span data-stu-id="a3581-110">[**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) function</span></span>|<span data-ttu-id="a3581-111">Associe un ensemble de sockets à un port de terminaison et récupère toutes les notifications qui sont déjà en attente sur ce port.</span><span class="sxs-lookup"><span data-stu-id="a3581-111">Associates a set of sockets with a completion port, and retrieves any notifications that are already pending on that port.</span></span> <span data-ttu-id="a3581-112">Une fois associé, le port de terminaison reçoit les notifications d’État du socket qui ont été spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a3581-112">Once associated, the completion port receives the socket state notifications that were specified.</span></span>|
|<span data-ttu-id="a3581-113">Structure [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)</span><span class="sxs-lookup"><span data-stu-id="a3581-113">[**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration) structure</span></span>|<span data-ttu-id="a3581-114">Représente les informations fournies à la fonction **ProcessSocketNotifications** .</span><span class="sxs-lookup"><span data-stu-id="a3581-114">Represents info supplied to the **ProcessSocketNotifications** function.</span></span>|
|<span data-ttu-id="a3581-115">[**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) fonction)</span><span class="sxs-lookup"><span data-stu-id="a3581-115">[**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) function</span></span>|<span data-ttu-id="a3581-116">Cette fonction d’assistance Inline est fournie à des fins pratiques pour récupérer le masque d’événements à partir d’un [**OVERLAPPED_ENTRY**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="a3581-116">This inline helper function is provided as a convenience to retrieve the events mask from an [**OVERLAPPED_ENTRY**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).</span></span>|

<span data-ttu-id="a3581-117">Le workflow commence par vous associant des sockets à un port de terminaison d’e/s ([**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) et [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)).</span><span class="sxs-lookup"><span data-stu-id="a3581-117">The workflow begins with you associating sockets with an I/O completion port ([**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) and [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)).</span></span> <span data-ttu-id="a3581-118">Après cela, le port fournit des informations sur les modifications de l’état des sockets à l’aide des méthodes de requête de port de terminaison d’e/s habituelles.</span><span class="sxs-lookup"><span data-stu-id="a3581-118">After that, the port delivers info about socket state changes using the usual I/O completion port query methods.</span></span>

<span data-ttu-id="a3581-119">Ces API permettent de construire facilement des abstractions indépendantes de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="a3581-119">These APIs allow easy construction of platform-agnostic abstractions.</span></span> <span data-ttu-id="a3581-120">Par conséquent, les indicateurs persistants et à déclenchement unique, ainsi que les indicateurs de niveau et de bord sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3581-120">As such, persistent and one-shot, and level- and edge-triggered flags are supported.</span></span> <span data-ttu-id="a3581-121">Par exemple, les inscriptions déclenchées au niveau d’une capture sont le modèle recommandé pour les serveurs multithread.</span><span class="sxs-lookup"><span data-stu-id="a3581-121">For example, one-shot level-triggered registrations are the recommended pattern for multi-threaded servers.</span></span>

## <a name="recommendations"></a><span data-ttu-id="a3581-122">Recommandations</span><span class="sxs-lookup"><span data-stu-id="a3581-122">Recommendations</span></span>

<span data-ttu-id="a3581-123">Ces API offrent une alternative évolutive aux API [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) et [**Select**](/windows/win32/api/winsock2/nf-winsock2-select) .</span><span class="sxs-lookup"><span data-stu-id="a3581-123">These APIs provide a scalable alternative to the [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/win32/api/winsock2/nf-winsock2-select) APIs.</span></span>

<span data-ttu-id="a3581-124">Ils constituent une alternative aux [e/s de socket avec chevauchement](/windows/win32/api/winsock2/nf-winsock2-wsasend#overlapped-socket-i-o) utilisées avec les [ports de terminaison d’e/s](/windows/win32/fileio/i-o-completion-ports), et ils évitent la nécessité de mémoires tampons d’e/s par socket permanentes.</span><span class="sxs-lookup"><span data-stu-id="a3581-124">They're an alternative to [overlapped socket I/O](/windows/win32/api/winsock2/nf-winsock2-wsasend#overlapped-socket-i-o) used with [I/O completion ports](/windows/win32/fileio/i-o-completion-ports), and they avoid the need for permanent per-socket I/O buffers.</span></span> <span data-ttu-id="a3581-125">Toutefois, dans un scénario où les mémoires tampons d’e/s par socket ne sont pas importantes (le nombre de sockets est relativement faible, ou ils sont constamment utilisés), les e/s de socket superposées peuvent avoir moins de surcharge en raison d’un plus petit nombre de transitions de noyau, ainsi que d’un modèle plus simple.</span><span class="sxs-lookup"><span data-stu-id="a3581-125">But in a scenario where per-socket I/O buffers aren't an important consideration (the number of sockets is relatively low, or they're constantly used), overlapped socket I/O might have less overhead due to a smaller number of kernel transitions, as well as a simpler model.</span></span>

<span data-ttu-id="a3581-126">Un socket ne peut être associé qu’à un seul port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="a3581-126">A socket may be associated with only a single I/O completion port.</span></span> <span data-ttu-id="a3581-127">Un socket ne peut être inscrit qu’une seule fois sur un port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="a3581-127">A socket may be registered with an I/O completion port only once.</span></span> <span data-ttu-id="a3581-128">Pour modifier les clés de saisie semi-automatique, annulez l’inscription de la notification, attendez la **SOCK_NOTIFY_EVENT_REMOVE** message (consultez les rubriques [**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) et [**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) ), puis réinscrivez le Socket.</span><span class="sxs-lookup"><span data-stu-id="a3581-128">To change completion keys, deregister the notification, wait for the **SOCK_NOTIFY_EVENT_REMOVE** message (see the [**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) and [**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) topics), and then re-register the socket.</span></span>

<span data-ttu-id="a3581-129">Pour éviter de libérer de la mémoire qui est toujours en cours d’utilisation, vous ne devez libérer les structures de données associées à l’inscription qu’après avoir reçu la notification **SOCK_NOTIFY_EVENT_REMOVE** pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="a3581-129">To avoid freeing memory that's still in use, you should free a registration's associated data structures only after receiving the **SOCK_NOTIFY_EVENT_REMOVE** notification for the registration.</span></span> <span data-ttu-id="a3581-130">Lorsque le descripteur de socket utilisé pour l’inscription aux notifications est fermé à l’aide de la fonction [opération closesocket](/windows/win32/api/winsock/nf-winsock-closesocket) , ses notifications sont automatiquement désinscrites.</span><span class="sxs-lookup"><span data-stu-id="a3581-130">When the socket descriptor used to register for notifications is closed using the [closesocket](/windows/win32/api/winsock/nf-winsock-closesocket) function, its notifications are automatically deregistered.</span></span> <span data-ttu-id="a3581-131">Toutefois, les notifications déjà mises en file d’attente peuvent toujours être remises.</span><span class="sxs-lookup"><span data-stu-id="a3581-131">However, already-queued notifications might still be delivered.</span></span> <span data-ttu-id="a3581-132">Une désinscription automatique via **opération closesocket** ne génère pas de notification **SOCK_NOTIFY_EVENT_REMOVE** .</span><span class="sxs-lookup"><span data-stu-id="a3581-132">An automatic deregistration via **closesocket** won't generate a **SOCK_NOTIFY_EVENT_REMOVE** notification.</span></span>

<span data-ttu-id="a3581-133">Si vous souhaitez le traitement multithread, vous devez utiliser un port de terminaison d’e/s unique avec plusieurs threads qui traitent les notifications.</span><span class="sxs-lookup"><span data-stu-id="a3581-133">If you want multi-threaded processing, then you should use a single I/O completion port with multiple threads processing notifications.</span></span> <span data-ttu-id="a3581-134">Cela permet au port de terminaison d’e/s de monter en charge le travail sur plusieurs threads, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a3581-134">This allows the I/O completion port to scale out the work across multiple threads, as necessary.</span></span> <span data-ttu-id="a3581-135">Évitez d’avoir plusieurs ports de terminaison d’e/s (par exemple, un par thread), car cette conception est vulnérable à la gorge de bouteille sur un seul thread alors que d’autres sont inactifs.</span><span class="sxs-lookup"><span data-stu-id="a3581-135">Avoid having multiple I/O completion ports (for example, one per thread), because that design is vulnerable to bottle-necking on a single thread while others are idle.</span></span>

<span data-ttu-id="a3581-136">Si plusieurs threads déposent des paquets de notification avec des notifications déclenchées par niveau, **SOCK_NOTIFY_TRIGGER_ONESHOT** doit être fourni pour éviter que plusieurs threads reçoivent des notifications pour un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="a3581-136">If multiple threads are dequeuing notification packets with level-triggered notifications, then **SOCK_NOTIFY_TRIGGER_ONESHOT** should be supplied to avoid multiple threads receiving notifications for a state change.</span></span> <span data-ttu-id="a3581-137">Une fois la notification de socket traitée, la notification doit être réinscrite.</span><span class="sxs-lookup"><span data-stu-id="a3581-137">Once the socket notification has been processed, the notification should be re-registered.</span></span>

<span data-ttu-id="a3581-138">Si plusieurs threads déposent des paquets de notification sur une connexion orientée flux où des messages individuels doivent être traités sur un thread unique, envisagez d’utiliser des notifications à une seule capture déclenchées par niveau.</span><span class="sxs-lookup"><span data-stu-id="a3581-138">If multiple threads are dequeuing notification packets on a stream-oriented connection where individual messages need to be processed on a single thread, then consider using level-triggered one-shot notifications.</span></span> <span data-ttu-id="a3581-139">Cela réduit la probabilité que plusieurs threads reçoivent des fragments de message qui doivent être réassemblés entre threads.</span><span class="sxs-lookup"><span data-stu-id="a3581-139">That reduces the likelihood that multiple threads will receive message fragments that need to be re-assembled cross-thread.</span></span> 

<span data-ttu-id="a3581-140">Si vous utilisez des notifications déclenchées par le bord, nous ne recommandons pas de notifications d’une seule capture, car le socket doit être vidé après l’activation des inscriptions.</span><span class="sxs-lookup"><span data-stu-id="a3581-140">If you're using edge-triggered notifications, then we don't recommend one-shot notifications because the socket needs to be drained after enabling registrations.</span></span> <span data-ttu-id="a3581-141">Il s’agit d’un modèle plus complexe à implémenter, qui est plus onéreux, car il requiert toujours un appel qui retourne **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="a3581-141">This is a more complicated pattern to implement, and is more expensive because it always requires a call that returns **WSAEWOULDBLOCK**.</span></span>

<span data-ttu-id="a3581-142">Si vous souhaitez que la montée en charge de l’acceptation de la connexion se fasse sur un socket d’écoute unique, les serveurs doivent utiliser la fonction [accepteurs](/windows/win32/api/mswsock/nf-mswsock-acceptex) au lieu de s’abonner aux notifications pour les demandes de connexion.</span><span class="sxs-lookup"><span data-stu-id="a3581-142">If you want connection acceptance scale-out on a single listening socket, then servers should use the [AcceptEx](/windows/win32/api/mswsock/nf-mswsock-acceptex) function instead of subscribing to notifications for connection requests.</span></span> <span data-ttu-id="a3581-143">L’acceptation des connexions en réponse aux notifications limite implicitement le taux d’acceptation de la connexion par rapport au traitement des demandes de connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="a3581-143">Accepting connections in response to notifications implicitly throttles the rate of connection acceptance relative to processing requests for existing connections.</span></span>

<span data-ttu-id="a3581-144">Vous trouverez ci-dessous des exemples de code illustrant certains scénarios de notification d’état de Socket.</span><span class="sxs-lookup"><span data-stu-id="a3581-144">Below are code examples illustrating some socket state notification scenarios.</span></span> <span data-ttu-id="a3581-145">Une partie du *code contient des éléments pour vos* propres applications.</span><span class="sxs-lookup"><span data-stu-id="a3581-145">Some of the code contains *to do* items for your own applications.</span></span>

## <a name="common-code"></a><span data-ttu-id="a3581-146">Code commun</span><span class="sxs-lookup"><span data-stu-id="a3581-146">Common code</span></span>

<span data-ttu-id="a3581-147">Tout d’abord, voici une liste de code qui contient des définitions et des fonctions communes utilisées par les scénarios qui suivent.</span><span class="sxs-lookup"><span data-stu-id="a3581-147">First, here's a code listing that contains some common definitions and functions that are used by the scenarios that follow.</span></span>

```cpp
#include "pch.h"
#include <winsock2.h>
#pragma comment(lib, "Ws2_32")

#define SERVER_ADDRESS          0x0100007f  // localhost
#define SERVER_PORT             0xffff      // TODO: select an actual valid port
#define MAX_TIMEOUT             1000
#define CLIENT_LOOP_COUNT       10

typedef struct SERVER_CONTEXT {
    HANDLE ioCompletionPort;
    SOCKET listenerSocket;
} SERVER_CONTEXT;

typedef struct CLIENT_CONTEXT {
    UINT32 transmitCount;
} CLIENT_CONTEXT;

SRWLOCK g_printLock = SRWLOCK_INIT;

VOID DestroyServerContext(_Inout_ _Post_invalid_ SERVER_CONTEXT* serverContext) {
    if (serverContext->listenerSocket != INVALID_SOCKET) {
        closesocket(serverContext->listenerSocket);
    }

    if (serverContext->ioCompletionPort != NULL) {
        CloseHandle(serverContext->ioCompletionPort);
    }

    free(serverContext);
}

DWORD CreateServerContext(_Outptr_ SERVER_CONTEXT** serverContext) {
    DWORD errorCode;
    SERVER_CONTEXT* localContext = NULL;
    sockaddr_in serverAddress = { };

    localContext = (SERVER_CONTEXT*)malloc(sizeof(*localContext));
    if (localContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(localContext, sizeof(*localContext));
    localContext->listenerSocket = INVALID_SOCKET;


    localContext->ioCompletionPort = CreateIoCompletionPort(INVALID_HANDLE_VALUE, NULL, 0, 0);
    if (localContext->ioCompletionPort == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    localContext->listenerSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (localContext->listenerSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (bind(localContext->listenerSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    if (listen(localContext->listenerSocket, 0) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    *serverContext = localContext;
    localContext = NULL;
    errorCode = ERROR_SUCCESS;

Exit:
    if (localContext != NULL) {
        DestroyServerContext(localContext);
    }

    return errorCode;
}

// Create a socket, connect to the server, send transmitCount copies of the
// payload, then disconnect.
DWORD
WINAPI
ClientThreadRoutine(_In_ PVOID clientContextPointer) {
    const UINT32 payload = 0xdeadbeef;
    CLIENT_CONTEXT* clientContext = (CLIENT_CONTEXT*)clientContextPointer;

    sockaddr_in serverAddress = {};
    SOCKET clientSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (clientSocket == INVALID_SOCKET) {
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (connect(clientSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        goto Exit;
    }

    for (UINT32 Index = 0; Index < clientContext->transmitCount; Index += 1) {
        if (send(clientSocket, (const char*)&payload, sizeof(payload), 0) < 0) {
            goto Exit;
        }
    }

    if (shutdown(clientSocket, SD_BOTH) != 0) {
        goto Exit;
    }

Exit:
    if (clientSocket != INVALID_SOCKET) {
        closesocket(INVALID_SOCKET);
    }

    free(clientContext);

    return 0;
}

DWORD CreateClientThread(_In_ UINT32 transmitCount) {
    DWORD errorCode = ERROR_SUCCESS;
    CLIENT_CONTEXT* clientContext = NULL;
    HANDLE clientThread = NULL;

    clientContext = (CLIENT_CONTEXT*)malloc(sizeof(*clientContext));
    if (clientContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(clientContext, sizeof(*clientContext));
    clientContext->transmitCount = transmitCount;

    clientThread = CreateThread(NULL, 0, ClientThreadRoutine, clientContext, 0, NULL);
    if (clientThread == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    clientContext = NULL;

Exit:
    if (clientContext != NULL) {
        free(clientContext);
    }

    if (clientThread != NULL) {
        CloseHandle(clientThread);
    }

    return errorCode;
}

VOID PrintError(DWORD errorCode) {
    AcquireSRWLockExclusive(&g_printLock);

    wprintf_s(L"Server thread %d encountered an error %d.", GetCurrentThreadId(), errorCode);
    WCHAR errorString[512];
    if (FormatMessageW(FORMAT_MESSAGE_FROM_SYSTEM,
        NULL,
        errorCode,
        0,
        errorString,
        RTL_NUMBER_OF(errorString),
        NULL) != 0)
    {
        wprintf_s(L"%s", errorString);
    }

    ReleaseSRWLockExclusive(&g_printLock);
}

// This routine must be used only if a single socket is registered. 
DWORD DeregisterAndWait(_In_ HANDLE ioCompletionPort, _In_ SOCKET socket) {
    DWORD errorCode;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    UINT32 notificationCount;

    // Keep looping until the registration is removed, or a timeout is hit.
    while (TRUE) {

        registration.operation = SOCK_NOTIFY_OP_REMOVE;
        registration.socket = socket;
        errorCode = ProcessSocketNotifications(ioCompletionPort,
            1,
            &registration,
            MAX_TIMEOUT,
            1,
            &notification,
            &notificationCount);

        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }

        if (registration.registrationResult != ERROR_SUCCESS) {
            errorCode = registration.registrationResult;
            goto Exit;
        }

        // Drops all non-removal notifications. Must be used only
        // if a single socket is registered.
        if (SocketNotificationRetrieveEvents(&notification) & SOCK_NOTIFY_EVENT_REMOVE) {
            break;
        }
    }

Exit:
    return errorCode;
}
```

## <a name="simple-replacement-for-polling"></a><span data-ttu-id="a3581-148">Remplacement simple pour l’interrogation</span><span class="sxs-lookup"><span data-stu-id="a3581-148">Simple replacement for polling</span></span>

<span data-ttu-id="a3581-149">Ce scénario illustre un remplacement des applications à l’aide de l’interrogation ([**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)) ou des API similaires.</span><span class="sxs-lookup"><span data-stu-id="a3581-149">This scenario demonstrates a drop-in replacement for applications using poll ([**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)) or similar APIs.</span></span> <span data-ttu-id="a3581-150">Il s’agit d’un monothread et utilise des inscriptions permanentes (et non une capture).</span><span class="sxs-lookup"><span data-stu-id="a3581-150">It's single-threaded, and makes use of persistent (not one-shot) registrations.</span></span> <span data-ttu-id="a3581-151">Étant donné que l’inscription n’a pas besoin d’être réinscrite, elle utilise [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) pour défiler les notifications.</span><span class="sxs-lookup"><span data-stu-id="a3581-151">Because the registration doesn't need to be re-registered, it uses [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) to dequeue notifications.</span></span>

```cpp
VOID SimplePollReplacement() {
    DWORD errorCode;
    WSADATA wsaData;
    SERVER_CONTEXT* serverContext = NULL;
    SOCKET tcpAcceptSocket = INVALID_SOCKET;
    u_long nonBlocking = 1;
    SOCKET currentSocket;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    ULONG notificationCount;
    UINT32 events;
    CHAR dataBuffer[512];

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    errorCode = CreateServerContext(&serverContext);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    tcpAcceptSocket = accept(serverContext->listenerSocket, NULL, NULL);
    if (tcpAcceptSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    if (ioctlsocket(tcpAcceptSocket, FIONBIO, &nonBlocking) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Register the accepted connection.
    registration.completionKey = (PVOID)tcpAcceptSocket;
    registration.eventFilter = SOCK_NOTIFY_REGISTER_EVENT_IN | SOCK_NOTIFY_REGISTER_EVENT_HANGUP;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_LEVEL;
    registration.socket = tcpAcceptSocket;
    errorCode = ProcessSocketNotifications(serverContext->ioCompletionPort,
        1,
        &registration,
        0,
        0,
        NULL,
        NULL);

    // Make sure all registrations were processed.
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Make sure each registration was successful.
    if (registration.registrationResult != ERROR_SUCCESS) {
        errorCode = registration.registrationResult;
        goto Exit;
    }

    // Keep receiving data until the client disconnects.
    while (TRUE) {

        wprintf_s(L"Waiting for client action...\r\n");

        if (!GetQueuedCompletionStatusEx(serverContext->ioCompletionPort,
            &notification,
            1,
            &notificationCount,
            MAX_TIMEOUT,
            FALSE))
        {
            errorCode = GetLastError();
            goto Exit;
        }

        // The completion key is the socket we supplied above.
        //
        // This is true only because the registration supplied the socket as the completion
        // key. A more typical pattern is to supply a context pointer. This example supplies
        // the socket directly, for simplicity.
        //
        // The events are stored in the number-of-bytes-received field.
        events = SocketNotificationRetrieveEvents(&notification);

        currentSocket = (SOCKET)notification.lpCompletionKey;
        if (events & SOCK_NOTIFY_EVENT_IN) {

            // We don't check for a 0-size receive because we subscribed to hang-up notifications.
            if (recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0) < 0) {
                errorCode = GetLastError();
                goto Exit;
            }

            wprintf_s(L"Received client data.\r\n");
        }

        if (events & SOCK_NOTIFY_EVENT_HANGUP) {
            wprintf_s(L"Client hung up. Exiting. \r\n");
            break;
        }

        if (events & SOCK_NOTIFY_EVENT_ERR) {
            wprintf_s(L"The socket was ungracefully reset or another error occurred. Exiting.\r\n");
            // Obtain a more detailed error code by issuing a non-blocking receive.
            recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            errorCode = GetLastError();
            goto Exit;
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
    }

    if (serverContext != NULL) {
        if (tcpAcceptSocket != INVALID_SOCKET) {
            DeregisterAndWait(serverContext->ioCompletionPort, tcpAcceptSocket);
        }

        DestroyServerContext(serverContext);
    }

    if (tcpAcceptSocket != INVALID_SOCKET) {
        closesocket(tcpAcceptSocket);
    }

    WSACleanup();
}
```

## <a name="edge-triggered-udp-server"></a><span data-ttu-id="a3581-152">Serveur UDP déclenché par Edge</span><span class="sxs-lookup"><span data-stu-id="a3581-152">Edge-triggered UDP server</span></span>

<span data-ttu-id="a3581-153">Il s’agit d’une illustration simple de l’utilisation des API avec le déclenchement Edge.</span><span class="sxs-lookup"><span data-stu-id="a3581-153">This is a simple illustration of how to use the APIs with edge-triggering.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3581-154">Le serveur doit continuer à recevoir jusqu’à ce qu’il reçoive un **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="a3581-154">The server must keep receiving until it receives a **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="a3581-155">Dans le cas contraire, il est impossible de s’assurer qu’une arête en augmentation est observée.</span><span class="sxs-lookup"><span data-stu-id="a3581-155">Otherwise, it can't be sure that a rising edge will be observed.</span></span> <span data-ttu-id="a3581-156">Par conséquent, le socket du serveur doit également être non bloquant.</span><span class="sxs-lookup"><span data-stu-id="a3581-156">As such, the server's socket must also be non-blocking.</span></span>

<span data-ttu-id="a3581-157">Cet exemple utilise UDP pour démontrer l’absence d’une notification de **raccrochage** .</span><span class="sxs-lookup"><span data-stu-id="a3581-157">This example uses UDP to demonstrate the lack of a **HANGUP** notification.</span></span> <span data-ttu-id="a3581-158">En supposant que les applications d’assistance courantes créent des sockets UDP si nécessaire, il faut créer des libertés.</span><span class="sxs-lookup"><span data-stu-id="a3581-158">It takes some liberties with assuming the common helpers create UDP sockets if needed.</span></span>

```cpp
// This example assumes that substantially similar helpers are available for UDP sockets.
VOID SimpleEdgeTriggeredSample() {
    DWORD errorCode;
    WSADATA wsaData;
    SOCKET serverSocket = INVALID_SOCKET;
    SOCKET currentSocket;
    HANDLE ioCompletionPort = NULL;
    sockaddr_in serverAddress = { };
    u_long nonBlocking = 1;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    ULONG notificationCount;
    UINT32 events;
    CHAR dataBuffer[512];
    UINT32 datagramCount;
    int receiveResult;

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    ioCompletionPort = CreateIoCompletionPort(INVALID_HANDLE_VALUE, NULL, 0, 0);
    if (ioCompletionPort == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    serverSocket = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
    if (serverSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Register the server UDP socket before binding to a port to ensure data doesn't become
    // present before the registration. Otherwise, the server could miss the notification and
    // hang.
    //
    // Edge-triggered is not recommended with one-shot due to the difficulty in re-registering.
    registration.completionKey = (PVOID)serverSocket;
    registration.eventFilter = SOCK_NOTIFY_EVENT_IN;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_EDGE;
    registration.socket = serverSocket;
    errorCode = ProcessSocketNotifications(ioCompletionPort, 1, &registration, 0, 0, NULL, NULL);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    if (registration.registrationResult != ERROR_SUCCESS) {
        errorCode = registration.registrationResult;
        goto Exit;
    }

    // Use non-blocking sockets with edge-triggered notifications, since the data must be
    // drained before a rising edge can be observed again.
    errorCode = ioctlsocket(serverSocket, FIONBIO, &nonBlocking);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (bind(serverSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Create the client.
    // While CreateClientThread connects to a TCP socket and sends data over it, for this example
    // assume that CreateClientThread creates a UDP socket instead, and sends data over it.
    errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Receive the packets.
    datagramCount = 0;
    while (datagramCount < CLIENT_LOOP_COUNT) {

        wprintf_s(L"Waiting for client action...\r\n");

        if (!GetQueuedCompletionStatusEx(ioCompletionPort,
            &notification,
            1,
            &notificationCount,
            MAX_TIMEOUT,
            FALSE))
        {
            errorCode = GetLastError();
            goto Exit;
        }

        // The completion key is the socket we supplied above.
        //
        // This is true only because the registration supplied the socket as the completion
        // key. A more typical pattern is to supply a context pointer. This example supplies
        // the socket directly, for simplicity.
        //
        // The events are the integer value of the overlapped pointer.
        events = SocketNotificationRetrieveEvents(&notification);

        currentSocket = (SOCKET)notification.lpCompletionKey;
        if (events & SOCK_NOTIFY_EVENT_ERR) {
            // Obtain a more detailed error code by issuing a non-blocking receive.
            recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            errorCode = GetLastError();
            goto Exit;
        }

        if ((events & SOCK_NOTIFY_EVENT_IN) == 0) {
            continue;
        }

        // Keep looping receiving data until the read would block, otherwise the edge may not
        // have been reset.
        while (TRUE) {
            receiveResult = recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            if (receiveResult < 0) {
                errorCode = GetLastError();
                if (errorCode != WSAEWOULDBLOCK) {
                    goto Exit;
                }

                break;
            }

            datagramCount += 1;
            wprintf_s(L"Received client data.\r\n");
        }
    }

    wprintf_s(L"Received all data. Exiting... \r\n");
    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
    }

    if (serverSocket != INVALID_SOCKET) {
        if (ioCompletionPort != NULL) {
            DeregisterAndWait(ioCompletionPort, serverSocket);
        }

        closesocket(serverSocket);
    }

    if (ioCompletionPort != NULL) {
        CloseHandle(ioCompletionPort);
    }

    WSACleanup();
}
```

## <a name="multi-threaded-server"></a><span data-ttu-id="a3581-159">Serveur multithread</span><span class="sxs-lookup"><span data-stu-id="a3581-159">Multi-threaded server</span></span>

<span data-ttu-id="a3581-160">Cet exemple illustre un modèle d’utilisation multithread plus réaliste qui utilise les fonctionnalités de montée en puissance parallèle du port de terminaison d’e/s pour répartir le travail sur plusieurs threads de serveur.</span><span class="sxs-lookup"><span data-stu-id="a3581-160">This example demonstrates a more realistic multi-threaded use pattern that uses the I/O completion port's scale-out capabilities to distribute work across multiple server threads.</span></span> <span data-ttu-id="a3581-161">Le serveur utilise le déclenchement d’un niveau à une seule capture pour éviter que plusieurs threads sélectionnent des notifications pour le même socket et autorisent chaque thread à vider les données reçues segment par segment.</span><span class="sxs-lookup"><span data-stu-id="a3581-161">The server uses one-shot level-triggering to avoid multiple threads picking up notifications for the same socket, and to allow each thread to drain received data one chunk at a time.</span></span>

<span data-ttu-id="a3581-162">Il montre également quelques modèles courants utilisés avec le port de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3581-162">It also demonstrates some common patterns used with the completion port.</span></span> <span data-ttu-id="a3581-163">La clé de saisie semi-automatique est utilisée pour fournir un pointeur de contexte par socket.</span><span class="sxs-lookup"><span data-stu-id="a3581-163">The completion key is used to supply a per-socket context pointer.</span></span> <span data-ttu-id="a3581-164">Le pointeur de contexte a un en-tête qui décrit le type de socket utilisé, afin que plusieurs types de sockets puissent être utilisés sur un port de terminaison unique.</span><span class="sxs-lookup"><span data-stu-id="a3581-164">The context pointer has a header that describes the type of socket being used, so that multiple sockets types can be used on a single completion port.</span></span> <span data-ttu-id="a3581-165">Les commentaires dans l’exemple mettent en évidence que les saisies semi-automatiques arbitraires peuvent être déplacées dans la file d’attente (comme avec la fonction [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) ), et non uniquement les notifications de Socket.</span><span class="sxs-lookup"><span data-stu-id="a3581-165">Comments in the example highlight that arbitrary completions can be dequeued (just as with the [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) function), not only socket notifications.</span></span> <span data-ttu-id="a3581-166">L’API [**PostQueuedCompletionStatus**](/windows/win32/fileio/postqueuedcompletionstatus) est utilisée pour envoyer des messages aux threads et les mettre en éveil sans avoir à attendre l’arrivée d’une notification de Socket.</span><span class="sxs-lookup"><span data-stu-id="a3581-166">The [**PostQueuedCompletionStatus**](/windows/win32/fileio/postqueuedcompletionstatus) API is used to post messages to threads, and wake them without having to wait for the arrival of a socket notification.</span></span>

<span data-ttu-id="a3581-167">Enfin, l’exemple montre quelques subtilités de la désinscription et du nettoyage corrects des contextes de socket dans une charge de travail avec thread.</span><span class="sxs-lookup"><span data-stu-id="a3581-167">Finally, the example demonstrates some of the intricacies of correctly deregistering and cleaning up socket contexts in a threaded workload.</span></span> <span data-ttu-id="a3581-168">Dans cet exemple, le contexte de socket est implicitement détenu par le thread qui reçoit la notification.</span><span class="sxs-lookup"><span data-stu-id="a3581-168">In this example, socket context is implicitly owned by the thread that receives the notification.</span></span> <span data-ttu-id="a3581-169">Le thread maintient la propriété s’il ne parvient pas à inscrire la notification.</span><span class="sxs-lookup"><span data-stu-id="a3581-169">The thread maintains ownership if it fails to register the notification.</span></span>

```cpp
#define CLIENT_THREAD_COUNT         100
// The I/O completion port infrastructure ensures that the system isn't over-subscribed by
// ensuring server-side threads block if they exceed the number of logical processors. If the
// machine has more than 16 logical processors, then this can be observed by increasing this number.
#define SERVER_THREAD_COUNT         16
#define SERVER_DEQUEUE_COUNT        3
#define SERVER_EXIT_KEY             ((ULONG_PTR)-1)

typedef struct SERVER_THREAD_CONTEXT {
    SERVER_CONTEXT* commonContext;
    SRWLOCK stateLock;
    _Guarded_by_(stateLock) UINT32 deregisterCount;
    _Guarded_by_(stateLock) BOOLEAN shouldExit;
} SERVER_THREAD_CONTEXT;

typedef enum SOCKET_TYPE {
    SOCKET_TYPE_LISTENER,
    SOCKET_TYPE_ACCEPT
} SOCKET_TYPE;

typedef struct SOCKET_CONTEXT {
    SOCKET_TYPE socketType;
    SOCKET socket;
} SOCKET_CONTEXT;

VOID CancelServerThreadsAsync(_Inout_ SERVER_THREAD_CONTEXT* serverThreadContext) {
    AcquireSRWLockExclusive(&serverThreadContext->stateLock);
    serverThreadContext->shouldExit = TRUE;
    ReleaseSRWLockExclusive(&serverThreadContext->stateLock);
}

VOID IndicateServerThreadExit(_In_ HANDLE ioCompletionPort) {
    // Notify a server thread that it needs to exit. It can then notify the other threads when it
    // exits.
    //
    // If this fails, then server threads may hang, and this program will never terminate. That
    // is an unrecoverable error.
    if (!PostQueuedCompletionStatus(ioCompletionPort, 0, SERVER_EXIT_KEY, NULL)) {
        RaiseFailFastException(NULL, NULL, 0);
    }
}

VOID DestroySocketContext(_Inout_ _Post_invalid_ SOCKET_CONTEXT* socketContext) {
    if (socketContext->socket != INVALID_SOCKET) {
        closesocket(socketContext->socket);
    }

    free(socketContext);
}

DWORD AcceptConnection(_In_ SOCKET listenSocket, _Outptr_ SOCKET_CONTEXT** socketContextOut) {
    DWORD errorCode;
    SOCKET_CONTEXT* socketContext = NULL;

    socketContext = (SOCKET_CONTEXT*)malloc(sizeof(*socketContext));
    if (socketContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(socketContext, sizeof(*socketContext));
    socketContext->socketType = SOCKET_TYPE_ACCEPT;
    socketContext->socket = accept(listenSocket, NULL, NULL);
    if (socketContext->socket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    *socketContextOut = socketContext;
    socketContext = NULL;

Exit:
    if (socketContext != NULL) {
        _ASSERT(errorCode != ERROR_SUCCESS);
        DestroySocketContext(socketContext);
    }

    return errorCode;
}

DWORD
WINAPI
ServerThreadRoutine(_In_ PVOID serverThreadContextPointer) {
    DWORD errorCode;
    SERVER_THREAD_CONTEXT* serverThreadContext;
    HANDLE ioCompletionPort;
    // Accepting a connection requires two registrations: one to re-enable the listening socket
    // notification, and one to register the newly-accepted connection.
    SOCK_NOTIFY_REGISTRATION registrationBuffer[SERVER_DEQUEUE_COUNT * 2];
    UINT32 registrationCount;
    SOCK_NOTIFY_REGISTRATION* registration;
    OVERLAPPED_ENTRY notifications[SERVER_DEQUEUE_COUNT];
    UINT32 notificationCount;
    UINT32 events;
    SOCKET_CONTEXT* socketContext;
    SOCKET_CONTEXT* acceptedContext;
    BOOLEAN shouldExit;
    CHAR dataBuffer[512];

    serverThreadContext = (SERVER_THREAD_CONTEXT*)serverThreadContextPointer;
    ioCompletionPort = serverThreadContext->commonContext->ioCompletionPort;

    // Boot-strap the loop process.
    registrationCount = 0;

    // Keep looping, processing notifications until exit has been requested.
    while (TRUE) {

        AcquireSRWLockExclusive(&serverThreadContext->stateLock);
        shouldExit = serverThreadContext->shouldExit;
        ReleaseSRWLockExclusive(&serverThreadContext->stateLock);
        if (shouldExit) {
            goto Exit;
        }

        AcquireSRWLockExclusive(&g_printLock);
        wprintf_s(L"Server thread %d waiting for client action...\r\n", GetCurrentThreadId());
        ReleaseSRWLockExclusive(&g_printLock);

        // Process notifications and re-register one-shot notifications that were processed on a
        // previous iteration.
        errorCode = ProcessSocketNotifications(ioCompletionPort,
            registrationCount,
            (registrationCount == 0) ? NULL : registrationBuffer,
            MAX_TIMEOUT,
            RTL_NUMBER_OF(notifications),
            notifications,
            &notificationCount);

        // TODO: Production code should handle failure better. This can fail due to transient memory conditions, or due to
        // invalid input such as a bad handle. Retrying in case the memory conditions abate is
        // a reasonable strategy.
        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }

        // Check whether any registrations failed, and attempt to clean up if they did.
        errorCode = ERROR_SUCCESS;
        for (UINT32 i = 0; i < registrationCount; i += 1) {
            registration = &registrationBuffer[i];
            if (registration->registrationResult == ERROR_SUCCESS) {
                continue;
            }

            // Preserve the first failure code.
            if (errorCode == ERROR_SUCCESS) {
                errorCode = registration->registrationResult;
            }

            // All the registrations are oneshot, so if the registration failed, then only this thread
            // has access to the context. Attempt to clean up fully:
            // - The listening socket is owned by the main thread, so ignore that.
            // - If the socket hasn't been registered, just free its memory.
            // - Otherwise, attempt to deregister it.

            socketContext = (SOCKET_CONTEXT*)registration->completionKey;
            if (socketContext->socketType == SOCKET_TYPE_LISTENER) {
                continue;
            }

            // Best-effort de-registration. In case of failure, simply get rid of the socket and
            // context. This is safe to do because the notification for the socket can't be enabled.
            // Either it was never registered in the first place, or re-registration failed, and it
            // was previously disabled by nature of being a one-shot registration.
            registration->operation = SOCK_NOTIFY_OP_REMOVE;
            errorCode = ProcessSocketNotifications(ioCompletionPort,
                1,
                registration,
                0,
                0,
                NULL,
                NULL);

            if ((errorCode != ERROR_SUCCESS) ||
                (registration->registrationResult != ERROR_SUCCESS)) {
                DestroySocketContext(socketContext);
            }
        }

        // Process the notifications. Many will need to be re-enabled because they are one-shot,
        // so ensure that we can build that incrementally.
        registrationCount = 0;
        ZeroMemory(registrationBuffer, sizeof(registrationBuffer));

        for (UINT32 i = 0; i < notificationCount; i += 1) {
            if (notifications[i].lpCompletionKey == SERVER_EXIT_KEY) {
                _ASSERT(serverThreadContext->shouldExit);

                // On exit, this thread will post the next exit message.
                errorCode = ERROR_SUCCESS;
                goto Exit;
            }

            socketContext = (SOCKET_CONTEXT*)notifications[i].lpCompletionKey;
            events = SocketNotificationRetrieveEvents(&notifications[i]);

            // Process the socket notification, taking socket-specific actions.
            switch (socketContext->socketType) {
            case SOCKET_TYPE_LISTENER:

                // Accepting connections in response to notifications implicitly throttles
                // the rate at which incoming connections are accepted, and limits scale-out for
                // new connection acceptance. Consider using AcceptEx if greater scaling of
                //connection acceptance is desired.

                // Perform an accept regardless of the notification. The only possible notifications
                // are for available connections or error conditions. Any possible error conditions
                // will be processed as part of the accept.
                errorCode = AcceptConnection(socketContext->socket, &acceptedContext);
                if (errorCode == ERROR_SUCCESS) {
                    // Register the accepted connection.
                    registration = &registrationBuffer[registrationCount];
                    registration->socket = acceptedContext->socket;
                    registration->completionKey = acceptedContext;
                    registration->eventFilter = SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_HANGUP;
                    registration->operation =
                        SOCK_NOTIFY_OP_ENABLE;
                    registration->triggerFlags = SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                    registrationCount += 1;
                }

                // Re-arm the existing listening socket registration.
                registration = &registrationBuffer[registrationCount];
                registration->socket = socketContext->socket;
                registration->completionKey = socketContext;
                registration->eventFilter = SOCK_NOTIFY_EVENT_IN;
                registration->operation =
                    SOCK_NOTIFY_OP_ENABLE;
                registration->triggerFlags = SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                registrationCount += 1;
                break;

            case SOCKET_TYPE_ACCEPT:
                // The registration was removed. Clean up the context.
                if (events & SOCK_NOTIFY_EVENT_REMOVE) {
                    AcquireSRWLockExclusive(&serverThreadContext->stateLock);
                    serverThreadContext->deregisterCount += 1;
                    if (serverThreadContext->deregisterCount >= CLIENT_THREAD_COUNT) {
                        serverThreadContext->shouldExit = TRUE;
                    }
                    ReleaseSRWLockExclusive(&serverThreadContext->stateLock);

                    DestroySocketContext(socketContext);
                    continue;
                }

                registration = &registrationBuffer[registrationCount];

                // If a hangup occurred, then remove the registration. 
                if (events & SOCK_NOTIFY_EVENT_HANGUP) {
                    registration->eventFilter = 0;
                    registration->operation = SOCK_NOTIFY_OP_REMOVE;
                }

                // Receive data.
                if (events & (SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_ERR)) {
                    // TODO: Handle errors (for example, due to connection reset). The error from recv can
                    // be used to retrieve the underlying socket for a SOCK_NOTIFY_EVENT_ERR.
                    if (recv(socketContext->socket, dataBuffer, sizeof(dataBuffer), 0) < 0) {
                        registration->operation = SOCK_NOTIFY_OP_REMOVE;
                        registration->eventFilter = 0;
                    }
                    else {
                        registration->operation |=
                            SOCK_NOTIFY_OP_ENABLE;
                        registration->triggerFlags =
                            SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                        registration->eventFilter = SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_HANGUP;
                    }
                }

                registration->socket = socketContext->socket;
                registration->completionKey = socketContext;
                registrationCount += 1;
                break;

                // TODO:
                //
                // Other (potentially non-socket) I/O completion can be processed here. For instance,
                // this could also be processing disk I/O. The contexts will need to have a common
                // header that can be used to differentiate between the different context types,
                // similar to how the listening and accepted sockets are differentiated.
                //
                // case ... :

            default:
                _ASSERT(!"Unexpected socket type!");
                errorCode = ERROR_UNIDENTIFIED_ERROR;
                goto Exit;
            }
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    // If an error occurred, then ensure the other threads know they should exit.
    // TODO: use an error handling strategy that isn't just exiting.
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
        CancelServerThreadsAsync(serverThreadContext);
    }

    // Wake a remaining server thread.
    IndicateServerThreadExit(ioCompletionPort);

    AcquireSRWLockExclusive(&g_printLock);
    wprintf_s(L"Server thread %d exited\r\n", GetCurrentThreadId());
    ReleaseSRWLockExclusive(&g_printLock);

    return errorCode;
}

VOID MultiThreadedTcpServer() {
    DWORD errorCode;
    WSADATA wsaData;
    SERVER_THREAD_CONTEXT serverContext = { NULL, SRWLOCK_INIT, 0, FALSE };
    SOCKET_CONTEXT listenContext = {};
    SOCK_NOTIFY_REGISTRATION registration = {};
    HANDLE serverThreads[SERVER_THREAD_COUNT] = {};
    UINT32 serverThreadCount = 0;

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    listenContext.socket = INVALID_SOCKET;
    listenContext.socketType = SOCKET_TYPE_LISTENER;
    errorCode = CreateServerContext(&serverContext.commonContext);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Register the listening socket with the I/O completion port so the server threads are notified
    // of incoming connections.
    listenContext.socket = serverContext.commonContext->listenerSocket;
    registration.completionKey = &listenContext;
    registration.eventFilter = SOCK_NOTIFY_EVENT_IN;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_LEVEL | SOCK_NOTIFY_TRIGGER_PERSISTENT;
    registration.socket = listenContext.socket;
    errorCode = ProcessSocketNotifications(serverContext.commonContext->ioCompletionPort,
        1,
        &registration,
        0,
        0,
        NULL,
        NULL);

    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Create the server threads. These are likely over-subscribed, but the I/O completion port
    // ensures that they scale appropriately.
    while (serverThreadCount < RTL_NUMBER_OF(serverThreads)) {
        serverThreads[serverThreadCount] =
            CreateThread(NULL, 0, ServerThreadRoutine, &serverContext, 0, NULL);

        if (serverThreads[serverThreadCount] == NULL) {
            errorCode = GetLastError();
            goto Exit;
        }
    }

    // Create the client threads, which are badly over-subscribed.
    for (UINT32 i = 0; i < CLIENT_THREAD_COUNT; i += 1) {
        errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);

        // In case of error, ensure that all server threads know to exit.
        if (serverContext.commonContext != NULL) {
            CancelServerThreadsAsync(&serverContext);
            IndicateServerThreadExit(serverContext.commonContext->ioCompletionPort);
        }
    }

    if (serverThreadCount > 0) {
        wprintf_s(L"Waiting for %d server threads to exit...\r\n", serverThreadCount);
        errorCode = WaitForMultipleObjects(serverThreadCount, serverThreads, TRUE, INFINITE);
        _ASSERT(errorCode == ERROR_SUCCESS);
    }

    // TODO: In case of failure, clean up remaining state. For example, Accepted connections can be kept in
    // a global list, which can be closed from this thread.

    for (UINT32 i = 0; i < serverThreadCount; i += 1) {
        CloseHandle(serverThreads[i]);
    }

    DestroyServerContext(serverContext.commonContext);

    WSACleanup();
}
```

## <a name="see-also"></a><span data-ttu-id="a3581-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3581-170">See also</span></span>

* [<span data-ttu-id="a3581-171">ProcessSocketNotifications</span><span class="sxs-lookup"><span data-stu-id="a3581-171">ProcessSocketNotifications</span></span>](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications)
* [<span data-ttu-id="a3581-172">SOCK_NOTIFY_REGISTRATION</span><span class="sxs-lookup"><span data-stu-id="a3581-172">SOCK_NOTIFY_REGISTRATION</span></span>](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)
* [<span data-ttu-id="a3581-173">SocketNotificationRetrieveEvents</span><span class="sxs-lookup"><span data-stu-id="a3581-173">SocketNotificationRetrieveEvents</span></span>](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents)
