---
title: Bluetooth et WSALookupServiceBegin pour la consultation des appareils
description: Cette rubrique explique comment utiliser la fonction WSALookupServiceBegin pour effectuer une recherche sur des appareils visibles et fantômes. pour plus d’informations, consultez découverte d’appareils et de Services Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth et WSALookupServiceBegin pour la consultation des appareils Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af56e1d75a66d21ea4eb94c827f6d37f77ae4336b8aeac5331665288bfeef49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959288"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth et WSALookupServiceBegin pour la consultation des appareils

Cette rubrique explique comment utiliser la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour effectuer une recherche sur des appareils visibles et fantômes. pour plus d’informations, consultez [découverte d’appareils et de Services Bluetooth](discovering-bluetooth-devices-and-services.md).

La fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) utilise une structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) dans son premier paramètre, *lpqsRestrictions*, pour définir des critères de recherche. Bluetooth fournit des instructions spécifiques pour l’utilisation de la fonction **WSALookupServiceBegin** et **WSAQUERYSET**.

Le tableau suivant répertorie les restrictions qui s’appliquent à la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) transmise au paramètre *lpqsRestrictions* lors de l’interrogation des appareils.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membre WSAQUERYSET</th>
<th>Restriction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize nul</strong></td>
<td>Affectez la valeur <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>Ce membre contient un pointeur facultatif vers une structure d' <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>objet BLOB</strong></a> . Si ce membre est spécifié, les paramètres de recherche de l’appareil valides pour <strong>LUP_FLUSHCACHE</strong> sont les suivants :
<ul>
<li>Le membre <strong>cbSize</strong> de la structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> doit être <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li>
<li>le membre <strong>pBlobData</strong> est un pointeur vers une structure <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , pour laquelle le membre <strong>LAP</strong> est le code d’accès à la recherche Bluetooth et le membre de <strong>longueur</strong> est la longueur, en secondes, de la recherche.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Définissez sur <strong>NS_BTH</strong>.</td>
</tr>
<tr class="even">
<td>Autres membres</td>
<td>Les autres membres de la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> sont ignorés.</td>
</tr>
</tbody>
</table>



 

Les indicateurs répertoriés dans le tableau suivant sont utilisés dans le paramètre *dwControlFlags* pour contrôler les résultats de la requête. Les **lup \_ Containers** et **lup \_ FLUSHCACHE** Flags sont utilisés par la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; le reste des indicateurs est utilisé dans les appels à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Indicateur               | Résultat                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_conteneurs lup    | spécifie que l’objectif de la requête est d’obtenir une liste de Bluetooth appareils et non une liste de services. Cet indicateur doit être défini.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Déclenche une recherche d’appareils locaux ou fait en sorte que les résultats mis en cache des requêtes précédentes soient retournés.                                                                                                                                                                                                                                                                                                                |
| \_type de retour lup \_  | retournez le Bluetooth COD (classe de bits de périphérique) directement dans le membre **lpServiceClassId** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . La DCO est mappée au membre **Data1** du GUID.                                                                                                                                                                                                      |
| \_service lup res \_  | retourne les informations relatives à l’adresse de Bluetooth locale. Cet indicateur n’a d’effet que si **lup \_ renvoie \_ addr** est également spécifié.                                                                                                                                                                                                                                                                                       |
| LUP \_ nom de retour \_  | Retourne le nom complet de l’appareil dans le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour chaque appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Cet indicateur doit également être spécifié pour récupérer le membre **Name** de la structure d’informations de l' [**\_ appareil \_ BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) lors de la spécification de l’indicateur de retour de l' **\_ \_ objet BLOB lup** . |
| LUP \_ retour \_ addr  | Retournez une [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) qui contient l’adresse 48 bits de l’homologue dans le membre **LpcsaBuffer** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour chaque appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Les autres membres de la structure **\_ BTH sockaddr** sont vides.                                                            |
| LUP \_ retourne un \_ objet BLOB  | Retournez la structure d’informations sur l' [**\_ appareil \_ BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) à chaque appel suivant à [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Ignorez l’appareil disponible suivant et retournez l’appareil qui le suit.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bluetooth et WSALookupServiceBegin pour la détection de Service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth et WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth et WSAQUERYSET pour la consultation des appareils](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Détection des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**OBJET BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_périphérique de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 