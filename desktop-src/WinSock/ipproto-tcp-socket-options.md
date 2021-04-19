---
description: Le tableau suivant décrit les \_ options de socket TCP IPPROTO qui s’appliquent aux sockets créés pour les familles d’adresses IPv4 et IPv6 (AF \_ inet et AF \_ inet6) avec le paramètre de protocole à la fonction de socket spécifiée en tant que TCP (IPPROTO \_ TCP).
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: IPPROTO_TCP socket, options
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545435"
---
# <a name="ipproto_tcp-socket-options"></a>\_Options de socket TCP IPPROTO

Le tableau suivant décrit les options de socket **\_ TCP IPPROTO** qui s’appliquent aux sockets créés pour les familles d’adresses IPv4 et IPv6 (AF \_ inet et AF \_ inet6) avec le paramètre de *protocole* à la fonction de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) spécifiée en tant que TCP (IPPROTO \_ TCP). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Options

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Obtenir</th>
<th>Définissez</th>
<th>Type Optval</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Si la <strong>valeur est true</strong>, le fournisseur de services implémente le style BSD (Berkeley Software Distribution) (par défaut) pour la gestion des données expédiées. Cette option est l’inverse de l’option TCP_EXPEDITED_1122. Cette option ne peut être définie qu’une seule fois sur la connexion. Une fois cette option activée, cette option ne peut pas être désactivée. Cette option ne doit pas être implémentée par les fournisseurs de services. Par défaut, l’option est activée (définie à <strong>true</strong>).</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Si la <strong>valeur est true</strong>, le fournisseur de services implémente les données expédiées comme spécifié dans le document RFC-1222. Dans le cas contraire, le style BSD (Berkeley Software Distribution) (par défaut) est utilisé. Cette option ne peut être définie qu’une seule fois sur la connexion. Une fois cette option activée, cette option ne peut pas être désactivée. Cette option ne doit pas être implémentée par les fournisseurs de services.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Si la valeur est <strong>true</strong>, un appel d’API Connect retourne la réception d’une erreur ICMP avec la valeur WSAEHOSTUNREACH. L’adresse source de l’erreur sera ensuite disponible via l’option TCP_ICMP_ERROR_INFO Socket. Si la <strong>valeur est false</strong>, le socket se comporte normalement. La valeur par défaut est Disabled ( <strong>false</strong>). Pour la sécurité de type, vous devez utiliser les fonctions <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> et <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> au lieu d’utiliser directement l’option de Socket.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>Oui</td>
<td>non</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Récupère les informations d’une erreur ICMP reçue par le socket TCP pendant un appel de connexion ayant échoué. Valide uniquement sur un socket TCP où TCP_FAIL_CONNECT_ON_ICMP_ERROR a déjà été activé, et <strong>Connect</strong> a retourné WSAEHOSTUNREACH. La requête est non bloquante. Si la requête a réussi et que la valeur optlen retournée est 0, aucune erreur ICMP n’a été reçue depuis le dernier appel de connexion. Si une erreur ICMP a été reçue, ses informations sont disponibles jusqu’à ce que la <strong>connexion</strong> soit à nouveau appelée. Les informations sont retournées sous la forme d’une structure <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> . Pour la sécurité de type, vous devez utiliser la fonction <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> au lieu d’utiliser directement l’option de Socket.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD</td>
<td>Obtient ou définit le nombre de sondes KeepAlive TCP qui seront envoyées avant que la connexion ne soit terminée. Il n’est pas conforme de définir TCP_KEEPCNT sur une valeur supérieure à 255.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD</td>
<td>Si cette valeur n’est pas négative, elle représente le délai de connexion souhaité en secondes. Si la valeur est-1, elle représente une demande de désactivation du délai d’expiration de la connexion (c’est-à-dire que la connexion est retransmise définitivement). Si le délai de connexion est désactivé, le délai d’attente de retransmission augmente de façon exponentielle pour chaque retransmission jusqu’à sa valeur maximale de 60sec, puis reste là.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Active ou désactive l’algorithme Nagle pour les sockets TCP. Cette option est désactivée (définie sur FALSe) par défaut.</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Active ou désactive les horodatages RFC 1323. Notez qu’il existe également une configuration globale pour les horodateurs (la valeur par défaut est OFF), les &quot; horodateurs &quot; dans (Set/obten)-nettcpsetting. La définition de cette option de socket remplace ce paramètre de configuration globale.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD (booléen)</td>
<td>Active ou désactive la <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, qui vous permet de commencer à envoyer des données pendant la phase de négociation triple de l’ouverture d’une connexion. Notez que pour utiliser des ouvertures rapides, vous devez utiliser <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> pour établir la connexion initiale et spécifier les données dans le paramètre <em>lpSendBuffer</em> de cette fonction à transférer au cours du processus d’établissement de liaison. Certaines des données de <em>lpSendBuffer</em> seront transférées sous le protocole Fast Open.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD</td>
<td>Obtient ou définit le nombre de secondes pendant lesquelles une connexion TCP reste inactive avant que les sondes KeepAlive soient envoyées à l’adresse distante.
<blockquote>
[!Note]<br />
Cette option est disponible à partir de Windows 10, version 1709.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>Oui</td>
<td>Oui</td>
<td>DWORD</td>
<td>Obtient ou définit le nombre de secondes qu’une connexion TCP attendra pour une réponse KeepAlive avant d’envoyer une autre sonde KeepAlive.
<blockquote>
[!Note]<br />
Cette option est disponible à partir de Windows 10, version 1709.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Prise en charge de Windows pour les \_ options TCP IPPROTO

| Option | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x |
| TCP \_ expédié \_ 1122 | x | x | x | x |
| \_KEEPCNT TCP | À compter de Windows 10, version 1703 | | | |
| \_MAXRT TCP | x | x | x | x |
| TCP- \_ délai | x | x | x | x |
| \_horodateurs TCP | x | x | x | x |
| \_FASTOPEN TCP | À compter de Windows 10, version 1607 | | | |

<br/>

 | Option | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x | |
| TCP \_ expédié \_ 1122 | x | x | x | | |
| \_KEEPCNT TCP | | | | | |
| \_MAXRT TCP | | | | | |
| TCP- \_ délai | x | x | x | x | |
| \_horodateurs TCP | | | | | |
| \_FASTOPEN TCP | | | | | |

## <a name="remarks"></a>Notes

Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et le niveau **\_ TCP IPPROTO** est défini dans le fichier d’en-tête *Ws2def. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Les options de socket **\_ TCP IPPROTO** , à l’exception de **TCP \_ BSDURGENT**, sont définies dans le fichier d’en-tête *Ws2ipdef. h* qui est automatiquement inclus dans le fichier d’en-tête *Ws2tcpip. h* . L’option **TCP \_ BSDURGENT** pour les raisons historiques est définie dans le fichier d’en-tête *mswsock. h* . Les fichiers d’en-tête *Ws2def. h* et *Ws2ipdef. h* ne doivent jamais être utilisés directement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | <dl> <dt>Ws2def. h (inclure Winsock2. h); </dt> <dt>Winsock2. h sur Windows Server 2003, Windows XP et windows 2000</dt> </dl> |
