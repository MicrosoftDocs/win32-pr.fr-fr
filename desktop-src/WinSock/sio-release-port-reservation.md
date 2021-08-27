---
description: Le code de contrôle libère une réservation d’exécution pour un bloc de ports TCP ou UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Code de contrôle SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8d949e325292210ec7126da5ddf65c6ff30c5aa151cfaf85331fb7ebf3e5b346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097489"
---
# <a name="sio_release_port_reservation-control-code"></a>Code de contrôle SIO_RELEASE_PORT_RESERVATION

## <a name="description"></a>Description

Le code de contrôle de **\_ réservation du \_ port \_** de la version de SiO libère une réservation d’exécution pour un bloc de ports TCP ou UDP.
La réservation d’exécution à libérer doit avoir été obtenue à partir du processus d’émission à l’aide du [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Paramètres

### <a name="s"></a>s

Descripteur identifiant un Socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Code de contrôle de l’opération.
Utilisez **la \_ \_ \_ réservation de port de libération SIO** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre contient un pointeur vers une structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) avec le jeton de la réservation de port TCP ou UDP à libérer.

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre doit avoir au moins la taille de la structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Pointeur vers la mémoire tampon de sortie.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cboutbuffer"></a>cbOutBuffer

Taille, en octets, de la mémoire tampon de sortie.
Ce paramètre doit avoir la valeur zéro.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.

Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.

Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.

Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.
La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.
L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.

### <a name="lpvoverlapped"></a>lpvOverlapped

Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.

Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).
Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.

Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.
Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).

### <a name="lpthreadid"></a>lpThreadId

Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.

**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Pointeur vers le code d’erreur.

**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.

Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.
Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Code d'erreur | Signification |
|------------|---------|
| **\_e/s WSA \_ en attente** | L’opération d’e/s avec chevauchement est en cours. Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application. Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl. |
| **WSAEFAULT** | Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel. Cette erreur renvoyée par le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenue dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | Une opération de blocage est actuellement en cours d'exécution. Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue par un appel à **WSACancelBlockingCall**. Cette erreur est retournée si une opération de blocage a été interrompue. |
| **WSAEINVAL** | Argument non valide fourni. Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Une opération de socket a rencontré un réseau inactif. Cette erreur est retournée si le sous-système réseau a échoué. |
| **WSAENOTSOCK** | Une opération a été tentée sur un qui n’est pas un Socket. Cette erreur est retournée si le *descripteur* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est également retournée si l’IOCTL de réservation de port de la **\_ version \_ \_ SIO** n’est pas prise en charge par le fournisseur de transport. Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL de **\_ réservation de \_ port \_ de libération SIO** est effectuée sur un socket autre que UDP ou TCP. |

## <a name="remarks"></a>Remarques

l’IOCTL de réservation de PORT de la **\_ version \_ \_ SIO** est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.

Les applications et les services qui doivent réserver des ports sont répartis en deux catégories.
La première catégorie comprend des composants qui ont besoin d’un port particulier dans le cadre de leur fonctionnement.
De tels composants préfèrent généralement spécifier le port requis au moment de l’installation (dans un manifeste d’application, par exemple).
La deuxième catégorie comprend des composants qui ont besoin d’un port ou d’un bloc de ports disponibles au moment de l’exécution.
Ces deux catégories correspondent à des demandes de réservation de port génériques et spécifiques.
Les demandes de réservation spécifiques peuvent être persistantes ou d’exécution, tandis que les demandes de réservation de port génériques sont uniquement prises en charge au moment de l’exécution.

Le [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL est utilisé pour demander une réservation au moment de l’exécution pour un bloc de ports TCP ou UDP.
Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée.
Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL a été appelée.
En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.

L’IOCTL de réservation de port de la **\_ version \_ \_ SIO** est utilisée pour libérer une réservation d’exécution pour un bloc de ports TCP ou UDP.

Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont **null**, le socket dans cette fonction sera traité comme un socket non superposé.
Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.
Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.

Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.

Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.
Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.

L’IOCTL de **réservation de \_ port de libération \_ \_ SIO** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :

* La demande est annulée par le gestionnaire d’e/s.
* Le socket est fermé.

## <a name="examples"></a>Exemples

L’exemple suivant acquiert une réservation de port d’exécution, puis libère la réservation de port d’exécution.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>Voir aussi

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_ASSOCIATE_PORT_RESERVATION**](sio-associate-port-reservation.md)

[socle](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
