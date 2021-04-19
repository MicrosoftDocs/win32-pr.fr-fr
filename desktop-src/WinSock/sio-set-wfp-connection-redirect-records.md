---
description: Le code de contrôle définit l’enregistrement de redirection sur le nouveau socket TCP utilisé pour la connexion du service de redirection.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, code de contrôle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529345"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, code de contrôle

## <a name="description"></a>Description

Le code de contrôle des **\_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** définit l’enregistrement de redirection sur le nouveau socket TCP utilisé pour se connecter à la destination finale en vue d’une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>Paramètres

### <a name="s"></a>s

Descripteur identifiant un Socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Code de contrôle de l’opération.
Utilisez **SIO pour \_ définir les \_ \_ \_ \_ enregistrements de redirection de connexion WFP** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre contient un pointeur vers l’enregistrement de redirection WFP associé au socket.

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
| **\_opération WSA \_ abandonnée** | L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application. Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl. |
| **WSAEACCES** | Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès. Cette erreur est retournée dans plusieurs conditions : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application ne s’exécute pas dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ). |
| **WSAEFAULT** | Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel. Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | Une opération de blocage est actuellement en cours d'exécution. Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue par un appel à **WSACancelBlockingCall**. Cette erreur est retournée si une opération de blocage a été interrompue. |
| **WSAEINVAL** | Argument non valide fourni. Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié. |
| **WSAENETDOWN** | Une opération de socket a rencontré un réseau inactif. Cette erreur est retournée si le sous-système réseau a échoué. |
| **WSAENOTSOCK** | Une opération a été tentée sur un qui n’est pas un Socket. Cette erreur est retournée si le *descripteur* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est également retournée si **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** ne sont pas pris en charge par le fournisseur de transport. |

## <a name="remarks"></a>Notes

Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion SIO Set WFP** sont pris en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.

WFP autorise l’accès au chemin de traitement des paquets TCP/IP, où les paquets sortants et entrants peuvent être examinés ou modifiés avant d’autoriser leur traitement ultérieur.
En appuyant sur le chemin de traitement TCP/IP, les éditeurs de logiciels indépendants (ISV) peuvent créer plus facilement des pare-feu, des logiciels antivirus, des logiciels de diagnostic et d’autres types d’applications et de services.
WFP fournit des composants en mode utilisateur et en mode noyau afin que les éditeurs de logiciels indépendants puissent participer aux décisions de filtrage qui ont lieu dans plusieurs couches de la pile de protocole TCP/IP et dans tout le système d’exploitation.
La fonctionnalité de redirection de connexion WFP permet à un pilote de noyau de légende WFP de rediriger une connexion localement vers un processus en mode utilisateur, d’effectuer l’inspection du contenu en mode utilisateur et de transférer le contenu inspecté à l’aide d’une connexion différente à la destination d’origine.

La **\_ connexion SIO \_ Set \_ WFP \_ redirige les \_ enregistrements** IOCTL et plusieurs autres IOCTL connexes sont des composants en mode utilisateur utilisés pour permettre à plusieurs applications de proxy de connexion WFP d’inspecter le même flux de trafic de manière coopérative.
Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.
Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.
Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.

Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion SIO Set WFP** permettent d’assurer le suivi des connexions en proxy sur les connexions de socket redirigées.
Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Le [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL est utilisé par un service de redirection basé sur WFP pour récupérer l’enregistrement de redirection à partir de la connexion de paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou un socket UDP, par exemple) redirigé vers celui-ci par son compagnon en mode noyau qui est inscrit aux couches de  **\_ \_ redirection de connexion ALE** dans un pilote en mode noyau.
L’IOCTL [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) récupère le contexte de redirection pour un enregistrement de redirection, qui est utilisé.
Le contexte de redirection est facultatif et est utilisé si l’état de redirection actuel d’une connexion est que la connexion a été redirigée par le service de redirection appelant ou si la connexion a été précédemment redirigée par le service de redirection appelant, mais redirigée ultérieurement par un autre service de redirection. Le service de redirection transfère l’enregistrement de redirection récupéré au socket TCP qu’il utilise pour effectuer un proxy du contenu d’origine à l’aide de l' **SIO \_ définir la \_ connexion WFP des \_ \_ \_ enregistrements de redirection** ioctl.

L’application qui appelle **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** n’a pas besoin de comprendre l’objet blob contenant l’enregistrement de redirection en cours de définition.
Il s’agit d’un objet blob opaque de données que l’application doit renvoyer au nouveau Socket.

## <a name="see-also"></a>Voir aussi

[**Options de socket IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
