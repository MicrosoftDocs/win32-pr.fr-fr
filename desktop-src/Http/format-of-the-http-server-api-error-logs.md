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
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="acc1b-104">Format des journaux d’erreurs de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="acc1b-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="acc1b-105">En général, les fichiers journaux des erreurs de l’API du serveur HTTP ont le même format que les journaux des erreurs W3C, sauf que les fichiers journaux des erreurs de l’API du serveur HTTP ne contiennent pas d’en-têtes de colonnes.</span><span class="sxs-lookup"><span data-stu-id="acc1b-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="acc1b-106">Chaque ligne d’un journal des erreurs de l’API du serveur HTTP enregistre une erreur avec les champs dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="acc1b-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="acc1b-107">Chaque champ est séparé du champ précédent par un caractère d’espacement unique (0x0020).</span><span class="sxs-lookup"><span data-stu-id="acc1b-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="acc1b-108">Dans chaque champ, les espaces, les tabulations et les caractères de contrôle non imprimables sont remplacés par des signes plus (0x002B).</span><span class="sxs-lookup"><span data-stu-id="acc1b-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="acc1b-109">Le tableau suivant identifie les champs et l’ordre des champs dans un enregistrement du journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="acc1b-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="acc1b-110">Champ</span><span class="sxs-lookup"><span data-stu-id="acc1b-110">Field</span></span></th>
<th><span data-ttu-id="acc1b-111">Description</span><span class="sxs-lookup"><span data-stu-id="acc1b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="acc1b-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span><span class="sxs-lookup"><span data-stu-id="acc1b-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="acc1b-113">Le champ date suit le format W3C et est basé sur le temps universel coordonné (UTC, Universal Time Coordinated). Le champ date comporte toujours 10 caractères au format &quot; aaaa-mm-jj &quot; .</span><span class="sxs-lookup"><span data-stu-id="acc1b-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="acc1b-114">Par exemple, le 1er mai 2003 est exprimé sous la forme &quot; 2003-05-01 &quot; .</span><span class="sxs-lookup"><span data-stu-id="acc1b-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Simultanément</span><span class="sxs-lookup"><span data-stu-id="acc1b-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="acc1b-116">Le champ heure suit le format W3C et est basé sur l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="acc1b-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="acc1b-117">Le champ d’heure est toujours 8 caractères sous la forme &quot; mm : HH : SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="acc1b-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="acc1b-118">Par exemple, 5:30 PM (UTC) est exprimé sous la forme &quot; 17:30:00 &quot; .</span><span class="sxs-lookup"><span data-stu-id="acc1b-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc1b-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Adresse IP du client</span><span class="sxs-lookup"><span data-stu-id="acc1b-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="acc1b-120">L’adresse IP du client affecté qui peut être une adresse IPv4 ou une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="acc1b-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="acc1b-121">Si l’adresse IP du client est une adresse IPv6, le champ IDÉtendue est également inclus dans l’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc1b-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Port client</span><span class="sxs-lookup"><span data-stu-id="acc1b-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="acc1b-123">Numéro de port du client affecté.</span><span class="sxs-lookup"><span data-stu-id="acc1b-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc1b-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Adresse IP du serveur</span><span class="sxs-lookup"><span data-stu-id="acc1b-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="acc1b-125">L’adresse IP du serveur concerné qui peut être une adresse IPv4 ou une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="acc1b-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="acc1b-126">Si l’adresse IP du serveur est une adresse IPv6, le champ IDÉtendue est également inclus dans l’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc1b-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Port du serveur</span><span class="sxs-lookup"><span data-stu-id="acc1b-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="acc1b-128">Numéro de port du serveur concerné.</span><span class="sxs-lookup"><span data-stu-id="acc1b-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc1b-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Version du protocole</span><span class="sxs-lookup"><span data-stu-id="acc1b-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="acc1b-130">Version du protocole qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="acc1b-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="acc1b-131">Si la connexion n’a pas été analysée suffisamment pour déterminer la version du protocole, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</span><span class="sxs-lookup"><span data-stu-id="acc1b-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="acc1b-132">Si le numéro de version majeure ou mineure analysé est supérieur ou égal à 10, la version est enregistrée en tant que &quot; http/ ?. ? &quot; .</span><span class="sxs-lookup"><span data-stu-id="acc1b-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>DoVerb</span><span class="sxs-lookup"><span data-stu-id="acc1b-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="acc1b-134">État du verbe passé par la dernière demande analysée.</span><span class="sxs-lookup"><span data-stu-id="acc1b-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="acc1b-135">Les verbes inconnus sont inclus, mais tous les verbes dont la taille est supérieure à 255 octets sont tronqués à cette longueur.</span><span class="sxs-lookup"><span data-stu-id="acc1b-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="acc1b-136">Si un verbe n’est pas disponible, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</span><span class="sxs-lookup"><span data-stu-id="acc1b-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc1b-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + requête</span><span class="sxs-lookup"><span data-stu-id="acc1b-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="acc1b-138">L’URL et toute requête associée sont consignées en tant que champ unique, séparées par un point d’interrogation (0x3F).</span><span class="sxs-lookup"><span data-stu-id="acc1b-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="acc1b-139">Ce champ est tronqué à une limite de longueur de 4096 octets.</span><span class="sxs-lookup"><span data-stu-id="acc1b-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="acc1b-140">Si cette URL a été analysée ( &quot; cuit &quot; ), elle est journalisée avec la conversion de page de codes locale et est traitée comme un champ Unicode.</span><span class="sxs-lookup"><span data-stu-id="acc1b-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="acc1b-141">Si cette URL n’a pas été analysée ( &quot; cuit &quot; ) au moment de la journalisation, elle est copiée exactement, sans conversion Unicode.</span><span class="sxs-lookup"><span data-stu-id="acc1b-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="acc1b-142">Si l’API du serveur HTTP ne peut pas analyser cette URL, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</span><span class="sxs-lookup"><span data-stu-id="acc1b-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>État du protocole</span><span class="sxs-lookup"><span data-stu-id="acc1b-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="acc1b-144">L’état du protocole ne peut pas dépasser 999.</span><span class="sxs-lookup"><span data-stu-id="acc1b-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="acc1b-145">Si l’état de protocole de la réponse à une demande est disponible, il est consigné dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="acc1b-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="acc1b-146">Si l’état du protocole n’est pas disponible, un trait d’Union (0x002D) est utilisé comme espace réservé pour le champ vide.</span><span class="sxs-lookup"><span data-stu-id="acc1b-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc1b-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span><span class="sxs-lookup"><span data-stu-id="acc1b-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="acc1b-148">Non utilisé dans cette version de l’API du serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="acc1b-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="acc1b-149">Un trait d’Union d’espace réservé (0x002D) apparaît toujours dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="acc1b-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc1b-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Phrase motif</span><span class="sxs-lookup"><span data-stu-id="acc1b-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="acc1b-151">Ce champ contient une chaîne qui identifie le type d’erreur qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="acc1b-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="acc1b-152">Elle n’est jamais vide.</span><span class="sxs-lookup"><span data-stu-id="acc1b-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="acc1b-153">Les exemples de lignes suivants proviennent d’un journal des erreurs de l’API du serveur HTTP :</span><span class="sxs-lookup"><span data-stu-id="acc1b-153">The following sample lines are from an HTTP Server API error log:</span></span>

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

 

 





