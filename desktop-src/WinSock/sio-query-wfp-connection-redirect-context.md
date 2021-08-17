---
description: le code de contrôle récupère le contexte de redirection pour un enregistrement de redirection utilisé par un service de redirection de plateforme de filtrage Windows.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 268e1bf44c1370e49116414a367119ea8eb008a2711cbfcebdf64f6c3c1b8d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244939"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a>Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT

## <a name="description"></a>Description

le code de contrôle de contexte de redirection de **\_ \_ \_ connexion \_ \_ wfp de la requête SIO** récupère le contexte de redirection pour un enregistrement de redirection utilisé par un service de redirection de plateforme de filtrage Windows (WFP).

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
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
Utilisez **le \_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Pointeur vers la mémoire tampon de sortie.
Ce paramètre doit pointer vers un type de données **ULong** si les paramètres *lpOverlapped* et *lpCompletionRoutine* ont la **valeur null**.

### <a name="cboutbuffer"></a>cbOutBuffer

Taille, en octets, de la mémoire tampon de sortie.
Ce paramètre doit avoir au moins la taille d’un type de données **ULong** .

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
| **\_e/s WSA \_ en attente** | Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement. |
| **\_opération WSA \_ abandonnée** | Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande SIO_FLUSH IOCTL. |
| **WSAEFAULT** | Le paramètre *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’un type de données **ULong** . |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTCONN** | Le socket *n'* est pas connecté. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si l’IOCTL du **\_ \_ \_ \_ \_ contexte de redirection de la connexion WFP de la requête SIO** n’est pas prise en charge par le fournisseur de transport. |

## <a name="remarks"></a>Remarques

l’IOCTL du **\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO** est prise en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.

WFP autorise l’accès au chemin de traitement des paquets TCP/IP, où les paquets sortants et entrants peuvent être examinés ou modifiés avant d’autoriser leur traitement ultérieur.
En appuyant sur le chemin de traitement TCP/IP, les éditeurs de logiciels indépendants (ISV) peuvent créer plus facilement des pare-feu, des logiciels antivirus, des logiciels de diagnostic et d’autres types d’applications et de services.
WFP fournit des composants en mode utilisateur et en mode noyau afin que les éditeurs de logiciels indépendants puissent participer aux décisions de filtrage qui ont lieu dans plusieurs couches de la pile de protocole TCP/IP et dans tout le système d’exploitation.
La fonctionnalité de redirection de connexion WFP permet à un pilote de noyau de légende WFP de rediriger une connexion localement vers un processus en mode utilisateur, d’effectuer l’inspection du contenu en mode utilisateur et de transférer le contenu inspecté à l’aide d’une connexion différente à la destination d’origine.

L’IOCTL du **\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO** et plusieurs autres IOCTL connexes sont des composants en mode utilisateur permettant d’autoriser plusieurs applications de proxy de connexion WFP à inspecter le même flux de trafic de manière coopérative.
Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.
Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.
Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.

L’IOCTL du **\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO** permet à plusieurs applications de proxy de connexion WFP d’inspecter le même flux de trafic de manière coopérative.
Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.
Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.
Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.
L’IOCTL du **\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO** est utilisée pour fournir le suivi de connexion en proxy sur les connexions de socket redirigées.
Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Les **enregistrements de la \_ connexion WFP de la requête SIO \_ \_ \_ redirect \_** sont utilisés par un service de redirection basé sur WFP pour récupérer l’enregistrement de redirection à partir de la connexion au paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par le biais de son compagnon en mode noyau inscrit dans des couches de **\_ \_ redirection ALE** .
L’IOCTL du contexte de redirection de **\_ \_ \_ connexion \_ \_ WFP de la requête SIO** est utilisée par un service de redirection basé sur WFP pour récupérer le contexte de redirection d’un enregistrement de redirection à partir de la connexion de paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par le biais de sa légende associée inscrite sur **ALE_CONNECT_REDIRECT**
Le contexte de redirection est facultatif et est utilisé si l’état de redirection actuel d’une connexion est que la connexion a été redirigée par le service de redirection appelant ou si la connexion a été précédemment redirigée par le service de redirection appelant, mais redirigée ultérieurement par un autre service de redirection.
Le service de redirection transfère l’enregistrement de redirection récupéré au socket TCP qu’il utilise pour effectuer un proxy du contenu d’origine à l’aide de l' **SIO \_ définir la \_ connexion WFP des \_ \_ \_ enregistrements de redirection** ioctl.

Étant donné que le contexte de redirection WFP est un objet blob de données de longueur variable défini par le service de redirection, l’appelant peut soit fournir une mémoire tampon de sortie importante (une mémoire tampon de 1 Ko pointée par le paramètre *lpvOutBuffer* , par exemple), soit transmettre comme taille de mémoire tampon de sortie dans le paramètre *cbOutBuffer* de 0 pour interroger la taille de mémoire tampon requise pour
Si la taille de la mémoire tampon de sortie n’est pas suffisante pour conserver les données, les fonctions [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retournent l' **erreur \_ \_ mémoire tampon insuffisante** et la taille de mémoire tampon requise est retournée dans la valeur désignée par le paramètre *lpcbBytesReturned* .

L’application qui appelle **la \_ requête SIO \_ WF \ P_CONNECTION \_ Rediriger les \_ enregistrements** IOCTL n’a pas besoin de comprendre l’objet blob contenant les enregistrements de redirection récupérés.
Il s’agit d’un objet blob opaque de données que l’application doit récupérer et renvoyer au nouveau Socket.

## <a name="see-also"></a>Voir aussi

[**Options de socket IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**](sio-set-wfp-connection-redirect-records.md)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
