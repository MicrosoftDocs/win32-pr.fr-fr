---
title: Bluetooth et WSAQUERYSET pour la recherche de Service
description: Utilisation de la structure WSAQUERYSET avec les fonctions WSALookupServiceBegin et WSALookupServiceNext pour obtenir des informations sur le processus de demande de service.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth et WSAQUERYSET pour la recherche de Service Bluetooth
- WSAQUERYSET Bluetooth, pour la demande de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230777"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth et WSAQUERYSET pour la recherche de Service

Bluetooth utilise la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , avec différentes fonctions, pour faciliter la découverte des appareils et des services dans l’espace de noms Bluetooth, NS \_ BTH.

Les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) utilisent la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour obtenir des données sur le processus de demande de service. Le tableau suivant décrit comment définir les valeurs de membre dans la structure **WSAQUERYSET** à cet effet.




| Membre | Entrée dans WSALookupServiceBegin | Valeur retournée par WSALookupServiceNext | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize nul</strong> | Doit être défini sur <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retourné par System. | 
| <strong>dwOutputFlags</strong> | Non utilisé. | Non utilisé. | 
| <strong>lpszServiceInstanceName</strong> | Non utilisé. | nom complet du service, converti en une chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceName. Retourné si LUP_RETURN_NAME est spécifié. | 
| <strong>lpServiceClassId</strong> | Obligatoire. identificateur unique Bluetooth unique le plus spécifique pour les services pour lesquels la recherche est effectuée. Par exemple, si cette valeur est définie sur l’UUID du protocole L2CAP, elle retourne tous les services à l’aide du protocole L2CAP sur l’appareil cible. S’il est défini sur l’UUID d’un service spécifique, il ne retourne que les instances de ce service. | Non utilisé. | 
| <strong>lpVersion</strong> | Non utilisé. | Non utilisé. | 
| <strong>lpszComment</strong> | Non utilisé. | Description du service, convertie en chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceDescription. Retourné si <strong>LUP_RETURN_COMMENT</strong> est spécifié. | 
| <strong>dwNameSpace</strong> | Doit être NS_BTH. | Retourne NS_BTH. | 
| <strong>lpNSProviderId</strong> | Non utilisé. | Non utilisé. | 
| <strong>lpszContext</strong> | Obligatoire. Bluetooth adresse d’appareil avec laquelle établir une connexion SDP et interroger les services. Cette valeur doit être une chaîne qui a été convertie à l’aide de l’appel de fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . si l’adresse de l’appareil Bluetooth local est fournie, la base de données SDP locale est recherchée. | Non utilisé. | 
| <strong>dwNumberOfProtocols</strong> | Non utilisé. | Non utilisé. | 
| <strong>lpafpProtocols</strong> | Non utilisé. | Non utilisé. | 
| <strong>lpszQueryString</strong> | Non utilisé. | Non utilisé. | 
| <strong>dwNumberOfCsAddrs</strong> | Non utilisé. | Indique le nombre d’éléments dans le tableau de structures de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> . | 
| <strong>lpcsaBuffer</strong> | Non utilisé. | pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> dont le membre <strong>LocalAddr. lpSockaddr</strong> pointe vers une <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> qui contient l’adresse connectable complète du service distant, convertie à partir de la première entrée de l’attribut SDP Bluetooth ProtocolDescriptorList. Retourné si <strong>LUP_RETURN_ADDR</strong> est spécifié. | 
| <strong>lpBlob</strong> | facultatif. Pointeur vers une structure <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> qui contient des paramètres avancés pour limiter les résultats de la recherche. S’il est fourni, <strong>lpServiceClassId</strong> est ignoré et les requêtes mises en cache échouent. | <ul><li>Si une recherche de service est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne les handles de service. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcule le nombre de handles. <strong>BLOB. pBlobData</strong> est un tableau de valeurs ulong représentant les handles de service.</li><li>Si une recherche d’attribut ou de serviceAttribute est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne l’enregistrement SDP binaire. <strong>BLOB. cbSize</strong> est la taille de l’enregistrement SDP binaire. <strong>BLOB. pBlobData</strong> pointe vers l’enregistrement lui-même. L’enregistrement SDP binaire est nécessaire dans de nombreux cas, car seul un nombre limité d’attributs SDP peuvent être convertis dans la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> , et seules les chaînes UTF-8 encodées par défaut sont converties. les fonctions pour faciliter l’analyse de l’enregistrement SDP binaire sont fournies dans la section <a href="bluetooth-reference.md">référence de Bluetooth</a> .</li><li>Retourné si LUP_RETURN_BLOB est spécifié.</li></ul> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bluetooth et WSAQUERYSET pour Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth et WSAQUERYSET pour la consultation des appareils](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth et objet BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth et WSALookupServiceNext
</dt> <dt>

[Bluetooth Faire](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_service de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_informations CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
