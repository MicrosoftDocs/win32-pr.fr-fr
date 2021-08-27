---
description: Code de contrôle qui configure les paramètres de délai de retransmission initiaux (RTO) sur un Socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Code de contrôle SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 63ebbfd0d8d56c03d62c7bba417d69e3ac1a576abfc8c72ac489117a7d8b74c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097479"
---
# <a name="sio_tcp_initial_rto-control-code"></a>Code de contrôle SIO_TCP_INITIAL_RTO

## <a name="description"></a>Description

Le code de contrôle **SIO_TCP_INITIAL_RTO** configure les paramètres de délai de retransmission initiaux (RTO) sur un Socket.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
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
Utilisez **SIO_TCP_INITIAL_RTO** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre contient un pointeur vers le [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associé au socket.

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.

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
| **\_opération WSA \_ abandonnée** | L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application. Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl. |
| **WSAEACCES** | Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès. Cette erreur est retournée dans plusieurs conditions : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application ne s’exécute pas dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ). |
| **WSAEFAULT** | Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel. Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | Une opération de blocage est actuellement en cours d'exécution. Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue par un appel à *WSACancelBlockingCall*. Cette erreur est retournée si une opération de blocage a été interrompue. |
| **WSAEINVAL** | Argument non valide fourni. Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Une opération de socket a rencontré un réseau inactif. Cette erreur est retournée si le sous-système réseau a échoué. |
| **WSAENOTSOCK** | Une opération a été tentée sur un qui n’est pas un Socket. Cette erreur est retournée si le descripteur n’est pas un Socket. |
| **WSAEOPNOTSUPP** | L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est également retournée si le **SIO_TCP_INITIAL_RTO** IOCTL n’est pas pris en charge par le fournisseur de transport. |

## <a name="remarks"></a>Remarques

Une application peut utiliser le **SIO_TCP_INITIAL_RTO** ioctl pour contrôler les caractéristiques de retransmission initiales (SYN/SYN + ACK) d’un socket TCP, si nécessaire.
Si vous utilisez cette option, une application doit fournir des valeurs appropriées avant de démarrer une tentative de connexion TCP sur le Socket.

Le [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL permet à une application de configurer le délai de retransmission (SYN) initial (RTO) utilisé par le Socket.

Un pointeur vers une structure [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passée dans le paramètre *lpvInBuffer* permet à une application de configurer la durée de boucle initiale (RTT) initiale utilisée pour calculer le délai de retransmission.
L’application peut également configurer le nombre de retransmissions qui seront tentées avant que la tentative de connexion échoue.

## <a name="see-also"></a>Voir aussi

[socle](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
