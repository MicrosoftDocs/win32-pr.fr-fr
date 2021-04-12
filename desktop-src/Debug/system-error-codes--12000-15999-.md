---
description: Décrit les codes d’erreur 12000-1599 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Codes d’erreur système (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483321"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="ee4c6-103">Codes d’erreur système (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="ee4c6-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="ee4c6-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ee4c6-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="ee4c6-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 12000 à 15999).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="ee4c6-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="ee4c6-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="ee4c6-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Erreur \_ \_Internet \** _</span><span class="sxs-lookup"><span data-stu-id="ee4c6-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-110">12000-12175 (0x2EE0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-111">Consultez [codes d’erreur Internet](../wininet/wininet-errors.md) et wininet. h.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *erreur la \_ stratégie de QM IPSec est \_ \_ \_ inexistante*\*</span><span class="sxs-lookup"><span data-stu-id="ee4c6-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-113">13000 (0x32C8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-114">La stratégie de mode rapide spécifiée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERREUR \_ la \_ stratégie de QM IPSec est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-116">13001 (0x32C9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-117">La stratégie de mode rapide spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERREUR \_ \_ de la \_ stratégie de QM IPSec \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-119">13002 (0x32CA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-120">La stratégie de mode rapide spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERREUR \_ la \_ stratégie IPSec mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-122">13003 (0x32CB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-123">La stratégie de mode principal spécifiée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERREUR \_ la \_ stratégie IPSec mm est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-125">13004 (0x32CC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-126">La stratégie de mode principal spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERREUR \_ \_ de la stratégie IPSec mm \_ \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-128">13005 (0x32CD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-129">La stratégie de mode principal spécifiée est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERREUR \_ le \_ filtre IPSec mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-131">13006 (0x32CE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-132">Le filtre en mode principal spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERREUR \_ de \_ filtre IPSec mm \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-134">13007 (0x32CF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-135">Le filtre de mode principal spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERREUR \_ le \_ filtre de transport IPSec \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-137">13008 (0x32D0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-138">Le filtre de mode de transport spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERREUR \_ de \_ filtre de transport IPSec \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-140">13009 (0x32D1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-141">Le filtre de mode de transport spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ existe**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-143">13010 (0x32D2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-144">La liste d’authentification en mode principal spécifiée existe.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-146">13011 (0x32D3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-147">La liste d’authentification du mode principal spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-149">13012 (0x32D4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-150">La liste d’authentification en mode principal spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERREUR \_ la \_ stratégie mm par défaut IPSec est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-152">13013 (0x32D5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-153">La stratégie de mode principal par défaut spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERREUR \_ la \_ valeur par défaut de l' \_ authentification mm IPSec est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-155">13014 (0x32D6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-156">La liste d’authentification du mode principal par défaut spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERREUR \_ \_ stratégie de QM par défaut IPSec \_ \_ \_ non \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-158">13015 (0x32D7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-159">La stratégie de mode rapide par défaut spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERREUR \_ de \_ filtre de tunnel IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-161">13016 (0x32D8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-162">Le filtre de mode de tunnel spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERREUR \_ de \_ filtre de tunnel IPSec \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-164">13017 (0x32D9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-165">Le filtre de mode de tunnel spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-167">13018 (0x32DA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-168">Le filtre en mode principal est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre de transport IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-170">13019 (0x32DB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-171">Le filtre de transport est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre de tunnel IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-173">13020 (0x32DC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-174">Le filtre de tunnel est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente de la stratégie IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-176">13021 (0x32DD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-177">La stratégie en mode principal est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente d’authentification IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-179">13022 (0x32DE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-180">Le bundle d’authentification en mode principal est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente de la stratégie de QM IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-182">13023 (0x32DF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-183">La stratégie de mode rapide est en attente de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**Avertissement de la \_ \_ stratégie IPSec mm \_ \_ nettoyée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-185">13024 (0x32E0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-186">La stratégie en mode principal a été ajoutée avec succès, mais certaines des offres demandées ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**Avertissement de la \_ \_ stratégie de QM IPSec \_ \_ nettoyée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-188">13025 (0x32E1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-189">La stratégie de mode rapide a été ajoutée avec succès, mais certaines des offres demandées ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERREUR lors du démarrage de l’état de la \_ sécurité \_ Ike Ike \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-191">13800 (0x35E8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-192">ERREUR lors du démarrage de l’état de la \_ sécurité \_ Ike Ike \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee4c6-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERREUR d’échec de l' \_ \_ authentification IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-194">13801 (0x35E9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-195">Les informations d’authentification IKE ne sont pas acceptables.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERREUR \_ d' \_ \_ échec d’attrib IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-197">13802 (0x35EA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-198">Les attributs de sécurité IKE ne sont pas acceptables.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERREUR \_ de \_ négociation IKE IPSec \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-200">13803 (0x35EB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-201">Négociation IKE en cours.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**erreur \_ de \_ \_ traitement général \_ IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-203">13804 (0x35EC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-204">Erreur de traitement général.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERREUR \_ IPSec \_ IKE \_ expiré \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-206">13805 (0x35ED)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-207">Expiration du délai d’attente de la négociation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERREUR \_ IPSec \_ IKE \_ aucun \_ certificat**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-209">13806 (0x35EE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-210">IKE n’a pas pu trouver un certificat d’ordinateur valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="ee4c6-211">Contactez votre administrateur de sécurité réseau pour installer un certificat valide dans le magasin de certificats approprié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERREUR \_ IPSec \_ IKE \_ sa \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-213">13807 (0x35EF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-214">SA IKE supprimée par l’homologue avant la fin de l’établissement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERREUR d' \_ Association de sécurité \_ Ike Ike \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-216">13808 (0x35F0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-217">SA IKE a été supprimée avant la fin de l’établissement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERREUR de suppression de l' \_ acquisition d’IPSec \_ IKE \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-219">13809 (0x35F1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-220">La demande de négociation est restée trop longue dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERREUR d’obtention de la suppression du \_ \_ QM IPsec IKE \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-222">13810 (0x35F2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-223">La demande de négociation est restée trop longue dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERREUR \_ de \_ \_ Suppression de file d’attente IKE \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-225">13811 (0x35F3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-226">La demande de négociation est restée trop longue dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERREUR de suppression de la \_ \_ \_ file d’attente IKE IPSec \_ \_ non \_ mm**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-228">13812 (0x35F4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-229">La demande de négociation est restée trop longue dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERREUR \_ de \_ Suppression d’absence de \_ réponse IPsec IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-231">13813 (0x35F5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-232">Aucune réponse de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERREUR \_ de \_ \_ \_ suppression différée IPsec IKE mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-234">13814 (0x35F6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-235">La négociation a pris trop de temps.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERREUR \_ de \_ \_ suppression du délai de QM IKE \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-237">13815 (0x35F7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-238">La négociation a pris trop de temps.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**erreur \_ IPSec \_ IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-240">13816 (0x35F8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-241">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERREUR \_ \_ \_ échec de la liste de révocation de certificats IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-243">13817 (0x35F9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-244">Échec de la vérification de la révocation des certificats.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERREUR d’utilisation de la \_ \_ \_ clé non valide IPsec IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-246">13818 (0x35FA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-247">Utilisation de clé de certificat non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERREUR \_ de \_ \_ type de \_ certificat non valide IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-249">13819 (0x35FB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-250">Type de certificat non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERREUR \_ IPSec \_ IKE \_ sans \_ \_ clé privée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-252">13820 (0x35FC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-253">La négociation IKE a échoué, car le certificat de l’ordinateur utilisé n’a pas de clé privée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="ee4c6-254">Les certificats IPsec nécessitent une clé privée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="ee4c6-255">Contactez votre administrateur de sécurité réseau pour remplacer par un certificat qui a une clé privée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERREUR \_ de \_ \_ régénération simultanée d’IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-257">13821 (0x35FD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-258">Des retouches simultanées ont été détectées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERREUR \_ IPSec \_ IKE \_ DH \_ échoue**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-260">13822 (0x35FE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-261">Échec dans le calcul de la Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERREUR \_ de \_ \_ charge utile critique IKE IPSec \_ \_ non \_ reconnue**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-263">13823 (0x35FF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-264">Je ne sais pas comment traiter la charge utile critique.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERREUR \_ d' \_ \_ \_ en-tête IPsec IKE non valide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-267">En-tête non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERREUR \_ IPSec \_ IKE \_ aucune \_ stratégie**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-270">Aucune stratégie n’est configurée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERREUR \_ de \_ signature IPsec IKE \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-273">Impossible de vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**erreur \_ IPSec \_ IKE \_ IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-276">Échec de l’authentification à l’aide de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERREUR \_ IPSec \_ IKE \_ aucune \_ \_ clé publique**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-279">Le certificat de l’homologue n’a pas de clé publique.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERREUR \_ de \_ processus IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-282">Erreur lors du traitement de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERREUR \_ du \_ processus Ike Ike de l' \_ \_ \_ Association de sécurité**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-285">Erreur lors du traitement de la charge de SA.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**erreur de traitement de l’erreur du \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-288">Erreur lors du traitement de la charge utile de la proposition.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERREUR \_ de \_ \_ transfert de processus IKE \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-291">Erreur lors du traitement de la charge utile de transformation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**erreur \_ de \_ \_ processus IKE \_ IKE \_ de l’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-294">Erreur lors du traitement de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**erreur ID d’erreur du \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-296">13834 (0x360A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-297">Erreur lors du traitement de la charge utile de l’ID.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**erreur de certificat d’erreur de \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-299">13835 (0x360B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-300">Erreur lors du traitement de la charge utile du certificat.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERREUR \_ de \_ \_ certificat du processus Ike Ike \_ \_ de \_ l’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-302">13836 (0x360C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-303">Erreur lors du traitement de la charge utile de la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERREUR \_ de \_ \_ hachage d’Err de processus IKE \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-305">13837 (0x360D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-306">Erreur lors du traitement de la charge utile de hachage.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**erreur d’erreur du \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-308">13838 (0x360E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-309">Erreur lors du traitement de la charge utile de la signature.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERREUR de la valeur à usage \_ \_ unique du processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-311">13839 (0x360F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-312">Erreur lors du traitement de la charge à usage unique.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**erreur de traitement de l’erreur du \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-315">Erreur lors du traitement de la charge utile de notification.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERREUR de suppression de l' \_ \_ Err du processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-318">Erreur lors du traitement de la charge utile de suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**erreur fournisseur d’erreur de \_ \_ processus IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-321">Erreur lors du traitement de la charge du ID de message.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-324">Charge utile non valide reçue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERREUR de chargement de la \_ \_ \_ \_ \_ sa logicielle IPsec IKE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-327">SA logicielle chargée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERREUR \_ d' \_ Association de sécurité logicielle Ike Ike \_ \_ \_ endommagée \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-330">SA détruite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERREUR \_ de \_ cookie IPsec IKE \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-333">Cookie non valide reçu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERREUR \_ IPSec \_ IKE \_ aucun \_ certificat homologue \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-336">L’homologue n’a pas pu envoyer un certificat d’ordinateur valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERREUR \_ \_ \_ \_ échec de la liste de révocation de certificats homologues IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-339">Échec de la vérification de la révocation de certification du certificat de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERREUR de modification de la \_ \_ stratégie IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-342">Nouvelle stratégie non validée par une SAP formée avec l’ancienne stratégie.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERREUR \_ \_ stratégie IPsec IKE \_ non \_ mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-344">13850 (0x361A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-345">Il n’existe aucune stratégie IKE en mode principal disponible.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERREUR \_ IPSec \_ IKE \_ NOTCBPRIV**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-347">13851 (0x361B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-348">Échec de l’activation du privilège TCB.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERREUR \_ IPSec \_ IKE \_ SECLOADFAIL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-350">13852 (0x361C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-351">Impossible de charger SECURITY.DLL.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERREUR \_ IPSec \_ IKE \_ FAILSSPINIT**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-353">13853 (0x361D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-354">Échec de l’obtention de l’adresse de distribution de la table de fonctions de sécurité à partir de SSPI.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERREUR \_ IPSec \_ IKE \_ FAILQUERYSSP**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-356">13854 (0x361E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-357">Impossible d’interroger le package Kerberos pour obtenir la taille de jeton maximale.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERREUR \_ IPSec \_ IKE \_ SRVACQFAIL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-359">13855 (0x361F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-360">Échec de l’obtention des informations d’identification du serveur Kerberos pour le service IKE/d’erreur ISAKMP/ERROR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ee4c6-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="ee4c6-361">L’authentification Kerberos ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="ee4c6-362">La raison la plus probable de ce problème est l’absence d’appartenance au domaine.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="ee4c6-363">Cela est normal si votre ordinateur est membre d’un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERREUR \_ IPSec \_ IKE \_ SRVQUERYCRED**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-366">Impossible de déterminer le nom principal SSPI pour le \_ service IKE/erreur IPSec \_ IKE ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERREUR \_ IPSec \_ IKE \_ GETSPIFAIL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-369">Échec de l’obtention du nouveau SPI pour la SA entrante à partir du pilote IPsec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="ee4c6-370">La cause la plus courante est que le pilote n’a pas le bon filtre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="ee4c6-371">Vérifiez votre stratégie pour vérifier les filtres.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERREUR \_ de \_ \_ filtre non valide IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-374">Le filtre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERREUR \_ \_ \_ \_ de \_ mémoire insuffisante IPsec IKE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-377">L'allocation de mémoire a échoué.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERREUR Échec de l’ajout de la \_ \_ \_ clé de \_ mise à jour IPSec \_ IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-380">Échec de l’ajout de l’Association de sécurité au pilote IPsec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="ee4c6-381">La cause la plus courante est que la négociation IKE a mis trop de temps à se terminer.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="ee4c6-382">Si le problème persiste, réduisez la charge sur l’ordinateur défaillant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERREUR \_ de \_ \_ stratégie non valide IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-384">13861 (0x3625)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-385">Stratégie non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERREUR \_ IPSec \_ IKE \_ inconnu \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-388">DOI non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-391">Situation non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERREUR \_ IPSec \_ IKE \_ DH \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-394">Échec de la Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERREUR \_ de \_ \_ groupe non valide IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-397">Groupe de Diffie-Hellman non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERREUR \_ de \_ \_ chiffrement IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-399">13866 (0x362A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-400">Erreur lors du chiffrement de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERREUR \_ de \_ \_ déchiffrement IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-402">13867 (0x362B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-403">Erreur lors du déchiffrement de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERREUR de correspondance de la \_ \_ stratégie IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-405">13868 (0x362C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-406">Erreur de correspondance de stratégie.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERREUR \_ \_ \_ ID non pris en charge IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-408">13869 (0x362D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-409">ID non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERREUR \_ de \_ \_ hachage non valide IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-411">13870 (0x362E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-412">Échec de la vérification du hachage.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERREUR \_ IPSec \_ IKE \_ \_ hash \_ ALG non valide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-414">13871 (0x362F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-415">Algorithme de hachage non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ taille de hachage non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-418">Taille de hachage non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERREUR \_ IPSec \_ IKE \_ \_ chiffrement non valide \_ ALG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-421">Algorithme de chiffrement non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ authentification non valide \_ ALG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-424">Algorithme d’authentification non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-427">Signature de certificat non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERREUR \_ \_ échec du \_ chargement \_ IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-430">Échec du chargement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERREUR \_ IPSec \_ IKE \_ RPC \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-433">Supprimé par le biais de l’appel RPC.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERREUR \_ IPSec \_ IKE \_ Bénin- \_ Réinit**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-436">État temporaire créé pour effectuer la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="ee4c6-437">Il ne s’agit pas d’une défaillance réelle.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERREUR \_ de \_ durée \_ de \_ vie du répondeur non valide IPsec IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-440">La valeur de durée de vie reçue dans la notification de durée de vie du répondeur est inférieure à la valeur minimale configurée pour Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="ee4c6-441">Corrigez la stratégie sur l’ordinateur homologue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERREUR \_ IPSec \_ IKE \_ \_ version majeure non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-444">Le destinataire ne peut pas gérer la version d’IKE spécifiée dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERREUR \_ IPSec \_ IKE \_ certificat non valide \_ \_ KEYLEN**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-447">La longueur de clé dans le certificat est trop petite pour les exigences de sécurité configurées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERREUR \_ de \_ limite IPsec IKE \_ mm \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-449">13882 (0x363A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-450">Le nombre maximal de MM SAs établies à l’homologue est dépassé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERREUR \_ de \_ négociation IKE IPSec \_ \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-452">13883 (0x363B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-453">IKE a reçu une stratégie qui désactive la négociation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERREUR de la \_ \_ limite de QM IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-455">13884 (0x363C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-456">Limite maximale du mode rapide atteinte pour le mode principal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="ee4c6-457">Le nouveau mode principal démarrera.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERREUR \_ IPSec \_ IKE \_ mm \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-459">13885 (0x363D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-460">Durée de vie de la SA de mode principal expirée ou l’homologue a envoyé une suppression en mode principal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERREUR \_ IPSec \_ IKE \_ pair \_ mm \_ pris en défaut \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-462">13886 (0x363E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-463">La SA de mode principal est supposée être non valide, car l’homologue a cessé de répondre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERREUR \_ d' \_ \_ \_ \_ incompatibilité de stratégie de chaîne de certificats IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-465">13887 (0x363F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-466">Le certificat n’est pas lié à une racine approuvée dans la stratégie IPsec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERREUR \_ d' \_ \_ ID de \_ message \_ inattendu IPsec IKE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-469">Réception d’un ID de message inattendu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ charge d’authentification non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-472">Offres d’authentification non valides reçues.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERREUR \_ de \_ \_ cookie dos IKE IPSec \_ \_ envoyé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-475">Envoi d’une notification de cookie DoS à l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERREUR \_ IPsec IKE en cours d' \_ \_ arrêt \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-478">Arrêt du service IKE en cours.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERREUR d’échec de l' \_ \_ authentification du CGA IPsec IKE \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-481">Impossible de vérifier la liaison entre l’adresse CGA et le certificat.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERREUR \_ de \_ processus IKE IPSec- \_ \_ \_ OTAN**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-484">Erreur lors du traitement de la charge de l’Otana.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_ mm \_ pour \_ QM**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-487">Les paramètres du mode principal ne sont pas valides pour ce mode rapide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERREUR \_ IPSec \_ IKE \_ QM \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-490">La SA du mode rapide a expiré par le pilote IPsec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERREUR \_ IPSec \_ IKE \_ trop \_ grand nombre de \_ filtres**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-493">Un trop grand nombre de filtres IKEEXT ajoutés dynamiquement ont été détectés.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERREUR de fin d’état de la \_ sécurité \_ Ike Ike IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-496">ERREUR de fin d’état de la \_ sécurité \_ Ike Ike IPSec \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee4c6-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERREUR \_ IPSec \_ IKE- \_ supprimer le \_ \_ tunnel NAP factice \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-498">13898 (0x364A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-499">La réauthentification NAP a réussi et doit supprimer le tunnel IKEv2 NAP factice.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERREUR d’affectation de l' \_ \_ \_ \_ adresse IP interne \_ Ike Ike \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-501">13899 (0x364B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-502">Erreur lors de l’affectation de l’adresse IP interne à l’initiateur en mode tunnel.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERREUR \_ IPSec \_ IKE \_ exiger \_ une \_ charge utile CP \_ manquante**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-504">13900 (0x364C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-505">La charge utile de configuration requise est manquante.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERREUR \_ de \_ négociation d’emprunt d’identité du module de clé IPSec \_ \_ \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-507">13901 (0x364D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-508">Une négociation s’exécutant comme principe de sécurité qui a émis la connexion est en cours.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERREUR \_ de \_ \_ Suppression de coexistence IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-510">13902 (0x364E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-511">SA a été supprimée en raison de la vérification de la coexistence de la coexistence IKEv1/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERREUR \_ de \_ \_ suppression du RATELIMIT IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-513">13903 (0x364F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-514">La requête SA entrante a été supprimée en raison de la limitation du taux d’adresses IP d’homologue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERREUR \_ IPSec \_ IKE \_ Peer \_ ne \_ prend pas en charge \_ MOBIKE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-517">L’homologue ne prend pas en charge MOBIKE.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERREUR \_ \_ \_ d’échec d’autorisation IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-520">L'établissement d'associations de sécurité n'est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERREUR \_ \_ \_ \_ \_ d’autorisation d’identification d’identification renforcée IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-523">L’établissement de SA n’est pas autorisé, car il n’y a pas d’informations d’identification PKINIT suffisamment fortes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERREUR \_ \_ \_ d’autorisation IKE IPSec avec une \_ \_ \_ \_ nouvelle tentative facultative**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-526">L'établissement d'associations de sécurité n'est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-526">SA establishment is not authorized.</span></span> <span data-ttu-id="ee4c6-527">Vous devrez peut-être entrer des informations d’identification mises à jour ou différentes, telles qu’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERREUR \_ \_ \_ d’autorisation d’identification d’identification forte IPsec IKE \_ \_ \_ et \_ échec de CERTMAP \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-530">L’établissement de SA n’est pas autorisé, car il n’y a pas d’informations d’identification PKINIT suffisamment fortes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="ee4c6-531">Cela peut être lié à un échec de mappage de certificat à compte pour l’administrateur système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERREUR \_ de \_ \_ \_ \_ fin étendue d’état de la sécurité Ike Ike IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-534">ERREUR \_ de \_ \_ \_ \_ fin étendue d’état de la sécurité Ike Ike IPSec \_</span><span class="sxs-lookup"><span data-stu-id="ee4c6-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERREUR \_ IPSec \_ mauvais \_ SPI**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-537">Le SPI du paquet ne correspond pas à une association de sécurité IPsec valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERREUR \_ durée de vie de l’Association de sécurité IPSec \_ \_ \_ expirée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-540">Le paquet a été reçu sur une association de sécurité IPsec dont la durée de vie a expiré.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**erreur IPSec erreur d’association de \_ sécurité \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-543">Le paquet a été reçu sur une association de sécurité IPsec qui ne correspond pas aux caractéristiques du paquet.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERREUR lors de la vérification de la \_ \_ relecture IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-546">Échec de la vérification de la relecture du numéro de séquence du paquet.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERREUR \_ de \_ paquet non valide IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-548">13914 (0x365A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-549">L’en-tête et/ou le code de fin IPsec du paquet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERREUR \_ échec de la \_ vérification de l’intégrité IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-551">13915 (0x365B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-552">Échec de la vérification de l’intégrité IPsec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERREUR \_ d' \_ effacement du texte en clair IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-554">13916 (0x365C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-555">IPsec a supprimé un paquet de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERREUR \_ de \_ \_ suppression du pare-feu d’authentification IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-557">13917 (0x365D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-558">IPsec a supprimé un paquet ESP entrant en mode pare-feu authentifié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="ee4c6-559">Cette suppression est sans gravité.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERREUR \_ de \_ Suppression d’accélération IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-561">13918 (0x365E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-562">IPsec a supprimé un paquet en raison d’une limitation de la sécurité de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERREUR \_ de \_ bloc DOSP IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-565">La protection DoS IPsec correspond à une règle de blocage explicite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERREUR \_ IPSec \_ DOSP \_ reçue par la \_ multidiffusion**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-568">La protection DoS IPsec a reçu un paquet de multidiffusion spécifique à IPsec, ce qui n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERREUR \_ IPSec \_ DOSP \_ paquet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-571">La protection DoS IPsec a reçu un paquet mis en forme de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERREUR \_ échec de la recherche d' \_ État DOSP IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-574">La protection DoS IPsec n’a pas pu Rechercher l’État.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERREUR \_ \_ \_ nombre maximal d' \_ entrées IPSec DOSP**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-577">La protection DoS IPsec n’a pas pu créer l’État, car le nombre maximal d’entrées autorisées par la stratégie a été atteint.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERREUR \_ IPSec \_ DOSP \_ KEYMOD \_ non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-579">13930 (0x366A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-580">La protection DoS IPsec a reçu un paquet de négociation IPsec pour un module de génération de clé qui n’est pas autorisé par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERREUR \_ IPSec \_ DOSP \_ non \_ installé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-582">13931 (0x366B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-583">La protection DoS IPsec n’a pas été activée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERREUR \_ IPSec \_ DOSP \_ Max. \_ par \_ RATELIMIT de \_ \_ files d’attente IP**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-585">13932 (0x366C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-586">La protection DoS IPsec n’a pas pu créer une file d’attente par limite de débit IP interne, car le nombre maximal de files d’attente autorisées par la stratégie a été atteint.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**la section SxS de l’erreur est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-588">14000 (0x36B0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-589">La section demandée n’était pas présente dans le contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERREUR \_ SxS \_ Impossible \_ GEN \_ ACTCTX**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-591">14001 (0x36B1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-592">L’application n’a pas pu démarrer, car sa configuration côte à côte est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="ee4c6-593">Pour plus d’informations, consultez le journal des événements de l’application ou utilisez l’outil de sxstrace.exe de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERREUR \_ SxS \_ \_ format de ACTCTXDATA non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-595">14002 (0x36B2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-596">Le format des données de liaison d’application n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERREUR \_ SxS \_ assembly \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-598">14003 (0x36B3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-599">L’assembly référencé n’est pas installé sur votre système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**erreur \_ SxS \_ - \_ erreur de format du manifeste \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-601">14004 (0x36B4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-602">Le fichier manifeste ne commence pas par la balise et les informations de format nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERREUR \_ SxS \_ \_ erreur d’analyse du manifeste \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-604">14005 (0x36B5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-605">Le fichier manifeste contient une ou plusieurs erreurs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERREUR \_ de \_ contexte d’activation SxS \_ \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-607">14006 (0x36B6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-608">L’application a essayé d’activer un contexte d’activation désactivé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERREUR \_ SxS \_ clé \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-610">14007 (0x36B7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-611">La clé de recherche demandée est introuvable dans un contexte d’activation actif.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERREUR \_ de \_ conflit de version SxS \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-613">14008 (0x36B8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-614">Une version de composant requise par l’application est en conflit avec une autre version de composant déjà active.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERREUR \_ SxS \_ \_ type de section incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-616">14009 (0x36B9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-617">La section de contexte d’activation demandée du type ne correspond pas à l’API de requête utilisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERREUR \_ de \_ requête de thread SxS \_ \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-619">14010 (0x36BA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-620">L’absence de ressources système exige que l’activation isolée soit désactivée pour le thread d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERREUR \_ SxS le \_ processus \_ par défaut est \_ déjà \_ défini**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-622">14011 (0x36BB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-623">Une tentative de définition du contexte d’activation par défaut du processus a échoué, car le contexte d’activation par défaut du processus était déjà défini.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERREUR \_ SxS \_ - \_ groupe d’encodage inconnu \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-625">14012 (0x36BC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-626">L’identificateur de groupe d’encodage spécifié n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERREUR \_ SxS \_ \_ encodage inconnu**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-628">14013 (0x36BD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-629">L’encodage demandé n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERREUR \_ SxS \_ \_ URI d' \_ espace de noms XML non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-631">14014 (0x36BE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-632">Le manifeste contient une référence à un URI non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERREUR \_ SxS \_ la \_ dépendance du manifeste racine \_ n’est \_ pas \_ installée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-634">14015 (0x36BF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-635">Le manifeste d’application contient une référence à un assembly dépendant qui n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERREUR \_ SxS la dépendance du manifeste de la \_ feuille \_ n’est \_ \_ pas \_ installée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-637">14016 (0x36C0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-638">Le manifeste d’un assembly utilisé par l’application a une référence à un assembly dépendant qui n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERREUR \_ SxS \_ \_ attribut d’identité d’assembly non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-640">14017 (0x36C1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-641">Le manifeste contient un attribut pour l’identité de l’assembly qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERREUR \_ côte au \_ manifeste \_ manquant espace de \_ \_ noms par défaut requis \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-643">14018 (0x36C2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-644">Le manifeste ne contient pas la spécification d’espace de noms par défaut requise sur l’élément d’assembly.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERREUR \_ SxS \_ manifeste de l’espace de \_ \_ \_ noms par défaut requis non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-646">14019 (0x36C3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-647">Le manifeste a un espace de noms par défaut spécifié sur l’élément assembly, mais sa valeur n’est pas « urn : schemas-microsoft-com : ASM. v1 ».</span><span class="sxs-lookup"><span data-stu-id="ee4c6-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERREUR \_ SxS \_ \_ \_ chemin d’accès croisé du manifeste privé \_ \_ avec le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-649">14020 (0x36C4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-650">Le manifeste privé détecté a franchi un chemin d’accès avec un point d’analyse non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERREUR \_ SxS \_ nom de la dll dupliquée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-652">14021 (0x36C5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-653">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des fichiers portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERREUR \_ SxS \_ \_ nom de WINDOWCLASS dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-655">14022 (0x36C6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-656">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des classes de fenêtre portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERREUR \_ SxS \_ doublon \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-658">14023 (0x36C7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-659">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont les mêmes CLSID du serveur COM.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERREUR \_ SxS \_ en doublon d' \_ IID**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-661">14024 (0x36C8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-662">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des proxies pour les mêmes IID de l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERREUR \_ SxS \_ en double \_ TLBID (**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-664">14025 (0x36C9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-665">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont la même bibliothèque de types COM TLBIDs.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERREUR \_ SxS \_ en doublon \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-667">14026 (0x36CA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-668">Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont les mêmes ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERREUR \_ SxS \_ \_ nom d’assembly dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-670">14027 (0x36CB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-671">Au moins deux composants référencés directement ou indirectement par le manifeste d’application sont des versions différentes du même composant, ce qui n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERREUR \_ SxS \_ \_ incompatibilité de hachage de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-673">14028 (0x36CC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-674">Le fichier d’un composant ne correspond pas aux informations de vérification présentes dans le manifeste du composant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**erreur d’analyse de la \_ \_ stratégie SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-676">14029 (0x36CD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-677">Le manifeste de la stratégie contient une ou plusieurs erreurs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGQUOTE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-679">14030 (0x36CE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-680">Erreur d’analyse du manifeste : un littéral de chaîne était attendu, mais aucun caractère de guillemet d’ouverture n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERREUR \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-682">14031 (0x36CF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-683">Erreur d’analyse du manifeste : une syntaxe incorrecte a été utilisée dans un commentaire.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-685">14032 (0x36D0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-686">Erreur d’analyse du manifeste : un nom a été démarré avec un caractère non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-688">14033 (0x36D1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-689">Erreur d’analyse du manifeste : un nom contenait un caractère non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADCHARINSTRING**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-691">14034 (0x36D2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-692">Erreur d’analyse du manifeste : un littéral de chaîne contenait un caractère non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERREUR \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-694">14035 (0x36D3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-695">Erreur d’analyse du manifeste : syntaxe non valide pour une déclaration XML.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADCHARDATA**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-697">14036 (0x36D4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-698">Erreur d’analyse du manifeste : un caractère non valide a été trouvé dans le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-700">14037 (0x36D5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-701">Erreur d’analyse du manifeste : un espace blanc requis était manquant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERREUR \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-703">14038 (0x36D6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-704">Erreur d’analyse du manifeste : le caractère' > 'était attendu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-706">14039 (0x36D7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-707">Erreur d’analyse du manifeste : un point-virgule était attendu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-709">14040 (0x36D8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-710">Erreur d’analyse du manifeste : parenthèses non équilibrées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERREUR \_ SxS \_ XML \_ E \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-712">14041 (0x36D9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-713">Erreur d’analyse du manifeste : erreur interne.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ espace inattendu \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-715">14042 (0x36DA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-716">Erreur d’analyse du manifeste : un espace blanc n’est pas autorisé à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERREUR \_ SxS \_ XML \_ E \_ \_ encodage incomplet**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-718">14043 (0x36DB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-719">Erreur d’analyse du manifeste : la fin du fichier a atteint un État non valide pour l’encodage actuel.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERREUR \_ SxS \_ XML \_ E \_ manquant \_ parenthèse**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-721">14044 (0x36DC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-722">Erreur d’analyse du manifeste : parenthèses manquantes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERREUR \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-724">14045 (0x36DD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-725">Erreur d’analyse du manifeste : un guillemet simple ou double de fermeture ( \\ 'ou \\ ") est manquant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERREUR \_ SxS \_ XML \_ E \_ plusieurs \_ signes deux-points**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-727">14046 (0x36DE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-728">Erreur d’analyse du manifeste : plusieurs signes deux-points ne sont pas autorisés dans un nom.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERREUR \_ SxS \_ XML \_ E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-730">14047 (0x36DF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-731">Erreur d’analyse du manifeste : caractère non valide pour un chiffre décimal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERREUR \_ SxS \_ XML \_ E \_ hexadécimal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-733">14048 (0x36E0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-734">Erreur d’analyse du manifeste : caractère non valide pour un chiffre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERREUR \_ SxS \_ XML \_ E \_ Unicode non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-736">14049 (0x36E1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-737">Erreur d’analyse du manifeste : valeur de caractère Unicode non valide pour cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERREUR \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-739">14050 (0x36E2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-740">Erreur d’analyse du manifeste : espace blanc attendu ou' ? '.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-742">14051 (0x36E3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-743">Erreur d’analyse du manifeste : balise de fin non attendue à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-745">14052 (0x36E4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-746">Erreur d’analyse du manifeste : les balises suivantes n’ont pas été fermées : %1.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERREUR \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-748">14053 (0x36E5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-749">Erreur d’analyse du manifeste : attribut dupliqué.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERREUR \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-751">14054 (0x36E6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-752">Erreur d’analyse du manifeste : un seul élément de niveau supérieur est autorisé dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-754">14055 (0x36E7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-755">Erreur d’analyse du manifeste : non valide au niveau supérieur du document.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADXMLDECL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-757">14056 (0x36E8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-758">Erreur d’analyse du manifeste : déclaration XML non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGROOT**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-760">14057 (0x36E9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-761">Erreur d’analyse du manifeste : le document XML doit avoir un élément de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-763">14058 (0x36EA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-764">Erreur d’analyse du manifeste : fin de fichier inattendue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-766">14059 (0x36EB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-767">Erreur d’analyse du manifeste : les entités de paramètre ne peuvent pas être utilisées dans des déclarations de balisage dans un sous-ensemble interne.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-769">14060 (0x36EC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-770">Erreur d’analyse du manifeste : l’élément n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-772">14061 (0x36ED)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-773">Erreur d’analyse du manifeste : le caractère' > 'est manquant dans l’élément de fin.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-775">14062 (0x36EE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-776">Erreur d’analyse du manifeste : un littéral de chaîne n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-778">14063 (0x36EF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-779">Erreur d’analyse du manifeste : un commentaire n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-781">14064 (0x36F0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-782">Erreur d’analyse du manifeste : une déclaration n’a pas été fermée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-784">14065 (0x36F1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-785">Erreur d’analyse du manifeste : une section CDATA n’a pas été fermée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-787">14066 (0x36F2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-788">Erreur d’analyse du manifeste : le préfixe de l’espace de noms n’est pas autorisé à démarrer avec la chaîne réservée « xml ».</span><span class="sxs-lookup"><span data-stu-id="ee4c6-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDENCODING**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-790">14067 (0x36F3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-791">Erreur d’analyse du manifeste : le système ne prend pas en charge l’encodage spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDSWITCH**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-793">14068 (0x36F4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-794">Erreur d’analyse du manifeste : le passage de l’encodage actuel à l’encodage spécifié n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADXMLCASE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-796">14069 (0x36F5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-797">Erreur d’analyse du manifeste : le nom’XML’est réservé et doit être en minuscules.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERREUR \_ SxS \_ XML \_ E \_ non valide \_ autonome**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-799">14070 (0x36F6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-800">Erreur d’analyse du manifeste : l’attribut autonome doit avoir la valeur’Yes’ou’no'.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERREUR \_ SxS \_ XML \_ E \_ inattendu en mode \_ autonome**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-802">14071 (0x36F7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-803">Erreur d’analyse du manifeste : l’attribut autonome ne peut pas être utilisé dans des entités externes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERREUR \_ SxS \_ XML \_ E \_ version non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-805">14072 (0x36F8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-806">Erreur d’analyse du manifeste : numéro de version non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGEQUALS**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-808">14073 (0x36F9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-809">Erreur d’analyse du manifeste : signe égal manquant entre l’attribut et la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERREUR d’échec de la récupération de la \_ \_ protection SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-811">14074 (0x36FA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-812">Erreur de protection de l’assembly : impossible de récupérer l’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERREUR \_ de \_ clé publique de protection SxS \_ \_ \_ trop \_ brève**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-814">14075 (0x36FB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-815">Erreur de protection de l’assembly : la clé publique d’un assembly est trop petite pour être autorisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERREUR \_ du \_ catalogue de protection SxS \_ \_ non \_ valide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-817">14076 (0x36FC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-818">Erreur de protection de l’assembly : le catalogue d’un assembly n’est pas valide ou ne correspond pas au manifeste de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERREUR \_ SxS \_ untranslateable \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-820">14077 (0x36FD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-821">Un HRESULT n’a pas pu être traduit en code d’erreur Win32 correspondant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERREUR \_ SxS \_ fichier du catalogue de protection \_ \_ \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-823">14078 (0x36FE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-824">Erreur de protection de l’assembly : le catalogue d’un assembly est manquant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERREUR \_ SxS \_ \_ attribut d' \_ identité d’assembly manquant \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-826">14079 (0x36FF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-827">L’identité d’assembly fournie ne contient pas un ou plusieurs attributs qui doivent être présents dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERREUR \_ SxS \_ \_ nom d' \_ attribut d’identité d’assembly non \_ valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-830">L’identité d’assembly fournie a un ou plusieurs noms d’attribut qui contiennent des caractères non autorisés dans les noms XML.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERREUR de l' \_ \_ assembly SxS \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-833">L’assembly référencé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERREUR \_ SxS \_ , \_ pile d’activation endommagée \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-836">La pile d’activation du contexte d’activation pour le thread d’exécution en cours d’exécution est endommagée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERREUR \_ SxS d' \_ altération**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-839">Les métadonnées d’isolation d’application pour ce processus ou ce thread sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERREUR \_ SxS \_ la \_ désactivation précoce**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-842">Le contexte d’activation en cours de désactivation n’est pas le contexte activé le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERREUR \_ SxS \_ \_ désactivation non valide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-845">Le contexte d’activation en cours de désactivation n’est pas actif pour le thread d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERREUR \_ SxS \_ plusieurs \_ désactivations**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-848">Le contexte d’activation en cours de désactivation a déjà été désactivé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERREUR \_ d' \_ arrêt de processus SxS \_ \_ demandée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-851">Un composant utilisé par la fonctionnalité d’isolation a demandé l’arrêt du processus.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERREUR \_ côte \_ à \_ l’activation de la libération \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-854">Un composant en mode noyau publie une référence sur un contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERREUR \_ SxS \_ \_ contexte d’activation par défaut du système SxS \_ \_ \_ vide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-857">Impossible de générer le contexte d’activation de l’assembly par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERREUR \_ SxS \_ \_ valeur d' \_ attribut d’identité non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-859">14090 (0x370A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-860">La valeur d’un attribut dans une identité n’est pas comprise dans la plage autorisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERREUR \_ SxS \_ \_ nom d' \_ attribut d’identité non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-862">14091 (0x370B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-863">Le nom d’un attribut dans une identité n’est pas compris dans la plage légale.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERREUR \_ SxS- \_ attribut d’identité \_ en double \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-865">14092 (0x370C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-866">Une identité contient deux définitions pour le même attribut.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERREUR \_ SxS \_ \_ erreur d’analyse \_ de l’identité**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-868">14093 (0x370D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-869">La chaîne d’identité est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-869">The identity string is malformed.</span></span> <span data-ttu-id="ee4c6-870">Cela peut être dû à une virgule de fin, à plus de deux attributs sans nom, à un nom d’attribut manquant ou à une valeur d’attribut manquante.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERREUR \_ de \_ chaîne de substitution incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-872">14094 (0x370E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-873">Une chaîne contenant du contenu substitué localisé est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="ee4c6-874">Le signe dollar ($) a été suivi d’un autre signe dollar ou d’un autre signe dollar ou bien la parenthèse droite d’une substitution est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERREUR \_ SxS \_ \_ jeton de \_ clé \_ publique incorrect**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-876">14095 (0x370F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-877">Le jeton de clé publique ne correspond pas à la clé publique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERREUR de \_ chaîne de substitution non mappée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-880">Aucune chaîne de substitution n’a été mappée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERREUR \_ SxS \_ assembly \_ non \_ verrouillé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-882">14097 (0x3711)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-883">Le composant doit être verrouillé avant d’effectuer la demande.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERREUR \_ du \_ magasin de composants SxS \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-886">Le magasin de composants a été endommagé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERREUR \_ \_ échec du programme d’installation avancé \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-889">Un programme d’installation avancé a échoué lors de l’installation ou de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERREUR \_ d' \_ incompatibilité d’encodage XML \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-892">L’encodage de caractères dans la déclaration XML ne correspondait pas à l’encodage utilisé dans le document.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERREUR \_ SxS \_ identité du manifeste, \_ \_ \_ mais \_ contenu \_ différent**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-895">Les identités des manifestes sont identiques, mais leur contenu est différent.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERREUR \_ SxS \_ différente des identités \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-898">Les identités des composants sont différentes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERREUR \_ SxS l' \_ assembly \_ n’est \_ pas \_ un \_ déploiement**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-901">L’assembly n’est pas un déploiement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERREUR \_ SxS \_ fichier \_ ne \_ faisant pas partie \_ de l' \_ assembly**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-904">Le fichier ne fait pas partie de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERREUR \_ SxS le \_ manifeste est \_ trop \_ volumineux**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-907">La taille du manifeste dépasse la valeur maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERREUR \_ SxS \_ paramètre \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-909">14106 (0x371A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-910">Le paramètre n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERREUR \_ SxS \_ transaction \_ Closure \_ incomplète**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-912">14107 (0x371B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-913">Un ou plusieurs membres requis de la transaction ne sont pas présents.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERREUR \_ SMI \_ primitive le \_ programme d’installation \_ a échoué**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-915">14108 (0x371C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-916">Le programme d’installation primitif de SMI a échoué lors de l’installation ou de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**échec de la \_ commande générique d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-918">14109 (0x371D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-919">Un exécutable de commande générique a retourné un résultat qui indique un échec.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERREUR \_ de \_ hachage du fichier SxS \_ \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-921">14110 (0x371E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-922">Il manque des informations de vérification de fichier dans le manifeste d’un composant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERREUR \_ evt \_ \_ chemin de canal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-924">15000 (0x3A98)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-925">Le chemin d’accès au canal spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERREUR \_ evt \_ requête non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-927">15001 (0x3A99)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-928">La requête spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERREUR \_ evt \_ métadonnées du serveur de publication \_ \_ \_ introuvables**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-930">15002 (0x3A9A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-931">Les métadonnées du serveur de publication sont introuvables dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**le \_ modèle d’événement d’erreur evt est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-933">15003 (0x3A9B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-934">Le modèle d’une définition d’événement est introuvable dans la ressource (erreur = %1).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERREUR \_ evt \_ \_ nom d’éditeur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-936">15004 (0x3A9C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-937">Le nom du serveur de publication spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERREUR \_ evt \_ \_ données d’événement non valides \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-939">15005 (0x3A9D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-940">Les données d’événement générées par le serveur de publication ne sont pas compatibles avec la définition du modèle d’événement dans le manifeste de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERREUR \_ de \_ canal \_ evt \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-942">15007 (0x3A9F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-943">Le canal spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-943">The specified channel could not be found.</span></span> <span data-ttu-id="ee4c6-944">Vérifiez la configuration du canal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERREUR \_ evt \_ \_ texte XML mal formé \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-946">15008 (0x3AA0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-947">Le texte XML spécifié n’est pas correctement formé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="ee4c6-948">Pour plus d’informations, consultez erreur étendue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERREUR \_ evt \_ abonnement \_ au \_ \_ canal direct**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-950">15009 (0x3AA1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-951">L’appelant tente de s’abonner à un canal direct qui n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="ee4c6-952">Les événements d’un canal direct accèdent directement à un fichier journal et ne peuvent pas être abonnés à.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erreur de configuration de l’erreur \_ evt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-954">15010 (0x3AA2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-955">Erreur de configuration.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERREUR \_ evt \_ résultat de la requête \_ \_ obsolète**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-957">15011 (0x3AA3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-958">Le résultat de la requête est obsolète/non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-958">The query result is stale / invalid.</span></span> <span data-ttu-id="ee4c6-959">Cela peut être dû au fait que le journal est effacé ou basculé après la création du résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="ee4c6-960">Les utilisateurs doivent gérer ce code en libérant l’objet de résultat de la requête et en réémettant la requête.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERREUR \_ evt \_ résultat de la requête- \_ \_ position non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-962">15012 (0x3AA4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-963">Le résultat de la requête est actuellement à une position non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERREUR \_ evt \_ non- \_ validation de \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-965">15013 (0x3AA5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-966">Le MSXML inscrit ne prend pas en charge la validation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERREUR \_ evt \_ Filter \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-968">15014 (0x3AA6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-969">Une expression ne peut être suivie que par une modification de l’opération d’étendue si elle correspond à un ensemble de nœuds et qu’elle ne fait pas déjà partie d’une autre modification de l’opération d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERREUR \_ evt \_ Filter \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-971">15015 (0x3AA7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-972">Impossible d’effectuer une opération d’étape à partir d’un terme qui ne représente pas un ensemble d’éléments.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERREUR \_ evt \_ Filter \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-974">15016 (0x3AA8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-975">Les arguments côté gauche des opérateurs binaires doivent être des attributs, des nœuds ou des variables et les arguments de la partie droite doivent être des constantes.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERREUR \_ evt \_ Filter \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-977">15017 (0x3AA9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-978">Une opération d’étape doit impliquer un test de nœud ou, dans le cas d’un prédicat, une expression algébrique sur laquelle tester chaque nœud de l’ensemble de nœuds identifié par l’ensemble de nœuds précédent peut être évaluée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERREUR \_ evt \_ Filter \_ INVTYPE**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-980">15018 (0x3AAA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-981">Ce type de données n’est actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERREUR \_ evt \_ Filter \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-983">15019 (0x3AAB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-984">Une erreur de syntaxe s’est produite à la position %1 ! d !.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERREUR \_ evt \_ Filter \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-986">15020 (0x3AAC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-987">Cet opérateur n’est pas pris en charge par cette implémentation du filtre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERREUR \_ evt \_ Filter \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-989">15021 (0x3AAD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-990">Le jeton rencontré était inattendu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERREUR \_ evt \_ opération non valide \_ \_ sur le \_ \_ canal direct activé \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-992">15022 (0x3AAE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-993">L’opération demandée ne peut pas être effectuée sur un canal direct activé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="ee4c6-994">Le canal doit d’abord être désactivé avant d’effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERREUR \_ evt \_ \_ valeur de \_ propriété de canal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-996">15023 (0x3AAF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-997">Propriété de canal %1 ! s !</span><span class="sxs-lookup"><span data-stu-id="ee4c6-997">Channel property %1!s!</span></span> <span data-ttu-id="ee4c6-998">contient une valeur non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-998">contains invalid value.</span></span> <span data-ttu-id="ee4c6-999">Le type de la valeur n’est pas valide, est en dehors de la plage valide, ne peut pas être mis à jour ou n’est pas pris en charge par ce type de canal.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERREUR \_ evt \_ valeur de la \_ propriété Publisher non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1001">15024 (0x3AB0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1002">Propriété du serveur de publication %1 ! s !</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1002">Publisher property %1!s!</span></span> <span data-ttu-id="ee4c6-1003">contient une valeur non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1003">contains invalid value.</span></span> <span data-ttu-id="ee4c6-1004">Le type de la valeur n’est pas valide, est en dehors de la plage valide, ne peut pas être mis à jour ou n’est pas pris en charge par ce type de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERREUR \_ \_ Impossible d' \_ \_ activer le canal evt**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1006">15025 (0x3AB1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1007">L’activation du canal échoue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERREUR \_ de \_ filtre evt \_ trop \_ complexe**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1009">15026 (0x3AB2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1010">L’expression XPath a dépassé la complexité prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="ee4c6-1011">Symplifyz-le ou fractionnez-le en deux ou plusieurs expressions simples.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MESSAGE d’erreur \_ evt \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1013">15027 (0x3AB3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1014">la ressource de message est présente, mais le message est introuvable dans la table de chaînes/messages.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERREUR \_ evt \_ ID de message \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1016">15028 (0x3AB4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1017">L’ID de message du message souhaité est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERREUR \_ evt \_ - \_ Insérer une valeur non résolue \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1019">15029 (0x3AB5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1020">La chaîne de substitution pour l’instruction INSERT index (%1) est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERREUR \_ evt \_ - \_ Insérer un paramètre non résolu \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1022">15030 (0x3AB6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1023">La chaîne de description de la référence de paramètre (%1) est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERREUR \_ evt \_ nombre maximal d' \_ insertions \_ atteint**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1025">15031 (0x3AB7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1026">Le nombre maximal de remplacements a été atteint.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERREUR \_ evt \_ définition de l’événement \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1028">15032 (0x3AB8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1029">La définition de l’événement est introuvable pour l’ID d’événement (%1).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERREUR \_ evt \_ message \_ local \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1031">15033 (0x3AB9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1032">La ressource spécifique aux paramètres régionaux pour le message souhaité n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERREUR \_ evt \_ version \_ trop \_ ancienne**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1034">15034 (0x3ABA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1035">La ressource est trop ancienne pour être compatible.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERREUR \_ evt \_ version \_ insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1037">15035 (0x3ABB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1038">La ressource est trop nouvelle pour être compatible.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERREUR \_ evt \_ Impossible \_ d’ouvrir le \_ canal \_ de la \_ requête**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1040">15036 (0x3ABC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1041">Le canal à l’index %1 ! d !</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1041">The channel at index %1!d!</span></span> <span data-ttu-id="ee4c6-1042">Impossible d’ouvrir la requête.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERREUR \_ evt serveur de \_ publication \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1044">15037 (0x3ABD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1045">Le serveur de publication a été désactivé et sa ressource n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="ee4c6-1046">Cela se produit généralement lorsque le serveur de publication est en cours de désinstallation ou de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERREUR \_ \_ de filtre \_ evt \_ hors \_ limites**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1048">15038 (0x3ABE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1049">Tentative de création d’un type numérique qui est en dehors de sa plage valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERREUR \_ \_ Impossible d' \_ \_ activer l’abonnement EC**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1051">15080 (0x3AE8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1052">L’activation de l’abonnement échoue.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERREUR \_ de \_ journalisation EC \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1054">15081 (0x3AE9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1055">Le journal de l’abonnement est dans un état désactivé et ne peut pas être utilisé pour transférer des événements à.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="ee4c6-1056">Le journal doit d’abord être activé pour que l’abonnement puisse être activé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERREUR \_ de \_ transfert circulaire ce \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1058">15082 (0x3AEA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1059">Lors du transfert d’événements de l’ordinateur local à lui-même, la requête de l’abonnement ne peut pas contenir le journal cible de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERREUR \_ EC \_ CREDSTORE \_ Full**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1061">15083 (0x3AEB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1062">La Banque d’informations d’identification utilisée pour enregistrer les informations d’identification est complète.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERREUR \_ EC \_ \_ non \_ trouvé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1064">15084 (0x3AEC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1065">Les informations d’identification utilisées par cet abonnement sont introuvables dans la Banque d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERREUR \_ EC \_ non \_ active \_ Channel**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1067">15085 (0x3AED)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1068">Aucun canal actif n’a été trouvé pour la requête.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_fichier MUI \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1070">15100 (0x3AFC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1071">Le chargeur de ressources n’a pas pu trouver le fichier MUI.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERREUR \_ de \_ fichier non valide MUI \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1073">15101 (0x3AFD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1074">Le chargeur de ressources n’a pas pu charger le fichier MUI car le fichier n’a pas réussi à réussir la validation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERREUR \_ de \_ \_ configuration RC non valide pour MUI \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1076">15102 (0x3AFE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1077">Le manifeste RC est endommagé avec des données de garbage collection ou une version non prise en charge ou un élément requis manquant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERREUR \_ MUI \_ \_ nom de paramètres régionaux non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1079">15103 (0x3AFF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1080">Le manifeste RC a un nom de culture non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERREUR \_ ULTIMATEFALLBACK nom de l’interface MUI \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1082">15104 (0x3B00)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1083">Le manifeste RC a un nom de ultimatefallback non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERREUR lors du chargement du \_ \_ fichier MUI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1085">15105 (0x3B01)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1086">Le cache du chargeur de ressources n’a pas d’entrée MUI chargée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**arrêt de l' \_ énumération des ressources d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1088">15106 (0x3B02)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1089">L’utilisateur a arrêté l’énumération des ressources.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERREUR \_ MUI \_ INTLSETTINGS \_ UILANG \_ non \_ installé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1091">15107 (0x3B03)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1092">Échec de l’installation de la langue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERREUR \_ MUI \_ INTLSETTINGS \_ \_ nom de paramètres régionaux non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1094">15108 (0x3B04)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1095">Échec de l’installation des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERREUR \_ MRM \_ Runtime \_ sans \_ ressource par défaut \_ ou \_ neutre \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1097">15110 (0x3B06)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1098">Une ressource n’a pas de valeur par défaut ou neutre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERREUR \_ MRM \_ fichier priconfig non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1100">15111 (0x3B07)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1101">Fichier de configuration PRI non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERREUR \_ MRM \_ \_ type de fichier non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1103">15112 (0x3B08)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1104">Type de fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERREUR \_ MRM \_ \_ qualificateur inconnu**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1106">15113 (0x3B09)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1107">Qualificateur inconnu.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERREUR \_ MRM \_ valeur de qualificateur non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1109">15114 (0x3B0A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1110">Valeur de qualificateur non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERREUR \_ MRM \_ aucun \_ candidat**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1112">15115 (0x3B0B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1113">Aucun candidat n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERREUR \_ MRM \_ aucune \_ correspondance \_ ou \_ candidat par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1115">15116 (0x3B0C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1116">ResourceMap ou NamedResource a un élément qui n’a pas de ressource par défaut ou neutre..</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type de ressource MRM \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1118">15117 (0x3B0D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1119">Type de ResourceCandidate non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERREUR \_ MRM \_ \_ nom de mappage dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1121">15118 (0x3B0E)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1122">Mappage de ressources en double.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERREUR \_ MRM de l' \_ entrée dupliquée \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1124">15119 (0x3B0F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1125">Entrée dupliquée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERREUR \_ MRM \_ \_ identificateur de ressource non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1127">15120 (0x3B10)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1128">Identificateur de ressource non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**erreur MRM le chemin d’erreur est \_ \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1130">15121 (0x3B11)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1131">FilePath trop long.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERREUR \_ MRM \_ type de répertoire non pris en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1133">15122 (0x3B12)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1134">Type de répertoire non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERREUR \_ MRM \_ \_ fichier PRI non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1136">15126 (0x3B16)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1137">Fichier PRI non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERREUR \_ MRM \_ nommée \_ ressource \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1139">15127 (0x3B17)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1140">NamedResource introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERREUR \_ de \_ mappage de MRM \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1142">15135 (0x3B1F)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1143">ResourceMap introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERREUR \_ MRM \_ type de profil non pris en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1145">15136 (0x3B20)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1146">Type de profil MRT non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERREUR \_ MRM \_ opérateur de qualificateur non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1148">15137 (0x3B21)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1149">Opérateur de qualificateur non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERREUR \_ MRM \_ \_ valeur du qualificateur indéterminé \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1151">15138 (0x3B22)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1152">Impossible de déterminer la valeur du qualificateur ou la valeur du qualificateur n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERREUR \_ de \_ fusion automatique MRM \_ activée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1154">15139 (0x3B23)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1155">La fusion automatique est activée dans le fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERREUR \_ MRM \_ trop \_ de \_ ressources**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1157">15140 (0x3B24)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1158">Trop de ressources définies pour le package.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERREUR \_ MCA \_ \_ chaîne de fonctionnalités non valides \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1160">15200 (0x3B60)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1161">Le moniteur a renvoyé une chaîne de fonctionnalités DDC/CI qui n’était pas conforme à la spécification ACCESS. bus 3,0, DDC/CI 1,1 ou MCCS 2 révision 1.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERREUR \_ MCA \_ \_ version du VCP non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1163">15201 (0x3B61)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1164">Le code VCP de la version du moniteur VCP (0xDF) a retourné une valeur de version non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**une erreur \_ MCA \_ Monitor enfreint la \_ \_ \_ spécification MCCS**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1166">15202 (0x3B62)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1167">Le moniteur n’est pas conforme à la spécification MCCS qu’il prétend prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de version de MCA MCCS \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1169">15203 (0x3B63)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1170">La version MCCS de la fonctionnalité MCCS ver d’un moniteur \_ ne correspond pas à la version MCCS que le moniteur signale lorsque le code VCP version (0xDF) VCP est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERREUR \_ de \_ \_ version MCCS non prise en charge par MCA \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1172">15204 (0x3B64)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1173">L’API de configuration de l’analyse fonctionne uniquement avec les analyses qui prennent en charge la spécification MCCS 1,0, la spécification MCCS 2,0 ou la spécification MCCS 2,0 révision 1.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERREUR \_ MCA erreur \_ interne \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1175">15205 (0x3B65)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1176">Une erreur de l’API de configuration de l’analyse interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERREUR \_ MCA \_ type de technologie non valide \_ \_ \_ retourné**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1178">15206 (0x3B66)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1179">Le moniteur a retourné un type de technologie d’analyse non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="ee4c6-1180">CRT, plasma et LCD (TFT) sont des exemples de types de technologies de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="ee4c6-1181">Cette erreur signifie que le moniteur n’est pas conforme à la spécification MCCS 2,0 ou MCCS 2,0 révision 1.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERREUR \_ MCA \_ température de couleur non prise en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1183">15207 (0x3B67)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1184">L’appelant de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) a spécifié une température de couleur que le moniteur en cours ne prenait pas en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="ee4c6-1185">Cette erreur signifie que le moniteur n’est pas conforme à la spécification MCCS 2,0 ou MCCS 2,0 révision 1.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERREUR \_ de \_ périphérique système ambigu \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1187">15250 (0x3B92)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1188">L’appareil système demandé ne peut pas être identifié en raison de plusieurs périphériques indifférenciables susceptibles de correspondre aux critères d’identification.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_périphérique système d’erreur \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1190">15299 (0x3BC3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1191">Le périphérique système demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**hachage d’erreur \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1193">15300 (0x3BC4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1194">La génération de hachage pour la version de hachage et le type de hachage spécifiés n’est pas activée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_hachage d' \_ erreur \_ absent**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1196">15301 (0x3BC5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1197">Le hachage demandé à partir du serveur n’est pas disponible ou n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERREUR \_ \_ fournisseur IC \_ secondaire \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1199">15321 (0x3BD9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1200">L’instance de contrôleur d’interruption secondaire qui gère l’interruption spécifiée n’est pas inscrite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERREUR \_ d' \_ informations du client GPIO \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1202">15322 (0x3BDA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1203">Les informations fournies par le pilote du client GPIO ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERREUR \_ \_ version GPIO \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1205">15323 (0x3BDB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1206">La version spécifiée par le pilote du client GPIO n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERREUR \_ GPIO \_ \_ paquet d’inscription non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1208">15324 (0x3BDC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1209">Le paquet d’inscription fourni par le pilote du client GPIO n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERREUR de l' \_ \_ opération GPIO \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1211">15325 (0x3BDD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1212">L’opération demandée n’est pas prise en charge pour le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERREUR \_ GPIO \_ mode de \_ connexion incompatible \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1214">15326 (0x3BDE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1215">Le mode de connexion demandé est en conflit avec un mode existant sur une ou plusieurs des broches spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERREUR \_ GPIO \_ interruption \_ déjà \_ démasquée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1217">15327 (0x3BDF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1218">L’interruption demandée pour être démasquée n’est pas masquée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**l’erreur \_ ne peut pas \_ basculer \_ RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1220">15400 (0x3C28)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1221">Le commutateur de niveau d’exécution demandé ne peut pas être exécuté correctement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERREUR \_ de \_ paramètre RUNLEVEL non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1223">15401 (0x3C29)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1224">Le service a un paramètre de niveau d’exécution non valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="ee4c6-1225">Le niveau d’exécution d’un service ne doit pas être supérieur au niveau d’exécution de ses services dépendants.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERREUR \_ de \_ \_ délai d’attente du commutateur RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1227">15402 (0x3C2A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1228">Le commutateur de niveau d’exécution demandé ne peut pas être exécuté correctement, car un ou plusieurs services ne s’arrêteront pas ou ne redémarreront pas dans le délai spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERREUR \_ RUNLEVEL \_ du commutateur de \_ l’agent \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1230">15403 (0x3C2B)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1231">Un agent de commutation au niveau de l’exécution n’a pas répondu dans le délai imparti.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERREUR \_ \_ de commutateur RUNLEVEL \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1233">15404 (0x3C2C)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1234">Un commutateur au niveau de l’exécution est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_échec du \_ \_ démarrage automatique des services d’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1236">15405 (0x3C2D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1237">Un ou plusieurs services n’ont pas pu démarrer au cours de la phase de démarrage du service d’un commutateur de niveau d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERREUR d’arrêt de la \_ \_ tâche com \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1239">15501 (0x3C8D)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1240">La demande d’arrêt de la tâche ne peut pas être effectuée immédiatement, car la tâche a besoin de plus de temps pour s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERREUR d’installation de l' \_ \_ ouverture du \_ package \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1242">15600 (0x3CF0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1243">Impossible d’ouvrir le package.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERREUR lors de l' \_ installation du \_ package \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1245">15601 (0x3CF1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1246">Le package est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERREUR d’installation d’un \_ \_ package non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1248">15602 (0x3CF2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1249">Les données du package ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**échec de la résolution de l’erreur d’installation de la \_ \_ \_ dépendance \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1251">15603 (0x3CF3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1252">Échec des mises à jour du package, de la dépendance ou de la validation des conflits.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERREUR \_ \_ d’installation \_ de \_ l' \_ espace disque insuffisant**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1254">15604 (0x3CF4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1255">L’espace disque est insuffisant sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="ee4c6-1256">Libérez de l’espace et réessayez.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERREUR lors de l’installation d’une \_ \_ \_ défaillance réseau**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1258">15605 (0x3CF5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1259">Un problème est survenu lors du téléchargement de votre produit.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERREUR \_ \_ d’échec d’enregistrement d’installation \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1261">15606 (0x3CF6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1262">Le package n’a pas pu être inscrit.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERREUR \_ d’installation de \_ l’échec de l’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1264">15607 (0x3CF7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1265">L’inscription du package n’a pas pu être annulée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERREUR d' \_ installation \_ Annuler**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1267">15608 (0x3CF8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1268">L’utilisateur a annulé la demande d’installation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**échec de l' \_ installation \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1270">15609 (0x3CF9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1271">Échec de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1271">Install failed.</span></span> <span data-ttu-id="ee4c6-1272">Veuillez contacter votre fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**échec de la suppression de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1274">15610 (0x3CFA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1275">Échec de la suppression.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1275">Removal failed.</span></span> <span data-ttu-id="ee4c6-1276">Veuillez contacter votre fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**le \_ package d’erreurs \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1278">15611 (0x3CFB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1279">Le package fourni est déjà installé, et la réinstallation du package a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="ee4c6-1280">Pour plus d’informations, consultez le journal des événements AppXDeployment-Server.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERREUR \_ nécessitant une \_ Correction**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1282">15612 (0x3CFC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1283">Impossible de démarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1283">The application cannot be started.</span></span> <span data-ttu-id="ee4c6-1284">Essayez de réinstaller l’application pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERREUR lors de l’échec de l' \_ installation des \_ composants requis \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1286">15613 (0x3CFD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1287">Un composant requis pour une installation n’a pas pu être satisfait.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**DÉPÔT de packages d’erreurs \_ \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1289">15614 (0x3CFE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1290">Le référentiel du package est endommagé.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERREUR lors de l’installation de la \_ \_ stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1292">15615 (0x3CFF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1293">Pour installer cette application, vous avez besoin d’une licence de développeur Windows ou d’un système compatible chargement.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_ \_ mise à jour du package d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1295">15616 (0x3D00)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1296">L’application ne peut pas être démarrée car elle est en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERREUR \_ \_ de déploiement bloqué \_ par la \_ stratégie**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1298">15617 (0x3D01)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1299">L’opération de déploiement de package est bloquée par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="ee4c6-1300">Contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_packages \_ d’erreurs en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1302">15618 (0x3D02)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1303">Le package n’a pas pu être installé car les ressources qu’il modifie sont actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**fichier de récupération d’erreur \_ \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1305">15619 (0x3D03)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1306">Le package n’a pas pu être récupéré car les données nécessaires à la récupération ont été endommagées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERREUR \_ de \_ signature intermédiaire non valide \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1308">15620 (0x3D04)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1309">La signature n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1309">The signature is invalid.</span></span> <span data-ttu-id="ee4c6-1310">Pour s’inscrire en mode développeur, AppxSignature. p7x et AppxBlockMap.xml doivent être valides ou ne doivent pas être présents.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERREUR lors de \_ la suppression du \_ \_ magasin APPLICATIONDATA existant \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1312">15621 (0x3D05)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1313">Une erreur s’est produite lors de la suppression des données d’application précédemment existantes du package.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERREUR lors de l’installation du package à une \_ \_ \_ version antérieure**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1315">15622 (0x3D06)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1316">Le package n’a pas pu être installé car une version plus récente de ce package est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**le \_ système d’erreur \_ doit être mis à \_ jour**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1318">15623 (0x3D07)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1319">Une erreur a été détectée dans un fichier binaire système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="ee4c6-1320">Essayez d’actualiser le PC pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**erreur d’erreur d' \_ \_ intégrité AppX \_ \_ CLR \_ Ngen**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1322">15624 (0x3D08)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1323">Un fichier binaire NGEN CLR endommagé a été détecté sur le système.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_fichier de résilience des erreurs \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1325">15625 (0x3D09)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1326">Impossible de reprendre l’opération, car les données nécessaires à la récupération ont été endommagées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERREUR lors de l' \_ installation du \_ service pare-feu \_ \_ \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1328">15626 (0x3D0A)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1329">Le package n’a pas pu être installé car le service pare-feu Windows n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="ee4c6-1330">Activez le service pare-feu Windows, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_erreur APPMODEL \_ aucun \_ package**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1332">15700 (0x3D54)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1333">Le processus n’a pas d’identité de package.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Runtime du package d’erreurs APPMODEL \_ \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1335">15701 (0x3D55)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1336">Les informations d’exécution du package sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_identité du package d’erreur APPMODEL \_ \_ \_ endommagée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1338">15702 (0x3D56)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1339">L’identité du package est endommagée.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**erreur APPMODEL- \_ \_ aucune \_ application**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1341">15703 (0x3D57)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1342">Le processus n’a pas d’identité d’application.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_échec du \_ magasin de chargement d’état d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1344">15800 (0x3DB8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1345">Échec du chargement du magasin d’État.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**échec de la récupération de la version de l’état d’erreur \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1347">15801 (0x3DB9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1348">Échec de la récupération de la version d’état de l’application.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**échec de la version du jeu d' \_ État d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1350">15802 (0x3DBA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1351">Échec de la définition de la version d’état de l’application.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_échec de \_ la \_ réinitialisation structurée d’état d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1353">15803 (0x3DBB)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1354">Échec de la réinitialisation de l’État structuré de l’application.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**échec de l’état d’erreur d' \_ \_ ouverture du \_ conteneur \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1356">15804 (0x3DBC)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1357">Le gestionnaire d’État n’a pas pu ouvrir le conteneur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**échec de la \_ \_ création du \_ conteneur d’état \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1359">15805 (0x3DBD)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1360">Le gestionnaire d’État n’a pas pu créer le conteneur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**échec de la suppression de l’état d’erreur du \_ \_ \_ conteneur \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1362">15806 (0x3DBE)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1363">Le gestionnaire d’État n’a pas pu supprimer le conteneur.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_échec du \_ paramètre de lecture \_ \_ de l’état d’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1365">15807 (0x3DBF)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1366">Le gestionnaire d’État n’a pas pu lire le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_échec du \_ paramètre d’écriture d’état d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1368">15808 (0x3DC0)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1369">Le gestionnaire d’État n’a pas pu écrire le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_échec du \_ paramètre de suppression \_ \_ de l’état d’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1371">15809 (0x3DC1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1372">Le gestionnaire d’État n’a pas pu supprimer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_échec du \_ paramètre de requête d’état d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1374">15810 (0x3DC2)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1375">Le gestionnaire d’État n’a pas pu interroger le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_échec de \_ lecture \_ du \_ paramètre composite \_ de l’état d’erreur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1377">15811 (0x3DC3)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1378">Le gestionnaire d’État n’a pas pu lire le paramètre composite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**échec de l’écriture de l' \_ état \_ \_ composite du paramètre composite \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1380">15812 (0x3DC4)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1381">Le gestionnaire d’État n’a pas pu écrire le paramètre composite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**échec de l’énumération de l’état d’erreur du \_ \_ \_ conteneur \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1383">15813 (0x3DC5)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1384">Le gestionnaire d’État n’a pas pu énumérer les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**échec de l' \_ \_ énumération de l’état d' \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1386">15814 (0x3DC6)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1387">Le gestionnaire d’État n’a pas pu énumérer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_limite de \_ taille de valeur de paramètre composite d’état d’erreur \_ \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1389">15815 (0x3DC7)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1390">La taille de la valeur du paramètre composite du gestionnaire d’État a dépassé la limite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**limite de taille de valeur de paramètre d’état d’erreur \_ \_ \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1392">15816 (0x3DC8)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1393">La taille de la valeur du paramètre du gestionnaire d’État a dépassé la limite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**paramètre d’état d’erreur- \_ \_ limite de taille de \_ nom \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1395">15817 (0x3DC9)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1396">La longueur du nom du paramètre du gestionnaire d’État a dépassé la limite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**le \_ nom du conteneur d’état d’erreur \_ \_ \_ \_ a dépassé la limite de taille \_**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1398">15818 (0x3DCA)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1399">La longueur du nom de conteneur du gestionnaire d’État a dépassé la limite.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee4c6-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API d’erreur \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4c6-1401">15841 (0x3DE1)</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="ee4c6-1402">Cette API ne peut pas être utilisée dans le contexte du type d’application de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee4c6-1403">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1403">Requirements</span></span>



| <span data-ttu-id="ee4c6-1404">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1404">Requirement</span></span> | <span data-ttu-id="ee4c6-1405">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4c6-1406">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4c6-1407">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee4c6-1408">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4c6-1409">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee4c6-1410">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4c6-1411"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4c6-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4c6-1412">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4c6-1413">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="ee4c6-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
