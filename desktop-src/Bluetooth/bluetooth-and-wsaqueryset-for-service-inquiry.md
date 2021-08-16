---
title: Bluetooth et WSAQUERYSET pour la recherche de Service
description: Utilisation de la structure WSAQUERYSET avec les fonctions WSALookupServiceBegin et WSALookupServiceNext pour obtenir des informations sur le processus de demande de service.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth et WSAQUERYSET pour la recherche de Service Bluetooth
- WSAQUERYSET Bluetooth, pour la demande de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959158"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth et WSAQUERYSET pour la recherche de Service

Bluetooth utilise la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , avec différentes fonctions, pour faciliter la découverte des appareils et des services dans l’espace de noms Bluetooth, NS \_ BTH.

Les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) utilisent la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour obtenir des données sur le processus de demande de service. Le tableau suivant décrit comment définir les valeurs de membre dans la structure **WSAQUERYSET** à cet effet.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Membre</th>
<th>Entrée dans WSALookupServiceBegin</th>
<th>Valeur retournée par WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize nul</strong></td>
<td>Doit être défini sur <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retourné par System.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>Non utilisé.</td>
<td>nom complet du service, converti en une chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceName. Retourné si LUP_RETURN_NAME est spécifié.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obligatoire. identificateur unique Bluetooth unique le plus spécifique pour les services pour lesquels la recherche est effectuée. Par exemple, si cette valeur est définie sur l’UUID du protocole L2CAP, elle retourne tous les services à l’aide du protocole L2CAP sur l’appareil cible. S’il est défini sur l’UUID d’un service spécifique, il ne retourne que les instances de ce service.</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>Non utilisé.</td>
<td>Description du service, convertie en chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceDescription. Retourné si <strong>LUP_RETURN_COMMENT</strong> est spécifié.</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Doit être NS_BTH.</td>
<td>Retourne NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td><strong>lpszContext</strong></td>
<td>Obligatoire. Bluetooth adresse d’appareil avec laquelle établir une connexion SDP et interroger les services. Cette valeur doit être une chaîne qui a été convertie à l’aide de l’appel de fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . si l’adresse de l’appareil Bluetooth local est fournie, la base de données SDP locale est recherchée.</td>
<td>Non utilisé.</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>Non utilisé.</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>Non utilisé.</td>
<td>Indique le nombre d’éléments dans le tableau de structures de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>Non utilisé.</td>
<td>pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> dont le membre <strong>LocalAddr. lpSockaddr</strong> pointe vers une <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> qui contient l’adresse connectable complète du service distant, convertie à partir de la première entrée de l’attribut SDP Bluetooth ProtocolDescriptorList. Retourné si <strong>LUP_RETURN_ADDR</strong> est spécifié.</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>Facultatif. Pointeur vers une structure <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> qui contient des paramètres avancés pour limiter les résultats de la recherche. S’il est fourni, <strong>lpServiceClassId</strong> est ignoré et les requêtes mises en cache échouent.</td>
<td><ul>
<li>Si une recherche de service est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne les handles de service. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcule le nombre de handles. <strong>BLOB. pBlobData</strong> est un tableau de valeurs ulong représentant les handles de service.</li>
<li>Si une recherche d’attribut ou de serviceAttribute est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne l’enregistrement SDP binaire. <strong>BLOB. cbSize</strong> est la taille de l’enregistrement SDP binaire. <strong>BLOB. pBlobData</strong> pointe vers l’enregistrement lui-même. L’enregistrement SDP binaire est nécessaire dans de nombreux cas, car seul un nombre limité d’attributs SDP peuvent être convertis dans la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> , et seules les chaînes UTF-8 encodées par défaut sont converties. les fonctions pour faciliter l’analyse de l’enregistrement SDP binaire sont fournies dans la section <a href="bluetooth-reference.md">référence de Bluetooth</a> .</li>
<li>Retourné si LUP_RETURN_BLOB est spécifié.</li>
</ul></td>
</tr>
</tbody>
</table>



 

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

[**OBJET BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
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

 

 