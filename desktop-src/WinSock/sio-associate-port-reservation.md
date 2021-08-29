---
description: Le code de contrôle associe un socket à une réservation persistante ou d’exécution pour un bloc de TCP ou UDP identifié par le jeton de réservation de port.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Code de contrôle SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a427cec68124cf0132b13a8d8420311106e8c8f3ba647ddcc912ef7f1415fb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244949"
---
# <a name="sio_associate_port_reservation-control-code"></a>Code de contrôle SIO_ASSOCIATE_PORT_RESERVATION

## <a name="description"></a>Description

Le code de contrôle de **\_ réservation de \_ port \_ SIO Associate** associe un socket à une réservation persistante ou d’exécution pour un bloc de TCP ou UDP identifié par le jeton de réservation de port.
Cette IOCTL doit être émise avant que le socket ne soit lié.
Si et quand le socket est lié, le port qui lui est assigné est sélectionné à partir de la réservation de port identifiée par le jeton donné.
Si aucun port n’est disponible à partir de la réservation spécifiée, l’appel de fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
Utilisez **la \_ \_ \_ réservation de port SIO Associate** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre contient un pointeur vers une structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) avec le jeton de la réservation de port TCP ou UDP à associer au socket.

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
|**\_e/s WSA \_ en attente** | L’opération d’e/s avec chevauchement est en cours. Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application. Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush IOCTL** . |
| **WSAEACCES** | Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès. Cette erreur est retournée dans plusieurs conditions pour les réservations de port persistantes, notamment : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application n’est pas exécutée dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ). |
| **WSAEFAULT** | Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel. Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | Une opération de blocage est actuellement en cours d'exécution. Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Cette erreur est retournée si une opération de blocage a été interrompue. |
| **WSAEINVAL** | Argument non valide fourni. Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Une opération de socket a rencontré un réseau inactif. Cette erreur est retournée si le sous-système réseau a échoué. |
| **WSAENOTSOCK** | Une opération a été tentée sur un qui n’est pas un Socket. Cette erreur est retournée si le *descripteur* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est également retournée si l’IOCTL de **\_ réservation de \_ port \_ SIO Associate** n’est pas prise en charge par le fournisseur de transport. Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL de **\_ réservation de \_ port \_ SIO Associate** est effectuée sur un socket autre que UDP ou TCP. |

## <a name="remarks"></a>Remarques

l’IOCTL de **\_ réservation de \_ PORT \_ SIO ASSOCIATE** est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.

Les applications et les services qui doivent réserver des ports sont répartis en deux catégories.
La première catégorie comprend des composants qui ont besoin d’un port particulier dans le cadre de leur fonctionnement.
De tels composants préfèrent généralement spécifier le port requis au moment de l’installation (dans un manifeste d’application, par exemple).
La deuxième catégorie comprend des composants qui ont besoin d’un port ou d’un bloc de ports disponibles au moment de l’exécution.
Ces deux catégories correspondent à des demandes de réservation de port génériques et spécifiques.
Les demandes de réservation spécifiques peuvent être persistantes ou d’exécution, tandis que les demandes de réservation de port génériques sont uniquement prises en charge au moment de l’exécution.

L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** est utilisée pour associer une réservation de port TCP ou UDP à une réservation persistante ou d’exécution.

La fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) permet à une application ou à un service de réserver un bloc persistant de ports TCP ou UDP.
Les réservations de port persistantes sont enregistrées dans un magasin persistant pour le module TCP ou UDP dans Windows.
Notez que le jeton pour une réservation de port persistant donnée peut changer chaque fois que le système est redémarré.

Une fois qu’une réservation de port TCP ou UDP persistante a été obtenue, une application peut demander des affectations de port à partir de la réservation de port en ouvrant un socket TCP ou UDP, puis en appelant la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) en spécifiant l’IOCTL de **réservation de \_ \_ port \_ SIO Associate** et en passant le jeton de réservation avant d’émettre un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sur le Socket.

Le [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL peut être utilisé pour demander une réservation d’exécution pour un bloc de ports TCP ou UDP.
Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée.
Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL a été appelée.
En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.

Une fois qu’une réservation de port TCP ou UDP du runtime a été obtenue, une application peut demander des affectations de port à partir de la réservation de port en ouvrant un socket TCP ou UDP, puis en appelant la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) en spécifiant l’IOCTL de **réservation de \_ \_ port \_ SIO Associate** et en passant le jeton de réservation avant d’émettre un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sur le Socket.

Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont NULL, le socket dans cette fonction sera traité comme un socket non superposé.
Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.
Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.

Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.

Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.
Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.

L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** peut échouer avec **WSAEINTR** ou **WSA_OPERATION_ABORTED** dans les cas suivants :

* La demande est annulée par le gestionnaire d’e/s.
* Le socket est fermé.

L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** transmise à la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** pour une réservation de port persistante ne peut être utilisée que dans une application lorsque l’utilisateur a ouvert une session en tant que membre du groupe administrateurs.
Si **SIO \_ associer \_ la \_ réservation de port** IOCTL est utilisée dans une application lorsque l’utilisateur n’est pas membre du groupe administrateurs, l’appel de fonction échoue et **WSAEACCES** est retourné.
l’utilisation de l’IOCTL de **\_ réservation de \_ PORT \_ SIO ASSOCIATE** peut également échouer en raison du contrôle de compte d’utilisateur (UAC) sur Windows Vista et versions ultérieures.
Si une application qui utilise cette IOCTL avec une réservation de port persistant est exécutée par un utilisateur ayant ouvert une session en tant que membre du groupe administrateurs autre que l’administrateur intégré, cet appel échoue, sauf si l’application a été marquée dans le fichier manifeste avec un **requestedExecutionLevel** défini sur *requireAdministrator*.
Si l’application ne dispose pas de ce fichier manifeste, un utilisateur ayant ouvert une session en tant que membre du groupe administrateurs autre que l’administrateur intégré doit exécuter l’application dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ) pour que cette fonction aboutisse.

## <a name="see-also"></a>Voir aussi

[**établis**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[socle](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
