---
description: Code de contrôle obtient une liste d’adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Code de contrôle SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523331"
---
# <a name="sio_address_list_query-control-code"></a>Code de contrôle SIO_ADDRESS_LIST_QUERY

## <a name="description"></a>Description

Le code de contrôle de requête de la **\_ liste d’adresses \_ \_ SIO** obtient une liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.
La liste des adresses varie en fonction de la famille d’adresses et certaines adresses sont exclues de la liste.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
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
Utilisez **la \_ \_ \_ requête de liste d’adresses SIO** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Pointeur vers la mémoire tampon de sortie.

### <a name="cboutbuffer"></a>cbOutBuffer

Taille, en octets, de la mémoire tampon de sortie.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.

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

Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.

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
| **\_opération WSA \_ abandonnée** | Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl. |
| **WSAEFAULT** | Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbInBuffer* n’a pas la valeur **null**. |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOBUFS** | Aucun espace de mémoire tampon n’est disponible. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si l’IOCTL de la **\_ requête de \_ liste \_ d’adresses SIO** n’est pas prise en charge par le fournisseur de transport. |

## <a name="remarks"></a>Notes

La **requête IOCTL de \_ \_ liste \_ d’adresses SIO** est prise en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.

Le code de contrôle de requête de la **\_ liste d’adresses \_ \_ SIO** obtient une liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.
La liste des adresses varie en fonction de la famille d’adresses.

Pour la famille d’adresses inet6 de la même \_ façon, toutes les adresses sont retournées, à l’exception des suivantes :

* Toute adresse IP où l’état de détection d’adresse dupliquée (DAD) n’est pas IpDadStatePreferred.
* Toute adresse IP avec un niveau d’étendue inférieur à ScopeLevelSubnet sur une interface où le type d’interface est **si le \_ type de \_ \_ bouclage logiciel** est activé.
Cela signifie que les adresses Link-local (FE80 : *) et de bouclage ( :: 1) sur les interfaces de si le type de **\_ \_ \_ bouclage logiciel** est exclu, mais pas si ces adresses se trouvent sur une interface avec un type différent.

Pour la famille d’adresses d' **\_ inet AF** , toutes les adresses sont retournées, à l’exception des suivantes :

* Toute adresse IP où l’état de détection d’adresse dupliquée (DAD) n’est pas IpDadStatePreferred.
* Toute adresse IP sur une interface où le type d’interface est **si le \_ type de \_ \_ bouclage logiciel** et le lien est local.
Cela signifie que les adresses lien-local (169,254.*) et de bouclage (127.*) sur les interfaces de si le type de **\_ \_ \_ bouclage logiciel** est exclu, mais pas si ces adresses se trouvent sur une interface avec un type différent.

Pour plus d’informations sur l’État DAD, consultez la documentation d’assistance IP sur l’énumération [**IP \_ Dad \_ State**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) et la structure d' [**\_ \_ \_ adresse de monodiffusion de carte IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) et la documentation MIB sur la structure de [**\_ \_ ligne MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .
Pour plus d’informations sur le type d’interface, consultez la documentation d’assistance IP sur la structure d' [**\_ \_ adresses IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) et la fonction [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) et la documentation MIB sur [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.
Pour plus d’informations sur le niveau de l’étendue, consultez la documentation d’assistance IP sur la structure [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) et l’énumération [**\_ au niveau**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) de l’étendue.

La liste renvoyée dans la mémoire tampon de sortie vers laquelle pointe le paramètre *lpvOutBuffer* se présente sous la forme d’une structure de [**liste d' \_ adresses \_ de sockets**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .

Si la mémoire tampon de sortie spécifiée dans le paramètre *lpvOutBuffer* n’est pas assez grande pour contenir la liste d’adresses, l' **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).
La taille requise, en octets, de la mémoire tampon de sortie est retournée dans le paramètre *lpcbBytesReturned* dans ce cas.
Notez que le code d’erreur [WSAEFAULT](windows-sockets-error-codes-2.md) est également retourné si le paramètre *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.

La requête IOCTL de la **\_ liste d’adresses \_ \_ SIO** est normalement appelée de façon synchrone avec le paramètre *lpvOverlapped* défini sur **null**, car la liste des adresses est immédiatement retournée.

**Remarque**  Dans les environnements plug-and-Play Windows, les adresses peuvent être ajoutées et supprimées dynamiquement.
Par conséquent, les applications ne peuvent pas compter sur la persistance des informations retournées par la **\_ requête de \_ liste \_ d’adresses SIO** .
Les applications peuvent s’inscrire à des notifications de changement d’adresse par le biais de l’IOCTL de **\_ modification de \_ liste \_ d’adresses SIO** qui fournit une notification par le biais d’un événement d’e/s ou de modification de la **\_ \_ liste \_ d’adresses FD** .
La séquence d’actions suivante peut être utilisée pour garantir que l’application dispose toujours des informations de liste d’adresses actuelles :

* Émettre l’IOCTL de modification de la **\_ liste d’adresses \_ \_ SIO**
* Émettre l’IOCTL de **\_ requête de \_ liste \_ d’adresses SIO**
* Chaque fois que l’appel de la **\_ liste d’adresses SIO \_ \_ change** IOCTL notifie l’application d’une modification de liste d’adresses (via des e/s avec chevauchement ou en signalant un événement de modification de **\_ \_ liste \_ d’adresses FD** ), toute la séquence d’actions doit être répétée.

Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et le code de contrôle de **\_ requête de \_ liste \_ d’adresses SIO** est défini dans le fichier d’en-tête *Ws2def. h* .
Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

## <a name="see-also"></a>Voir aussi

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
