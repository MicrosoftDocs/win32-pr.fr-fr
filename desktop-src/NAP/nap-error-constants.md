---
title: Constantes d’erreur NAP (WinError. h)
description: Les constantes d’erreur NAP suivantes sont définies dans WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942624"
---
# <a name="nap-error-constants"></a><span data-ttu-id="32e3e-103">Constantes d’erreur NAP</span><span class="sxs-lookup"><span data-stu-id="32e3e-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="32e3e-104">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="32e3e-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="32e3e-105">Les constantes d’erreur NAP suivantes sont définies dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="32e3e-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="32e3e-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_paquet NAP E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="32e3e-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-107">\_HRESULT \_ typedef \_ (0x80270001L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-108">Le paquet de [**déclaration d’intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="32e3e-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**SOH de la protection d’accès réseau \_ \_ manquante \_**</span><span class="sxs-lookup"><span data-stu-id="32e3e-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-110">\_HRESULT \_ typedef \_ (0x80270002L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-111">Une [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) était manquante dans le paquet NAP.</span><span class="sxs-lookup"><span data-stu-id="32e3e-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ID en \_ conflit NAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="32e3e-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-113">\_HRESULT \_ typedef \_ (0x80270003L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-114">L’ID d’entité est en conflit avec un ID d’entité déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="32e3e-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**E/r NAP \_ \_ non \_ mis en cache \_**</span><span class="sxs-lookup"><span data-stu-id="32e3e-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-116">\_HRESULT \_ typedef \_ (0x80270004L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-117">Aucune déclaration d' [**intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) mise en cache n’est présente.</span><span class="sxs-lookup"><span data-stu-id="32e3e-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**la protection NAP est \_ \_ toujours \_ liée**</span><span class="sxs-lookup"><span data-stu-id="32e3e-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-119">\_HRESULT \_ typedef \_ (0x80270005L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-120">L’entité est toujours liée au système NAP.</span><span class="sxs-lookup"><span data-stu-id="32e3e-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="32e3e-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-122">\_HRESULT \_ typedef \_ (0x80270006L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-123">L’entité n’est pas inscrite auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="32e3e-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ non \_ initialisé**</span><span class="sxs-lookup"><span data-stu-id="32e3e-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-125">\_HRESULT \_ typedef \_ (0x80270007L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-126">L’entité n’est pas initialisée avec le système NAP.</span><span class="sxs-lookup"><span data-stu-id="32e3e-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ID non \_ compatible NAP \_**</span><span class="sxs-lookup"><span data-stu-id="32e3e-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-128">\_HRESULT \_ typedef \_ (0x80270008L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-129">Les ID de corrélation dans la requête [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et la réponse **SOH** ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="32e3e-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ non \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="32e3e-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-131">\_HRESULT \_ typedef \_ (0x80270009L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-132">La saisie semi-automatique a été indiquée sur une demande qui n’est pas actuellement en attente.</span><span class="sxs-lookup"><span data-stu-id="32e3e-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ID NAP \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="32e3e-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-134">\_HRESULT \_ typedef \_ (0x8027000AL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-135">L’ID du composant NAP est introuvable.</span><span class="sxs-lookup"><span data-stu-id="32e3e-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ trop \_ petit**</span><span class="sxs-lookup"><span data-stu-id="32e3e-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-137">\_HRESULT \_ typedef \_ (0x8027000BL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-138">La taille maximale de la connexion est trop petite pour un paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="32e3e-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_service E \_ NAP \_ non \_ exécuté**</span><span class="sxs-lookup"><span data-stu-id="32e3e-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-140">\_HRESULT \_ typedef \_ (0x8027000CL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-141">Le service NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="32e3e-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_certificat NAP \_ S \_ déjà \_ présent**</span><span class="sxs-lookup"><span data-stu-id="32e3e-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-143">\_HRESULT \_ typedef \_ (0x0027000DL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="32e3e-144">Un certificat est déjà présent dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="32e3e-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entité NAP \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="32e3e-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-146">\_HRESULT \_ typedef \_ (0x8027000EL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-147">L’entité est désactivée avec le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="32e3e-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_erreur NAP E \_ netsh \_ GROUPPOLICY \_**</span><span class="sxs-lookup"><span data-stu-id="32e3e-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-149">\_HRESULT \_ typedef \_ (0x8027000FL)</span><span class="sxs-lookup"><span data-stu-id="32e3e-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-150">Stratégie de groupe n’est pas configurée.</span><span class="sxs-lookup"><span data-stu-id="32e3e-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ trop \_ d' \_ appels**</span><span class="sxs-lookup"><span data-stu-id="32e3e-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-152">\_HRESULT \_ typedef \_ (0x80270010L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-153">Appels simultanés trop nombreux.</span><span class="sxs-lookup"><span data-stu-id="32e3e-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**la \_ configuration NAP E \_ SHV \_ \_ existait**</span><span class="sxs-lookup"><span data-stu-id="32e3e-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-155">\_HRESULT \_ typedef \_ (0x80270011L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-156">La configuration SHV existe déjà.</span><span class="sxs-lookup"><span data-stu-id="32e3e-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="32e3e-157">Pris en charge dans Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="32e3e-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="32e3e-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-159">\_HRESULT \_ typedef \_ (0x80270012L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-160">La configuration SHV est introuvable.</span><span class="sxs-lookup"><span data-stu-id="32e3e-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="32e3e-161">Pris en charge dans Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="32e3e-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="32e3e-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_ \_ \_ délai d’attente du SHV NAP E**</span><span class="sxs-lookup"><span data-stu-id="32e3e-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3e-163">\_HRESULT \_ typedef \_ (0x80270013L)</span><span class="sxs-lookup"><span data-stu-id="32e3e-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="32e3e-164">Le SHV a expiré sur la demande.</span><span class="sxs-lookup"><span data-stu-id="32e3e-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="32e3e-165">Pris en charge dans Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="32e3e-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e3e-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32e3e-166">Requirements</span></span>



| <span data-ttu-id="32e3e-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e3e-167">Requirement</span></span> | <span data-ttu-id="32e3e-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e3e-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32e3e-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e3e-169">Minimum supported client</span></span><br/> | <span data-ttu-id="32e3e-170">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e3e-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32e3e-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e3e-171">Minimum supported server</span></span><br/> | <span data-ttu-id="32e3e-172">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e3e-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32e3e-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="32e3e-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e3e-174"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e3e-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e3e-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e3e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e3e-176">**Constantes NAP**</span><span class="sxs-lookup"><span data-stu-id="32e3e-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





