---
title: Bluetooth et WSALookupServiceBegin pour la consultation des appareils
description: Cette rubrique explique comment utiliser la fonction WSALookupServiceBegin pour effectuer une recherche sur des appareils visibles et fantômes. Pour plus d’informations, consultez découverte des appareils et services Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth et WSALookupServiceBegin pour la consultation des appareils Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102473"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="7bb3c-105">Bluetooth et WSALookupServiceBegin pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="7bb3c-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="7bb3c-106">Cette rubrique explique comment utiliser la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour effectuer une recherche sur des appareils visibles et fantômes.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="7bb3c-107">Pour plus d’informations, consultez [découverte des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="7bb3c-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="7bb3c-108">La fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) utilise une structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) dans son premier paramètre, *lpqsRestrictions*, pour définir des critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="7bb3c-109">Bluetooth fournit des instructions spécifiques pour l’utilisation de la fonction **WSALookupServiceBegin** et **WSAQUERYSET**.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="7bb3c-110">Le tableau suivant répertorie les restrictions qui s’appliquent à la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) transmise au paramètre *lpqsRestrictions* lors de l’interrogation des appareils.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bb3c-111">Membre WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="7bb3c-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="7bb3c-112">Restriction</span><span class="sxs-lookup"><span data-stu-id="7bb3c-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bb3c-113"><strong>dwSize nul</strong></span><span class="sxs-lookup"><span data-stu-id="7bb3c-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="7bb3c-114">Affectez la valeur <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="7bb3c-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bb3c-115"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="7bb3c-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="7bb3c-116">Ce membre contient un pointeur facultatif vers une structure d' <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>objet BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="7bb3c-117">Si ce membre est spécifié, les paramètres de recherche de l’appareil valides pour <strong>LUP_FLUSHCACHE</strong> sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7bb3c-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="7bb3c-118">Le membre <strong>cbSize</strong> de la structure <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> doit être <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span><span class="sxs-lookup"><span data-stu-id="7bb3c-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="7bb3c-119">Le membre <strong>pBlobData</strong> est un pointeur vers une structure <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , pour laquelle le membre <strong>Lap</strong> est le code d’accès de requête Bluetooth et le membre de <strong>longueur</strong> est la longueur, en secondes, de la recherche.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bb3c-120"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="7bb3c-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="7bb3c-121">Définissez sur <strong>NS_BTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bb3c-122">Autres membres</span><span class="sxs-lookup"><span data-stu-id="7bb3c-122">Other members</span></span></td>
<td><span data-ttu-id="7bb3c-123">Les autres membres de la structure <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7bb3c-124">Les indicateurs répertoriés dans le tableau suivant sont utilisés dans le paramètre *dwControlFlags* pour contrôler les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="7bb3c-125">Les **lup \_ Containers** et **lup \_ FLUSHCACHE** Flags sont utilisés par la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; le reste des indicateurs est utilisé dans les appels à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="7bb3c-126">Indicateur</span><span class="sxs-lookup"><span data-stu-id="7bb3c-126">Flag</span></span>               | <span data-ttu-id="7bb3c-127">Résultats</span><span class="sxs-lookup"><span data-stu-id="7bb3c-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb3c-128">\_conteneurs lup</span><span class="sxs-lookup"><span data-stu-id="7bb3c-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="7bb3c-129">Spécifie que l’objectif de la requête est d’obtenir une liste d’appareils Bluetooth et non une liste de services.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="7bb3c-130">Cet indicateur doit être défini.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7bb3c-131">LUP \_ FLUSHCACHE</span><span class="sxs-lookup"><span data-stu-id="7bb3c-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="7bb3c-132">Déclenche une recherche d’appareils locaux ou fait en sorte que les résultats mis en cache des requêtes précédentes soient retournés.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7bb3c-133">\_type de retour lup \_</span><span class="sxs-lookup"><span data-stu-id="7bb3c-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="7bb3c-134">Retournez le COD Bluetooth (classe des bits d’appareil) directement dans le membre **lpServiceClassId** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="7bb3c-135">La DCO est mappée au membre **Data1** du GUID.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="7bb3c-136">\_service lup res \_</span><span class="sxs-lookup"><span data-stu-id="7bb3c-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="7bb3c-137">Retourne des informations pour l’adresse Bluetooth locale.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="7bb3c-138">Cet indicateur n’a d’effet que si **lup \_ renvoie \_ addr** est également spécifié.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7bb3c-139">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="7bb3c-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="7bb3c-140">Retourne le nom complet de l’appareil dans le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour chaque appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="7bb3c-141">Cet indicateur doit également être spécifié pour récupérer le membre **Name** de la structure d’informations de l' [**\_ appareil \_ BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) lors de la spécification de l’indicateur de retour de l' **\_ \_ objet BLOB lup** .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="7bb3c-142">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="7bb3c-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="7bb3c-143">Retournez une [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) qui contient l’adresse 48 bits de l’homologue dans le membre **LpcsaBuffer** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour chaque appel à la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7bb3c-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="7bb3c-144">Les autres membres de la structure **\_ BTH sockaddr** sont vides.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="7bb3c-145">LUP \_ retourne un \_ objet BLOB</span><span class="sxs-lookup"><span data-stu-id="7bb3c-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="7bb3c-146">Retournez la structure d’informations sur l' [**\_ appareil \_ BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) à chaque appel suivant à [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="7bb3c-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7bb3c-147">LUP \_ FLUSHPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="7bb3c-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="7bb3c-148">Ignorez l’appareil disponible suivant et retournez l’appareil qui le suit.</span><span class="sxs-lookup"><span data-stu-id="7bb3c-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7bb3c-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7bb3c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb3c-150">Bluetooth et WSALookupServiceBegin pour la détection de service</span><span class="sxs-lookup"><span data-stu-id="7bb3c-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="7bb3c-151">Bluetooth et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="7bb3c-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="7bb3c-152">Bluetooth et WSAQUERYSET pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="7bb3c-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="7bb3c-153">Détection des appareils et services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7bb3c-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="7bb3c-154">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="7bb3c-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="7bb3c-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="7bb3c-157">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="7bb3c-158">**\_périphérique de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="7bb3c-159">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="7bb3c-160">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="7bb3c-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="7bb3c-161">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="7bb3c-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 