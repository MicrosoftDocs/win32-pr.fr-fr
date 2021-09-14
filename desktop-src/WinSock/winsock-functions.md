---
description: La liste suivante fournit des descriptions concises de chaque fonction Winsock. Pour plus d’informations sur les fonctions, cliquez sur le nom de la fonction.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Fonctions Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918912"
---
# <a name="winsock-functions"></a>Fonctions Winsock

La liste suivante fournit des descriptions concises de chaque fonction Winsock. Pour plus d’informations sur les fonctions, cliquez sur le nom de la fonction.

| Fonction | Description |
|-|-|
| [**valide**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Autorise une tentative de connexion entrante sur un Socket. |
| [**Accepte**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Accepte une nouvelle connexion, retourne l’adresse locale et distante et reçoit le premier bloc de données envoyé par l’application cliente. |
| [**établis**](/windows/win32/api/winsock/nf-winsock-bind) | Associe une adresse locale à un Socket. |
| [**opération closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Ferme un socket existant. |
| [**entre**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Établit une connexion à un socket spécifié. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Établit une connexion à un socket spécifié et envoie éventuellement des données une fois la connexion établie. Pris en charge uniquement sur les sockets orientés connexion. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Ferme une connexion sur un socket et permet la réutilisation du handle de Socket. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Récupère des informations sur un ensemble spécifié de protocoles réseau qui sont actifs sur un hôte local. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Libère les informations d’adresse que la fonction [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) alloue dynamiquement dans les structures [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) . |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Libère les informations d’adresse que la fonction [**API getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) alloue dynamiquement dans les structures [**addrinfoex**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) . |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Libère les informations d’adresse que la fonction [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) alloue dynamiquement dans les structures [**addrinfoW**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) . |
| [**gai \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Aide à l’impression des messages d’erreur basés sur les \_ \* Erreurs EAI retournées par la fonction [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analyse les données obtenues à partir d’un appel à la fonction [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex) . |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Interroge un espace de noms, ou un ensemble d’espaces de noms par défaut, pour récupérer des informations d’adresse réseau pour un service réseau spécifié. Ce processus est appelé « résolution de noms de service ». Un service réseau peut également utiliser la fonction pour obtenir des informations sur l’adresse locale qu’il peut utiliser avec la fonction de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) . |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Fournit la traduction indépendante du protocole d’un nom d’hôte ANSI en une adresse. |
| [**API getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Fournit la résolution de noms indépendante du protocole avec des paramètres supplémentaires pour qualifier les fournisseurs d’espace de noms qui doivent gérer la requête. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Annule une opération asynchrone par la fonction [**API getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Obtient le code de retour pour une structure **OVERLAPPED** utilisée par une opération asynchrone pour la fonction [**API getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Fournit la traduction indépendante du protocole d’un nom d’hôte Unicode en une adresse. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Récupère les informations de l’hôte correspondant à une adresse réseau. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Récupère les informations d’hôte correspondant à un nom d’hôte à partir d’une base de données hôte. Déconseillé : utilisez plutôt [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**GetHostName**](/windows/win32/api/winsock/nf-winsock-gethostname) | Récupère le nom d’hôte standard de l’ordinateur local. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Récupère le nom d’hôte standard de l’ordinateur local sous la forme d’une chaîne Unicode. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Récupère l’état de filtre de multidiffusion pour un socket IPv4. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Récupère le nom d’un service réseau pour le type de service spécifié. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Fournit la résolution de noms d’une adresse IPv4 ou IPv6 à un nom d’hôte ANSI et d’un numéro de Port au nom de service ANSI. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Fournit la résolution de noms d’une adresse IPv4 ou IPv6 à un nom d’hôte Unicode et d’un numéro de Port au nom de service Unicode. |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | Récupère l’adresse de l’homologue auquel un socket est connecté. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Récupère les informations de protocole correspondant à un nom de protocole. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Récupère les informations de protocole correspondant à un numéro de protocole. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Récupère des informations de service correspondant à un nom de service et à un protocole. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Récupère des informations de service correspondant à un port et à un protocole. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Récupère des informations sur un service réseau dans le contexte d’un ensemble d’espaces de noms par défaut ou d’un espace de noms spécifié. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Récupère le nom local d’un Socket. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Récupère une option de Socket. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Récupère l’état de filtre de multidiffusion pour un socket IPv4 ou IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Récupère un GUID de type de service pour un service réseau spécifié par son nom. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Convertit un **double** de l’hôte en ordre d’octet réseau TCP/IP (qui est Big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Convertit une valeur **float** de l’hôte en ordre d’octet réseau TCP/IP (Big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Convertit **une \_ valeur u** de l’hôte en ordre d’octet réseau TCP/IP (qui est Big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Convertit un **unsigned \_ \_ Int64** de l’hôte en ordre d’octet réseau TCP/IP (qui est Big-endian). |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | Convertit **un \_ short u** de l’hôte en ordre d’octet réseau TCP/IP (qui est Big-endian). |
| [**\_ADR inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Convertit une chaîne contenant une adresse pointée du protocole Internet (IPv4) en adresse correcte pour la structure [**\_ addr**](/windows/win32/api/winsock2/ns-winsock2-in_addr) . |
| [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Convertit une adresse réseau Internet (IPv4) en une chaîne au format avec points standard Internet. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | Convertit une adresse réseau Internet IPv4 ou IPv6 en une chaîne au format Internet standard. La version ANSI de cette fonction est [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Convertit une adresse réseau Internet IPv4 ou IPv6 dans sa forme de présentation texte standard en sa forme binaire numérique. La version ANSI de cette fonction est [**inet \_ PTON**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Contrôle le mode d’e/s d’un Socket. |
| [**listen**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Place un socket dans un État où il écoute une connexion entrante. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Convertit un **unsigned \_ \_ Int64** de l’ordre de réseau TCP/IP en ordre d’octet hôte (qui est Little-endian sur les processeurs Intel) et retourne un **double**. |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Convertit un **unsigned \_ \_ Int32** de l’ordre de réseau TCP/IP en ordre d’octet hôte (qui est Little-endian sur les processeurs Intel) et retourne un **float**. |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Convertit une \_ valeur u de l’ordre de réseau TCP/IP en ordre d’octet hôte (ce qui est Little-endian sur les processeurs Intel). |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Convertit un **unsigned \_ \_ Int64** de l’ordre de réseau TCP/IP en ordre d’octet hôte (qui est Little-endian sur les processeurs Intel). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Convertit une \_ valeur courte de l’ordre des octets du réseau TCP/IP en ordre d’octet hôte (ce qui est Little-endian sur les processeurs Intel). |
| [**reçu**](/windows/win32/api/winsock/nf-winsock-recv) | Reçoit des données à partir d’un socket connecté ou lié. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Reçoit un datagramme et stocke l’adresse source. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Ferme une file d’attente de saisie semi-automatique existante utilisée pour la notification d’achèvement d’e/s en envoyant et en recevant des demandes avec les extensions d’e/s inscrites Winsock. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Crée une file d’attente d’achèvement d’e/s d’une taille spécifique pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Crée un descripteur de socket d’e/s inscrit à l’aide d’un socket spécifié et de files d’attente d’e/s à utiliser avec les extensions d’e/s inscrites Winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Supprime les entrées d’une file d’attente d’achèvement d’e/s pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Annule l’inscription d’une mémoire tampon inscrite utilisée avec les extensions d’e/s inscrites Winsock. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Inscrit la méthode à utiliser pour le comportement de notification avec une file d’attente d’achèvement d’e/s à utiliser avec les extensions d’e/s inscrites Winsock. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Reçoit des données réseau sur un socket TCP d’e/s inscrit connecté ou un socket UDP d’e/s lié lié pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Reçoit des données réseau sur un socket TCP d’e/s inscrit connecté ou un socket UDP d’e/s lié lié avec des options supplémentaires à utiliser avec les extensions d’e/s inscrites par Winsock. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Inscrit un [**Rio \_ l’élément bufferID**](rio-bufferid.md), un descripteur de mémoire tampon enregistré, avec une mémoire tampon spécifiée pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Redimensionne une file d’attente d’achèvement d’e/s pour qu’elle soit plus grande ou plus petite pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Redimensionne une file d’attente de demandes pour qu’elle soit plus grande ou plus petite pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Envoie des données réseau sur un socket TCP d’e/s inscrit connecté ou un socket UDP d’e/s lié lié pour une utilisation avec les extensions d’e/s inscrites Winsock. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Envoie des données réseau sur un socket TCP e/s inscrit connecté ou un socket UDP d’e/s lié lié avec des options supplémentaires à utiliser avec les extensions d’e/s inscrites Winsock. |
| [**sélectionné**](/windows/win32/api/Winsock2/nf-winsock2-select) | Détermine l’état d’un ou plusieurs sockets, en attente, le cas échéant, d’effectuer des e/s synchrones. |
| [**Envoyer**](/windows/win32/api/Winsock2/nf-winsock2-send) | Envoie des données sur un socket connecté. |
| [**SendTo**](/windows/win32/api/winsock/nf-winsock-sendto) | Envoie des données vers une destination spécifique. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Inscrit un hôte et un nom de service, ainsi que les adresses associées avec un fournisseur d’espaces de noms spécifique. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Définit l’état du filtre de multidiffusion pour un socket IPv4. |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Inscrit ou supprime du registre un service réseau dans un ou plusieurs espaces de noms. Peut également ajouter ou supprimer un type de service réseau dans un ou plusieurs espaces de noms. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Indique si le réseau doit être utilisé pour transférer le média de diffusion en continu qui requiert la qualité de service. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Définit une option de Socket. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Définit l’état du filtre de multidiffusion pour un socket IPv4 ou IPv6. |
| [**correct**](/windows/win32/api/winsock/nf-winsock-shutdown) | Désactive les envois ou les réceptions sur un Socket. |
| [**socle**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Crée un socket qui est lié à un fournisseur de services spécifique. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Transmet des données de fichier sur un handle de socket connecté. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Transmet des données ou des données de fichier en mémoire sur un socket connecté. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Accepte de manière conditionnelle une connexion basée sur la valeur de retour d’une fonction de condition, fournit des spécifications de workflow de qualité de service et autorise le transfert de données de connexion. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Convertit tous les composants d’une structure [**sockaddr**](sockaddr-2.md) en une représentation sous forme de chaîne explicite de l’adresse. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Récupère de manière asynchrone les informations sur l’hôte qui correspondent à une adresse. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Récupère de manière asynchrone les informations sur l’hôte qui correspondent à un nom d’hôte. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Récupère de manière asynchrone les informations de protocole qui correspondent à un nom de protocole. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Récupère de manière asynchrone les informations de protocole qui correspondent à un numéro de protocole. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Récupère de manière asynchrone les informations de service qui correspondent à un nom de service et à un port. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Récupère de manière asynchrone les informations de service qui correspondent à un port et à un protocole. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | demande Windows notification basée sur les messages des événements réseau d’un socket. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Annule une opération asynchrone incomplète. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Met fin à l’utilisation du \_32.DLL Ws2. |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Ferme un handle d’objet d’événement ouvert. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Établit une connexion à une autre application de socket, échange des données de connexion et spécifie la qualité de service nécessaire en fonction de la structure de [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) spécifiée. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Établit une connexion à un à partir d’une collection de points de terminaison possibles représentés par un jeu d’adresses de destination (noms d’hôte et ports). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Établit une connexion à une autre application de socket sur un hôte et un port spécifiés |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Crée un nouvel objet d’événement. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Supprime l’association entre un nom de cible d’homologue et une adresse IP pour un Socket. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Retourne une structure qui peut être utilisée pour créer un nouveau descripteur de socket pour un socket partagé. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Récupère des informations sur les espaces de noms disponibles. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Récupère des informations sur les espaces de noms disponibles. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Détecte les occurrences des événements réseau pour le socket indiqué, efface les enregistrements d’événements de réseau interne et réinitialise les objets d’événement (facultatif). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Récupère des informations sur les protocoles de transport disponibles. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Spécifie un objet d’événement à associer à l’ensemble spécifié d' \_ événements réseau FD xxx. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Spécifie si un socket est inclus dans un ensemble de descripteurs de Socket. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Interroge l’état de l’option de socket [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Interroge l’adresse source d’une erreur ICMP reçue sur un socket TCP pendant la configuration de la connexion. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Récupère la MTU de couche IP définie par l’utilisateur pour un Socket. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Retourne l’état d’erreur pour la dernière opération qui a échoué. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Récupère les résultats d’une opération Overlapped sur le socket spécifié. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Initialise une structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) basée sur un modèle nommé, ou fournit une mémoire tampon pour récupérer une énumération des noms de modèles disponibles. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Récupère les informations de classe (schéma) appartenant à une classe de service spécifiée à partir d’un fournisseur d’espace de noms spécifié. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Récupère le nom du service associé au type spécifié. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Récupère la taille maximale d’un message reçu et fusionné pour un socket UDP. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Récupère la taille de message de segmentation pour un socket UDP. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Convertit une \_ valeur u de l’ordre d’octet hôte en ordre d’octet réseau. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Convertit une \_ valeur Short de l’ordre d’octet hôte en ordre d’octet réseau. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Utilisé pour emprunter l’identité du principal de sécurité correspondant à un homologue de socket afin d’effectuer une autorisation au niveau de l’application. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Inscrit un schéma de classe de service dans un espace de noms. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Contrôle le mode d’un Socket. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Joint un nœud terminal dans une session multipoint, échange des données Connect et spécifie la qualité de service nécessaire en fonction des structures spécifiées. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Lance une requête cliente qui est concédée par les informations contenues dans une structure [**WSAQUERYSET**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) . |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Libère le handle utilisé par les appels précédents à [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta). |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Récupérer les informations de service demandées. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Développeurs qui effectuent des appels de contrôle d’e/s à un espace de noms inscrit. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Convertit une \_ valeur u de l’ordre d’octet réseau en ordre d’octet hôte. |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Convertit une \_ valeur de type u Short de l’ordre d’octet réseau en ordre d’octet hôte. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Détermine l’état d’un ou plusieurs Sockets. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Avertit l’application lorsque la configuration du fournisseur est modifiée. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Interroge les informations relatives à la sécurité appliquée à une connexion sur un Socket. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Reçoit des données à partir d’un socket connecté. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Met fin à la réception sur un socket et récupère les données de déconnexion si le socket est orienté connexion. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Reçoit des données à partir d’un socket connecté. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Reçoit un datagramme et stocke l’adresse source. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Reçoit des données et des informations de contrôle facultatives à partir de sockets connectés et non connectés. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Supprime définitivement le schéma de classe de service du Registre. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Réinitialise l’état de l’objet d’événement spécifié à non signalé. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Met fin à l’emprunt d’identité d’un homologue de Socket. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Envoie des données sur un socket connecté. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Lance l’arrêt de la connexion pour le socket et envoie les données de déconnexion. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Envoie des données et des informations de contrôle facultatives à partir de sockets connectés et non connectés. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Envoie des données à une destination spécifique, à l’aide des e/s avec chevauchement, le cas échéant. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Définit l’état de l’objet d’événement spécifié à signalé. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Définit l’état de l’option de socket [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Définit l’unité de transmission de la couche IP définie par l’utilisateur sur un Socket. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Définit le code d’erreur. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Inscrit ou supprime du Registre une instance de service dans un ou plusieurs espaces de noms. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Utilisé pour spécifier le nom de la cible de l’homologue (SPN) qui correspond à une adresse IP d’homologue. Ce nom cible est destiné à être spécifié par les applications clientes afin d’identifier en toute sécurité l’homologue qui doit être authentifié. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Active et applique la sécurité pour un Socket. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Définit la taille maximale d’un ensemble de messages fusionnés sur un socket UDP. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Définit la taille des messages de segmentation sur un socket UDP. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Crée un socket qui est lié à un fournisseur de services de transport spécifique. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Initie l’utilisation de WS2 \_32.DLL par un processus. |
| [**WSAStringToAddress n'**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Convertit une chaîne numérique en une structure [**sockaddr**](sockaddr-2.md) . |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Retourne lorsque l’un des objets d’événement spécifiés se trouve à l’état signalé ou lorsque l’intervalle de délai d’attente expire. |
