---
description: Demande comment la pile de mise en réseau doit gérer certains comportements pour lesquels la méthode par défaut de gestion du comportement peut varier entre les différentes versions de Windows.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: Code de contrôle SIO_SET_COMPATIBILITY_MODE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514017"
---
# <a name="sio_set_compatibility_mode-control-code"></a>Code de contrôle SIO_SET_COMPATIBILITY_MODE

## <a name="description"></a>Description

Le code de contrôle du **mode de compatibilité SIO Set demande comment la pile de mise \_ \_ \_ en** réseau doit gérer certains comportements pour lesquels la méthode par défaut de gestion du comportement peut varier d’une version à l’autre de Windows.

Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
Utilisez **le \_ \_ \_ mode de compatibilité SIO Set** pour cette opération.

### <a name="lpvinbuffer"></a>lpvInBuffer

Pointeur vers la mémoire tampon d’entrée.
Ce paramètre doit pointer vers une structure de **\_ \_ mode de compatibilité WSA** .

### <a name="cbinbuffer"></a>cbInBuffer

Taille, en octets, de la mémoire tampon d’entrée.
Ce paramètre doit être supérieur ou égal à la taille de la structure du **\_ \_ mode de compatibilité WSA** vers laquelle pointe le paramètre *lpvInBuffer* .

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
| **WSAEINVAL** | Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié. Cette erreur est retournée si le paramètre *cbInBuffer* est inférieur à la structure **du \_ \_ mode de compatibilité WSA** .
| **WSAENETDOWN** | Le sous-système réseau a échoué. |
| **WSAENOPROTOOPT** | L’option de socket n’est pas prise en charge sur le protocole spécifié. |
| **WSAENOTCONN** | Le socket n’est pas connecté. |
| **WSAENOTSOCK** | Le descripteur *s* n’est pas un Socket. |
| **WSAEOPNOTSUPP** | La commande IOCTL spécifiée n’est pas prise en charge. Cette erreur est retournée si l’IOCTL du **\_ mode de \_ compatibilité \_ SIO Set** n’est pas prise en charge par le fournisseur de transport. Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL du **\_ mode de \_ compatibilité \_ SIO Set** est effectuée sur un socket datagramme. |

## <a name="remarks"></a>Notes

l’IOCTL du **mode de compatibilité Set SIO demande comment la pile de mise \_ \_ \_ en** réseau doit gérer certains comportements pour lesquels la méthode par défaut de gestion du comportement peut varier d’une version à l’autre de Windows.
La structure d’arguments d’entrée pour le **\_ \_ \_ mode de compatibilité Set SIO** est spécifiée dans la structure du **\_ \_ mode de compatibilité WSA** définie dans le fichier d’en-tête *Mswsockdef. h* .
Un pointeur vers la structure du **\_ \_ mode de compatibilité WSA** est passé dans le paramètre *cbInBuffer* .
Cette structure est définie comme suit :

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

La valeur spécifiée dans le membre **BehaviorId** indique le comportement demandé.
La valeur spécifiée dans le membre **TargetOsVersion** indique la version de Windows demandée pour le comportement.

Le membre **BehaviorId** peut être l’une des valeurs du type d’énumération d’ID de **\_ \_ comportement \_ de compatibilité WSA** défini dans le fichier d’en-tête *Mswsockdef. h* .
Les valeurs possibles pour le membre **BehaviorId** sont les suivantes :

| Terme | Description |
|------|-------------|
| WsaBehaviorAll | Cela équivaut à demander tous les comportements compatibles possibles définis pour l’ID de **\_ comportement de \_ \_ compatibilité WSA**. |
| WsaBehaviorReceiveBuffering | Lorsque le membre **TargetOsVersion** est défini sur une valeur pour Windows Vista ou version ultérieure, la réduction de la taille de la mémoire tampon de réception TCP sur ce socket à l’aide de l’option de socket **\_ RCVBUF** est autorisée même après l’établissement d’une connexion TCP. Lorsque le membre **TargetOsVersion** est défini sur une valeur antérieure à Windows Vista, la réduction de la taille de la mémoire tampon de réception TCP sur ce socket à l’aide de l’option de socket **\_ RCVBUF** n’est pas autorisée après l’établissement de la connexion. |
| WsaBehaviorAutoTuning | Quand le membre **TargetOsVersion** est défini sur une valeur pour Windows Vista ou version ultérieure, le réglage automatique de la fenêtre de réception est activé et le facteur d’échelle de la fenêtre TCP est réduit à 2 de la valeur par défaut 8. Lorsque le **TargetOsVersion** est défini sur une valeur antérieure à Windows Vista, le réglage automatique de la fenêtre de réception est désactivé. L’option de mise à l’échelle de la fenêtre TCP est également désactivée et la taille maximale de la fenêtre de réception est limitée à 65 535 octets. L’option de mise à l’échelle de la fenêtre TCP ne peut pas être négociée sur la connexion même si l’option de socket **\_ RCVBUF** a été appelée sur ce socket en spécifiant une valeur supérieure à 65 535 octets avant l’établissement de la connexion. |

Le membre **TargetOsVersion** peut être l’une des constantes de version NTDDI définies dans le fichier d’en-tête *Sdkddkver. h* .
Les valeurs possibles pour le membre **TargetOsVersion** sont les suivantes :

| Terme | Description |
|------|-------------|
| NTDDI \_ LONGHORN | Le comportement de la cible est le comportement par défaut de Windows Vista. |
| NTDDI \_ WS03 | Le comportement de la cible est la valeur par défaut pour Windows Server 2003. |
| NTDDI \_ WinXP | Le comportement de la cible est la valeur par défaut pour Windows XP. |
| NTDDI \_ Win2K | Le comportement cible est la valeur par défaut pour Windows 2000. |

L’impact principal du membre **TargetOsVersion** est le fait que ce membre soit défini sur une valeur égale ou supérieure à **NTDDI \_ LONGHORN**.

Les performances TCP dépendent non seulement du taux de transfert proprement dit, mais plutôt du produit du taux de transfert et du délai d’aller-retour.
Ce produit Bandwidth-Delay mesure la quantité de données qui « rempliront le canal ».
Ce produit Bandwidth-delay est l’espace de la mémoire tampon requis au niveau de l’expéditeur et du récepteur pour obtenir un débit maximal sur la connexion TCP sur le chemin d’accès.
Cet espace de mémoire tampon représente la quantité de données sans accusé de réception que TCP doit gérer afin de garder le pipeline complet.
Des problèmes de performances TCP surviennent lorsque le produit Bandwidth-delay est volumineux.
Un chemin d’accès réseau fonctionnant sous ces conditions est souvent appelé « long, pipe ».
Citons par exemple des liaisons de satellite à haute capacité, des liaisons sans fil à haut débit et des liens fibre optique terrestre sur de longues distances.

L’en-tête TCP utilise un champ de données 16 bits (le champ de fenêtre dans l’en-tête de paquet TCP) pour signaler la taille de la fenêtre de réception à l’expéditeur.
Par conséquent, la plus grande fenêtre qui peut être utilisée est 65 535 octets.
Pour contourner cette limitation, une option d’extension TCP, mise à l’échelle de la fenêtre TCP, a été ajoutée au protocole TCP hautes performances pour permettre à Windows de plus de 65 535 octets.
L’option de mise à l’échelle de la fenêtre TCP (WSopt) est définie dans le document RFC 1323 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF.
L’extension WSopt étend la définition de la fenêtre TCP à 32 bits à l’aide d’un facteur d’échelle logarithmique sur un octet pour étendre le champ de fenêtre de 16 bits dans l’en-tête TCP.
L’extension WSopt définit un facteur d’échelle implicite (2 à une puissance), qui est utilisé pour multiplier la valeur de taille de fenêtre trouvée dans un en-tête TCP pour obtenir la taille réelle de la fenêtre.
Par conséquent, un facteur d’échelle de fenêtre de 8 entraînerait une taille de fenêtre réelle égale à la valeur du champ de fenêtre dans l’en-tête TCP multiplié par 2 ^ 8 ou 256.
Par conséquent, si le champ de fenêtre dans l’en-tête TCP était défini sur la valeur maximale de 65 535 octets et que le facteur d’échelle WSopt a été négocié à une valeur de 8, la taille de la fenêtre réelle est de 16 776 960 octets.

La taille réelle de la fenêtre de réception et par conséquent, le facteur d’échelle est déterminé par l’espace de la mémoire tampon de réception maximal.
Cet espace de mémoire tampon maximal correspond à la quantité de données qu’un destinataire TCP autorise à envoyer à un expéditeur TCP avant d’avoir à attendre un accusé de réception.
Une fois la connexion établie, la taille de la fenêtre de réception est publiée dans chaque segment TCP (le champ de la fenêtre de l’en-tête TCP).
La publication de la quantité maximale de données que l’expéditeur peut envoyer est un mécanisme de contrôle de workflow côté réception qui empêche l’expéditeur d’envoyer des données que le destinataire ne peut pas stocker.
Un hôte d’envoi peut envoyer uniquement la quantité maximale de données publiées par le destinataire avant d’attendre un accusé de réception et une mise à jour de la taille de la fenêtre de réception.

Sur Windows Server 2003 et Windows XP, l’espace de mémoire tampon de réception maximal qui représente la taille de la fenêtre de réception pour la pile TCP/IP a une valeur par défaut en fonction de la vitesse de liaison de l’interface d’envoi.
La valeur réelle s’ajuste automatiquement à des incréments pairs de la taille maximale de segment (MSS) négociée pendant l’établissement de la connexion TCP.
Par conséquent, pour un lien de 10 Mbits/s, la taille de la fenêtre de réception par défaut est normalement définie à 16 Ko, tandis que sur un lien 100 MBit/s, la taille de la fenêtre de réception par défaut est définie sur 65 535 octets.

Sur Windows Server 2003 et Windows XP, la véritable taille de fenêtre de réception maximale pour la pile TCP/IP peut être configurée manuellement à l’aide des valeurs de Registre suivantes sur une interface spécifique ou pour l’ensemble du système :

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

La valeur de Registre pour **TcpWindowSize** peut être définie sur un maximum de 65 535 octets si vous n’utilisez pas l’extension WSopt ou un maximum de 1 073 741 823 octets lors de l’utilisation de l’extension WSopt (un facteur d’échelle maximal de 4 est pris en charge).
Sans la mise à l’échelle de la fenêtre, une application peut uniquement atteindre un débit d’environ 5 mégabits par seconde (Mbits/s) sur un chemin d’accès avec un temps d’aller-retour de 100 millisecondes, quelle que soit la bande passante du chemin d’accès.
Ce débit peut être mis à l’échelle sur un gigabit par seconde (Gbits/s) avec la mise à l’échelle de la fenêtre, ce qui permet à TCP de négocier le facteur de mise à l’échelle pour la taille de la fenêtre pendant l’établissement de la connexion.

Sur Windows Server 2003 et Windows XP, l’extension WSopt peut être activée en définissant la valeur de Registre suivante.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

La valeur de Registre **TCP1323Opts** est un **DWORD** encodé de telle sorte que lorsque le bit 0 est défini, l’extension TCP WSopt est activée.
Lorsque le bit 1 est défini, l’option d’horodatage TCP (TSopt) définie dans la RFC 1323 est activée.
Par conséquent, la valeur 1 ou 3 active l’extension WSopt.

Sur Windows Server 2003 et Windows XP, la valeur par défaut est que les valeurs de Registre TCPWindowSize et Tcp1323Opts ne sont pas créées.
Par conséquent, la valeur par défaut est que l’extension WSopt est désactivée et que la taille de la fenêtre de réception TCP est définie par le système à la valeur maximale, jusqu’à 65 535 octets, en fonction de la vitesse de liaison.
Lorsque la mise à l’échelle des fenêtres est activée sur Windows Server 2003 et Windows XP en définissant la valeur de Registre Tcp1323Opts, la mise à l’échelle des fenêtres sur une connexion TCP est toujours utilisée uniquement lorsque l’expéditeur et le destinataire incluent une option d’échelle de fenêtre TCP dans le segment Synchronize (SYN) qui est envoyé les uns aux autres pour négocier un facteur d’échelle de fenêtre.
Lorsque la mise à l’échelle des fenêtres est utilisée sur une connexion, le champ fenêtre dans l’en-tête TCP est défini sur 65 535 octets et le facteur d’échelle de la fenêtre est utilisé pour ajuster la taille réelle de la fenêtre de réception par rapport au facteur d’échelle de la fenêtre négocié lorsque la connexion est établie.

Une application peut spécifier la taille de la fenêtre de réception TCP pour une connexion à l’aide de l’option de socket **so \_ RCVBUF** .
La taille de la fenêtre de réception TCP pour un socket peut être augmentée à tout moment à l’aide de **so \_ RCVBUF**, mais elle ne peut être réduite qu’avant d’établir une connexion.
Pour pouvoir utiliser la mise à l’échelle de la fenêtre, une application doit spécifier une taille de fenêtre supérieure à 65 535 octets lors de l’utilisation de l’option de socket **so \_ RCVBUF** avant l’établissement de la connexion.

La valeur idéale pour la taille de la fenêtre de réception TCP est souvent difficile à déterminer.
Pour remplir la capacité du réseau entre l’expéditeur et le destinataire, la taille de la fenêtre de réception doit être définie sur le produit Bandwidth-Delay pour la connexion, qui est la bande passante multipliée par la durée aller-retour.
Même si une application peut déterminer correctement le produit de délai de bande passante, il n’est toujours pas connu de la vitesse à laquelle l’application réceptrice récupère les données du tampon de données entrant (taux de récupération de l’application).
Malgré la prise en charge de la mise à l’échelle de la fenêtre TCP, la taille maximale de la fenêtre de réception dans Windows Server 2003 et Windows XP peut toujours limiter le débit, car il s’agit d’une taille maximale fixe pour toutes les connexions TCP (sauf si elles sont spécifiées par application à l’aide de **so \_ RCVBUF**), ce qui peut améliorer le débit pour certaines connexions et réduire le
En outre, la taille de fenêtre de réception maximale fixe pour une connexion TCP ne varie pas en fonction des conditions de réseau modifiées.

Pour résoudre le problème consistant à déterminer correctement la valeur de la taille maximale de la fenêtre de réception pour une connexion TCP en fonction des conditions actuelles du réseau, la pile TCP/IP de Windows Vista prend en charge une fonctionnalité de réglage automatique de la fenêtre de réception.
Lorsque cette fonctionnalité est activée, le réglage automatique de la fenêtre de réception détermine continuellement la taille optimale de la fenêtre de réception en mesurant le produit Bandwidth-Delay et le taux de récupération de l’application, et ajuste la taille maximale réelle de la fenêtre de réception en fonction des conditions de réseau modifiées.
Le réglage automatique de la fenêtre de réception active l’extension TCP WSopt par défaut, ce qui autorise jusqu’à 16 776 960 octets pour la taille réelle de la fenêtre.
À mesure que les données circulent sur la connexion, la pile TCP/IP surveille la connexion, mesure le produit de délai de bande passante actuel pour la connexion et la vitesse de réception de l’application, et ajuste la taille réelle de la fenêtre de réception pour optimiser le débit.
La pile TCP/IP modifie la valeur du champ fenêtre dans l’en-tête TCP en fonction des conditions du réseau, puisque le facteur d’échelle WSopt est fixe lorsque la connexion est établie pour la première fois.

La pile TCP/IP dans Windows Vista n’utilise plus les valeurs de Registre **TcpWindowSize** .
Avec un meilleur débit entre les homologues TCP, l’utilisation de la bande passante réseau augmente pendant le transfert de données.
Si toutes les applications sont optimisées pour recevoir des données TCP, l’utilisation globale du réseau peut augmenter considérablement, ce qui rend l’utilisation de la qualité de service (QoS) plus importante sur les réseaux qui fonctionnent à la capacité ou à une approche proche.

Le comportement par défaut de Windows Vista pour la mise en mémoire tampon de réception lorsque le **mode de \_ \_ compatibilité \_ SIO Set** n’est pas spécifié à l’aide de **WsaBehaviorReceiveBuffering** est qu’aucune réduction de la taille de la fenêtre de réception à l’aide de l’option **\_ RCVBUF** socket n’est autorisée après l’établissement d’une connexion.

Le comportement par défaut de Windows Vista pour le réglage automatique **lorsque \_ SIO \_ Set \_ mode de compatibilité** n’est pas spécifié à l’aide de **WsaBehaviorAutoTuning** est que la pile reçoit le réglage automatique de la fenêtre à l’aide d’un facteur d’échelle de fenêtre de 8.
Notez que si une application définit une taille de fenêtre de réception valide avec l’option de socket **so \_ RCVBUF** , la pile utilise la taille spécifiée et le réglage automatique de la réception de fenêtre est désactivé.
Le réglage automatique de Windows peut également être désactivé entièrement à l’aide de la commande suivante, `netsh interface tcp set global autotuninglevel=disabled` , auquel cas la spécification de **WsaBehaviorAutoTuning** n’a aucun effet.
Le réglage automatique de la réception de fenêtre peut également être désactivé en fonction de la stratégie de groupe définie sur Windows Server 2008.

L’option **WsaBehaviorAutoTuning** est nécessaire sur Windows Vista pour certains pare-feu et périphériques de passerelle Internet qui ne prennent pas correctement en charge les flux de données pour les connexions TCP qui utilisent l’extension WSopt et un facteur d’échelle Windows.
Sur Windows Vista, un récepteur négocie par défaut un facteur d’échelle de fenêtre de 8 pour une taille de fenêtre réelle maximale de 16 776 960 octets.
Lorsque les données commencent à circuler sur une liaison rapide, Windows commence par utiliser une taille de fenêtre de 64 kilo-octets en affectant au champ de la fenêtre de l’en-tête TCP la valeur 256 et en définissant le facteur d’échelle de la fenêtre sur 8 dans les options TCP (256 * 2 ^ 8 = 64 Ko).
Certains pare-feu et périphériques de passerelle Internet ignorent le facteur d’échelle de la fenêtre et examinent uniquement le champ de fenêtre publié dans l’en-tête TCP spécifié comme 256, et suppriment les paquets entrants pour la connexion contenant plus de 256 octets de données TCP.
Pour prendre en charge la mise à l’échelle de la fenêtre de réception TCP, un pare-feu ou un périphérique de passerelle doit surveiller le protocole de transfert TCP et suivre le facteur d’échelle de la fenêtre négociée dans le cadre des données de connexion TCP.
Certaines applications et implémentations de pile TCP sur d’autres plateformes ignorent également l’extension WSopt TCP et le facteur d’échelle de la fenêtre.
L’hôte distant qui envoie les données peut donc envoyer des données à la fréquence annoncée dans le champ de la fenêtre de l’en-tête TCP (256 octets).
Cela peut entraîner un ralentissement de la réception des données par le récepteur.

Le fait de définir le membre **BehaviorId** sur **WsaBehaviorAutoTuning** et le **TargetOsVersion** sur Windows Vista réduit le facteur d’échelle de la fenêtre à 2. par conséquent, le champ de la fenêtre de l’en-tête TCP est initialement défini à 16 384 octets et le facteur d’échelle de la fenêtre est défini sur 2 pour une taille initiale réelle de la réception de 64 octets.
La fonctionnalité de réglage automatique de la fenêtre peut ensuite augmenter la taille réelle de la réception de la fenêtre, jusqu’à 262 140 octets, en affectant au champ de la fenêtre de l’en-tête TCP la valeur 65 535 octets.
Une application doit définir l’IOCTL du **\_ \_ \_ mode de compatibilité Set SIO** dès qu’un socket est créé, car cette option n’a aucun sens ou s’applique après l’envoi d’un SYN.
La définition de cette option a le même impact que la commande suivante : `netsh interface tcp set global autotuninglevel=highlyrestricted`

Notez que le fichier d’en-tête *Mswsockdef. h* est automatiquement inclus dans *mswsock. h* ou *Netiodef. h* et qu’il ne doit pas être utilisé directement.

## <a name="see-also"></a>Voir aussi

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
