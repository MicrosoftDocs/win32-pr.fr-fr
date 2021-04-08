---
description: 'Les fonctions de résolution de noms peuvent être regroupées en trois catégories : installation de service, requêtes client et application auxiliaire (avec macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Résumé des fonctions de résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751397"
---
# <a name="summary-of-name-resolution-functions"></a>Résumé des fonctions de résolution de noms

Les fonctions de résolution de noms peuvent être regroupées en trois catégories : installation de service, requêtes client et application auxiliaire (avec macros). Les sections qui suivent identifient les fonctions de chaque catégorie et décrivent brièvement leur utilisation prévue. Les structures de données clés sont également décrites.

## <a name="service-installation"></a>Installation du service

-   [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Quand la classe de service requise n’existe pas encore, une application utilise [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) pour installer une nouvelle classe de service en fournissant un nom de classe de service, un GUID pour l’identificateur de classe de service et une série de structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Ces structures sont spécifiques à un espace de noms particulier et fournissent des valeurs communes telles que des numéros de port TCP recommandés ou des identificateurs SAP SAP. Une classe de service peut être supprimée en appelant [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) et en fournissant le GUID correspondant à l’identificateur de classe.

Une fois qu’une classe de service existe, les instances spécifiques d’un service peuvent être installées ou supprimées par le biais de [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea). Cette fonction prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme paramètre d’entrée avec un code d’opération et des indicateurs d’opération. Le code d’opération indique si le service est en cours d’installation ou de suppression. La structure **WSAQUERYSET** fournit toutes les informations pertinentes relatives au service, notamment l’identificateur de classe de service, le nom de service (pour cette instance), l’identificateur d’espace de noms applicable et les informations de protocole, ainsi qu’un ensemble d’adresses de transport sur lequel le service écoute. Les services doivent appeler **WSASetService** lorsqu’ils s’initialisent pour annoncer leur présence dans les espaces de noms dynamiques.

## <a name="client-query"></a>Requête cliente

-   [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

La fonction [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permet à une application de découvrir quels espaces de noms sont accessibles par le biais de fonctions de résolution de noms Winsock. Elle permet également à une application de déterminer si un espace de noms donné est pris en charge par plusieurs fournisseurs d’espaces de noms, et de découvrir l’identificateur de fournisseur pour n’importe quel fournisseur d’espace de noms particulier. À l’aide d’un identificateur de fournisseur, l’application peut limiter une opération de requête à un fournisseur d’espaces de noms spécifié.

Espace de noms Winsock : les opérations de requête impliquent une série d’appels : [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), suivis d’un ou plusieurs appels à [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) et se terminant par un appel à [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **WSALookupServiceBegin** prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme entrée pour définir les paramètres de requête avec un jeu d’indicateurs pour fournir un contrôle supplémentaire sur l’opération de recherche. Elle retourne un handle de requête qui est utilisé dans les appels suivants à **WSALookupServiceNext** et **WSALookupServiceEnd**.

L’application appelle [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) pour obtenir les résultats de la requête, avec les résultats fournis dans une mémoire tampon [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie par l’application. L’application continue d’appeler **WSALookupServiceNext** jusqu’à ce que le code d’erreur « wsa \_ E » \_ \_ soit retourné, indiquant que tous les résultats ont été récupérés. La recherche est ensuite terminée par un appel à [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). La fonction **WSALookupServiceEnd** peut également être utilisée pour annuler un **WSALookupServiceNext** actuellement en attente en cas d’appel à partir d’un autre thread.

Dans Windows Sockets 2, les codes d’erreur en conflit sont définis pour WSAENOMORE (10102) et WSA \_ E \_ \_ (10110). Le code d’erreur WSAENOMORE sera supprimé dans une version ultérieure et seul le WSA \_ E ne \_ \_ sera pas conservé. Pour Windows Sockets 2, toutefois, les applications doivent vérifier à la fois WSAENOMORE et WSA \_ E pour \_ \_ la compatibilité la plus étendue possible avec les fournisseurs d’espaces de noms qui utilisent l’un ou l’autre.

## <a name="helper-functions"></a>Fonctions d’assistance

-   [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress n'**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**WSAGetServiceClassInfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

Les fonctions d’assistance de résolution de noms incluent une fonction permettant de récupérer un nom de classe de service en fonction d’un identificateur de classe de service, une paire de fonctions utilisées pour traduire une adresse de transport entre une structure [**sockaddr**](sockaddr-2.md) et une représentation sous forme de chaîne ASCII, une fonction pour récupérer les informations de schéma de la classe de service pour une classe de service donnée et un ensemble de macros pour

Les macros suivantes de Winsock2. h facilitent le mappage entre les classes de service connues et les espaces de noms suivants :

| Macro                                                                                                            | Description                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| SVCID \_ TCP (port) SVCID \_ UDP (port)<br/> SVCID \_ NetWare (type d’objet)<br/>                              | Avec un port pour TCP/IP ou UDP/IP ou le type d’objet dans le cas de NetWare, retourne le GUID (numéro de port dans l’ordre de l’ordinateur hôte). |
| \_SVCID \_ TCP (Guid) est-il \_ SVCID \_ UDP (Guid)<br/> IS \_ SVCID \_ NetWare (Guid)<br/>                          | Retourne la **valeur true** si le GUID est dans la plage autorisée.                                                                |
| DÉFINIR \_ TCP \_ SVCID (Guid, port) définir \_ UDP \_ SVCID (Guid, port)<br/>                                                | Initialise une structure GUID avec le GUID équivalent pour un numéro de port TCP ou UDP (le numéro de port doit être dans l’ordre de l’ordinateur hôte).    |
| PORT \_ à partir du \_ \_ port SVCID TCP (Guid) \_ à partir de \_ SVCID \_ UDP (Guid)<br/> SAPId \_ à partir de \_ SVCID \_ NetWare (Guid)<br/> | Retourne le port ou le type d’objet associé au GUID (numéro de port dans l’ordre de l’ordinateur hôte).                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**API getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Structures de données de résolution de noms](name-resolution-data-structures-2.md)
</dt> <dt>

[Modèle de résolution de noms](name-resolution-model-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




