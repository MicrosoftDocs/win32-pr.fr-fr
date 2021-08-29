---
description: La structure WSAQUERYSET permet de former des requêtes pour la fonction NSPLookupServiceBegin et de fournir des résultats de requête pour la fonction NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related les structures de données dans l’index SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcbd83ab427a6ec3f09c67f416fe5eb8d7ebaad165bf4e687dfd31dce882cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569363"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related les structures de données dans l’index SPI

La structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) permet de former des requêtes pour [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)et de fournir des résultats de requête pour [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext). Il s’agit d’une structure complexe, car elle contient des pointeurs vers plusieurs autres structures, dont certaines font référence à d’autres structures. La relation entre **WSAQUERYSET** et les structures qu’elle référence est illustrée comme suit :

![structures wsaqueryset](images/ovrvw3-2.png)

Au sein de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la plupart des membres sont explicites, mais certaines méritent une explication supplémentaire. Le **dwSize nul** sera rempli avec sizeof ( **WSAQUERYSET**) et peut être utilisé par les fournisseurs d’espaces de noms pour détecter et s’adapter aux différentes versions de la structure **WSAQUERYSET** qui peuvent apparaître.

Le membre **dwOutputFlags** est utilisé par un fournisseur d’espaces de noms pour fournir des données supplémentaires sur les résultats de la requête. Pour plus d’informations, consultez [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

La structure [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) référencée par **lpVersion** est utilisée pour la contrainte de requête et les résultats. Pour les requêtes, le membre **dwVersion** indique la version souhaitée du service. Le membre **ecHow** est un type énuméré qui spécifie la façon dont la comparaison sera effectuée. Les choix possibles sont \_ égal à, ce qui nécessite qu’une correspondance exacte dans la version se produit, ou comp \_ NOTLESS qui spécifie que le numéro de version du service ne doit pas être inférieur à la valeur de **dwVersion**.

L’interprétation de **dwNameSpace** et de **lpNSProviderId** dépend de la façon dont la structure est utilisée et est décrite plus en détail dans les descriptions de fonction individuelles qui utilisent cette structure.

Le membre **lpszContext** s’applique aux espaces de noms hiérarchiques et spécifie le point de départ d’une requête ou l’emplacement dans la hiérarchie où le service réside. Les règles générales sont les suivantes :

-   La valeur **null**("") commence la recherche dans le contexte par défaut.
-   La valeur « \\ » démarre la recherche en haut de l’espace de noms.
-   Toute autre valeur commence la recherche au point désigné.

Les fournisseurs qui ne prennent pas en charge la relation contenant-contenu peuvent retourner une erreur si tout autre chose que « » ou « » \\ est spécifié. Les fournisseurs qui prennent en charge la relation contenant-contenu limitée, tels que les groupes, doivent accepter « », « » \\ ou un point désigné. Les contextes sont spécifiques à l’espace de noms. Si **dwNameSpace** est \_ All NS, seul « » ou « » \\ doit être passé comme contexte, car ceux-ci sont reconnus par tous les espaces de noms.

Le membre **lpszQueryString** est utilisé pour fournir des informations supplémentaires sur les requêtes spécifiques à l’espace de noms, telles qu’une chaîne décrivant un service et un nom de protocole de transport bien connus, comme dans « FTP/TCP ».

La structure [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) référencée par **lpafpProtocols** est utilisée à des fins de requête uniquement et fournit une liste de protocoles pour contraindre la requête. Ces protocoles sont représentés par des paires (de famille d’adresses, protocole), car les valeurs de protocole n’ont que la signification dans le contexte d’une famille d’adresses.

Le tableau de la structure d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) référencé par **lpcsaBuffer** contient toutes les informations requises pour qu’un service soit utilisé pour établir une écoute ou un client à utiliser lors de l’établissement d’une connexion au service. Les membres **LocalAddr** et **RemoteAddr** contiennent directement une structure [**d' \_ adresse de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) . Un service crée un socket à l’aide du tuple (LocalAddr. lpSockaddr->sa \_ Family, iSocketType, iProtocol). Il lie le socket à une adresse locale à l’aide de LocalAddr. lpSockaddr et LocalAddr. lpSockaddrLength. Le client crée son socket avec le Tuple (RemoteAddr. lpSockaddr->sa \_ Family, iSocketType, iProtocol) et utilise la combinaison de RemoteAddr. lpSockaddr et RemoteAddr. lpSockaddrLength lors de l’établissement d’une connexion à distance.

 

 
