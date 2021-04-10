---
description: Le code de contrôle active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Code de contrôle SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114903"
---
# <a name="sio_keepalive_vals-control-code"></a>Code de contrôle SIO_KEEPALIVE_VALS

## <a name="description"></a>Description

Le code de contrôle **\_ KeepAlive SIO \_ Vals** active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Utilisez **SIO \_ KeepAlive \_ Vals** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre doit pointer vers une structure **\_ KeepAlive TCP** .

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre doit être supérieur ou égal à la taille de la **structure \_ KeepAlive TCP** vers laquelle pointe le paramètre *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Pointeur vers la mémoire tampon de sortie.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cboutbuffer"></a>cbOutBuffer

Taille, en octets, de la mémoire tampon de sortie.
Ce paramètre doit avoir la valeur zéro.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.
Ce paramètre retourné pointe vers une valeur **DWORD** égale à zéro pour cette opération, car il n’y a pas de sortie.

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
|**\_e/s WSA \_ en attente** | Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH IOCTL** . |
| **WSAEFAULT** | Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. Cette erreur est retournée pour un socket datagramme. |
| **WSAENOTSOCK** | Le descripteur s n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si le **SIO \_ KeepAlive \_ Vals** IOCTL n’est pas pris en charge par le fournisseur de transport. |

## <a name="remarks"></a>Notes

Le **SIO \_ KeepAlive \_ Vals** IOCTL est pris en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.

Le code de contrôle **\_ KeepAlive \_ Vals SIO** active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP utilisés pour les paquets TCP Keep-Alive.
Pour plus d’informations sur l’option Keep-Alive, consultez la section 4.2.3.6 sur la configuration requise pour les hôtes Internet — couches de communication spécifiées dans le document RFC 1122 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF.
(Cette ressource peut uniquement être disponible en anglais.)

Le paramètre *lpvInBuffer* doit pointer vers une structure **TCP \_ KeepAlive** définie dans le fichier d’en-tête *Mstcpip. h* .
Cette structure est définie comme suit :

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

La valeur spécifiée dans le membre **microphone** détermine si TCP Keep-Alive est activé ou désactivé.
Si le membre **microphone** est défini sur une valeur différente de zéro, TCP Keep-Alive est activé et les autres membres de la structure sont utilisés.
Le membre **keepAliveTime** spécifie le délai d’attente, en millisecondes, sans activité jusqu’à l’envoi du premier paquet Keep-Alive.
Le membre **keepAliveInterval** spécifie l’intervalle, en millisecondes, entre l’envoi des paquets Keep-Alive successifs si aucun accusé de réception n’est reçu.

L’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , qui est l’une des [**Options de socket SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), peut également être utilisée pour activer ou désactiver le protocole TCP Keep-Alive sur une connexion, ainsi que pour interroger l’état actuel de cette option.
Pour demander si TCP Keep-Alive est activé sur un socket, la fonction getsockopt peut être appelée avec l’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Pour activer ou désactiver le protocole TCP Keep-Alive, la fonction **setsockopt** peut être appelée avec l’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Si TCP Keep-Alive est activé avec [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), les paramètres TCP par défaut sont utilisés pour le délai d’expiration et l’intervalle Keep-Alive, à moins que ces valeurs aient été modifiées à l’aide de **SIO \_ KeepAlive \_ Vals**.

La valeur par défaut au niveau du système du délai d’expiration Keep-Alive est contrôlable via le paramètre de Registre [**keepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) qui prend une valeur en millisecondes. Si la clé n’est pas définie, le délai d’expiration persistant par défaut est de 2 heures.
La valeur par défaut à l’ensemble du système de l’intervalle Keep-Alive est contrôlable via le paramètre de Registre [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) qui prend une valeur en millisecondes. Si la clé n’est pas définie, l’intervalle de conservation par défaut est de 1 seconde.

Sur Windows Vista et versions ultérieures, le nombre de sondes KeepAlive (retransmissions de données) est défini sur 10 et ne peut pas être modifié.

Sur Windows Server 2003, Windows XP et Windows 2000, le paramètre par défaut pour le nombre de sondes KeepAlive est 5.
Le nombre de sondes KeepAlive est contrôlable via les paramètres de Registre **TcpMaxDataRetransmissions** et [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .
Le nombre de sondes KeepAlive est défini sur la plus grande des deux valeurs de clé de registre.
Si ce nombre est 0, les sondes de conservation des connexions actives ne sont pas envoyées.
Si ce nombre est supérieur à 255, il est ajusté à 255.

## <a name="see-also"></a>Voir aussi

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[socle](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
