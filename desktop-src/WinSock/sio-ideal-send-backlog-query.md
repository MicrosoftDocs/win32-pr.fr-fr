---
description: Le code de contrôle récupère la valeur de backlog d’envoi idéale pour la connexion sous-jacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Code de contrôle SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8ae2c47487ab1b1cd946c05133ef96520dffc72e9e7c3176478917f969f7f374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111536"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>Code de contrôle SIO_IDEAL_SEND_BACKLOG_QUERY

## <a name="description"></a>Description

Le code de contrôle de **\_ requête de journal des travaux en \_ \_ souffrance \_ d’envoi idéal SIO** récupère la valeur d’un backlog d’envoi idéal pour la connexion sous-jacente.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
Utilisez **SIO \_ pour \_ \_ \_** cette opération.

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
| **WSAEFAULT** | Le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur. |
| **WSAEINPROGRESS** | La fonction est appelée lorsqu’un rappel est en cours. |
| **WSAEINTR** | Une opération de blocage a été interrompue. |
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’un type de données **ULong** .
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTCONN** | Le socket n’est pas connecté. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si l’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** n’est pas prise en charge par le fournisseur de transport. Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL d' **\_ envoi de journal des travaux en \_ \_ \_ souffrance SIO idéal** est effectuée sur un socket datagramme. |

## <a name="remarks"></a>Remarques

l’IOCTL de **\_ requête d’envoi de \_ \_ BACKLOG \_ SIO idéale** est prise en charge sur Windows Server 2008, Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.

lors de l’envoi de données via une connexion TCP à l’aide de Windows sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé.
La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal.
La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).

la valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.
L’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** peut être utilisée par une application pour recevoir une notification lorsque la valeur ISB change de manière dynamique pour une connexion.

sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation, les [**SIO de \_ \_ \_ journalisation des travaux en souffrance \_ d’envoi idéales**](sio-ideal-send-backlog-change.md) et SIO sont pris en charge sur les sockets orientés flux qui sont dans un état connecté. **\_ \_ \_ \_**

La plage de la valeur ISB pour une connexion TCP peut théoriquement varier de 0 à 16 mégaoctets au maximum.

L’utilisation classique de la [**SIO \_ de \_ \_ journalisation \_ des travaux en souffrance des envois**](sio-ideal-send-backlog-change.md) et SIO idéale d’envoi de **Journal des travaux en \_ \_ \_ souffrance \_** est basée sur la méthode Send utilisée par les applications.
Deux cas courants sont abordés.

Les applications qui exécutent une requête d’envoi de blocage ou non bloquant à la fois s’appuient généralement sur la mise en mémoire tampon d’envoi interne par Winsock pour atteindre un débit correct.
La limite de mémoire tampon d’envoi pour une connexion donnée est contrôlée par l’option de socket **\_ SNDBUF** .
Pour la méthode de blocage et d’envoi non bloquant, la limite de mémoire tampon d’envoi détermine la quantité de données conservées en attente dans TCP.
Si la valeur d’ISB pour la connexion est supérieure à la limite de mémoire tampon d’envoi, le débit atteint sur la connexion n’est pas optimal.
Afin d’obtenir un meilleur débit, les applications peuvent définir la limite de mémoire tampon d’envoi en fonction du résultat de la requête ISB, car les notifications de modification ISB se produisent sur la connexion.

Pour les applications qui utilisent la méthode Send avec chevauchement avec plusieurs demandes d’envoi en attente, la quantité de données restantes en suspens dans TCP est déterminée par la limite de mémoire tampon d’envoi dans Winsock et par la quantité totale de données contenues dans les demandes d’envoi superposées en suspens.
Dans ce cas, les applications doivent utiliser la valeur ISB pour déterminer le nombre de demandes d’envoi en suspens qu’elles doivent conserver et la taille des données pour chaque demande d’envoi.
Dans l’idéal, l’application doit tenter de garder l’équation suivante satisfaite :

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

Notez que l’utilisation des IOCTL d’ISB sur des sockets TCP de la manière ci-dessus peut entraîner une augmentation de l’utilisation de la mémoire dans Exchange pour une augmentation du débit sur les connexions avec un produit avec un délai de bande passante élevé.
l’implémentation TCP dans Windows permet de limiter les valeurs ISB en fonction de l’utilisation de la mémoire système globale.

L’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** est autorisée uniquement sur un socket de flux qui est dans l’état connecté.
Dans le cas contraire, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** échouera avec **WSAENOTCONN**.

Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.
Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.

L’IOCTL d’une **requête de BACKLOG d' \_ \_ envoi \_ \_ SIO idéale** n’est pas susceptible de se bloquer et est normalement appelée en mode synchrone avec les paramètres *lpOverlapped* et *lpCompletionRoutine* définis sur **null**.

L’IOCTL d’une **requête de BACKLOG d' \_ \_ envoi \_ \_ SIO idéale** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :

La connexion TCP est déconnectée en douceur dans le sens de l’envoi.
Cela peut se produire à la suite d’un appel à la fonction Shutdown avec la méthode How définie sur l' **\_ envoi SD**, d’un appel à la fonction **DisconnectEx** ou d’un appel à la fonction **TransmitFile** ou **TransmitPackets** avec le paramètre *dwFlags* défini sur **tf \_ Disconnect** ou **tf \_** Remain.
La connexion TCP a été réinitialisée ou abandonnée.
La demande est annulée par le gestionnaire d’e/s.

Deux fonctions wrapper Inline pour ces IOCTL sont définies dans le fichier d’en-tête *Ws2tcpip. h* .
Il est recommandé d’utiliser ces fonctions inline au lieu d’utiliser la [**SIO \_ de \_ \_ journalisation \_ des travaux en souffrance Send idéale**](sio-ideal-send-backlog-change.md) et SIO des IOCTL de **\_ \_ \_ \_ requête Send backlog** directement.

La fonction de wrapper Inline pour le [**SIO \_ idéal \_ Send \_ BACKLOG \_ change**](sio-ideal-send-backlog-change.md) IOCTL est la fonction **idealsendbacklognotify** .

La fonction de wrapper Inline pour l’IOCTL de **requête d' \_ envoi de \_ \_ BACKLOG \_ SIO idéale** est la fonction **idealsendbacklogquery** .

la mise en mémoire tampon d’envoi dynamique pour TCP a été ajoutée sur Windows 7 et Windows Server 2008 R2.
Par défaut, la mise en mémoire tampon d’envoi dynamique pour TCP est activée, sauf si une application définit l’option de socket **\_ SNDBUF** sur le socket de flux.

L’utilisation de netsh est la méthode recommandée pour interroger ou définir la mise en mémoire tampon d’envoi dynamique pour TCP.

La valeur actuelle de la mise en mémoire tampon d’envoi dynamique pour TCP peut être récupérée à l’aide de la commande suivante :

`netsh winsock show autotuning`

La mise en mémoire tampon d’envoi dynamique pour TCP peut être désactivée à l’aide de la commande suivante :

`netsh winsock set autotuning off`

La mise en mémoire tampon d’envoi dynamique pour TCP peut être activée à l’aide de la commande suivante :

`netsh winsock set autotuning on`

Bien qu’elle soit déconseillée, la mise en mémoire tampon d’envoi dynamique peut être désactivée à partir d’une application en affectant à la valeur de Registre suivante la valeur zéro :

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

Lors de la modification de la valeur de la mise en mémoire tampon d’envoi dynamique à l’aide de NetSh.exe ou de la modification de la valeur de Registre, l’ordinateur doit être redémarré pour que la modification prenne effet.

avec la mise en mémoire tampon d’envoi dynamique sur Windows 7 et Windows Server 2008 R2, l’utilisation de la [**SIO de \_ \_ \_ journalisation des travaux en souffrance \_**](sio-ideal-send-backlog-change.md) des envois idéale SIO et des ioctl de requête d' **envoi de journal des travaux en \_ \_ \_ souffrance \_** sont nécessaires uniquement dans des circonstances particulières.

## <a name="see-also"></a>Voir aussi

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
