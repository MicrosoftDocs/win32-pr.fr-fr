---
description: Rubrique de navigation pour les IOCTL de socket Windows Sockets (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: Winsock IOCTLs (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadf4a0e2799d6123bf81069fe65ea16313af444
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550254"
---
# <a name="winsock-ioctls"></a>IOCTL Winsock

Cette section décrit les contrôles d’entrée/sortie (IOCTL) du socket Winsock pour différentes éditions des systèmes d’exploitation Windows. Utilisez la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) pour émettre une IOCTL Winsock afin de contrôler le mode d’un socket, le protocole de transport ou le sous-système de communication.

Certaines IOCTL Winsock requièrent plus d’explications que ce tableau ne peut communiquer ; ces options contiennent des liens vers des rubriques supplémentaires.

Il est possible d’adopter un schéma d’encodage qui conserve les OpCodes [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) actuellement définis tout en fournissant un moyen pratique de partitionner l’espace d’identificateur opcode dans autant que le paramètre *dwIoControlCode* soit maintenant une entité 32 bits. Le paramètre *dwIoControlCode* est conçu pour permettre l’indépendance du protocole et du fournisseur lors de l’ajout de nouveaux codes de contrôle tout en conservant la compatibilité descendante avec les codes de contrôle Windows sockets 1,1 et UNIX. Le paramètre *dwIoControlCode* se présente sous la forme suivante.

| I  | O  | V  | T  | Fournisseur/famille d’adresses | Code                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Les bits dans le paramètre *dwIoControlCode* affiché dans la table doivent être lus verticalement de haut en bas par colonne. Le bit le plus à gauche est le bit 31, le bit suivant est le bit 30 et le bit le plus à droite est le bit 0.

I est défini si la mémoire tampon d’entrée est valide pour le code, comme avec **IOC_IN**.

O est défini si la mémoire tampon de sortie est valide pour le code, comme avec **IOC_OUT**. Les codes de contrôle utilisant à la fois les mémoires tampons d’entrée et de sortie définissent à la fois I et O.

V est défini s’il n’y a aucun paramètre pour le code, comme avec **IOC_VOID**.

T est une quantité de 2 bits qui définit le type de l’IOCTL. Les valeurs suivantes sont définies :

0 l’IOCTL est un code IOCTL UNIX standard, comme avec **FIONREAD** et **FIONBIO**.

1 l’IOCTL est un code IOCTL Windows Sockets 2 générique. Les nouveaux codes IOCTL définis pour Windows Sockets 2 auront T = = 1.

2 l’IOCTL s’applique uniquement à une famille d’adresses spécifique.

3 l’IOCTL s’applique uniquement au fournisseur d’un fournisseur spécifique, comme avec **IOC_VENDOR**. Ce type permet aux entreprises d’obtenir un numéro de fournisseur qui apparaît dans le paramètre de **famille fournisseur/adresse** . Ensuite, le fournisseur peut définir de nouvelles IOCTL propres à ce fournisseur sans avoir à inscrire l’IOCTL auprès d’un centre d’échanges de données, offrant ainsi de la flexibilité et de la confidentialité des fournisseurs.

**Fournisseur/famille d’adresses** Quantité de 11 bits qui définit le fournisseur propriétaire du code (si T = = 3) ou qui contient la famille d’adresses à laquelle le code s’applique (si T = = 2). S’il s’agit d’un code UNIX IOCTL (T = = 0), ce paramètre a la même valeur que le code sur UNIX. S’il s’agit d’un IOCTL Windows Sockets 2 générique (T = = 1), ce paramètre peut être utilisé en tant qu’extension du paramètre de code pour fournir des valeurs de code supplémentaires.

**Code** Quantité de 16 bits qui contient le code IOCTL spécifique pour l’opération.

## <a name="unix-ioctl-codes"></a>Codes IOCTL UNIX

Les codes (commandes) IOCTL UNIX suivants sont pris en charge.

### <a name="fionbio"></a>FIONBIO

Activez ou désactivez le mode non bloquant sur le socket *s*. Le paramètre *lpvInBuffer* pointe vers un **long non signé** (QoS), qui est différent de zéro si le mode non bloquant est activé et zéro s’il doit être désactivé. Lorsqu’un socket est créé, il fonctionne en mode blocage (autrement dit, le mode non bloquant est désactivé). Cela est cohérent avec les sockets BSD.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) ou [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) définit automatiquement un socket en mode non bloquant. Si **WSAAsyncSelect** ou **WSAEventSelect** a été émis sur un socket, toute tentative d’utilisation de [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour rétablir le socket en mode blocage échoue avec WSAEINVAL. Pour rétablir le socket en mode blocage, une application doit d’abord désactiver **WSAAsyncSelect** en appelant **WSAAsyncSelect** avec le paramètre *lEvent* égal à zéro, ou désactiver **WSAEventSelect** en appelant **WSAEventSelect** avec le paramètre *lNetworkEvents* égal à zéro.

### <a name="fionread"></a>FIONREAD

Déterminez la quantité de données pouvant être lues de manière atomique à partir du socket *s*. Le paramètre *lpvOutBuffer* pointe vers un **long non signé** dans lequel [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) stocke le résultat.

Si le socket passé dans le paramètre *s* est orienté flux (par exemple, tapez un flux de type chaussette \_ ), **FIONREAD** retourne la quantité totale de données pouvant être lues dans une opération de réception unique. il s’agit généralement du même volume de données en file d’attente sur le socket (dans la mesure où un flux de données est orienté octet, ce n’est pas garanti).

Si le socket passé dans le paramètre *s* est orienté message (par exemple, tapez chaussette \_ DGRAM), **FIONREAD** retourne le nombre total d’octets disponibles pour la lecture, et non la taille du premier datagramme (message) mis en file d’attente sur le Socket.

### <a name="siocatmark"></a>SIOCATMARK

Déterminez si toutes les données OOB ont été lues. Cela s’applique uniquement à un socket de type flux de données (par exemple, type de flux de chaussette \_ ) qui a été configuré pour la réception en ligne de toutes les données OOB (par conséquent \_ OOBINLINE). Si aucune donnée OOB n’est en attente de lecture, l’opération retourne la valeur TRUE. Sinon, elle retourne **false** et l’opération de réception suivante effectuée sur le socket récupère une partie ou la totalité des données précédant la marque ; l’application doit utiliser l’opération **SIOCATMARK** pour déterminer si elle est conservée. Si des données normales précèdent les données urgentes (hors bande), elles seront reçues dans l’ordre. (Notez que les opérations de [**réception**](/windows/desktop/api/winsock/nf-winsock-recv) ne mélangeront jamais les données OOB et normales dans le même appel.) *lpvOutBuffer* pointe vers un booléen dans lequel [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) stocke le résultat.

## <a name="windows-sockets-2-commands"></a>Commandes Windows Sockets 2

Les commandes Windows Sockets 2 suivantes sont prises en charge.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (paramètre opcode : I, T = = 3)

Demandez une réservation d’exécution pour un bloc de ports TCP ou UDP. Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée. Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel l’IOCTL [**SIO \_ Acquire \_ port \_ reservation**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) a été appelée. En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.

Pour plus d’informations, consultez la référence sur la [**\_ réservation de \_ port \_ SIO Acquire**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

[**SIO \_ L’acquisition de la \_ \_ réservation de port**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>\_Modification de la liste d’adresses SIO \_ \_ (paramètre opcode : V, T = = 1)

Pour recevoir une notification des modifications apportées à la liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier. Aucune information de sortie ne sera fournie à la fin de cette IOCTL. la saisie semi-automatique indique simplement que la liste des adresses locales disponibles a changé et doit être interrogée à nouveau par le biais d’une **\_ requête de \_ liste \_ d’adresses SIO**.

Il est supposé que l’application utilise des e/s avec chevauchement pour être informé de la modification par l’achèvement de la demande de modification de la **\_ liste d’adresses \_ \_ SIO** . En guise d’alternative, si la **\_ liste d’adresses SIO \_ \_ change** IOCTL est émise sur un socket non bloquant et sans les paramètres superposés (*lpOverlapped* /  *lpCompletionRoutine* est défini sur **null**), elle se termine immédiatement avec l’erreur [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md). L’application peut ensuite attendre les événements de modification de la liste d’adresses via un appel à [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ou [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) avec \_ le bit de modification de liste d’adresses FD \_ \_ défini dans le masque de bits d’événement réseau.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>\_ \_ Requête de liste d’adresses SIO \_ (paramètre opcode : O, T = = 1)

Obtient la liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier. La liste des adresses varie en fonction de la famille d’adresses et certaines adresses sont exclues de la liste.

> [!Note] 
> Dans les environnements plug-and-Play Windows, les adresses peuvent être ajoutées et supprimées dynamiquement. Par conséquent, les applications ne peuvent pas compter sur la persistance des informations retournées par la **\_ requête de \_ liste \_ d’adresses SIO** . Les applications peuvent s’inscrire à des notifications de changement d’adresse par le biais de l’IOCTL de **\_ modification de \_ liste \_ d’adresses SIO** qui fournit une notification par le biais d’un événement d’e/s ou de modification de la \_ liste d’adresses FD \_ \_ . La séquence d’actions suivante peut être utilisée pour garantir que l’application dispose toujours des informations de liste d’adresses actuelles :

-  Problème de modification de la **\_ liste d’adresses \_ \_ SIO** IOCTL
-  Émettre une requête IOCTL de **\_ liste d’adresses \_ \_ SIO**
-  Chaque fois que la **\_ liste d’adresses SIO \_ \_ change** IOCTL avertit l’application de la modification de la liste d’adresses (via des e/s avec chevauchement ou en signalant un événement de modification de la \_ \_ liste d’adresses FD \_ ), toute la séquence d’actions doit être répétée.

Pour plus d’informations, consultez la référence de [**\_ requête de \_ liste \_ d’adresses SIO**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) . **SIO \_ La \_ \_ requête de liste d’adresses** est prise en charge sur Windows 2000 et versions ultérieures.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ appliquer \_ le \_ paramètre de transport (paramètre opcode : I, T = = 3)

Applique un paramètre de transport à un Socket. Le paramètre de transport appliqué est basé sur l' [**\_ \_ ID de paramètre de transport**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passé dans le paramètre *lpvInBuffer* .

Le seul paramètre de transport actuellement défini est pour la fonctionnalité de **\_ fonctionnalité de \_ notification \_ en temps réel** sur un socket TCP.

Si l' [**\_ \_ ID de paramètre de transport**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) transmis a le membre **GUID** défini sur la **\_ \_ \_ fonctionnalité de notification en temps réel**, il s’agit d’une demande d’application des paramètres de notification en temps réel pour le socket TCP utilisé avec [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) pour recevoir des notifications de réseau en arrière-plan dans une application Windows Store.

Pour plus d’informations, consultez la référence des [**\_ \_ \_ paramètres de transport Apply SIO**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) . **SIO \_ APPLIQUER \_ les \_ paramètres de transport** est pris en charge sur Windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>\_Handle SIO Associate \_ (paramètre opcode : I, T = = 1)

Associe ce socket au handle spécifié d'une interface connexe. La mémoire tampon d’entrée contient la valeur entière correspondant à la constante de manifeste de l’interface associée (par exemple, TH \_ netdev et Th \_ TAPI.), suivie d’une valeur qui est un handle de l’interface associée spécifiée, ainsi que d’autres informations requises. Reportez-vous à la section appropriée dans les [annexes Winsock](winsock-annexes.md) pour obtenir des détails spécifiques à une interface connexe particulière. La taille totale est reflétée dans la longueur de la mémoire tampon d’entrée. Aucune mémoire tampon de sortie n’est requise. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge cette ioctl. Le descripteur associé à cette IOCTL peut être récupéré à l’aide du **\_ \_ handle SIO translate**.

Une interface auxiliaire peut être utilisée, par exemple, si un fournisseur particulier fournit (1) un grand nombre de contrôles supplémentaires sur le comportement d’un socket et (2) les contrôles sont suffisamment spécifiques au fournisseur pour qu’ils ne soient pas mappés à des fonctions de socket Windows existantes ou qu’il est probable qu’elles soient définies à l’avenir. Il est recommandé d’utiliser le modèle COM (Component Object Model) à la place de cette IOCTL pour découvrir et suivre les autres interfaces qui peuvent être prises en charge par un Socket. Cette IOCTL est présente pour la compatibilité (inverse) avec les systèmes où COM n’est pas disponible ou ne peut pas être utilisé pour une autre raison.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>\_ \_ Réservation de port SIO Associate \_ (paramètre opcode : I, T = = 3)

Associez un socket à une réservation persistante ou d’exécution pour un bloc de ports TCP ou UDP identifiés par le jeton de réservation de port. L’IOCTL de [**\_ réservation de \_ port \_ SIO Associate**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) doit être émise avant que le socket ne soit lié. Si et quand le socket est lié, le port qui lui est assigné est sélectionné à partir de la réservation de port identifiée par le jeton donné. Si aucun port n’est disponible à partir de la réservation spécifiée, l’appel de fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.

Pour plus d’informations, consultez la référence de [**\_ réservation de \_ port \_ SIO Associate**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) .

[**SIO \_ La \_ \_ réservation de port associée**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>\_ \_ Descripteur de base SIO (paramètre opcode : O, T = = 1)

Récupère le handle du fournisseur de services de base pour un socket donné. La valeur retournée est un **Socket**.

Un fournisseur de services en couche n’intercepte jamais cette IOCTL puisque la valeur de retour doit être le handle de socket du fournisseur de services de base.

Si la mémoire tampon de sortie n’est pas assez grande pour un handle de socket (le *cbOutBuffer* est inférieur à la taille d’un **Socket**) ou si le paramètre *lpvOutBuffer* est un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ Le \_ descripteur de base** est défini dans le fichier d’en-tête *mswsock. h* et pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>\_Handle BSP SIO \_ (paramètre opcode : O, T = = 1)

Récupère le handle du fournisseur de services de base pour un socket utilisé par la fonction [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . La valeur retournée est un **Socket**.

Cette IOCTL est utilisée par un fournisseur de services en couche pour s’assurer que le fournisseur intercepte la fonction [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Si la mémoire tampon de sortie n’est pas assez grande pour un handle de socket (le *cbOutBuffer* est inférieur à la taille d’un **Socket**) ou si le paramètre *lpvOutBuffer* est un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ Le \_ descripteur BSP** est défini dans le fichier d’en-tête *mswsock. h* et pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ du \_ handle BSP \_ Select (paramètre opcode : O, T = = 1)

Récupère le handle du fournisseur de services de base pour un socket utilisé par la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) . La valeur retournée est un **Socket**.

Cette IOCTL est utilisée par un fournisseur de services en couche pour s’assurer que le fournisseur intercepte la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) .

Si la mémoire tampon de sortie n’est pas assez grande pour un handle de socket (le *cbOutBuffer* est inférieur à la taille d’un **Socket**) ou si le paramètre *lpvOutBuffer* est un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ Le \_ handle BSP \_ Select** est défini dans le fichier d’en-tête *mswsock. h* et pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>\_Interrogation \_ de handle BSP SIO \_ (paramètre opcode : O, T = = 1)

Récupère le handle du fournisseur de services de base pour un socket utilisé par la fonction [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . Le paramètre *lpOverlapped* doit être un pointeur **null** . La valeur retournée est un **Socket**.

Cette IOCTL est utilisée par un fournisseur de services en couche pour s’assurer que le fournisseur intercepte la fonction [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Si la mémoire tampon de sortie n’est pas assez grande pour un handle de socket (le *cbOutBuffer* est inférieur à la taille d’un **Socket**), le paramètre *lpvOutBuffer* est un pointeur **null** ou le paramètre *lpOverlapped* n’est pas un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ Le \_ \_ sondage du handle BSP** est défini dans le fichier d’en-tête *mswsock. h* et pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>SIO \_ chk \_ QoS (paramètre opcode : I, O, T = = 3)

Récupère des informations sur les caractéristiques du trafic QoS. Pendant la phase de transition sur le système d’envoi entre la configuration de flux et la réception d’un message RESV (voir [Comment le service RSVP appelle TC](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) pour plus d’informations sur la phase de transition), le trafic associé à un flux RSVP est mis en forme en fonction du type de service ([meilleur effort](/previous-versions/windows/desktop/qos/best-effort), [charge contrôlée](/previous-versions/windows/desktop/qos/controlled-load)ou [garantie](/previous-versions/windows/desktop/qos/guaranteed)). Pour plus d’informations, consultez [utilisation de SiO \_ chk \_ QoS](/previous-versions/windows/desktop/qos/using-sio-chk-qos) dans la section [qualité de service](/previous-versions/windows/desktop/qos/qos-start-page) du kit de développement logiciel (SDK) de plateforme.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (paramètre opcode : I, T = = 3)

Active le partage de port et la parallélisation des indications de réception. Lorsque votre application utilise cette option de socket pour associer des sockets à différents processeurs, puis lie les sockets à la même adresse, les indications de réception sont distribuées sur les sockets en fonction du hachage RSS (Receive Side Scaling). Les paramètres RSS ne changent pas. par conséquent, tout flux donné (point de terminaison local, paire de point de terminaison distant) sera toujours indiqué sur le même processeur. Par conséquent, tous les paquets appartenant à un Flow donné seront signalés au même socket. Cette IOCTL doit être appelée avant la liaison, sinon WSAEINVAL est retourné. La mémoire tampon d’entrée est un index de processeur (de base 0) de type USHORT. L’IOCTL est incompatible avec SO_REUSEADDR et SO_REUSE_MULTICASTPORT. Pris en charge uniquement pour les sockets UDP.

> [!NOTE]
> Si vous ciblez la version 10.0.19041.0 (Windows 10, version 2004) du SDK Windows, utilisez la valeur `0x98000015` au lieu du nom **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ activer \_ la \_ file d’attente circulaire (paramètre opcode : V, T = = 1)

Indique au fournisseur de services orienté message sous-jacent qu’un message nouvellement arrivé ne doit jamais être supprimé en raison d’un dépassement de capacité de la mémoire tampon. Au lieu de cela, le message le plus ancien de la file d’attente doit être éliminé afin de prendre en compte le message nouvellement arrivé. Aucune mémoire tampon d’entrée et de sortie n’est requise. Notez que cette IOCTL n’est valide que pour les sockets associés à des protocoles non fiables et orientés message. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge cette ioctl.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ Rechercher l' \_ itinéraire (paramètre opcode : O, T = = 1)

Une fois émis, cette IOCTL demande que l’itinéraire vers l’adresse distante spécifiée comme [**sockaddr**](sockaddr-2.md) dans la mémoire tampon d’entrée soit détecté. Si l’adresse existe déjà dans le cache local, son entrée est invalidée. Dans le cas de IPX de Novell, cet appel initie un GetLocalTarget IPX (GLT), qui interroge le réseau pour l’adresse distante donnée.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ Flush (paramètre opcode : V, T = = 1)

Ignore le contenu actuel de la file d’attente d’envoi associée à ce Socket. Aucune mémoire tampon d’entrée et de sortie n’est requise. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge cette ioctl.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ Obtient \_ l' \_ adresse de diffusion (paramètre opcode : O, T = = 1)

Cette IOCTL remplit la mémoire tampon de sortie avec une structure [sockaddr](sockaddr-2.md) contenant une adresse de diffusion appropriée pour une utilisation avec [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Cette IOCTL n’est pas prise en charge pour les sockets IPv6 et retourne le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) .

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ Obtient \_ le \_ pointeur de fonction d’extension \_ (paramètre opcode : O, I, T = = 1)

Récupère un pointeur vers la fonction d’extension spécifiée prise en charge par le fournisseur de services associé. La mémoire tampon d’entrée contient un identificateur global unique (**GUID**) dont la valeur identifie la fonction d’extension en question. Le pointeur vers la fonction souhaitée est retourné dans la mémoire tampon de sortie. Les identificateurs de fonction d’extension sont établis par les fournisseurs de fournisseurs de services et doivent être inclus dans la documentation du fournisseur qui décrit les fonctionnalités et la sémantique des fonctions d’extension.

Les valeurs GUID pour les fonctions d’extension prises en charge par le fournisseur de services TCP/IP Windows sont définies dans le fichier d’en-tête *mswsock. h* . La valeur possible pour ces GUID est la suivante :

| Terme                                                                                                                | Description                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ accepted<br/>                                     | Fonction d’extension [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | Fonction d’extension [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) . <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | Fonction d’extension [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) . <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | Fonction d’extension [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) .<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>WSAID \_ TRANSMITFILE<br/>                         | Fonction d’extension [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) .<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>WSAID \_ TRANSMITPACKETS<br/>                | Fonction d’extension [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) . <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | Fonction d’extension [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | Fonction d’extension [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ obtient le \_ groupe \_ QoS (paramètre opcode : O, I, T = = 1)

Réservé pour une utilisation ultérieure avec les sockets.

Récupérez la structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) associée au groupe de sockets auquel appartient ce Socket. La mémoire tampon d’entrée est facultative. Certains protocoles (par exemple, RSVP) autorisent l’utilisation de la mémoire tampon d’entrée pour qualifier une demande de qualité de service. La structure **QoS** sera copiée dans la mémoire tampon de sortie. Si ce socket n’appartient pas à un groupe de sockets approprié, les membres **SendingFlowspec** et **ReceivingFlowspec** de la structure **QoS** retournée ont la valeur **null**. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge la qualité de service.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ obtient la \_ liste d’interfaces \_ (paramètre opcode : O, T = = 0)

Retourne une liste d’interfaces IP configurées et leurs paramètres sous la forme d’un tableau de structures d' [**\_ informations d’interface**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) .

> [!Note]  
> La prise en charge de cette commande est obligatoire pour les fournisseurs de services TCP/IP compatibles Windows Sockets 2.

Le paramètre *lpvOutBuffer* pointe vers la mémoire tampon dans laquelle stocker les informations sur les interfaces sous la forme d’un tableau de structures d' [**\_ informations d’interface**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) pour les adresses IP de monodiffusion sur les interfaces. Le paramètre *cbOutBuffer* spécifie la longueur de la mémoire tampon de sortie. Le nombre d’interfaces retournées (nombre de structures retournées dans la mémoire tampon vers laquelle pointe le paramètre *lpvOutBuffer* ) peut être déterminé en fonction de la longueur réelle de la mémoire tampon de sortie retournée dans le paramètre *lpcbBytesReturned* .

Si la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) est appelée avec **la \_ \_ \_ liste d’interfaces d’extraction SIO** et que le membre de niveau du paramètre du socket n’est pas défini en tant qu' **\_ adresse IP IPPROTO**, **WSAEINVAL** est retourné.  Un appel à la fonction **WSAIoctl** avec **SIO \_ obtenir l' \_ interface \_ List** retourne **WSAEFAULT** si le paramètre *cbOutBuffer* qui spécifie la longueur de la mémoire tampon de sortie est trop petit pour recevoir la liste des interfaces configurées.

**SIO \_ La \_ \_ liste des interfaces de récupération** est prise en charge sur Windows Me/98 et Windows NT 4,0 avec SP4 et versions ultérieures.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ obtient la \_ liste des interfaces par \_ \_ exemple (paramètre opcode : O, T = = 0)

Réservé pour une utilisation ultérieure avec les sockets.

Retourne une liste d’interfaces IP configurées et leurs paramètres sous la forme d’un tableau de structures d' [**informations d’interface \_ \_ ex**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) .

Le paramètre *lpvOutBuffer* pointe vers la mémoire tampon dans laquelle stocker les informations sur les interfaces sous la forme d’un tableau d’informations d' [**interface \_ \_ ex**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) structures pour les adresses IP de monodiffusion sur l’interface. Le paramètre *cbOutBuffer* spécifie la longueur de la mémoire tampon de sortie. Le nombre d’interfaces retournées (nombre de structures retournées dans *lpvOutBuffer*) peut être déterminé en fonction de la longueur réelle de la mémoire tampon de sortie retournée dans le paramètre *lpcbBytesReturned* .

**SIO \_ L’accès à la \_ liste d’interfaces par \_ \_ exemple** n’est actuellement pas pris en charge sur Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ Obtient \_ QoS (paramètre opcode : O, T = = 1)

Réservé pour une utilisation ultérieure avec les sockets. Récupérez la structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) associée au socket. La mémoire tampon d’entrée est facultative. Certains protocoles (par exemple, RSVP) autorisent l’utilisation de la mémoire tampon d’entrée pour qualifier une demande de qualité de service. La structure **QoS** sera copiée dans la mémoire tampon de sortie. La taille de la mémoire tampon de sortie doit être suffisamment grande pour pouvoir contenir la structure de **QoS** complète. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge la qualité de service.

Un expéditeur ne peut pas appeler **SIO \_ obtenir \_ QoS** tant que le socket n’est pas connecté.

Un récepteur peut appeler **SIO \_ obtenir \_ QoS** dès qu’il est lié.

### <a name="sio_get_tx_timestamp"></a>SIO_GET_TX_TIMESTAMP

IOCTL de socket utilisé pour obtenir des horodateurs pour les paquets transmis (TX). Valide uniquement pour les sockets de datagrammes.

Le code de contrôle de **SIO_GET_TX_TIMESTAMP** supprime un horodateur de transmission de la file d’attente des horodateurs de transmission d’un Socket. Activez d’abord la réception des horodateurs à l’aide du [**SIO_TIMESTAMPING**](#sio_timestamping) de socket ioctl. Ensuite, récupérez les horodateurs TX par ID en appelant la fonction [**WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) (ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))) avec les paramètres suivants.

Pour **SIO_GET_TX_TIMESTAMP**, l’entrée est un ID d’horodatage **UInt32** et la sortie est une valeur d’horodatage **UINT64** . En cas de réussite, l’horodateur TX est disponible et est retourné. Si aucun horodatage de transmission n’est disponible, [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retourne **WSAEWOULDBLOCK**.

> [!NOTE]
> Les horodateurs TX ne sont pas pris en charge lors d’un envoi fusionné via **UDP_SEND_MSG_SIZE**.

Voir aussi [horodatage Winsock](/windows/win32/winsock/winsock-timestamping).

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ la \_ \_ modification de BACKLOG d’envoi idéale \_ (paramètre opcode : V, T = = 0)

Avertit une application lorsque la valeur d’un backlog d’envoi (ISB) idéal change pour la connexion sous-jacente.

Lors de l’envoi de données via une connexion TCP à l’aide de Windows Sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé. La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal. La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).

La valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation. L’IOCTL **SIO de modification de \_ BACKLOG d' \_ envoi \_ \_ idéale** peut être utilisée par une application pour recevoir une notification lorsque la valeur ISB change de manière dynamique pour une connexion.

Pour plus d’informations, consultez la référence de [**\_ modification du BACKLOG d' \_ envoi \_ \_ SIO idéale**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) .

[**SIO \_ La \_ \_ \_ modification de la file d’attente d’envoi idéale**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) est prise en charge sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ \_ \_ requête de BACKLOG d’envoi idéale \_ (paramètre opcode : O, T = = 0)

Récupère la valeur d’un backlog d’envoi idéal pour la connexion sous-jacente.

Lors de l’envoi de données via une connexion TCP à l’aide de Windows Sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé. La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal. La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).

La valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008 et versions ultérieures. L’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** peut être utilisée par une application pour interroger la valeur ISB pour une connexion.

Pour plus d’informations, consultez la référence de [**\_ requête de journal des travaux en \_ souffrance d’envoi \_ \_ SIO idéale**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) .

[**SIO \_ La \_ \_ \_ requête d’envoi de BACKLOG idéale**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) est prise en charge sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KeepAlive \_ Vals (paramètre opcode : I, T = = 3)

Active ou désactive le paramètre par connexion de l’option TCP **Keep-Alive** qui spécifie le délai d’expiration et l’intervalle de conservation TCP. Pour plus d’informations sur l’option Keep-Alive, consultez la section 4.2.3.6 sur la *Configuration requise pour les hôtes Internet — couches de communication* spécifiées dans le document RFC 1122 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF. (Cette ressource peut uniquement être disponible en anglais.)

**SIO \_ KEEPALIVE \_ Vals** peut être utilisé pour activer ou désactiver les sondes KeepAlive et définir le délai d’expiration et l’intervalle de maintien de l’activité. Le délai d’attente Keep-Alive spécifie le délai d’attente, en millisecondes, sans activité jusqu’à l’envoi du premier paquet Keep-Alive. L’intervalle Keep-Alive spécifie l’intervalle, en millisecondes, entre l’envoi des paquets Keep-Alive successifs si aucun accusé de réception n’est reçu.

L’option [**so \_ KeepAlive**](so-keepalive.md) , qui est l’une des [options de \_ Socket](sol-socket-socket-options.md)de socket sol, peut également être utilisée pour activer ou désactiver le protocole TCP Keep-Alive sur une connexion, ainsi que pour interroger l’état actuel de cette option. Pour demander si TCP Keep-Alive est activé sur un socket, la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) peut être appelée avec l’option **so \_ KeepAlive** . Pour activer ou désactiver le protocole TCP Keep-Alive, la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) peut être appelée avec l’option [**so \_ KeepAlive**](so-keepalive.md) . Si TCP Keep-Alive est activé avec **\_ KeepAlive**, les paramètres TCP par défaut sont utilisés pour le délai d’expiration et l’intervalle de conservation, sauf si ces valeurs ont été modifiées à l’aide de **SIO \_ KeepAlive \_ Vals**.

Pour plus d’informations, consultez la référence [**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) . **SIO \_ KEEPALIVE \_ Vals** est pris en charge sur Windows 2000 et versions ultérieures.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>\_ \_ \_ Chemin d’accès rapide de bouclage SIO (paramètre opcode : I, T = = 3)

Configure un socket TCP pour une latence plus faible et des opérations plus rapides sur l’interface de bouclage. Cette IOCTL demande que la pile TCP/IP utilise un chemin d’accès rapide spécial pour les opérations de bouclage sur ce Socket. L’IOCTL du [**\_ \_ \_ chemin d’accès rapide de bouclage SIO**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) peut être utilisé uniquement avec les sockets TCP. Cette IOCTL doit être utilisée des deux côtés de la session de bouclage. Le chemin d’accès rapide de bouclage TCP est pris en charge à l’aide de l’interface de bouclage IPv4 ou IPv6. Par défaut, **le \_ \_ \_ chemin d’accès rapide de bouclage SIO** est désactivé.

Pour plus d’informations, consultez la référence sur le [**\_ \_ \_ chemin d’accès rapide de bouclage SIO**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) . **SIO \_ Le \_ \_ chemin d’accès rapide de bouclage** est pris en charge sur Windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ multipoint \_ loopback (paramètre opcode : V, T = = 1)

Contrôle si les données envoyées par une application sur l’ordinateur local (pas nécessairement par le même socket) dans une session de multidiffusion sont reçues par un socket joint au groupe de destination de multidiffusion sur l’interface de bouclage. La valeur **true** entraîne la remise des données de multidiffusion envoyées par une application sur l’ordinateur local à un socket d’écoute sur l’interface de bouclage. La valeur **false** empêche la remise des données de multidiffusion envoyées par une application sur l’ordinateur local à un socket d’écoute sur l’interface de bouclage. Par défaut, **le \_ \_ bouclage multipoint SIO** est activé.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>\_Étendue de multidiffusion SIO \_ (paramètre opcode : I, T = = 1)

Spécifie la portée sur laquelle les transmissions par multidiffusion auront lieu. L’étendue est définie comme le nombre de segments de réseau routé à couvrir. Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local. Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs. Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis. Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP. Par défaut, l’étendue est 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>\_ \_ Informations sur le processeur RSS de la requête SIO \_ \_ (paramètre opcode : O, T = = 1)

Interroge l’association entre un socket et un cœur de processeur RSS et un nœud NUMA.

Les [**informations IOCTL du \_ \_ \_ processeur \_ RSS de la requête SIO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) renvoient une structure d' [**\_ \_ affinité de processeur de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) qui contient le [**\_ numéro de processeur**](/windows/win32/api/winnt/ns-winnt-processor_number) et l’ID de nœud NUMA. La structure retournée du **\_ numéro de processeur** contient un numéro de groupe et un numéro de processeur relatif dans le groupe.

Pour plus d’informations, consultez la [**référence \_ \_ \_ \_ informations sur le processeur RSS de la requête SIO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) . **SIO \_ Les \_ \_ \_ informations sur le processeur RSS** de la requête sont prises en charge sur Windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>\_Informations d' \_ extensibilité du flux RSS des requêtes SIO \_ \_ (paramètre opcode : O, T = = 3)

Interroge les interfaces de déchargement pour la capacité de mise à l’échelle côté réception (RSS). La structure d’arguments retournée pour les **\_ \_ \_ \_ informations d’extensibilité RSS des requêtes SIO** est spécifiée dans la structure d' **\_ \_ informations d’extensibilité RSS** définie dans le fichier d’en-tête *Mstcpip. h* . Cette structure est définie comme suit :

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

La valeur retournée dans le membre **RssEnabled** indique si RSS est activé sur au moins une interface.

Si la mémoire tampon de sortie n’est pas assez grande pour la structure d' **\_ \_ informations d’extensibilité RSS** (le *cbOutBuffer* est inférieur à la taille d’une **\_ \_ information d’extensibilité RSS**) ou si le paramètre *lpvOutBuffer* est un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEINVAL](windows-sockets-error-codes-2.md).

Dans une mise en réseau haut débit où plusieurs UC résident dans un seul système, la capacité de la pile de protocole réseau à évoluer correctement sur un système multi-PROCESSEURs est inhibée, car l’architecture de NDIS 5,1 et des versions antérieures limite le traitement de protocole à un seul processeur. La mise à l’échelle côté réception (RSS) résout ce problème en autorisant l’équilibrage de la charge réseau à partir d’une carte réseau sur plusieurs processeurs.

**SIO \_ Les \_ \_ \_ informations de scalabilité RSS** de la requête sont prises en charge sur Windows Vista et versions ultérieures.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>\_ \_ \_ Paramètre de transport de requête SIO (paramètre opcode : I, T = = 3)

Interroge les paramètres de transport sur un Socket. Le paramètre de transport interrogé est basé sur l' [**ID de \_ paramètre \_ de transport**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passé dans le paramètre *lpvInBuffer* .

Le seul paramètre de transport actuellement défini est pour la fonctionnalité de **\_ fonctionnalité de \_ notification \_ en temps réel** sur un socket TCP.

Si l' [**\_ \_ ID du paramètre de transport**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) a le membre **GUID** défini sur la **\_ \_ \_ fonctionnalité de notification en temps réel**, il s’agit d’une demande d’interrogation des paramètres de notification en temps réel pour le socket TCP utilisé avec [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) pour recevoir des notifications de réseau en arrière-plan dans une application Windows Store. Si l’appel [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) réussit, cette IOCTL retourne une structure de sortie de [**\_ \_ \_ paramètre \_ de notification en temps réel**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) avec l’état actuel.

Pour plus d’informations, consultez la référence des [**\_ paramètres de \_ transport \_ de requête SIO**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) . **SIO \_ Le \_ \_ paramètre de transport de requête** est pris en charge sur Windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>\_ \_ \_ \_ Handle de point de terminaison ALE de la requête SIO \_ (paramètre opcode : O, T = = 3)

Interroge le descripteur de point de terminaison ALE.

La plateforme de filtrage Windows (WFP) prend en charge l’inspection et la modification du trafic réseau. Sur Windows Vista, WFP se concentre sur les scénarios où l’ordinateur hôte est le point de terminaison de communication. Sur Windows Server 2008, toutefois, il existe des implémentations de pare-feu de périmètre qui souhaitent tirer parti de la plateforme WFP pour inspecter et transmettre le trafic direct par proxy. Le serveur Internet Security and Acceleration (ISA) est un exemple de périphérique de périmètre.

Certains scénarios de pare-feu peuvent nécessiter la possibilité d’injecter un paquet entrant dans le chemin d’envoi associé à un point de terminaison existant. Il doit exister un mécanisme pour découvrir le handle de point de terminaison de la couche de transport associé au point de terminaison de destination. L’application qui a créé le point de terminaison est propriétaire des points de terminaison de la couche de transport. Cette IOCTL est utilisée pour fournir le descripteur de socket au mappage de handle de point de terminaison de couche de transport.

Si la mémoire tampon de sortie n’est pas assez grande pour le handle de point de terminaison ( *cbOutBuffer* est inférieur à la taille d’un **UINT64**) ou si le paramètre *lpvOutBuffer* est un pointeur **null** , une **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEINVAL](windows-sockets-error-codes-2.md).

**SIO \_ Le \_ \_ \_ \_ descripteur de point de terminaison ALE WFP de requête** est pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ interroger le \_ \_ \_ contexte de redirection de connexion WFP \_ (paramètre opcode : I, T = = 3)

Interroge le contexte de redirection pour un enregistrement de redirection utilisé par un service de redirection de plateforme de filtrage Windows (WFP).

L’IOCTL du [**\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) est utilisée pour fournir le suivi de connexion en proxy sur les connexions de socket redirigées. Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Pour plus d’informations, consultez la référence du [**\_ \_ \_ \_ \_ contexte de redirection de connexion WFP de la requête SIO**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) . **SIO \_ Interroger le \_ \_ \_ \_ contexte de redirection de connexion WFP** est pris en charge sur windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ interroger les \_ \_ \_ enregistrements de redirection de connexion WFP \_ (paramètre opcode : I, T = = 3)

Interroge l’enregistrement de redirection pour la connexion TCP/IP acceptée en vue d’une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).

Les [**\_ enregistrements de \_ \_ \_ redirection \_ de connexion WFP de la requête SIO**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) sont utilisés pour fournir le suivi de connexion en proxy sur les connexions de socket redirigées. Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Pour plus d’informations, consultez la référence des [**\_ \_ \_ \_ \_ enregistrements de redirection de connexion WFP de la requête SIO**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) . **SIO \_ Les \_ \_ enregistrements de \_ redirection \_ de connexion WFP de requête** sont pris en charge sur windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (paramètre opcode : I, T = = 3)

Permet à un socket de recevoir tous les paquets IPv4 ou IPv6 transmettant throuigh une interface réseau. Le descripteur de socket passé à la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) doit être l’un des suivants :

-   Un socket IPv4 créé avec la famille d’adresses définie sur AF \_ inet, le type de socket défini sur chaussette \_ RAW et le protocole défini sur IP IPPROTO \_ .
-   Un socket IPv6 qui a été créé avec la famille d’adresses définie sur AF \_ inet6, le type de socket défini sur chaussette \_ RAW et le protocole défini sur IPPROTO \_ IPv6.

Le socket doit également être lié à une interface IPv4 ou IPv6 locale explicite, ce qui signifie que vous ne pouvez pas effectuer de liaison pour **inadr \_ any** ou **in6addr \_ any**.

Sur Windows Server 2008 et versions antérieures, le paramètre IOCTL [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) ne capture pas les paquets locaux envoyés à partir d’une interface réseau. Cela inclut les paquets reçus sur une autre interface et a transmis l’interface réseau spécifiée pour l’IOCTL **SIO \_ RCVALL** .

Sur Windows 7 et Windows Server 2008 R2, cela a été modifié afin que les paquets locaux envoyés à partir d’une interface réseau soient également capturés. Cela comprend les paquets reçus sur une autre interface, puis le transfert de l’interface réseau liée au socket avec [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) ioctl.

La définition de cette IOCTL requiert des privilèges d’administrateur sur l’ordinateur local.

Cette fonctionnalité est parfois appelée « mode promiscuité ».

Les valeurs possibles de l’option **SIO \_ RCVALL** IOCTL sont spécifiées dans l’énumération de la **\_ valeur RCVALL** définie dans le fichier d’en-tête *Mstcpip. h* . Les valeurs possibles pour SIO \_ RCVALL sont les suivantes :

| Terme                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ désactivé<br/>                                     | Désactivez cette option pour qu’un socket ne reçoive pas tous les paquets IPv4 ou IPv6 sur le réseau. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_ sur<br/>                                        | Activez cette option pour qu’un socket reçoive tous les paquets IPv4 ou IPv6 sur le réseau. Cette option active le mode de proximité sur la carte d’interface réseau (NIC), si la carte réseau prend en charge le mode de proximité. Sur un segment LAN avec un concentrateur réseau, une carte réseau qui prend en charge le mode promiscuité capture tout le trafic IPv4 ou IPv6 sur le réseau local, y compris le trafic entre les autres ordinateurs sur le même segment de réseau local. Tous les paquets capturés (IPv4 ou IPv6, selon le socket) sont remis au socket brut. <br/> Cette option ne capture pas les autres paquets (paquets ARP, IPX et NetBEUI, par exemple) sur l’interface.<br/> Netmon utilise le même mode pour l’interface réseau, mais n’utilise pas cette option pour capturer le trafic.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL \_ SOCKETLEVELONLY<br/> | Cette fonctionnalité n’est pas implémentée pour l’instant. par conséquent, la définition de cette option n’a aucun effet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL \_ IPLEVEL<br/>                         | Activez cette option pour qu’un socket IPv4 ou IPv6 reçoive tous les paquets au niveau IP sur le réseau. Cette option n’active pas le mode de proximité sur la carte d’interface réseau. Cette option affecte uniquement le traitement des paquets au niveau de l’adresse IP. La carte réseau reçoit toujours uniquement les paquets dirigés vers ses adresses de monodiffusion et de multidiffusion configurées. Toutefois, un socket avec cette option activée recevra non seulement les paquets dirigés vers des adresses IP spécifiques, mais recevra tous les paquets IPv4 ou IPv6 reçus par la carte réseau.<br/> Cette option ne capture pas les autres paquets (par exemple, les paquets ARP, IPX et NetBEUI) reçus sur l’interface.<br/>                                                                                             |



 

Pour plus d’informations, consultez la référence [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

**SIO \_ RCVALL** est pris en charge sur Windows 2000 et versions ultérieures.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ IGMPMCAST (paramètre opcode : I, T = = 3)

Permet à un socket de recevoir tout le trafic IP de multidiffusion IGMP sur le réseau, sans recevoir d’autre trafic IP de multidiffusion. Le descripteur de socket passé à la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) doit avoir une \_ famille d’adresses d’inet AF, un type de socket brut de chaussette et le \_ \_ protocole IGMP IPPROTO. Le socket doit également être lié à une interface locale explicite, ce qui signifie que vous ne pouvez pas effectuer de liaison à \_ n’importe laquelle.

Une fois que le socket est lié et que l’IOCTL est défini, les appels aux fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retournent des datagrammes IP de multidiffusion passant par l’interface donnée. Notez que vous devez fournir une mémoire tampon suffisamment grande. La définition de cette IOCTL requiert des privilèges d’administrateur sur l’ordinateur local.

**SIO \_ RCVALL \_ IGMPMCAST** est pris en charge sur Windows 2000 et versions ultérieures.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ MCAST (paramètre opcode : I, T = = 3)

Permet à un socket de recevoir tout le trafic IP de multidiffusion sur le réseau (c’est-à-dire, tous les paquets IP destinés à des adresses IP comprises dans la plage 224.0.0.0 à 239.255.255.255). Le descripteur de socket passé à la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) doit être de \_ type de famille d’adresses d’inet AF, de type de socket brut de chaussette et de \_ \_ protocole UDP IPPROTO. Le socket doit également effectuer une liaison à une interface locale explicite, ce qui signifie que vous ne pouvez pas effectuer de liaison à inadr \_ Any. Le socket doit se lier au port zéro.

Une fois que le socket est lié et que l’IOCTL est défini, les appels aux fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retournent des datagrammes IP de multidiffusion passant par l’interface donnée. Notez que vous devez fournir une mémoire tampon suffisamment grande. La définition de cette IOCTL requiert des privilèges d’administrateur sur l’ordinateur local.

**SIO \_ RCVALL \_ MCAST** est pris en charge sur Windows 2000 et versions ultérieures.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>\_ \_ Réservation de port SIO Release \_ (paramètre opcode : I, T = = 3)

Libère une réservation d’exécution pour un bloc de ports TCP ou UDP. La réservation de runtime à libérer doit avoir été obtenue à partir du processus d’émission à l’aide de l’IOCTL de [**\_ réservation de \_ port \_ SIO Acquire**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

Pour plus d’informations, consultez la référence sur la réservation du port de la [**\_ version \_ \_ SIO**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) .

[**SIO \_ La \_ \_ réservation de port de version**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>\_ \_ Modification de l’interface de routage SIO \_ (paramètre opcode : I, T = = 1)

Pour recevoir une notification d’une modification de l’interface de routage qui doit être utilisée pour atteindre l’adresse distante dans la mémoire tampon d’entrée (spécifiée comme structure [**sockaddr**](sockaddr-2.md) ). Aucune information de sortie sur la nouvelle interface de routage n’est fournie à l’achèvement de cette IOCTL. la saisie semi-automatique indique simplement que l’interface de routage pour une destination donnée a changé et doit être interrogée à l’aide de l’IOCTL de requête de l' **\_ interface de routage \_ \_ SIO** .

Il est supposé, bien qu’il n’est pas obligatoire, que l’application utilise des e/s avec chevauchement pour être informé de la modification de l’interface de routage jusqu’à la fin de la demande de modification de l' **\_ interface de routage \_ \_ SIO** . En guise d’alternative, si l' **\_ interface de routage SIO \_ \_ change** IOCTL sur un socket non bloquant avec les paramètres *LpOverlapped* et *lpCompletionRoutine* définis sur la **valeur null**), elle se termine immédiatement et [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) comme une erreur, et l’application peut ensuite attendre les événements de changement de routage via un appel à [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ou [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) avec FD \_ interface de routage de \_ \_ changement défini dans le masque de bits d’événement réseau.

Il est reconnu que les informations de routage restent stables dans la plupart des cas, de sorte que l’application qui doit conserver plusieurs IOCTL en suspens pour obtenir des notifications sur toutes les destinations qui l’intéressent et faire en sorte que le fournisseur de services effectue le suivi de ces demandes de notification utilise une quantité significative de ressources système. Cette situation peut être évitée en étendant la signification des paramètres d’entrée et en détendant les exigences du fournisseur de services comme suit :

-   L’application peut spécifier une adresse générique spécifique à la famille de protocoles (identique à celle utilisée dans l’appel de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) lors de la demande de liaison à une adresse disponible) pour demander des notifications de modifications de routage. Cela permet à l’application de conserver uniquement une **\_ modification d' \_ interface \_ de routage SIO** en suspens pour tous les sockets et les destinations qu’elle possède, puis d’utiliser la **\_ \_ \_ requête d’interface de routage SIO** pour obtenir les informations de routage réelles.
-   Un fournisseur de services a la possibilité d’ignorer les informations spécifiées par l’application dans la mémoire tampon d’entrée de la modification de l' **\_ interface de routage \_ \_ SIO** (comme si l’application avait spécifié une adresse générique) et de terminer l’événement de modification de l’interface de **\_ routage SIO \_ \_** IOCTL ou de l’interface de routage de signal FD \_ \_ \_ dans le cas d’une modification des informations de routage

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>\_ \_ Requête de l’interface de routage SIO \_ (paramètre opcode : I, O, T = = 1)

Pour obtenir l’adresse de l’interface locale (représentée sous forme de structure [**sockaddr**](sockaddr-2.md) ) qui doit être utilisée pour envoyer à l’adresse distante spécifiée dans la mémoire tampon d’entrée (comme **sockaddr**). Les adresses de multidiffusion distantes peuvent être envoyées dans la mémoire tampon d’entrée pour obtenir l’adresse de l’interface préférée pour la transmission par multidiffusion. Dans tous les cas, l’adresse d’interface retournée peut être utilisée par l’application dans une requête BIND () suivante.

Notez que les itinéraires sont susceptibles d’être modifiés. Par conséquent, les applications ne peuvent pas compter sur la persistance des informations retournées par la requête de l' **\_ interface de routage \_ \_ SIO** . Les applications peuvent s’inscrire pour router les notifications de modification via l’IOCTL de modification de l' **\_ interface de routage \_ \_ SIO** , qui fournit une notification par le biais d’un événement d’e/s avec chevauchement ou d’un \_ événement de changement d’interface de routage FD \_ \_ . La séquence d’actions suivante peut être utilisée pour garantir que l’application dispose toujours des informations d’interface de routage actuelles pour une destination donnée :

-   Émettre une modification de l' **\_ interface de routage \_ \_ SIO** IOCTL
-   Émettre une requête IOCTL d' **\_ interface de routage \_ \_ SIO**
-   Chaque fois que l' **\_ interface de routage SIO \_ \_ change** IOCTL notifie l’application de modification du routage (via des e/s avec chevauchement ou en signalant un événement de modification de l' \_ interface de routage FD \_ \_ ), toute la séquence d’actions doit être répétée.

Si la mémoire tampon de sortie n’est pas assez grande pour contenir l’adresse de l’interface, l' \_ erreur de socket est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md). La taille requise de la mémoire tampon de sortie est retournée dans *lpcbBytesReturned* dans ce cas. Notez que le code d’erreur WSAEFAULT est également retourné si le paramètre *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.

Si l’adresse de destination spécifiée dans la mémoire tampon d’entrée ne peut pas être atteinte via l’une des interfaces disponibles, l' \_ erreur de socket est retournée à la suite de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAENETUNREACH](windows-sockets-error-codes-2.md) ou même [WSAENETDOWN](windows-sockets-error-codes-2.md) si l’ensemble de la connectivité réseau est perdu.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ définir \_ le \_ mode de compatibilité (paramètre opcode : I, T = = 3)

Demande comment la pile de mise en réseau doit gérer certains comportements pour lesquels la méthode par défaut de gestion du comportement peut varier entre les différentes versions de Windows. La structure d’arguments pour le **\_ \_ \_ mode de compatibilité Set SIO** est spécifiée dans la structure du **\_ \_ mode de compatibilité WSA** définie dans le fichier d’en-tête *Mswsockdef. h* . Cette structure est définie comme suit :

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

La valeur spécifiée dans le membre **BehaviorId** indique le comportement demandé. La valeur spécifiée dans le membre **TargetOsVersion** indique la version de Windows demandée pour le comportement.

Le membre **BehaviorId** peut être l’une des valeurs du type d’énumération d’ID de **\_ \_ comportement \_ de compatibilité WSA** défini dans le fichier d’en-tête *Mswsockdef. h* . Les valeurs possibles pour le membre **BehaviorId** sont les suivantes.

| Terme                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Cela équivaut à demander tous les comportements compatibles possibles définis pour l’ID de **\_ comportement de \_ \_ compatibilité WSA**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Lorsque le membre **TargetOsVersion** est défini sur une valeur pour Windows Vista ou version ultérieure, la réduction de la taille de la mémoire tampon de réception TCP sur ce socket à l’aide de l’option de socket **\_ RCVBUF** est autorisée même après l’établissement d’une connexion TCP. <br/> Lorsque le membre **TargetOsVersion** est défini sur une valeur antérieure à Windows Vista, la réduction de la taille de la mémoire tampon de réception TCP sur ce socket à l’aide de l’option de socket **\_ RCVBUF** n’est pas autorisée après l’établissement de la connexion. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Quand le membre **TargetOsVersion** est défini sur une valeur pour Windows Vista ou version ultérieure, le réglage automatique de la fenêtre de réception est activé et le facteur d’échelle de la fenêtre TCP est réduit à 2 de la valeur par défaut 8.<br/> Lorsque le **TargetOsVersion** est défini sur une valeur antérieure à Windows Vista, le réglage automatique de la fenêtre de réception est désactivé. L’option de mise à l’échelle de la fenêtre TCP est également désactivée et la taille maximale de la fenêtre de réception est limitée à 65 535 octets. L’option de mise à l’échelle de la fenêtre TCP ne peut pas être négociée sur la connexion même si l’option de socket **\_ RCVBUF** a été appelée sur ce socket en spécifiant une valeur supérieure à 65 535 octets avant l’établissement de la connexion.<br/> |



 

Pour plus d’informations, consultez la référence sur le [**\_ mode de \_ compatibilité \_ SIO Set**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) .

**SIO \_ Le \_ \_ mode de compatibilité défini** est pris en charge sur Windows Vista et versions ultérieures.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ définir la \_ qualité de service du groupe \_ (paramètre opcode : I, T = = 1)

Réservé.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (paramètre opcode : I, T = = 3)

Fournit un indicateur au protocole de transport sous-jacent pour traiter le trafic sur ce Socket avec une priorité spécifique. *LpvInBuffer* doit pointer vers une variable de type **PRIORITY_HINT** avec *cbInBuffer* défini sur sizeof (PRIORITY_HINT). Les paramètres *lpvOutBuffer* et *CbOutBuffer* doivent être **null** et 0, respectivement. L’implémentation Microsoft Windows TCP prend en charge cette IOCTL à compter de Windows 10, version 1809 (10,0 ; Générez 17763) et versions ultérieures comme suit : lorsque la valeur de priorité demandée est définie sur **IoPriorityHintVeryLow**, TCP utilise une version modifiée de l’algorithme LEDBAT (définie dans RFC 6817) pour contrôler le taux de trafic sortant sur le Socket. Le trafic entrant n’est pas affecté par cette IOCTL. LEDBAT est un algorithme de nettoyage, et son objectif est de maintenir la latence faible et d’empêcher tout effet néfaste sur le trafic de priorité normale en se déroulant lorsque le trafic de priorité normale est présent.

Consultez également [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** est pris en charge sur Windows 10, version 1809 (10,0 ; Build 17763) et versions ultérieures.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ Set \_ QoS (paramètre opcode : I, T = = 1)

Associe la structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) spécifiée au socket. Aucune mémoire tampon de sortie n’est requise, la structure **QoS** est obtenue à partir de la mémoire tampon d’entrée. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge la qualité de service.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (paramètre opcode : I, T = = 3)

Contrôle les caractéristiques de retransmission initiales (SYN/SYN + ACK) d’un socket TCP en configurant les paramètres du délai d’attente de retransmission initial (RTO). Les paramètres de configuration sont spécifiés dans une structure de [**\_ \_ \_ paramètres de RTO initial TCP**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) .

Pour plus d’informations, consultez la référence [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) . [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) est pris en charge sur Windows 8, windows server 2012 et versions ultérieures.

### <a name="sio_timestamping"></a>SIO_TIMESTAMPING

IOCTL de socket utilisé pour configurer la réception des horodateurs de transmission/réception de Socket. Valide uniquement pour les sockets de datagrammes. Le type d’entrée pour **SIO_TIMESTAMPING** est la structure [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) .

Voir aussi [horodatage Winsock](/windows/win32/winsock/winsock-timestamping).

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>\_Handle SIO translate \_ (paramètre opcode : I, O, T = = 1)

Pour obtenir un handle correspondant pour le *socket qui* est valide dans le contexte d’une interface associée (par exemple, Th \_ netdev et Th \_ TAPI). Une constante de manifeste identifiant l’interface auxiliaire avec tous les autres paramètres nécessaires est spécifiée dans la mémoire tampon d’entrée. Le handle correspondant sera disponible dans la mémoire tampon de sortie une fois cette fonction terminée. Reportez-vous à la section appropriée dans les [annexes Winsock](winsock-annexes.md) pour obtenir des détails spécifiques à une interface connexe particulière. Le code d’erreur [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) est indiqué pour les fournisseurs de services qui ne prennent pas en charge cette ioctl pour l’interface associée spécifiée. Cette IOCTL récupère le descripteur associé à l’aide du **\_ \_ handle SIO translate**.

Il est recommandé d’utiliser le modèle COM (Component Object Model) à la place de cette IOCTL pour découvrir et suivre les autres interfaces qui peuvent être prises en charge par un Socket. Ce IOCTL est présent pour la compatibilité descendante avec les systèmes où COM n’est pas disponible ou ne peut pas être utilisé pour une autre raison.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (paramètre opcode : I, T = = 3)

**Windows XP :** Contrôle si les messages du PORT UDP \_ inaccessible sont signalés. Affectez la valeur **true** pour activer la création de rapports. Affectez la valeur **false** pour désactiver la création de rapports.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ définir \_ les \_ \_ enregistrements de redirection de connexion WFP \_ (paramètre opcode : I, T = = 3)

Définit l’enregistrement de redirection sur le nouveau socket TCP utilisé pour la connexion à la destination finale en vue d’une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).

Les [**\_ enregistrements de \_ \_ \_ redirection \_ de connexion SIO Set WFP**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) sont utilisés dans le cadre du suivi de connexion par proxy sur les connexions de socket redirigées. Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.

Pour plus d’informations, consultez la référence des [**\_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) . **SIO \_ Les \_ \_ enregistrements de \_ redirection \_ de connexion WFP** sont pris en charge sur windows 8, Windows Server 2012 et versions ultérieures.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ info (paramètre d’opcode : I, O, T = = 3)

Récupère les statistiques TCP pour un Socket. Les statistiques TCP sont fournies dans une structure de l' [**\_ information TCP \_ v0**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) .

Contrairement à la récupération des statistiques TCP avec la fonction [**GetPerTcpConnectionEStats**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , la récupération des statistiques TCP avec ce code de contrôle ne nécessite pas que le code utilisateur charge, stocke et filtre la table de connexion TCP et ne nécessite pas de privilèges élevés pour utiliser.

Pour plus d’informations, consultez [**SIO \_ TCP \_ info**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SIO \_ Les \_ informations TCP** sont prises en charge sur Windows 10, version 1703, windows server 2016 et versions ultérieures.

## <a name="remarks"></a>Remarques

Les IOCTL Winsock sont définis dans plusieurs fichiers d’en-tête différents. Celles-ci incluent le fichier d’en-tête *Winsock2. h*, *mswsock. h* et *Mstcpip. h* .

Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et un certain nombre d’IOCTL d’IOCTL Winsock sont également définis dans les fichiers d’en-tête *Ws2def. h*, *Ws2ipdef. h* et *Mswsockdef. h* . Le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Le fichier d’en-tête *Ws2ipdef. h* est automatiquement inclus dans le fichier d’en-tête *Ws2tcpip. h* . Le fichier d’en-tête *Mswsockdef. h* est automatiquement inclus dans le fichier d’en-tête *Mswsockdef. h* .

## <a name="requirements"></a>Spécifications

|Condition requise|Valeur|
|-|-|
| En-tête<br/> | <dl> <dt>Winsock2. h ; </dt> <dt>Mstcpip. h ; </dt> <dt>Mswsock. h ; </dt> <dt>Mswsockdef. h sur Windows Vista, Windows Server 2008 et Windows 7 (inclure mswsock. h); </dt> <dt>Ws2def. h sur Windows Vista, Windows Server 2008 et Windows 7 (inclure Winsock2. h); </dt> <dt>Ws2ipdef. h sur Windows Vista, Windows Server 2008 et Windows 7 (inclure Ws2tcpip. h)</dt> </dl> |
