---
description: Un fournisseur d’espaces de noms implémente un mappage d’interface entre le SPI d’espace de noms Winsock et l’interface de programmation native d’un service de noms existant, tel que DNS, X. 500 ou Services d’annuaire NetWare (NDS) (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Fournisseurs de services d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e6ecc9ad0dcb9667bdd3d08049b9d41c3211de422cae0530506f6103494527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822637"
---
# <a name="namespace-service-providers"></a>Fournisseurs de services d’espace de noms

Un fournisseur d’espaces de noms implémente un mappage d’interface entre le SPI d’espace de noms Winsock et l’interface de programmation native d’un service de noms existant, tel que DNS, X. 500 ou Services d’annuaire NetWare (NDS) (NDS). Bien qu’un fournisseur d’espaces de noms ne prenne en charge qu’un seul espace de noms, il est possible d’installer plusieurs fournisseurs pour un espace de noms donné. Il est également possible pour une DLL unique de créer une instance de plusieurs fournisseurs d’espaces de noms. Au fur et à mesure de l’installation de fournisseurs d’espaces de noms, un catalogue de structures d' [**\_ informations WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) est conservé. Une application peut utiliser [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) pour détecter les espaces de noms pris en charge sur un ordinateur.

sur Windows Vista et versions ultérieures, une structure [**\_ INFOEX WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) améliorée et une fonction [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) sont fournies.

Sur les plateformes 64 bits, les fonctions [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) et [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) similaires sont fournies pour énumérer le catalogue 32 bits.

Pour plus d’informations, consultez [Configuration requise du fournisseur de services d’espaces de noms Winsock](winsock-namespace-service-provider-requirements.md) .

## <a name="legacy-getxbyy-service-providers"></a>Fournisseurs de services GetXbyY hérités

Windows sockets 2 prend entièrement en charge les fonctionnalités de résolution de noms propres à TCP/IP qui se trouvent dans Windows sockets version 1,1. Pour ce faire, il inclut l’ensemble des fonctions **GetXbyY** dans le SPI. Toutefois, le traitement de cet ensemble de fonctions est légèrement différent du reste des fonctions SPI. Les fonctions **GetXbyY** figurant dans le SPI sont précédées de GETXBYYSP \_ et sont résumées dans le tableau suivant.

Fonctions de style Berkeley



| Nom de la fonction SPI           | Description                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Fournit une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) pour l’adresse d’hôte spécifiée.        |
| GETXBYYSP \_ gethostbyname    | Fournit une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) pour le nom d’hôte spécifié.           |
| GETXBYYSP \_ getprotobyname   | Fournit une structure [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) pour le nom de protocole spécifié.     |
| GETXBYYSP \_ getprotobynumber | Fournit une structure [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) pour le numéro de protocole spécifié.   |
| GETXBYYSP \_ getservbyname    | Fournit une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) pour le Nam de service spécifié.        |
| GETXBYYSP \_ getservbyport    | Fournit une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) pour le service au niveau du port spécifié. |
| GETXBYYSP \_ GetHostName      | Retourne le nom d’hôte standard de l’ordinateur local.                                   |



 

Fonctions de style asynchrone



| Nom de la fonction SPI                   | Description                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Fournit une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) pour l’adresse d’hôte spécifiée.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Fournit une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) pour le nom d’hôte spécifié.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Fournit une structure [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) pour le nom de protocole spécifié.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Fournit une structure [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) pour le numéro de protocole spécifié.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Fournit une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) pour le nom de service spécifié.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Fournit une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) pour le service au niveau du port spécifié. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Annule une opération **GetXbyY** asynchrone.                                           |



 

La syntaxe et la sémantique de ces fonctions **GetXbyY** dans le SPI sont exactement les mêmes que celles documentées dans la spécification de l’API et ne sont donc pas répétées ici.

la DLL Windows sockets 2 permet à un seul fournisseur de services d’offrir ces services. Par conséquent, il n’est pas nécessaire d’inclure des pointeurs vers ces fonctions dans la table de procédure reçue des fournisseurs de services au démarrage. dans Windows environnements, le chemin d’accès à la DLL qui implémente ces fonctions est récupéré à partir de la valeur trouvée dans le chemin d’accès au registre suivant. Cette entrée de Registre n’existe pas par défaut :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** Winsock2 des services \\  de CurrentControlSet de système d’ordinateur local GetXByYLibraryPath

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In fournisseur de services GetXbyY par défaut

un fournisseur de services **GetXbyY** par défaut est intégré aux composants runtime Windows sockets 2 standard. Ce fournisseur par défaut implémente toutes les fonctions ci-dessus. par conséquent, il n’est pas nécessaire que ces fonctions soient implémentées par n’importe quel fournisseur d’espace de noms. Toutefois, un fournisseur d’espace de noms est libre de fournir une partie ou l’ensemble de ces fonctions (et donc de remplacer les valeurs par défaut) en stockant simplement la chaîne qui est le chemin d’accès à la DLL qui implémente ces fonctions dans la clé de Registre indiquée. Les fonctions **GetXbyY** qui ne sont pas exportées par la dll du fournisseur nommé seront fournies via les valeurs par défaut intégrées. Notez, toutefois, que si un fournisseur choisit de fournir une des versions Async des fonctions **GetXbyY** , il doit fournir toutes les fonctions Async afin que l’opération d’annulation fonctionne correctement.

L’implémentation actuelle du fournisseur de services **GetXbyY** par défaut réside dans le Wsock32.dll. Selon la façon dont les paramètres TCP/IP ont été établis par le biais du panneau de configuration, la résolution de noms se produit à l’aide de DNS ou de fichiers hôtes locaux. lorsque DNS est utilisé, le fournisseur de services **GetXbyY** par défaut utilise les appels d’API 1,1 sockets Windows standard pour communiquer avec le serveur DNS. Ces transactions sont effectuées à l’aide de la pile TCP/IP configurée comme pile TCP/IP par défaut. Toutefois, deux cas particuliers méritent une mention spéciale.

L’implémentation par défaut de GETXBYYSP \_ GetHostName obtient le nom d’hôte local à partir du Registre. Celui-ci correspond au nom attribué à « Poste de travail ». L’implémentation par défaut de GETXBYYSP \_ gethostbyname et GETXBYYSP \_ WSAAsyncGetHostByName compare toujours le nom d’hôte fourni avec le nom d’hôte local. S’ils correspondent, l’implémentation par défaut utilise une interface privée pour sonder la pile TCP/IP Microsoft afin de découvrir son adresse IP locale. Ainsi, pour être complètement indépendant de la pile TCP/IP Microsoft, un fournisseur d’espaces de noms doit implémenter à la fois GETXBYYSP \_ gethostbyname et GETXBYYSP \_ WSAAsyncGetHostByName.

 

 



