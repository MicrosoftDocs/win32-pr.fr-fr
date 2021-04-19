---
description: Le code de contrôle permet à un socket de recevoir tous les paquets IPv4 ou IPv6 passant par une interface réseau.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Code de contrôle SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517267"
---
# <a name="sio_rcvall-control-code"></a>Code de contrôle SIO_RCVALL

## <a name="description"></a>Description
Le code de contrôle **SIO \_ RCVALL** permet à un socket de recevoir tous les paquets IPv4 ou IPv6 passant par une interface réseau.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Paramètres

### <a name="s"></a>s

Descripteur identifiant un Socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Code de contrôle de l’opération.
Utilisez **SIO \_ RCVALL** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée qui doit contenir la valeur de l’option.
Les valeurs possibles de l’option **SIO \_ RCVALL** IOCTL sont spécifiées dans l’énumération **RCVALL_VALUE** définie dans le fichier d’en-tête *Mstcpip. h* .

Les valeurs possibles pour **SIO \_ RCVALL** sont les suivantes :

| Valeur | Signification |
|-------|---------|
| **RCVALL \_ désactivé** | Désactivez cette option pour qu’un socket ne reçoive pas tous les paquets IPv4 ou IPv6 passant par une interface réseau. |
| **RCVALL \_ sur** | Activez cette option pour qu’un socket reçoive tous les paquets IPv4 ou IPv6 passant par une interface réseau. Cette option active le mode de proximité sur la carte d’interface réseau (NIC), si la carte réseau prend en charge le mode de proximité. Sur un segment LAN avec un concentrateur réseau, une carte réseau qui prend en charge le mode promiscuité capture tout le trafic IPv4 ou IPv6 sur le réseau local, y compris le trafic entre les autres ordinateurs sur le même segment de réseau local. Tous les paquets capturés (IPv4 ou IPv6, selon le socket) sont remis au socket brut. Cette option ne capture pas les autres paquets (paquets ARP, IPX et NetBEUI, par exemple) sur l’interface. Netmon utilise le même mode pour l’interface réseau, mais n’utilise pas cette option pour capturer le trafic. |
| **RCVALL \_ SOCKETLEVELONLY** | Cette fonctionnalité n’est pas implémentée pour l’instant. par conséquent, la définition de cette option n’a aucun effet. |
| **RCVALL \_ IPLEVEL** | Activez cette option pour qu’un socket IPv4 ou IPv6 reçoive tous les paquets au niveau IP en passant par une interface réseau. Cette option n’active pas le mode de proximité sur la carte d’interface réseau. Cette option affecte uniquement le traitement des paquets au niveau de l’adresse IP. La carte réseau reçoit toujours uniquement les paquets dirigés vers ses adresses de monodiffusion et de multidiffusion configurées. Toutefois, un socket avec cette option activée recevra non seulement les paquets dirigés vers des adresses IP spécifiques, mais recevra tous les paquets IPv4 ou IPv6 reçus par la carte réseau. Cette option ne capture pas les autres paquets (par exemple, les paquets ARP, IPX et NetBEUI) reçus sur l’interface. |

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre doit être supérieur ou égal à la taille du **RCVALL_VALUE** valeur d’énumération vers laquelle pointe le paramètre *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Pointeur vers la mémoire tampon de sortie.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cboutbuffer"></a>cbOutBuffer

Taille, en octets, de la mémoire tampon de sortie.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.
Ce paramètre n’est pas utilisé pour cette opération.

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
| **\_e/s WSA \_ en attente** | Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl. |
| **WSAEFAULT** | Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est également retournée si le paramètre *cbInBuffer* est inférieur à `sizeof(UCHAR)` ou si le paramètre *lpvInBuffer* pointe vers une valeur qui n’est pas une **RCVALL_VALUE** valeur d’énumération. Cette erreur peut également être renvoyée si l’interface réseau associée au socket est introuvable. Cela peut se produire si l’interface réseau associée au socket est supprimée ou supprimée (par exemple, un périphérique réseau PCMCIA ou USB). |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOBUFS** | Aucun espace de mémoire tampon n’est disponible. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si l’IOCTL **SIO \_ RCVALL** n’est pas prise en charge par le fournisseur de transport. |

## <a name="remarks"></a>Notes

L’IOCTL **SIO \_ RCVALL** est prise en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.

L’IOCTL **SIO \_ RCVALL** permet à un socket de recevoir tous les paquets IPv4 ou IPv6 sur une interface réseau.
Le descripteur de socket passé à la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** doit être l’un des suivants :

* Un socket IPv4 qui a été créé avec la famille d’adresses définie sur AF_INET, le type de socket défini sur SOCK_RAW et le protocole défini sur IPPROTO_IP.
* Un socket IPv6 qui a été créé avec la famille d’adresses définie sur AF_INET6, le type de socket défini sur SOCK_RAW et le protocole défini sur IPPROTO_IPV6.

Pour plus d’informations sur les sockets bruts, consultez [**sockets bruts TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

Le socket doit également être lié à une interface IPv4 ou IPv6 locale explicite, ce qui signifie que vous ne pouvez pas effectuer de liaison pour **inadr \_ any** ou **in6addr \_ any**.

Une fois que le socket est lié et que l’IOCTL s’est terminée avec succès, les appels aux fonctions [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) renvoient des datagrammes IPv4 passant par l’interface IPv4 donnée ou retournent des datagrammes IPv6 passant par l’interface IPv6 donnée.
Notez que vous devez fournir une mémoire tampon suffisamment grande.
La définition de cette IOCTL ne capture que les paquets IPv4 ou IPv6 sur une interface donnée.
Cette IOCTL ne capture pas d’autres paquets (paquets ARP, IPX et NetBEUI, par exemple) sur l’interface.

Un socket lié à une interface locale spécifique avec l’IOCTL **SIO \_ RCVALL** recevra uniquement les paquets passant par cette interface.
Elle ne reçoit pas de paquets reçus sur une autre interface et est transférée vers une autre interface différente du socket lié à **SIO \_ RCVALL** ioctl.

Sur Windows Server 2008 et versions antérieures, le paramètre IOCTL **SIO \_ RCVALL** ne capture pas les paquets locaux envoyés à partir d’une interface réseau.
Cela inclut les paquets reçus sur une autre interface et a transmis l’interface réseau spécifiée pour l’IOCTL **SIO \_ RCVALL** .

Sur Windows 7 et Windows Server 2008 R2, cela a été modifié afin que les paquets locaux envoyés à partir d’une interface réseau soient également capturés.
Cela comprend les paquets reçus sur une autre interface, puis le transfert de l’interface réseau liée au socket avec **SIO \_ RCVALL** ioctl.

La définition de cette IOCTL requiert des privilèges d’administrateur sur l’ordinateur local.

Cette fonctionnalité est parfois appelée « mode promiscuité ».
Toute modification directe de l’application de cette option sur une interface, puis vers une autre interface avec un appel unique à l’aide de cette IOCTL n’est pas prise en charge.
Une application doit tout d’abord utiliser cette IOCTL pour désactiver le comportement sur la première interface, puis utiliser cette IOCTL pour activer le comportement sur une nouvelle interface.

## <a name="see-also"></a>Voir aussi

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Sockets bruts TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
