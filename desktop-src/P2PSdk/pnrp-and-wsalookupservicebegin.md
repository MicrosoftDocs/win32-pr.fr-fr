---
description: PNRP utilise la fonction WSALookupServiceBegin pour démarrer le processus qui permet à une application d’effectuer les opérations suivantes.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP et WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106522558"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="38057-103">PNRP et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="38057-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="38057-104">PNRP utilise la fonction [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) pour démarrer le processus qui permet à une application d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="38057-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="38057-105">Résolution d’un nom</span><span class="sxs-lookup"><span data-stu-id="38057-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="38057-106">Énumération des clouds réseau</span><span class="sxs-lookup"><span data-stu-id="38057-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="38057-107">Les clients qui tentent d’exécuter l’une des fonctions utilisent les fonctions [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** et **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="38057-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="38057-108">À l’aide de [**WSANSPIoctl**](winsock-nsp-reference-links.md), le service de recherche peut être utilisé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="38057-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="38057-109">Pour plus d’informations sur l’utilisation des fonctions de service de recherche de manière asynchrone, consultez [PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="38057-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="38057-110">Le processus d’utilisation des noms d’homologues diffère de l’utilisation des clouds.</span><span class="sxs-lookup"><span data-stu-id="38057-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="38057-111">Chaque processus est décrit séparément dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="38057-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="38057-112">Résolution d’un nom</span><span class="sxs-lookup"><span data-stu-id="38057-112">Resolving a Name</span></span>

<span data-ttu-id="38057-113">Une application utilise [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) pour obtenir l’adresse IP, le port et le protocole d’un service homologue inscrit sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="38057-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="38057-114">La fonction **WSALookupServiceBegin** est utilisée pour démarrer le processus de résolution de noms, et pour configurer les paramètres et les restrictions.</span><span class="sxs-lookup"><span data-stu-id="38057-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="38057-115">Un descripteur est retourné et doit être utilisé lors de l’appel de **WSALookupServiceNext** et **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="38057-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="38057-116">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="38057-116">lpqsRestrictions</span></span>

<span data-ttu-id="38057-117">Lors de la résolution d’un nom d’homologue, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRestrictions* doit contenir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38057-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="38057-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="38057-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="38057-119">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="38057-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="38057-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="38057-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="38057-121">Spécifie un nom d’homologue à résoudre.</span><span class="sxs-lookup"><span data-stu-id="38057-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="38057-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="38057-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="38057-123">Doit être **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="38057-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="38057-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="38057-125">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="38057-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="38057-127">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="38057-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="38057-129">Il doit s’agir de **NS \_ PNRPNAME** ou **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="38057-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="38057-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="38057-131">Doit être un **\_ fournisseur NS \_ PNRPNAME** ou **null**.</span><span class="sxs-lookup"><span data-stu-id="38057-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="38057-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="38057-133">Doit être un nom de Cloud, une chaîne vide ou une **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="38057-134">Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global \_ », est utilisé.</span><span class="sxs-lookup"><span data-stu-id="38057-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="38057-135">Dans le cas contraire, il doit pointer vers un nom de Cloud valide.</span><span class="sxs-lookup"><span data-stu-id="38057-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="38057-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="38057-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="38057-137">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="38057-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="38057-139">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="38057-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="38057-141">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="38057-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="38057-143">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="38057-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="38057-145">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="38057-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="38057-147">Doit être un pointeur vers une structure [**BLOB**](winsock-nsp-reference-links.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="38057-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="38057-148">Si la **valeur est null**, les valeurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="38057-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="38057-149">S’il est défini, **lpBlob** pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) , et les paramètres spécifiques de la structure **PNRPINFO** doivent être définis.</span><span class="sxs-lookup"><span data-stu-id="38057-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="38057-150">Pour plus d’informations, consultez les descriptions suivantes de la structure PNRPINFO.</span><span class="sxs-lookup"><span data-stu-id="38057-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="38057-151">PNRPINFO, structure</span><span class="sxs-lookup"><span data-stu-id="38057-151">PNRPINFO Structure</span></span>

<span data-ttu-id="38057-152">Si le membre **lpBlob** de la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) est défini, les membres suivants de la structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) doivent être définis :</span><span class="sxs-lookup"><span data-stu-id="38057-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="38057-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="38057-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="38057-154">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="38057-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="38057-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="38057-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="38057-156">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="38057-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="38057-158">Spécifie le nombre demandé de résolutions.</span><span class="sxs-lookup"><span data-stu-id="38057-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="38057-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="38057-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="38057-160">Spécifie le délai d’attente demandé pour les réponses.</span><span class="sxs-lookup"><span data-stu-id="38057-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="38057-161">La valeur par défaut est 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="38057-161">The default is 30 seconds.</span></span> <span data-ttu-id="38057-162">La valeur maximale est de 600 secondes (10 minutes).</span><span class="sxs-lookup"><span data-stu-id="38057-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="38057-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="38057-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="38057-164">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="38057-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="38057-166">Doit être l’une des valeurs autorisées.</span><span class="sxs-lookup"><span data-stu-id="38057-166">Must be one of the allowed values.</span></span> <span data-ttu-id="38057-167">La valeur par défaut est **PNRP \_ résoudre les \_ critères \_ non actifs du nom de l' \_ \_ \_ homologue \_**.</span><span class="sxs-lookup"><span data-stu-id="38057-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="38057-168">Les valeurs valides sont spécifiées par les [**\_ \_ critères de résolution PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span><span class="sxs-lookup"><span data-stu-id="38057-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="38057-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="38057-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="38057-170">Doit avoir la valeur zéro (0) ou l' **\_ indicateur PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="38057-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="38057-171">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**</span><span class="sxs-lookup"><span data-stu-id="38057-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="38057-173">Spécifie l’adresse IP de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="38057-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="38057-174">L’indicateur est utilisé lors de la tentative de recherche du nom de pair le plus proche.</span><span class="sxs-lookup"><span data-stu-id="38057-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="38057-175">Le format de l’indicateur est une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="38057-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="38057-176">Si **sahint** n’est pas spécifié lors de la recherche du nom d’homologue le plus proche, une adresse IPv6 de l’ordinateur local est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="38057-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="38057-177">Ce membre est ignoré si **dwFlags** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="38057-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="38057-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="38057-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="38057-179">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="38057-180">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="38057-180">dwControlFlags</span></span>

<span data-ttu-id="38057-181">Les indicateurs de \_ retour lup suivants \_ \* sont pris en charge par PNRP :</span><span class="sxs-lookup"><span data-stu-id="38057-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="38057-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="38057-182">Value</span></span>                | <span data-ttu-id="38057-183">Description</span><span class="sxs-lookup"><span data-stu-id="38057-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="38057-184">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="38057-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="38057-185">Retourne un nom et un contexte.</span><span class="sxs-lookup"><span data-stu-id="38057-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="38057-186">LUP \_ retourner le \_ Commentaire</span><span class="sxs-lookup"><span data-stu-id="38057-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="38057-187">Retourne un commentaire associé à un nom.</span><span class="sxs-lookup"><span data-stu-id="38057-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="38057-188">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="38057-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="38057-189">Retourne une adresse associée à un nom.</span><span class="sxs-lookup"><span data-stu-id="38057-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="38057-190">Énumération des clouds réseau</span><span class="sxs-lookup"><span data-stu-id="38057-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="38057-191">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="38057-191">lpqsRestrictions</span></span>

<span data-ttu-id="38057-192">Lors de l’énumération de Clouds, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRestrictions* doit contenir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38057-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="38057-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="38057-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="38057-194">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="38057-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="38057-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="38057-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="38057-196">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="38057-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="38057-198">Doit être **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="38057-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="38057-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="38057-200">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="38057-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="38057-202">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="38057-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="38057-204">Doit être **NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="38057-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="38057-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="38057-206">Doit être un **\_ fournisseur NS \_ PNRPCLOUD** ou **null**.</span><span class="sxs-lookup"><span data-stu-id="38057-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="38057-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="38057-208">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="38057-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="38057-210">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="38057-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="38057-212">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="38057-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="38057-214">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="38057-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="38057-216">Réservé, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="38057-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38057-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="38057-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="38057-218">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="38057-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="38057-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="38057-220">Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) .</span><span class="sxs-lookup"><span data-stu-id="38057-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="38057-221">Si **lpBlob** a la **valeur null**, tous les clouds sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="38057-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="38057-222">PNRPCLOUDINFO, structure</span><span class="sxs-lookup"><span data-stu-id="38057-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="38057-223">Lors de l’énumération de Clouds, les membres suivants de la structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) doivent être définis :</span><span class="sxs-lookup"><span data-stu-id="38057-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="38057-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="38057-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="38057-225">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="38057-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="38057-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Pluie**</span><span class="sxs-lookup"><span data-stu-id="38057-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="38057-227">Pointe vers une structure qui spécifie les critères que vous pouvez utiliser pour filtrer les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="38057-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="38057-228">Le membre **Cloud. Scope** peut correspondre à l' **\_ étendue PNRP Any \_**, à l’étendue **\_ globale \_ PNRP**, à l' **\_ \_ \_ étendue locale du site PNRP** ou à l' **\_ \_ \_ étendue locale du lien PNRP**.</span><span class="sxs-lookup"><span data-stu-id="38057-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="38057-229">Si **\_ \_ l’étendue PNRP** est spécifiée, tous les clouds sont retournés.</span><span class="sxs-lookup"><span data-stu-id="38057-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="38057-230">Sinon, seuls les clouds qui correspondent au **Cloud. Scope** sont retournés.</span><span class="sxs-lookup"><span data-stu-id="38057-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="38057-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="38057-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="38057-232">Réservé, doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="38057-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="38057-233">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="38057-233">dwControlFlags</span></span>

<span data-ttu-id="38057-234">Les indicateurs de \_ retour lup suivants \_ \* sont pris en charge par PNRP :</span><span class="sxs-lookup"><span data-stu-id="38057-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="38057-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="38057-235">Value</span></span>             | <span data-ttu-id="38057-236">Description</span><span class="sxs-lookup"><span data-stu-id="38057-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="38057-237">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="38057-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="38057-238">Retourne un nom et un contexte.</span><span class="sxs-lookup"><span data-stu-id="38057-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="38057-239">LUP \_ retourne un \_ objet BLOB</span><span class="sxs-lookup"><span data-stu-id="38057-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="38057-240">Retourne l' [objet BLOB](pnrp-and-blob.md) associé à ce Cloud.</span><span class="sxs-lookup"><span data-stu-id="38057-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="38057-241">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38057-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38057-242">PNRP et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="38057-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="38057-243">PNRP et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="38057-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="38057-244">PNRP et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="38057-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="38057-245">PNRP et WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="38057-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="38057-246">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="38057-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="38057-247">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="38057-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="38057-248">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="38057-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="38057-249">Codes d’erreur du NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="38057-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



