---
description: Le code de contrôle configure un socket TCP pour une latence plus faible et des opérations plus rapides sur l’interface de bouclage.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Code de contrôle SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740408"
---
# <a name="sio_loopback_fast_path-control-code"></a>Code de contrôle SIO_LOOPBACK_FAST_PATH

## <a name="description"></a>Description

le code de contrôle de **SIO \_ LOOPBACK \_ FAST \_ PATH** configure un socket TCP pour une latence plus faible et des opérations plus rapides sur l’interface de bouclage.

**Important**  le **\_ \_ \_ chemin d’accès FAST de bouclage SIO** est déconseillé et il n’est pas recommandé de l’utiliser dans votre code.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
utilisez **SIO \_ LOOPBACK \_ FAST \_ chemin d’accès** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre contient un pointeur vers une valeur booléenne qui indique si le socket doit être configuré pour les opérations de bouclage rapide.

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
|**\_e/s WSA \_ en attente** | L’opération d’e/s avec chevauchement est en cours. Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application. Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush IOCTL** . |
| **WSAEACCES** | Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès. Cette erreur est retournée dans plusieurs conditions pour les réservations de port persistantes, notamment : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application n’est pas exécutée dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ). |
| **WSAEFAULT** | Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel. Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | Une opération de blocage est actuellement en cours d'exécution. Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Cette erreur est retournée si une opération de blocage a été interrompue. |
| **WSAEINVAL** | Argument non valide fourni. Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Une opération de socket a rencontré un réseau inactif. Cette erreur est retournée si le sous-système réseau a échoué. |
| **WSAENOTSOCK** | Une opération a été tentée sur un qui n’est pas un Socket. Cette erreur est retournée si le *descripteur* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge. cette erreur est également retournée si **le \_ \_ \_ chemin d’accès FAST de bouclage SIO** n’est pas pris en charge par le fournisseur de transport. |

## <a name="remarks"></a>Remarques

une application peut utiliser le **\_ bouclage SIO \_ FAST \_ chemin** IOCTL pour réduire la latence et améliorer les performances des opérations de bouclage sur un socket TCP.
Cette IOCTL demande que la pile TCP/IP utilise un chemin d’accès rapide spécial pour les opérations de bouclage sur ce Socket.
l’IOCTL du **\_ \_ \_ chemin d’accès du FAST de bouclage SIO** peut être utilisé uniquement avec les sockets TCP.
Cette IOCTL doit être utilisée des deux côtés de la session de bouclage.
Le chemin d’accès rapide de bouclage TCP est pris en charge à l’aide de l’interface de bouclage IPv4 ou IPv6.

Le socket qui prévoit d’initier la demande de connexion doit appliquer cette IOCTL avant d’effectuer la demande de connexion.
Par conséquent, le socket utilisé par la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)ou [**WSACONNECTBYNAME**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) pour initier la connexion doit appliquer cette ioctl pour utiliser le chemin d’accès rapide pour les opérations de bouclage.

Le socket qui écoute la demande de connexion doit appliquer ce IOCTL avant d’accepter la connexion.
Par conséquent, le socket utilisé par la fonction listen doit appliquer cette IOCTL afin que tous les sockets acceptés utilisent le chemin d’accès rapide pour le bouclage.
Tous les sockets retournés par la fonction listen et transmis à la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**accepted**](/windows/desktop/api/winsock/nf-winsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) sont marqués pour utiliser le chemin d’accès rapide spécial pour les opérations de bouclage.

Une fois qu’une application établit la connexion sur une interface de bouclage à l’aide du chemin d’accès rapide, tous les paquets pour la durée de vie de la connexion doivent utiliser le chemin d’accès rapide.

l’application de **SIO \_ LOOPBACK \_ FAST \_ chemin d’accès** à un socket qui sera connecté à un chemin d’accès sans bouclage n’aura aucun effet.

Cette optimisation de bouclage TCP entraîne des paquets qui transitent par la couche de transport (TL) au lieu du bouclage traditionnel via la couche réseau.
Cette optimisation améliore la latence des paquets de bouclage.
Une fois qu’une application a défini un paramètre de niveau de connexion pour utiliser le chemin d’accès rapide de bouclage, tous les paquets suivent le chemin de bouclage.
Pour les communications de bouclage, la congestion et le rejet de paquets ne sont pas attendus.
La notion de contrôle d’encombrement et de remise fiable dans TCP n’est pas nécessaire.
Toutefois, cela n’est pas vrai pour le contrôle de Flow.
Sans contrôle de Flow, l’expéditeur peut saturer la mémoire tampon de réception, ce qui se traduit par un comportement de bouclage TCP erroné.
Le contrôle de Flow dans le chemin de bouclage optimisé TCP est conservé en plaçant les demandes Send dans une file d’attente.
Lorsque la mémoire tampon de réception est pleine, la pile TCP/IP garantit que les envois ne se terminent pas tant que la file d’attente ne prend pas en service le contrôle de Workflow.

les connexions de bouclage TCP fast path en présence d’une légende de plateforme de filtrage Windows (WFP) pour les données de connexion doivent prendre le chemin lent non optimisé pour le bouclage.
Par conséquent, les filtres WFP empêchent l’utilisation de ce nouveau chemin d’accès rapide de bouclage.
quand un filtre WFP est activé, le système utilise le chemin d’accès lent même si le **\_ \_ \_ chemin d’accès de FAST de bouclage SIO** a été défini.
Cela garantit que les applications en mode utilisateur disposent de la fonctionnalité de sécurité WFP complète.

par défaut, **le \_ \_ \_ chemin d’accès FAST de bouclage SIO** est désactivé.

seul un sous-ensemble des options de socket TCP/IP est pris en charge lorsque le **SIO \_ loopback \_ FAST \_ path** IOCTL est utilisé pour activer le chemin d’accès rapide de bouclage sur un socket.
La liste des options prises en charge comprend les éléments suivants :

* **\_TTL IP**
* **monodiffusion IP \_ \_ si**
* **\_Tronçons de monodiffusion IPv6 \_**
* **Monodiffusion IPV6 \_ \_ si**
* **\_V6ONLY IPv6**
* **\_accepter l' \_ acceptation conditionnelle**
* **\_EXCLUSIVEADDRUSE**
* **\_ \_ l’évolutivité des ports**
* **\_RCVBUF**
* **\_REUSEADDR**
* **\_BSDURGENT TCP**

## <a name="see-also"></a>Voir aussi

[**Options de socket IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**Options de socket IPPROTO_IPV6**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**Options de socket IPPROTO_TCP**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Options de socket SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
