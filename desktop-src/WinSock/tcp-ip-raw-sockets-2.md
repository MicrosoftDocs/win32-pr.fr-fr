---
description: Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Sockets bruts TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25cc08d59d80089a4e655f363e4a899edac8d2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517783"
---
# <a name="tcpip-raw-sockets"></a>Sockets bruts TCP/IP

Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent. Cette rubrique se concentre uniquement sur les sockets bruts et les protocoles IPv4 et IPv6. Cela est dû au fait que la plupart des autres protocoles, à l’exception de la technologie ATM, ne prennent pas en charge les sockets bruts. Pour utiliser des sockets bruts, une application doit avoir des informations détaillées sur le protocole sous-jacent utilisé.

Les fournisseurs de services Winsock pour le protocole IP peuvent prendre en charge un *type* de socket **\_ brut**. Le fournisseur Windows Sockets 2 pour TCP/IP inclus sur Windows prend en charge ce type de socket **\_ brut de chaussette** .

Il existe deux types de sockets bruts de base :

-   Le premier type utilise un type de protocole connu écrit dans l’en-tête IP qui est reconnu par un fournisseur de services Winsock. Un exemple du premier type de socket est un socket pour le protocole ICMP (type de protocole IP = 1) ou le protocole ICMPv6 (IP Protocole type = 58).
-   Le deuxième type autorise la spécification d’un type de protocole. Un exemple du second type est un protocole expérimental qui n’est pas directement pris en charge par le fournisseur de services Winsock, tel que le protocole SCTP (Stream Control Transmission Protocol).

## <a name="determining-if-raw-sockets-are-supported"></a>Détermination de la prise en charge des sockets bruts

Si un fournisseur de services Winsock prend en charge les Sockets **\_ bruts de chaussette** pour les \_ familles d’adresses AF inet ou AF \_ inet6, le type de socket **\_ RAW RAW** doit être inclus dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retournée par la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) pour un ou plusieurs des fournisseurs de transport disponibles.

Le **membre iAddressFamily** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) doit spécifier AF \_ inet ou AF \_ inet6 et le membre **iSocketType** de la structure d' **\_ informations WSAPROTOCOL** doit spécifier les membres de la **chaussette pour \_** l’un des fournisseurs de transport.

Le membre **iProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) peut être défini sur **\_ IP IPROTO**. Le membre **iProtocol** de la structure **WSAPROTOCOL \_ info** peut également être défini à zéro si le fournisseur de services permet à une application d’utiliser un type de socket **\_ brut de chaussette** pour d’autres protocoles réseau autres que le protocole Internet pour la famille d’adresses.

Les autres membres de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indiquent d’autres propriétés de la prise en charge de protocole pour les éléments **\_ bruts bruts** et indiquent comment un socket de **chaussette \_ brut** doit être traité. Ces autres membres de l' **WSAPROTOCOL \_ info** pour **chaussette \_ RAW** spécifient normalement que le protocole est sans connexion, orienté message, prend en charge la diffusion/multidiffusion (la \_ connexion XP1 sans connexion, le \_ message XP1 orienté, la diffusion de la \_ \_ prise en charge XP1 \_ et XP1 \_ prennent en charge les \_ bits multipoint sont définis dans le membre dwServiceFlags1) et peuvent avoir une taille de message maximale de 65 467 octets.

Sur Windows XP et versions ultérieures, la commande *NetSh.exe* peut être utilisée pour déterminer si les sockets bruts sont pris en charge. La commande suivante, exécutée à partir d’une fenêtre CMD, affiche les données du catalogue Winsock sur la console :

**netsh Winsock-afficher le catalogue**

La sortie inclut une liste contenant certaines des données des structures [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) prises en charge sur l’ordinateur local. Recherchez le terme RAW/IP ou RAW/IPv6 dans le champ Description pour rechercher les protocoles qui prennent en charge les sockets bruts.

## <a name="creating-a-raw-socket"></a>Création d’un socket brut

Pour créer un socket de type **chaussette \_ RAW**, appelez la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) avec le paramètre *AF* (famille d’adresses) défini sur \_ AF inet ou AF \_ inet6, le paramètre de *type* défini sur **chaussette \_ RAW** et le paramètre *Protocol* défini sur le numéro de protocole requis. Le paramètre *Protocol* devient la valeur de protocole dans l’en-tête IP (SCTP est 132, par exemple).

> [!Note]  
> Une application ne peut pas spécifier zéro (0) comme paramètre de *protocole* pour les fonctions [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)et [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) si le paramètre de *type* est défini sur **chaussette \_ RAW**.

 

Les sockets bruts offrent la possibilité de manipuler le transport sous-jacent, de sorte qu’ils peuvent être utilisés à des fins malveillantes qui constituent une menace pour la sécurité. Par conséquent, seuls les membres du groupe administrateurs peuvent créer des sockets de type chaussette \_ RAW sur Windows 2000 et versions ultérieures.

## <a name="send-and-receive-operations"></a>Opérations d’envoi et de réception

Une fois qu’une application a créé un socket de type **chaussette \_ RAW**, ce socket peut être utilisé pour envoyer et recevoir des données. Tous les paquets envoyés ou reçus sur un socket de type **chaussette \_ RAW** sont traités comme des datagrammes sur un socket non connecté.

Les règles suivantes s’appliquent aux opérations sur les Sockets **\_ bruts de chaussette** :

-   La fonction [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) ou [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) est normalement utilisée pour envoyer des données sur un socket de type **chaussette \_ RAW**. L’adresse de destination peut être toute adresse valide dans la famille d’adresses du socket, y compris une adresse de diffusion ou de multidiffusion. Pour envoyer à une adresse de diffusion, une application doit avoir utilisé [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avec la \_ diffusion activée. Dans le cas contraire, **sendto** ou **WSASendTo** échoue avec le code d’erreur [WSAEACCES](windows-sockets-error-codes-2.md). Pour l’adresse IP, une application peut envoyer vers n’importe quelle adresse de multidiffusion (sans devenir membre du groupe).
-   Lors de l’envoi de données IPv4, une application peut choisir de spécifier l’en-tête IPv4 au début du datagramme sortant pour le paquet. Si l’option de socket **\_ HDRINCL IP** est définie sur true pour un socket IPv4 (famille d’adresses d’AF \_ inet), l’application doit fournir l’en-tête IPv4 dans les données sortantes pour les opérations d’envoi. Si cette option de socket est false (paramètre par défaut), l’en-tête IPv4 ne doit pas être inclus dans les données sortantes pour les opérations d’envoi.
-   Lors de l’envoi de données IPv6, une application peut choisir de spécifier l’en-tête IPv6 au début du datagramme sortant pour le paquet. Si l’option de socket **IPv6 \_ HDRINCL** a la valeur true pour un socket IPv6 (famille d’adresses AF \_ inet6), l’application doit fournir l’en-tête IPv6 dans les données sortantes pour les opérations d’envoi. La valeur par défaut de cette option est false. Si cette option de socket est false (paramètre par défaut), l’en-tête IPv6 ne doit pas être inclus dans les données sortantes pour les opérations d’envoi. Pour IPv6, il n’est pas nécessaire d’inclure l’en-tête IPv6. Si des informations sont disponibles à l’aide des fonctions socket, l’en-tête IPv6 ne doit pas être inclus pour éviter des problèmes de compatibilité à l’avenir. Ces problèmes sont abordés dans le document RFC 3542 publié par l’IETF. L’utilisation de l’option de socket **IPv6 \_ HDRINCL** n’est pas recommandée et peut être dépréciée dans le futur.
-   La fonction [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) est normalement utilisée pour recevoir des données sur un socket de type **chaussette \_ RAW**. Ces deux fonctions ont une option pour retourner l’adresse IP source à partir de laquelle le paquet a été envoyé. Les données reçues sont un datagramme d’un socket non connecté.
-   Pour IPv4 (famille d’adresses de AF \_ inet), une application reçoit l’en-tête IP au début de chaque datagramme reçu, quelle que soit l’option de socket **\_ HDRINCL IP** .
-   Pour IPv6 (famille d’adresses d’AF \_ inet6), une application reçoit tout ce qui se trouve après le dernier en-tête IPv6 de chaque datagramme reçu, quelle que soit l’option de socket **IPv6 \_ HDRINCL** . L’application ne reçoit aucun en-tête IPv6 utilisant un socket brut.
-   Les Datagrammes reçus sont copiés dans tous les Sockets **\_ bruts de chaussette** qui remplissent les conditions suivantes :

    -   Le numéro de protocole spécifié dans le paramètre de *protocole* lors de la création du socket doit correspondre au numéro de protocole dans l’en-tête IP du datagramme reçu.
    -   Si une adresse IP locale est définie pour le socket, elle doit correspondre à l’adresse de destination telle qu’elle est spécifiée dans l’en-tête IP du datagramme reçu. Une application peut spécifier l’adresse IP locale en appelant la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) . Si aucune adresse IP locale n’est spécifiée pour le socket, les datagrammes sont copiés dans le socket, quelle que soit l’adresse IP de destination dans l’en-tête IP du datagramme reçu.
    -   Si une adresse étrangère est définie pour le socket, elle doit correspondre à l’adresse source telle qu’elle est spécifiée dans l’en-tête IP du datagramme reçu. Une application peut spécifier l’adresse IP étrangère en appelant la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) . Si aucune adresse IP étrangère n’est spécifiée pour le socket, les datagrammes sont copiés dans le socket, quelle que soit l’adresse IP source dans l’en-tête IP du datagramme reçu.

Il est important de comprendre que certains Sockets de type **chaussette \_ RAW** peuvent recevoir de nombreux datagrammes inattendus. Par exemple, un programme PING peut créer un socket de type **chaussette \_ RAW** pour envoyer des demandes d’écho ICMP et recevoir des réponses. Alors que l’application attend des réponses ICMP Echo, tous les autres messages ICMP (tels que \_ l’hôte ICMP inaccessible) peuvent également être remis à cette application. En outre, si plusieurs Sockets **\_ bruts de chaussette** sont ouverts sur un ordinateur en même temps, les mêmes datagrammes peuvent être remis à tous les sockets ouverts. Une application doit avoir un mécanisme pour reconnaître les datagrammes intéressants et ignorer toutes les autres. Pour un programme PING, un tel mécanisme peut inclure l’inspection de l’en-tête IP reçu pour identifier les identificateurs uniques dans l’en-tête ICMP (l’ID de processus de l’application, par exemple).

> [!Note]  
> L’utilisation d’un socket de type **chaussette \_ RAW** requiert des privilèges d’administrateur. Les utilisateurs qui exécutent des applications Winsock qui utilisent des sockets bruts doivent être membres du groupe Administrateurs sur l’ordinateur local, sinon les appels de socket brut échouent avec un code d’erreur [WSAEACCES](windows-sockets-error-codes-2.md). Sur Windows Vista et versions ultérieures, l’accès aux sockets bruts est appliqué au moment de la création du Socket. Dans les versions antérieures de Windows, l’accès aux sockets bruts est appliqué au cours d’autres opérations de Socket.

 

## <a name="common-uses-of-raw-sockets"></a>Utilisations courantes des sockets bruts

Une utilisation courante des sockets bruts consiste à dépanner les applications qui doivent examiner les paquets IP et les en-têtes en détail. Par exemple, un socket brut peut être utilisé avec l' \_ IOCTL SIO RCVALL pour permettre à un socket de recevoir tous les paquets IPv4 ou IPv6 passant par une interface réseau. Pour plus d’informations, consultez la référence [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

## <a name="limitations-on-raw-sockets"></a>Limitations sur les sockets bruts

Sur Windows 7, Windows Vista, Windows XP avec Service Pack 2 (SP2) et Windows XP avec Service Pack 3 (SP3), la possibilité d’envoyer du trafic sur des sockets bruts a été restreinte de plusieurs façons :

-   Impossible d’envoyer les données TCP sur des sockets bruts.
-   Les datagrammes UDP avec une adresse source non valide ne peuvent pas être envoyés sur des sockets bruts. L’adresse IP source de tout datagramme UDP sortant doit exister sur une interface réseau ou le datagramme est abandonné. Cette modification a été apportée pour limiter la capacité du code malveillant à créer des attaques par déni de service distribuées et limite la possibilité d’envoyer des paquets falsifiés (paquets TCP/IP avec une adresse IP source falsifiée).
-   Un appel à la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) avec un socket brut pour le \_ protocole TCP IPPROTO n’est pas autorisé.
    > [!Note]  
    > La fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) avec un socket brut est autorisée pour d’autres protocoles (IPPROTO \_ IP, IPPROTO \_ UDP ou IPPROTO \_ SCTP, par exemple).

     

Les restrictions ci-dessus ne s’appliquent pas à Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 ou aux versions du système d’exploitation antérieures à Windows XP avec SP2.

> [!Note]  
> L’implémentation Microsoft du protocole TCP/IP sur Windows est en charge de l’ouverture d’un socket UDP ou TCP brut basé sur les restrictions ci-dessus. D’autres fournisseurs Winsock peuvent ne pas prendre en charge l’utilisation de sockets bruts.

 

Il existe des limitations supplémentaires pour les applications qui utilisent un socket de type **chaussette \_ RAW**. Par exemple, toutes les applications qui écoutent un protocole spécifique recevront tous les paquets reçus pour ce protocole. Ce n’est peut-être pas ce que vous souhaitez pour plusieurs applications utilisant un protocole. Elle n’est pas non plus adaptée aux applications hautes performances. Pour contourner ces problèmes, il peut être nécessaire d’écrire un pilote de protocole réseau Windows (pilote de périphérique) pour le protocole réseau spécifique. Sur Windows Vista et versions ultérieures, Winsock kernel (WSK), une nouvelle interface de programmation réseau indépendante du transport, peut être utilisé pour écrire un pilote de protocole réseau. Sur Windows Server 2003 et versions antérieures, un fournisseur interface TDI (TDI) et une DLL d’assistance Winsock peuvent être écrits pour prendre en charge le protocole réseau. Le protocole réseau est ensuite ajouté au catalogue Winsock en tant que protocole pris en charge. Cela permet à plusieurs applications d’ouvrir des sockets pour ce protocole spécifique et le pilote de périphérique peut assurer le suivi du socket qui reçoit des paquets et des erreurs spécifiques. Pour plus d’informations sur l’écriture d’un fournisseur de protocole réseau, consultez les sections sur WSK et TDI dans le kit WDK (Windows Driver Kit).

Les applications doivent également connaître l’impact que les paramètres de pare-feu peuvent avoir sur l’envoi et la réception de paquets à l’aide de sockets bruts.

 

 
