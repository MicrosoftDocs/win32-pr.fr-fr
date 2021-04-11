---
title: Format des journaux d’erreurs de l’API du serveur HTTP
description: En général, les fichiers journaux des erreurs de l’API du serveur HTTP ont le même format que les journaux des erreurs W3C, sauf que les fichiers journaux des erreurs de l’API du serveur HTTP ne contiennent pas d’en-têtes de colonnes.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API serveur HTTP, format du journal des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190952"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Format des journaux d’erreurs de l’API du serveur HTTP

En général, les fichiers journaux des erreurs de l’API du serveur HTTP ont le même format que les journaux des erreurs W3C, sauf que les fichiers journaux des erreurs de l’API du serveur HTTP ne contiennent pas d’en-têtes de colonnes. Chaque ligne d’un journal des erreurs de l’API du serveur HTTP enregistre une erreur avec les champs dans un ordre spécifique. Chaque champ est séparé du champ précédent par un caractère d’espacement unique (0x0020). Dans chaque champ, les espaces, les tabulations et les caractères de contrôle non imprimables sont remplacés par des signes plus (0x002B).

Le tableau suivant identifie les champs et l’ordre des champs dans un enregistrement du journal des erreurs.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Champ</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date<br/></td>
<td>Le champ date suit le format W3C et est basé sur le temps universel coordonné (UTC, Universal Time Coordinated). Le champ date comporte toujours 10 caractères au format &quot; aaaa-mm-jj &quot; . Par exemple, le 1er mai 2003 est exprimé sous la forme &quot; 2003-05-01 &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Simultanément<br/></td>
<td>Le champ heure suit le format W3C et est basé sur l’heure UTC. Le champ d’heure est toujours 8 caractères sous la forme &quot; mm : HH : SS &quot; . Par exemple, 5:30 PM (UTC) est exprimé sous la forme &quot; 17:30:00 &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Adresse IP du client<br/></td>
<td>L’adresse IP du client affecté qui peut être une adresse IPv4 ou une adresse IPv6. Si l’adresse IP du client est une adresse IPv6, le champ IDÉtendue est également inclus dans l’adresse.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Port client<br/></td>
<td>Numéro de port du client affecté.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Adresse IP du serveur<br/></td>
<td>L’adresse IP du serveur concerné qui peut être une adresse IPv4 ou une adresse IPv6. Si l’adresse IP du serveur est une adresse IPv6, le champ IDÉtendue est également inclus dans l’adresse.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Port du serveur<br/></td>
<td>Numéro de port du serveur concerné.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Version du protocole<br/></td>
<td>Version du protocole qui est utilisé. <br/>
<ul>
<li>Si la connexion n’a pas été analysée suffisamment pour déterminer la version du protocole, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</li>
<li>Si le numéro de version majeure ou mineure analysé est supérieur ou égal à 10, la version est enregistrée en tant que &quot; http/ ?. ? &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>DoVerb<br/></td>
<td>État du verbe passé par la dernière demande analysée. Les verbes inconnus sont inclus, mais tous les verbes dont la taille est supérieure à 255 octets sont tronqués à cette longueur. Si un verbe n’est pas disponible, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + requête<br/></td>
<td>L’URL et toute requête associée sont consignées en tant que champ unique, séparées par un point d’interrogation (0x3F). Ce champ est tronqué à une limite de longueur de 4096 octets.
<ul>
<li>Si cette URL a été analysée ( &quot; cuit &quot; ), elle est journalisée avec la conversion de page de codes locale et est traitée comme un champ Unicode.</li>
<li>Si cette URL n’a pas été analysée ( &quot; cuit &quot; ) au moment de la journalisation, elle est copiée exactement, sans conversion Unicode.</li>
<li>Si l’API du serveur HTTP ne peut pas analyser cette URL, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>État du protocole<br/></td>
<td>L’état du protocole ne peut pas dépasser 999. <br/>
<ul>
<li>Si l’état de protocole de la réponse à une demande est disponible, il est consigné dans ce champ.</li>
<li>Si l’état du protocole n’est pas disponible, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br/></td>
<td>Non utilisé dans cette version de l’API du serveur HTTP. Un trait d’Union d’espace réservé (0x002D) apparaît toujours dans ce champ.<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Phrase motif<br/></td>
<td>Ce champ contient une chaîne qui identifie le type d’erreur qui est enregistré. Elle n’est jamais vide.<br/></td>
</tr>
</tbody>
</table>



 

Les exemples de lignes suivants proviennent d’un journal des erreurs de l’API du serveur HTTP :

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





