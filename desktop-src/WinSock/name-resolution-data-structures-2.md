---
description: Structures de données de résolution de noms dans Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Structures de données de résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1f76607ade81503a1057dc21890ac38d5ec265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558461"
---
# <a name="name-resolution-data-structures"></a>Structures de données de résolution de noms

Il existe plusieurs structures de données importantes qui sont largement utilisées dans les fonctions de résolution de noms.

## <a name="query-related-data-structures"></a>Structures de données de Query-Related

La structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) permet de former des requêtes pour [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)et de fournir des résultats de requête pour [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta). Il s’agit d’une structure complexe, car elle contient des pointeurs vers plusieurs autres structures, dont certaines font référence à d’autres structures. La relation entre la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) et les structures qu’elle référence est illustrée ci-dessous.

![relation entre wsaqueryset et ses structures associées](images/ovrvw3-2.png)

Au sein de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la plupart des membres sont explicites, mais certaines méritent une explication supplémentaire. Le membre **dwSize nul** doit toujours être renseigné avec sizeof (**WSAQUERYSET**), car il est utilisé par les fournisseurs d’espaces de noms pour détecter et s’adapter aux différentes versions de la structure **WSAQUERYSET** qui peuvent apparaître au fil du temps.

Le membre **dwOutputFlags** est utilisé par un fournisseur d’espaces de noms pour fournir des informations supplémentaires sur les résultats de la requête. Pour plus d’informations, consultez la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

La structure [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) référencée par le membre **lpVersion** est utilisée à la fois pour la contrainte de requête et les résultats. Pour les requêtes, le membre **dwVersion** indique la version souhaitée du service. Le membre **ecHow** est un type énuméré qui spécifie la façon dont la comparaison peut être effectuée. Les choix possibles sont \_ égal à, ce qui nécessite qu’une correspondance exacte dans la version se produise, ou comp \_ NOTLESS, qui spécifie que le numéro de version du service ne doit pas être inférieur à la valeur du membre **dwVersion** .

L’interprétation de **dwNameSpace** et de **lpNSProviderId** dépend de la façon dont la structure est utilisée et est décrite plus en détail dans les descriptions de fonction individuelles qui utilisent cette structure.

Le membre **lpszContext** s’applique aux espaces de noms hiérarchiques et spécifie le point de départ d’une requête ou l’emplacement dans la hiérarchie où le service réside. Les règles générales sont les suivantes :

-   La valeur **null**("") commence la recherche dans le contexte par défaut.
-   La valeur « \\ » démarre la recherche en haut de l’espace de noms.
-   Toute autre valeur commence la recherche au point désigné.

Les fournisseurs qui ne prennent pas en charge la relation contenant-contenu peuvent retourner une erreur si tout autre chose que « » ou « » \\ est spécifié. Les fournisseurs qui prennent en charge la relation contenant-contenu limitée, tels que les groupes, doivent accepter « », « » \\ ou un point désigné. Les contextes sont spécifiques à l’espace de noms. Si le membre **dwNameSpace** est NS \_ All, seul « » ou « » \\ doit être passé comme contexte, car ceux-ci sont reconnus par tous les espaces de noms.

Le membre **lpszQueryString** est utilisé pour fournir des informations supplémentaires sur les requêtes spécifiques à l’espace de noms, telles qu’une chaîne décrivant un service et un nom de protocole de transport bien connus, comme dans « FTP/TCP ».

La structure [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) référencée par le membre **lpafpProtocols** est utilisée à des fins de requête uniquement et fournit une liste de protocoles pour contraindre la requête. Ces protocoles sont représentés par des paires (de famille d’adresses, protocole), car les valeurs de protocole n’ont que la signification dans le contexte d’une famille d’adresses.

Le tableau de la structure d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) référencé par le membre **lpcsaBuffer** contient toutes les informations nécessaires pour qu’un service soit utilisé pour établir une écoute, ou pour qu’un client l’utilise pour établir une connexion au service. Les membres **LocalAddr** et **RemoteAddr** contiennent directement une structure [**d' \_ adresse de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) .

Un service crée un socket en appelant la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) à l’aide du Tuple *de LocalAddr. lpSockaddr->sa \_ Family*, *iSocketType* et *iProtocol* comme paramètres. Un service lie le socket à une adresse locale en appelant la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) à l’aide de *LocalAddr. lpSockaddr* et *LocalAddr. lpSockaddrLength* en tant que paramètres.

Un client crée son socket en appelant la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) à l’aide du tuple de *LocalAddr. lpSockaddr->sa \_ Family*, *iSocketType* et *iProtocol* comme paramètres. Un client utilise la combinaison de *RemoteAddr. lpSockaddr* et *RemoteAddr. lpSockaddrLength* comme paramètres lors de l’établissement d’une connexion à distance à l’aide de la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)ou [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) .

## <a name="service-class-data-structures"></a>Structures de données de classe de service

Quand une nouvelle classe de service est installée, une structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) doit être préparée et fournie. Cette structure se compose également de sous-structures qui contiennent une série de membres qui s’appliquent à des espaces de noms spécifiques. Une structure de données d’informations de classe se présente comme suit :

![architecture des structures de données de classe de service](images/ovrvw3-3.png)

Pour chaque classe de service, il existe une seule structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Dans la structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) , l’identificateur unique de la classe de service est contenu dans le membre **lpServiceClassId** , et une chaîne d’affichage associée est référencée par le membre **lpServiceClassName** . Il s’agit de la chaîne retournée par la fonction [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) .

Le membre **lpClassInfos** de la structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fait référence à un tableau de structures **WSANSCLASSINFO** , chacune d’elles fournissant un membre nommé et typé qui s’applique à un espace de noms spécifié. Exemples de valeurs pour le membre **lpszName** : « sapid », « TCPPort », « UdpPort », etc. Ces chaînes sont généralement spécifiques à l’espace de noms identifié dans le membre **dwNameSpace** . Les valeurs typiques du membre **dwValueType** peuvent être reg \_ DWORD, reg \_ SZ, etc. Le membre **dwValueSize** indique la longueur de l’élément de données vers lequel pointe **lpValue**.

L’intégralité de la collection de données représentée dans une structure **WSASERVICECLASSINFO** est fournie à chaque fournisseur d’espaces de noms lorsque la fonction [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) est appelée. Chaque fournisseur d’espace de noms individuel passe ensuite en revue la liste des structures **WSANSCLASSINFO** et conserve les informations qui lui sont applicables.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**\_informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Modèle de résolution de noms](name-resolution-model-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> <dt>

[**adresse du SOCKET \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Résumé des fonctions de résolution de noms](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
