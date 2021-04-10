---
title: Bluetooth et WSALookupServiceBegin pour la détection de service
description: Pour découvrir l’existence d’un service particulier sur un serveur Bluetooth, les clients utilisent les fonctions WSALookupServiceBegin, WSALookupServiceNext et WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth et WSALookupServiceBegin pour la détection de service Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842834"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth et WSALookupServiceBegin pour la détection de service

Pour découvrir l’existence d’un service particulier sur un serveur Bluetooth, les clients utilisent les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)et [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) . Les requêtes peuvent être exécutées pour des adresses locales et distantes, mais les connexions peuvent uniquement être établies avec des adresses distantes. Les descripteurs de service découverts pendant cette opération ne peuvent pas être utilisés pour supprimer le service via [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea). Le bouclage n’est pas pris en charge par RFCOMM.

Deux types de requêtes de découverte de service de base peuvent être exécutés :

-   Requêtes pour un ou plusieurs services sur l’appareil local
-   Requêtes pour un ou plusieurs services sur un appareil homologue spécifié

La fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) reçoit une structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) dans son paramètre *lpqsRestrictions* . **WSALookupServiceBegin** exécute une requête cliente en fonction de l’ensemble des restrictions de recherche contenues dans le **WSAQUERYSET** . Les clients Bluetooth doivent spécifier les restrictions, listées dans le tableau suivant, dans la structure **WSAQUERYSET** lors de l’utilisation de la fonction **WSALookupServiceBegin** pour rechercher des services.



| Membre WSAQUERYSET    | Restriction                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize nul**            | Affectez la valeur **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Définissez sur l’UUID Bluetooth le plus spécifique qui peut être utilisé pour déterminer l’étendue de la requête. Par exemple, la définition de **lpServiceClassId** sur l’UUID du protocole L2CAP aboutit à tous les services L2CAP retournés, en énumérant essentiellement tous les enregistrements SD sur la cible. Toutefois, la définition de l’UUID sur un service spécifique retourne uniquement les instances de ce service.<br/> |
| **dwNameSpace**       | Défini sur **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Définit la valeur 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Définissez sur l’adresse de l’appareil Bluetooth avec lequel établir une connexion SDP pour exécuter la requête des services. Ce membre doit être une chaîne qui est convertie à l’aide de la fonction [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Si l’adresse radio locale est fournie, les enregistrements SDP locaux sont recherchés.<br/>                                             |
| Autres membres         | Tous les autres membres de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) sont ignorés.                                                                                                                                                                                                                                                                                        |



 

La connexion SDP à l’appareil distant ne reste pas active une fois que la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a terminé une requête de service ; la connexion est arrêtée avant que **WSALookupServiceBegin** retourne. Les applications qui nécessitent la connexion SDP pour rester actives après la fin d’une requête de service doivent spécifier l’UUID de la classe de service à laquelle se connecter à l’aide du membre **serviceClassId** de la structure [**\_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) lors de l’émission de l’appel de fonction Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

Les indicateurs, répertoriés dans le tableau ci-dessous, sont utilisés dans le paramètre *dwControlFlags* des fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) pour contrôler les résultats de la requête. Les **lup \_ Containers** et **lup \_ FLUSHCACHE** Flags sont utilisés par la fonction **WSALookupServiceBegin** ; le reste des indicateurs est utilisé dans les appels à la fonction **WSALookupServiceNext** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indicateur</th>
<th>Résultats</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>Ne doit pas être défini.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>Les applications doivent généralement spécifier <strong>LUP_FLUSHCACHE</strong>. Cet indicateur indique au système d’ignorer toutes les informations mises en cache et d’établir une connexion SDP par voie hertzienne à l’appareil spécifié pour effectuer la recherche SDP. Cette opération sans mise en cache peut prendre plusieurs secondes (tandis qu’une recherche mise en cache est retournée rapidement). Actuellement, Bluetooth ne met pas en cache de manière proactive les enregistrements SDP à partir des appareils proches, pas plus qu’il ne met en cache de façon agressive les requêtes précédentes. Par conséquent, les applications doivent prévoir que les requêtes ne peuvent pas retourner de résultats (avec le code d’erreur <strong>WSASERVICE_NOT_FOUND</strong>) si <strong>LUP_FLUSHCACHE</strong> n’est pas spécifié. Les données mises en cache disponibles à l’aide de l’interface Windows Sockets peuvent être améliorées à l’avenir.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Retourne des informations sur l’adresse Bluetooth locale. Cet indicateur n’a d’effet que si <strong>LUP_RETURN_ADDR</strong> est également spécifié.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Retourne le nom complet du service dans le membre <strong>lpszServiceInstanceName</strong> de la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> pour chaque appel à la fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Retournez l’ID de classe de service dans le membre <strong>lpServiceClassId</strong> de la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .
<blockquote>
[!Note]<br />
L’utilisation de cet indicateur s’applique uniquement à la fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>WSALookupServiceBegin</strong></a> . Cette valeur est toujours égale à zéro pour <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Retourne une adresse dans le membre <strong>lpcsaBuffer</strong> à utiliser avec les appels de fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>Connect</strong></a> . L’adresse retournée contient le numéro de port.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Retourne les enregistrements SD correspondants dans le membre <strong>lpBlob</strong> , mis en forme selon la spécification de l’enregistrement SDP Bluetooth.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Retourne toutes les informations relatives aux indicateurs ci-dessus.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Retournez la description du service dans le membre <strong>lpszComment</strong> de la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> pour chaque appel à la fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Ignore l’enregistrement suivant disponible et retourne l’enregistrement qui le suit.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Requêtes de service avancées

Les opérations de requête décrites dans la section précédente peuvent être utilisées pour retourner tous les résultats d’un GUID unique, ce qui doit être suffisant pour la plupart des applications. Une requête avancée permet à une application de créer une requête plus spécifique ; Il offre la possibilité de faire correspondre les UUID et les attributs dans les informations retournées.

Pour effectuer une requête avancée pour les services, les clients Bluetooth doivent spécifier les restrictions suivantes dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) qui est passée dans le paramètre *lpqsRestrictions* .



| Membre WSAQUERYSET   | Restriction                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize nul**           | Affectez la valeur **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Définissez sur l’adresse de l’appareil Bluetooth avec lequel établir une connexion SDP pour exécuter la requête des services. Ce membre doit être une chaîne qui est convertie à l’aide de la fonction [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Si l’adresse radio locale est fournie, les enregistrements SDP locaux sont recherchés.<br/> |
| **lpBlob.pBlobData** | Pointeur vers une structure de [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) qui contient tous les paramètres qui limitent les résultats de la requête.                                                                                                                                                                                           |
| **dwNameSpace**      | Défini sur **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                 |
| Autres membres        | Tous les autres membres de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) sont ignorés.                                                                                                                                                                                                                                            |



 

Les indicateurs suivants sont passés dans le paramètre *dwControlFlags* de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour contrôler les résultats d’une requête avancée.

| Indicateur                     | Résultats                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_conteneurs lup**      | Ne doit pas être défini.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | Les applications doivent généralement spécifier **lup \_ FLUSHCACHE**. Cet indicateur indique au système d’ignorer toutes les informations mises en cache et d’établir une connexion SDP par voie hertzienne à l’appareil spécifié pour effectuer la recherche SDP. Cette opération sans mise en cache peut prendre plusieurs secondes (tandis qu’une recherche mise en cache est retournée rapidement). Bluetooth ne met pas en cache de manière proactive les enregistrements SDP à partir des appareils proches, ni ne met en cache de façon agressive les requêtes précédentes. Par conséquent, les applications doivent s’attendre à ce que les requêtes ne retournent souvent aucun résultat (**WSASERVICE \_ \_ introuvable**) si **lup \_ FLUSHCACHE** n’est pas spécifié. Les données mises en cache disponibles à l’aide de l’interface Windows Sockets peuvent être améliorées à l’avenir. |
| **\_service lup res \_**    | Retourne des informations pour l’adresse Bluetooth locale. La définition de cet indicateur n’a d’effet que si l' **\_ \_ adresse de retour lup** est également spécifiée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **LUP \_ nom de retour \_**    | Retourne le nom complet du service. Cet indicateur est ignoré pour **la \_ \_ \_ demande de recherche du service SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_type de retour lup \_**    | Retourne l’ID de classe du service. Cet indicateur est ignoré pour **la \_ \_ \_ demande de recherche du service SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ retour \_ addr**    | Retourne une adresse dans le membre **lpcsaBuffer** à utiliser avec les appels de fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) . L’adresse retournée contient le numéro de port. Cet indicateur est ignoré pour **la \_ \_ \_ demande de recherche du service SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **LUP \_ retourne un \_ objet BLOB**    | Retourne les enregistrements SD correspondants dans un format conforme à la spécification d’enregistrement SDP Bluetooth. Pour **une \_ \_ \_ demande de recherche de service SDP**, le résultat de **LpBlob** pour l’appel suivant à [**WSALOOKUPSERVICENEXT**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) est un tableau de handles de SDP Bluetooth. Pour la demande d’attribut de **\_ service \_ \_ SDP** et la **demande d’attribut de \_ recherche de service \_ \_ \_ SDP**, le résultat de chaque appel suivant à **WSALookupServiceNext** est un enregistrement SDP Bluetooth binaire dont les attributs sont limités à ceux spécifiés par le membre **Prange** de la requête. Cet indicateur est requis pour **la \_ \_ \_ demande de recherche du service SDP**.                                                               |
| **LUP \_ retourner le \_ Commentaire** | Retournez la description du service dans le membre **lpszComment** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour chaque appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | Ignore l’enregistrement suivant disponible et retourne l’enregistrement qui le suit.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

À l’entrée, **lpBlob** -> **pBlobData** pointe vers une structure de [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) qui contient les valeurs indiquées dans le tableau suivant.

> [!Note]  
> La demande de recherche initiale doit pouvoir tenir dans un paquet L2CAP. Toutefois, la réponse peut être divisée en plusieurs paquets L2CAP.

 



| Membre            | Valeur                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Type de recherche à effectuer. Cette valeur peut être l’une des demandes de **\_ recherche de service \_ \_ SDP**, de **\_ demande d' \_ attribut \_ de service SDP** ou de demande d' **attribut de \_ recherche de service \_ \_ \_ SDP**. Chaque type de recherche est associé à un mécanisme de recherche sous-jacent qui est défini par la spécification du SDP Bluetooth. Chaque retourne la forme décrite par la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) qui est définie précédemment dans la section (requêtes de service avancées). |
| **serviceHandle** | Utilisé pour les recherches d’attributs. Cette valeur spécifie le descripteur de service avec lequel interroger les attributs du membre **Prange** .                                                                                                                                                                                                                                                                                                                                            |
| **UUID**         | Utilisé pour les recherches de service et **serviceAttribute** . Cette valeur spécifie les UUID qu’un enregistrement doit contenir pour correspondre à la recherche. Si le **nombre d' \_ UUID \_ de \_ requête** inférieur à Max doit être interrogé, cette valeur définit l’élément SdpQueryUuid qui suit immédiatement le dernier UUID valide à zéro.                                                                                                                                                                       |
| **numRange**      | Utilisé pour les recherches d’attribut et **serviceAttribute** . Cette valeur spécifie le nombre d’éléments dans **Prange**.                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | Utilisé pour les recherches d’attribut et **serviceAttribute** . Cette valeur spécifie les valeurs d’attribut à récupérer pour tous les enregistrements correspondants.                                                                                                                                                                                                                                                                                                                                        |



 

Après chaque appel réussi à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , **lpBlob** -> **pBlobData** pointe vers un bloc de données qui contient les valeurs indiquées dans le tableau suivant.

| Valeur                                                                                | Description                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_demande de \_ recherche du service SDP \_**                                                    | Tableau de handles d’enregistrement SDP qui est identique à l' **ServiceRecordHandleList** défini par le sdp Bluetooth 1,1. Le nombre de descripteurs SDP renvoyés est calculé par (**lpBlob**->CBSIZE)/**sizeof**(ULONG). Tous les résultats sont retournés dans un seul appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . |
| **SDP \_ Demande \_ d' \_ attribut de service** ou **demande d’attribut de \_ recherche de service \_ \_ \_ SDP** | Enregistrement SDP Bluetooth binaire. Pour **une \_ \_ \_ demande d’attribut de service SDP**, tous les résultats sont retournés dans un seul appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                       |



 

> [!Note]  
> Si le membre **lpBlob** n’est pas spécifié pendant l’entrée d’une requête de service, une recherche de service et d’attribut est effectuée pour le service spécifié dans le membre **lpServiceClassId** sur les attributs de 0 à 0xFFFF.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WSAQUERYSET pour la recherche de service et Bluetooth](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Détection des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth et WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**\_service de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**entre**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

