---
title: WSAQUERYSET pour la recherche de service et Bluetooth
description: Utilisation de la structure WSAQUERYSET avec les fonctions WSALookupServiceBegin et WSALookupServiceNext pour obtenir des informations sur le processus de demande de service.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth et WSAQUERYSET pour la recherche de service Bluetooth
- WSAQUERYSET Bluetooth, demande de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732204"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="017e1-105">WSAQUERYSET pour la recherche de service et Bluetooth</span><span class="sxs-lookup"><span data-stu-id="017e1-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="017e1-106">Bluetooth utilise la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , avec différentes fonctions, pour faciliter la découverte des appareils et services dans l’espace de noms Bluetooth, NS \_ BTH.</span><span class="sxs-lookup"><span data-stu-id="017e1-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="017e1-107">Les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) utilisent la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour obtenir des données sur le processus de demande de service.</span><span class="sxs-lookup"><span data-stu-id="017e1-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="017e1-108">Le tableau suivant décrit comment définir les valeurs de membre dans la structure **WSAQUERYSET** à cet effet.</span><span class="sxs-lookup"><span data-stu-id="017e1-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="017e1-109">Membre</span><span class="sxs-lookup"><span data-stu-id="017e1-109">Member</span></span></th>
<th><span data-ttu-id="017e1-110">Entrée dans WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="017e1-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="017e1-111">Valeur retournée par WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="017e1-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="017e1-112"><strong>dwSize nul</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="017e1-113">Doit être défini sur <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="017e1-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="017e1-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retourné par System.</span><span class="sxs-lookup"><span data-stu-id="017e1-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-115"><strong>dwOutputFlags</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="017e1-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-116">Not used.</span></span></td>
<td><span data-ttu-id="017e1-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-118"><strong>lpszServiceInstanceName</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="017e1-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-119">Not used.</span></span></td>
<td><span data-ttu-id="017e1-120">Nom complet du service, converti en chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceName.</span><span class="sxs-lookup"><span data-stu-id="017e1-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="017e1-121">Retourné si LUP_RETURN_NAME est spécifié.</span><span class="sxs-lookup"><span data-stu-id="017e1-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-122"><strong>lpServiceClassId</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="017e1-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="017e1-123">Required.</span></span> <span data-ttu-id="017e1-124">UUID unique Bluetooth le plus spécifique pour les services pour lesquels la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="017e1-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="017e1-125">Par exemple, si cette valeur est définie sur l’UUID du protocole L2CAP, elle retourne tous les services à l’aide du protocole L2CAP sur l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="017e1-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="017e1-126">S’il est défini sur l’UUID d’un service spécifique, il ne retourne que les instances de ce service.</span><span class="sxs-lookup"><span data-stu-id="017e1-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="017e1-127">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-128"><strong>lpVersion</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="017e1-129">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-129">Not used.</span></span></td>
<td><span data-ttu-id="017e1-130">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-131"><strong>lpszComment</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="017e1-132">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-132">Not used.</span></span></td>
<td><span data-ttu-id="017e1-133">Description du service, convertie en chaîne encodée en UTF-8 à partir de l’encodage de langue par défaut de l’attribut SDP Bluetooth ServiceDescription.</span><span class="sxs-lookup"><span data-stu-id="017e1-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="017e1-134">Retourné si <strong>LUP_RETURN_COMMENT</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="017e1-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-135"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="017e1-136">Doit être NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="017e1-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="017e1-137">Retourne NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="017e1-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-138"><strong>lpNSProviderId</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="017e1-139">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-139">Not used.</span></span></td>
<td><span data-ttu-id="017e1-140">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-141"><strong>lpszContext</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="017e1-142">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="017e1-142">Required.</span></span> <span data-ttu-id="017e1-143">Adresse de l’appareil Bluetooth avec laquelle établir une connexion SDP et demander des services.</span><span class="sxs-lookup"><span data-stu-id="017e1-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="017e1-144">Cette valeur doit être une chaîne qui a été convertie à l’aide de l’appel de fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="017e1-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="017e1-145">Si l’adresse du périphérique Bluetooth local est fournie, la base de données SDP locale est recherchée.</span><span class="sxs-lookup"><span data-stu-id="017e1-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="017e1-146">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-147"><strong>dwNumberOfProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="017e1-148">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-148">Not used.</span></span></td>
<td><span data-ttu-id="017e1-149">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-150"><strong>lpafpProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="017e1-151">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-151">Not used.</span></span></td>
<td><span data-ttu-id="017e1-152">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-153"><strong>lpszQueryString</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="017e1-154">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-154">Not used.</span></span></td>
<td><span data-ttu-id="017e1-155">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-156"><strong>dwNumberOfCsAddrs</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="017e1-157">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-157">Not used.</span></span></td>
<td><span data-ttu-id="017e1-158">Indique le nombre d’éléments dans le tableau de structures de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="017e1-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="017e1-159"><strong>lpcsaBuffer</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="017e1-160">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e1-160">Not used.</span></span></td>
<td><span data-ttu-id="017e1-161">Pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> dont le membre <strong>LocalAddr. lpSockaddr</strong> pointe vers une <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> qui contient l’adresse connectable complète du service distant, convertie à partir de la première entrée de l’attribut SDP de ProtocolDescriptorList Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="017e1-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="017e1-162">Retourné si <strong>LUP_RETURN_ADDR</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="017e1-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="017e1-163"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="017e1-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="017e1-164">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="017e1-164">Optional.</span></span> <span data-ttu-id="017e1-165">Pointeur vers une structure <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> qui contient des paramètres avancés pour limiter les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="017e1-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="017e1-166">S’il est fourni, <strong>lpServiceClassId</strong> est ignoré et les requêtes mises en cache échouent.</span><span class="sxs-lookup"><span data-stu-id="017e1-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="017e1-167">Si une recherche de service est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne les handles de service.</span><span class="sxs-lookup"><span data-stu-id="017e1-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="017e1-168">(<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcule le nombre de handles.</span><span class="sxs-lookup"><span data-stu-id="017e1-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="017e1-169"><strong>BLOB. pBlobData</strong> est un tableau de valeurs ulong représentant les handles de service.</span><span class="sxs-lookup"><span data-stu-id="017e1-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="017e1-170">Si une recherche d’attribut ou de serviceAttribute est effectuée : pointeur vers une structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> qui retourne l’enregistrement SDP binaire.</span><span class="sxs-lookup"><span data-stu-id="017e1-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="017e1-171"><strong>BLOB. cbSize</strong> est la taille de l’enregistrement SDP binaire.</span><span class="sxs-lookup"><span data-stu-id="017e1-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="017e1-172"><strong>BLOB. pBlobData</strong> pointe vers l’enregistrement lui-même.</span><span class="sxs-lookup"><span data-stu-id="017e1-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="017e1-173">L’enregistrement SDP binaire est nécessaire dans de nombreux cas, car seul un nombre limité d’attributs SDP peuvent être convertis dans la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> , et seules les chaînes UTF-8 encodées par défaut sont converties.</span><span class="sxs-lookup"><span data-stu-id="017e1-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="017e1-174">Les fonctions pour faciliter l’analyse de l’enregistrement SDP binaire sont fournies dans la section <a href="bluetooth-reference.md">référence Bluetooth</a> .</span><span class="sxs-lookup"><span data-stu-id="017e1-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="017e1-175">Retourné si LUP_RETURN_BLOB est spécifié.</span><span class="sxs-lookup"><span data-stu-id="017e1-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="017e1-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="017e1-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="017e1-177">Bluetooth et WSAQUERYSET pour set service</span><span class="sxs-lookup"><span data-stu-id="017e1-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="017e1-178">Bluetooth et WSAQUERYSET pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="017e1-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="017e1-179">Bluetooth et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="017e1-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="017e1-180">Bluetooth et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="017e1-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="017e1-181">Bluetooth et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="017e1-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="017e1-182">Référence Bluetooth</span><span class="sxs-lookup"><span data-stu-id="017e1-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="017e1-183">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="017e1-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="017e1-184">**\_service de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="017e1-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="017e1-185">**\_informations CSADDR**</span><span class="sxs-lookup"><span data-stu-id="017e1-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="017e1-186">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="017e1-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="017e1-187">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="017e1-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="017e1-188">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="017e1-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="017e1-189">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="017e1-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 