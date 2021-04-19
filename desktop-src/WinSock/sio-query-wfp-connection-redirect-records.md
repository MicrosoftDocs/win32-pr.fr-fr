---
description: Le code de contrôle récupère l’enregistrement de redirection pour la connexion TCP/IP acceptée pour une utilisation par un service de redirection de plateforme de filtrage Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516989"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a>Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Description

Le code de contrôle des enregistrements de la **\_ \_ \_ connexion \_ \_ WFP de la requête SIO** récupère l’enregistrement de redirection pour la connexion TCP/IP acceptée pour une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Paramètres

### <a name="s"></a>s

Descripteur identifiant un Socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Code de contrôle de l’opération.
Utilisez **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion WFP de la requête SIO** pour cette opération.

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
| **ERREUR \_ de \_ mémoire tampon insuffisante** | La zone de données passée à un appel système est insuffisante. Cette erreur est retournée si la mémoire tampon vers laquelle pointe le paramètre *lpvOutBuffer* avec une taille de mémoire tampon passée dans le paramètre *cbOutBuffer* est trop petite. La taille de la mémoire tampon requise est retournée dans le paramètre *lpcbBytesReturned* . |
| **WSA_IO_PENDING** | Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement. |
| **WSA_OPERATION_ABORTED** | Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl. |
| **WSAEFAULT** | Le paramètre *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’un type de données **ULong** . |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTCONN** | Le socket *n'* est pas connecté. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si les enregistrements de la **\_ connexion WFP de la requête SIO \_ \_ \_ redirigent \_** IOCTL n’est pas pris en charge par le fournisseur de transport. |

## <a name="remarks"></a>Notes

Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion WFP de la requête SIO** sont pris en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.

WFP autorise l’accès au chemin de traitement des paquets TCP/IP, où les paquets sortants et entrants peuvent être examinés ou modifiés avant d’autoriser leur traitement ultérieur.
En appuyant sur le chemin de traitement TCP/IP, les éditeurs de logiciels indépendants (ISV) peuvent créer plus facilement des pare-feu, des logiciels antivirus, des logiciels de diagnostic et d’autres types d’applications et de services.
WFP fournit des composants en mode utilisateur et en mode noyau afin que les éditeurs de logiciels indépendants puissent participer aux décisions de filtrage qui ont lieu dans plusieurs couches de la pile de protocole TCP/IP et dans tout le système d’exploitation.
La fonctionnalité de redirection de connexion WFP permet à un pilote de noyau de légende WFP de rediriger une connexion localement vers un processus en mode utilisateur, d’effectuer l’inspection du contenu en mode utilisateur et de transférer le contenu inspecté à l’aide d’une connexion différente à la destination d’origine.

La **requête SIO la \_ \_ \_ connexion WFP \_ redirige les \_ enregistrements** IOCTL et plusieurs autres IOCTL connexes sont des composants en mode utilisateur utilisés pour permettre à plusieurs applications de proxy de connexion WFP d’inspecter le même flux de trafic de manière coopérative.
Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.
Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.
Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.

Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion WFP de la requête SIO** sont utilisés pour fournir le suivi de connexion en proxy sur les connexions de socket redirigées.
Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Les **enregistrements de la \_ connexion WFP de la requête SIO \_ \_ \_ redirect \_** sont utilisés par un service de redirection basé sur WFP pour récupérer l’enregistrement de redirection à partir de la connexion au paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par le biais de son compagnon en mode noyau inscrit sur **ALE_CONNECT_REDIRECT** couches dans un pilote en mode noyau
L’IOCTL du contexte de redirection de **\_ \_ \_ connexion \_ \_ WFP de la requête SIO** est utilisée par un service de redirection basé sur WFP pour récupérer le contexte de redirection d’un enregistrement de redirection à partir de la connexion de paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par son appel compagnon enregistré dans les couches de **\_ \_ redirection**
Le contexte de redirection est un contexte facultatif alloué par le pilote utilisé si l’état de redirection actuel d’une connexion est que la connexion a été redirigée par le service de redirection appelant ou que la connexion a été précédemment redirigée par le service de redirection appelant, mais redirigée ultérieurement par un autre service de redirection.
Pour une connexion de proxy TCP, le service de redirection transfère l’enregistrement de redirection récupéré au socket TCP qu’il utilise pour effectuer un proxy du contenu d’origine à l’aide de l’IOCTL **SIO \_ définir la \_ connexion WFP des \_ \_ \_ enregistrements de redirection** .

Lorsque le service de redirection redirige un socket non-TCP (UDP, par exemple), les enregistrements de redirection retournés par la **requête SIO les \_ \_ \_ \_ \_ enregistrements** de redirection de connexion WFP l’indiquent au service de redirection à l’aide de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) utilisée avec la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .
Le membre de contrôle de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) a un cmsg_type dans la structure **WSACMSGHDR** défini sur **l' \_ \_ \_ enregistrement de redirection de connexion IP**.
Le paramètre [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) doit être fourni par le service de redirection lors de l’acceptation de redirections non-TCP.

Pour le trafic non-TCP, l’enregistrement de redirection est transféré à l’aide de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) avec la fonction [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Notez que pour le trafic non-TCP, seul le paquet de création de flux contiendra l' **\_ \_ \_ enregistrement de redirection de connexion IP**.
Par conséquent, seul le premier paquet proxy doit inclure ces informations à l’aide de la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .

Étant donné que l’enregistrement de redirection WFP est un objet blob de données de longueur variable, l’appelant peut soit fournir une mémoire tampon de sortie importante (une mémoire tampon de 1 024 octets pointée par le paramètre *lpvOutBuffer* , par exemple), soit passer une taille de mémoire tampon de sortie dans le paramètre *cbOutBuffer* de 0 pour interroger la taille de mémoire tampon requise pour contenir l’objet BLOB retourné.
Si la taille de la mémoire tampon de sortie n’est pas suffisante pour contenir les données, les fonctions [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retournent l' **erreur \_ \_ mémoire tampon insuffisante** et la taille de mémoire tampon requise est retournée dans la valeur désignée par le paramètre *lpcbBytesReturned* .

L’application qui appelle le [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) n’a pas besoin de comprendre l’objet blob contenant le contexte de redirection récupéré.
Il s’agit d’un objet blob opaque de données que l’application doit récupérer et renvoyer au nouveau Socket.

## <a name="see-also"></a>Voir aussi

[**Options de socket IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
