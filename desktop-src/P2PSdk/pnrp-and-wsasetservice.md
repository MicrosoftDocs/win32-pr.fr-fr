---
description: PNRP utilise la fonction WSASetService pour inscrire ou supprimer des noms d’homologue.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP et WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527897"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="5c3e1-103">PNRP et WSASetService</span><span class="sxs-lookup"><span data-stu-id="5c3e1-103">PNRP and WSASetService</span></span>

<span data-ttu-id="5c3e1-104">PNRP utilise la fonction [**WSASetService**](winsock-nsp-reference-links.md) pour inscrire ou supprimer des [noms d’homologue](peer-names.md).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="5c3e1-105">Inscription d’un nom</span><span class="sxs-lookup"><span data-stu-id="5c3e1-105">Registering a Name</span></span>

<span data-ttu-id="5c3e1-106">L’inscription comprend un nom d’homologue et un ensemble de points de terminaison dans lesquels un service peut être contacté.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="5c3e1-107">Une inscription est spécifique à un Cloud PNRP.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="5c3e1-108">Une fois qu’un homologue est inscrit, il y a un délai entre l’inscription et la propagation des informations d’inscription à d’autres nœuds.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="5c3e1-109">Pendant ce temps, les autres nœuds peuvent ne pas être en mesure de résoudre un homologue nouvellement inscrit.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="5c3e1-110">L’inscription du service n’est pas persistante.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="5c3e1-111">Si un processus client qui inscrit un nom d’homologue s’arrête ou appelle [**WSACleanup**](winsock-nsp-reference-links.md), le nom de l’homologue n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="5c3e1-112">Si un nom d’homologue spécifié est déjà inscrit dans le même Cloud par le processus en cours, il est remplacé par de nouvelles valeurs d’inscription.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="5c3e1-113">Lors de l’inscription d’un nom d’homologue, les valeurs de paramètre suivantes doivent être indiquées :</span><span class="sxs-lookup"><span data-stu-id="5c3e1-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="5c3e1-114">le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="5c3e1-115">le paramètre *dwControlFlags* doit être égal à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="5c3e1-116">Lors de l’inscription d’un nom d’homologue, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRegInfo* doit contenir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c3e1-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5c3e1-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-118">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-120">Spécifie un nom d’homologue à inscrire.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-120">Specifies a peer name to register.</span></span> <span data-ttu-id="5c3e1-121">Si le [nom d’homologue](peer-names.md) n’est pas sécurisé, l’identité est facultative.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="5c3e1-122">Si l’identité est spécifiée comme étant **null**, PNRP utilise l’identité locale de l’ordinateur, par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-124">Doit être SVCID \_ PNRPNAME.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-126">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-126">Ignored.</span></span> <span data-ttu-id="5c3e1-127">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-129">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-129">Ignored.</span></span> <span data-ttu-id="5c3e1-130">Toutefois, la chaîne doit toujours contenir moins de 40 caractères, y compris la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="5c3e1-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-132">Il doit s’agir de **NS \_ PNRPNAME** ou **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-134">Doit être un **\_ fournisseur NS \_ PNRPNAME** ou **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-136">Doit être un nom de Cloud, une chaîne vide ou une **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="5c3e1-137">Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global », est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="5c3e1-138">Dans le cas contraire, il doit pointer vers un nom de Cloud valide.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-140">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-140">Ignored.</span></span> <span data-ttu-id="5c3e1-141">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-143">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-143">Ignored.</span></span> <span data-ttu-id="5c3e1-144">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-146">Spécifie le nombre d’adresses inscrites par un service.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="5c3e1-147">Le nombre maximal d’adresses pouvant être inscrites pour un seul nom est de 10.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-149">Pointeur vers une liste d’adresses à inscrire.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-151">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-151">Ignored.</span></span> <span data-ttu-id="5c3e1-152">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-154">Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="5c3e1-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="5c3e1-155">Les paramètres spécifiques de la structure **PNRPINFO** doivent être définis.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="5c3e1-156">Pour plus d’informations, consultez la section structure **PNRPINFO** suivante.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="5c3e1-157">PNRPINFO, structure</span><span class="sxs-lookup"><span data-stu-id="5c3e1-157">PNRPINFO Structure</span></span>

<span data-ttu-id="5c3e1-158">Si le membre **lpBlob** de la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) est défini, les membres suivants de la structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) doivent être définis :</span><span class="sxs-lookup"><span data-stu-id="5c3e1-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="5c3e1-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-160">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-162">Spécifie l’identité du nom d’homologue créé à l’aide de [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="5c3e1-163">Si un nom d’homologue n’est pas sécurisé, l’identité est facultative.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="5c3e1-164">Si l’identité est spécifiée comme étant **null**, PNRP utilise l’identité locale de l’ordinateur, par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-166">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-166">Ignored.</span></span> <span data-ttu-id="5c3e1-167">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-169">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-169">Ignored.</span></span> <span data-ttu-id="5c3e1-170">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-172">Spécifie le nombre de secondes entre les opérations d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-174">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-174">Ignored.</span></span> <span data-ttu-id="5c3e1-175">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-177">Doit avoir la valeur zéro (0) ou l' **\_ indicateur PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="5c3e1-178">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-178">The default is zero (0).</span></span> <span data-ttu-id="5c3e1-179">Cela signifie que la partie emplacement du service de l’ID PNRP est créée à l’aide de l’adresse IP dans **sahint**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="5c3e1-180">Dans le cas contraire, l’emplacement du service est généré à l’aide de la première adresse IP de la première entrée IPv6 du membre **lpcsaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="5c3e1-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-182">Spécifie l’adresse IPv6 de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-184">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-184">Ignored.</span></span> <span data-ttu-id="5c3e1-185">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="5c3e1-186">Annulation de l’inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="5c3e1-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="5c3e1-187">La liste suivante identifie les informations importantes sur l’annulation de l’inscription d’un nom d’homologue.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="5c3e1-188">Seule une application qui inscrit un nom d’homologue peut annuler son inscription.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="5c3e1-189">Un nom d’homologue est annulé automatiquement si [**WSACleanup**](winsock-nsp-reference-links.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="5c3e1-190">Le protocole PNRP supprime toujours l’enregistrement complet du nom de service.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="5c3e1-191">Elle n’autorise pas la suppression d’adresses individuelles.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="5c3e1-192">Lors de l’annulation de l’inscription d’un nom, le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="5c3e1-193">PNRP ne prend pas en charge la valeur **RNRSERVICE \_ Unregister**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="5c3e1-194">Le paramètre *dwControlFlags* doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="5c3e1-195">Lors de l’annulation de l’inscription d’un nom, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRegInfo* doit contenir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c3e1-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5c3e1-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-197">Spécifie la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-199">Spécifie un nom d’homologue dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-201">Doit être **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-203">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-203">Ignored.</span></span> <span data-ttu-id="5c3e1-204">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-206">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-206">Ignored.</span></span> <span data-ttu-id="5c3e1-207">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-209">Il doit s’agir de **NS \_ PNRPNAME** ou **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-211">Doit être un **\_ fournisseur NS \_ PNRPNAME** ou **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-213">Doit être un nom de Cloud, une chaîne vide ou une **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="5c3e1-214">Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global », est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="5c3e1-215">Dans le cas contraire, il doit pointer vers un nom de Cloud valide.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-217">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-217">Ignored.</span></span> <span data-ttu-id="5c3e1-218">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-220">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-220">Ignored.</span></span> <span data-ttu-id="5c3e1-221">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-223">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-223">Ignored.</span></span> <span data-ttu-id="5c3e1-224">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-226">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-226">Ignored.</span></span> <span data-ttu-id="5c3e1-227">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-229">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-229">Ignored.</span></span> <span data-ttu-id="5c3e1-230">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5c3e1-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5c3e1-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="5c3e1-232">Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="5c3e1-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="5c3e1-233">Le membre **lpszIdentity** de la structure **lpBlob** identifie le nom de l’identité qui est utilisée pour enregistrer un nom d’homologue.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="5c3e1-234">Les membres restants doivent être définis sur les mêmes valeurs que celles utilisées lors de l’inscription d’un nom.</span><span class="sxs-lookup"><span data-stu-id="5c3e1-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5c3e1-235">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c3e1-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c3e1-236">PNRP et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="5c3e1-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="5c3e1-237">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="5c3e1-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="5c3e1-238">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="5c3e1-239">Codes d’erreur du NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="5c3e1-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="5c3e1-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="5c3e1-241">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="5c3e1-241">**WSASetService**</span></span>
</dt> </dl>

 

 



