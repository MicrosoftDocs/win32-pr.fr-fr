---
description: Code de contrôle notifie une application lorsque la valeur de backlog d’envoi idéale change pour la connexion.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Code de contrôle SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: daa4141d3ef00b562082fbcff9804326e12bbef671ae8f5d593009fe9d06b7f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097519"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>Code de contrôle SIO_IDEAL_SEND_BACKLOG_CHANGE

## <a name="description"></a>Description

Le code de contrôle de **\_ modification du backlog d' \_ envoi \_ \_ SIO idéal** notifie une application lorsque la valeur d’un backlog d’envoi (ISB) idéal change pour la connexion.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
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
Utilisez **SIO pour la modification de \_ \_ BACKLOG d’envoi \_ \_ idéale** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre n’est pas utilisé pour cette opération.

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée. Ce paramètre n’est pas utilisé pour cette opération.

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
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbOutBuffer* n’est pas égal à zéro. |
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTCONN** | Le socket *n'* est pas connecté. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si la modification IOCTL du **\_ BACKLOG d' \_ envoi \_ \_ SIO idéale** n’est pas prise en charge par le fournisseur de transport. Cette erreur est également retournée lorsqu’une tentative d’utilisation de la **SIO de modification de \_ \_ BACKLOG d’envoi \_ \_ idéale** est effectuée sur un socket datagramme. |

## <a name="remarks"></a>Remarques

l’IOCTL **SIO de modification de \_ BACKLOG d' \_ envoi \_ \_ idéale** est prise en charge sur Windows Server 2008, Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.

lors de l’envoi de données via une connexion TCP à l’aide de Windows sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé.
La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal.
La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).

la valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.
L’IOCTL **SIO de modification de \_ BACKLOG d' \_ envoi \_ \_ idéale** peut être utilisée par une application pour recevoir une notification lorsque la valeur ISB change de manière dynamique pour une connexion.

sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation, les **SIO de \_ \_ \_ journalisation des travaux en souffrance \_ d’envoi idéales** et SIO sont pris en charge sur les sockets orientés flux qui sont dans un état connecté. [**\_ \_ \_ \_**](sio-ideal-send-backlog-query.md)

La plage de la valeur ISB pour une connexion TCP peut théoriquement varier de 0 à 16 mégaoctets au maximum.

Consultez la page de référence de la requête d’IOCTL de [**\_ Journal des travaux en \_ \_ souffrance \_ d’envoi SIO idéale**](sio-ideal-send-backlog-query.md) pour une utilisation classique du mécanisme ISB afin d’obtenir un meilleur débit sur les connexions de produits à bande passante élevée.

L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** est autorisé uniquement sur un socket de flux qui est dans l’état connecté.
Dans le cas contraire, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** échouera avec **WSAENOTCONN**.

L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** n’utilise aucune mémoire tampon d’entrée ou de sortie et pends ou bloque jusqu’à ce qu’une modification d’ISB se produise sur la connexion sous-jacente.
Lorsque cette IOCTL est terminée, une application Winsock peut utiliser l’IOCTL de [**\_ requête d’envoi de \_ \_ BACKLOG \_ SIO idéale**](sio-ideal-send-backlog-query.md) pour récupérer la nouvelle valeur ISB sur la connexion.

L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** ne prend pas en charge le mode non bloquant.
Une application est autorisée à émettre cette IOCTL sur un socket non bloquant, mais le IOCTL bloque simplement ou met en attente jusqu’à ce que la valeur ISB change.

Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont NULL, le socket dans cette fonction sera traité comme un socket non superposé.
Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.
Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.

Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.

Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.
Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.

L’IOCTL **SIO de modification de \_ BACKLOG d’envoi idéale \_ \_ \_** fournit une notification et doit bloquer ou mettre en attente jusqu’à ce que la valeur ISB change.
Il est donc communément appelé de façon asynchrone avec le paramètre *lpOverlapped* défini sur une structure WSAOVERLAPPED valide.

La **modification IOCTL du \_ \_ \_ BACKLOG \_ d’envoi SIO idéale** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :

* La connexion TCP est déconnectée en douceur dans le sens de l’envoi. Cela peut se produire à la suite d’un appel à la fonction Shutdown avec la méthode How définie sur l' **\_ envoi SD**, d’un appel à la fonction **DisconnectEx** ou d’un appel à la fonction **TransmitFile** ou **TransmitPackets** avec le paramètre *dwFlags* défini sur **tf \_ Disconnect** ou **tf \_** Remain.
* La connexion TCP a été réinitialisée ou abandonnée.
* L’application émet un ioctl de **modification de BACKLOG d’envoi SIO idéal lorsqu’il existe déjà une demande de notification en \_ \_ \_ attente \_** . Seules 1 1 en **attente SIO demande de \_ \_ modification de \_ BACKLOG \_ d’envoi idéale** sont autorisées à la fois.
* La demande est annulée par le gestionnaire d’e/s.
* Le socket est fermé.

Deux fonctions wrapper Inline pour ces IOCTL sont définies dans le fichier d’en-tête *Ws2tcpip. h* .
Il est recommandé d’utiliser ces fonctions inline au lieu d’utiliser la **SIO \_ de \_ \_ journalisation \_ des travaux en souffrance Send idéale** et SIO des IOCTL de [**\_ \_ \_ \_ requête Send backlog**](sio-ideal-send-backlog-query.md) directement.

La fonction de wrapper Inline pour le **SIO \_ idéal \_ Send \_ BACKLOG \_ change** IOCTL est la fonction **idealsendbacklognotify** .

La fonction de wrapper Inline pour l’IOCTL de [**requête d' \_ envoi de \_ \_ BACKLOG \_ SIO idéale**](sio-ideal-send-backlog-query.md) est la fonction **idealsendbacklogquery** .

## <a name="see-also"></a>Voir aussi

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
