---
description: Décrit les codes d’erreur 9000-11999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Codes d’erreur système (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748380"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="c5120-103">Codes d’erreur système (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="c5120-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="c5120-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="c5120-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="c5120-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c5120-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="c5120-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 9000 à 11999).</span><span class="sxs-lookup"><span data-stu-id="c5120-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="c5120-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="c5120-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="c5120-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="c5120-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="c5120-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**erreur DNS erreur de \_ \_ \_ format RCODE \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="c5120-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-111">Le serveur DNS ne peut pas interpréter le format.</span><span class="sxs-lookup"><span data-stu-id="c5120-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**erreur DNS- \_ \_ \_ défaillance du serveur RCODE \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-113">9002 (0x232A)</span><span class="sxs-lookup"><span data-stu-id="c5120-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-114">Échec du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**erreur DNS erreur de \_ \_ \_ nom RCODE \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-116">9003 (0x232B)</span><span class="sxs-lookup"><span data-stu-id="c5120-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-117">Le nom DNS n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_erreur DNS \_ RCODE \_ non \_ implémentée**</span><span class="sxs-lookup"><span data-stu-id="c5120-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-119">9004 (0x232C)</span><span class="sxs-lookup"><span data-stu-id="c5120-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-120">Demande DNS non prise en charge par le serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="c5120-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_erreur DNS \_ RCODE \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="c5120-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-122">9005 (0x232D)</span><span class="sxs-lookup"><span data-stu-id="c5120-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-123">Opération DNS refusée.</span><span class="sxs-lookup"><span data-stu-id="c5120-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_erreur DNS \_ RCODE \_ YXDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="c5120-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-125">9006 (0x232E)</span><span class="sxs-lookup"><span data-stu-id="c5120-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-126">Le nom DNS qui ne devrait pas exister existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c5120-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_erreur DNS \_ RCODE \_ YXRRSET**</span><span class="sxs-lookup"><span data-stu-id="c5120-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-128">9007 (0x232F)</span><span class="sxs-lookup"><span data-stu-id="c5120-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-129">Il n’existe pas d’ensemble de RR DNS qui ne devrait pas exister.</span><span class="sxs-lookup"><span data-stu-id="c5120-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_erreur DNS \_ RCODE \_ NXRRSET**</span><span class="sxs-lookup"><span data-stu-id="c5120-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="c5120-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-132">L’ensemble de RR DNS qui devrait exister n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_erreur DNS \_ RCODE \_ NOTAUTH**</span><span class="sxs-lookup"><span data-stu-id="c5120-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="c5120-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-135">Serveur DNS ne faisant pas autorité pour la zone.</span><span class="sxs-lookup"><span data-stu-id="c5120-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_erreur DNS \_ RCODE \_ NOTZONE**</span><span class="sxs-lookup"><span data-stu-id="c5120-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="c5120-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-138">Le nom DNS dans Update ou PREREQ n’est pas dans la zone.</span><span class="sxs-lookup"><span data-stu-id="c5120-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_erreur DNS \_ RCODE \_ BADSIG**</span><span class="sxs-lookup"><span data-stu-id="c5120-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="c5120-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-141">Échec de la vérification de la signature DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_erreur DNS \_ RCODE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="c5120-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="c5120-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-144">Clé DNS incorrecte.</span><span class="sxs-lookup"><span data-stu-id="c5120-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_erreur DNS \_ RCODE \_ BADTIME**</span><span class="sxs-lookup"><span data-stu-id="c5120-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-146">9018 (0x233A)</span><span class="sxs-lookup"><span data-stu-id="c5120-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-147">Validité de la signature DNS expirée.</span><span class="sxs-lookup"><span data-stu-id="c5120-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**erreur DNS- \_ \_ principal \_ requis**</span><span class="sxs-lookup"><span data-stu-id="c5120-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-149">9101 (0x238D)</span><span class="sxs-lookup"><span data-stu-id="c5120-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-150">Seul le serveur DNS agissant comme maître des clés pour la zone peut effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="c5120-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ une \_ zone signée**</span><span class="sxs-lookup"><span data-stu-id="c5120-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-152">9102 (0x238E)</span><span class="sxs-lookup"><span data-stu-id="c5120-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-153">Cette opération n’est pas autorisée sur une zone qui est signée ou qui possède des clés de signature.</span><span class="sxs-lookup"><span data-stu-id="c5120-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Erreur DNS \_ NSEC3 \_ incompatible \_ avec \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="c5120-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-155">9103 (0x238F)</span><span class="sxs-lookup"><span data-stu-id="c5120-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-156">NSEC3 n’est pas compatible avec l’algorithme RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="c5120-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="c5120-157">Choisissez un autre algorithme ou utilisez NSEC.</span><span class="sxs-lookup"><span data-stu-id="c5120-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="c5120-158">Cette valeur était également nommée **\_ erreur DNS \_ \_ \_ paramètres NSEC3 non valides**</span><span class="sxs-lookup"><span data-stu-id="c5120-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_erreur DNS \_ \_ insuffisante pour les \_ \_ descripteurs de clé de signature \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="c5120-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-161">La zone ne dispose pas de suffisamment de clés de signature.</span><span class="sxs-lookup"><span data-stu-id="c5120-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="c5120-162">Il doit y avoir au moins une clé de signature de clé (KSK) et au moins une clé de signature de zone (ZSK).</span><span class="sxs-lookup"><span data-stu-id="c5120-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_algorithme d’erreur DNS \_ non pris en charge \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="c5120-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-165">L’algorithme spécifié n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5120-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_erreur DNS \_ \_ taille de clé non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="c5120-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-168">La taille de clé spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c5120-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_clé de signature d’erreur DNS \_ \_ \_ \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="c5120-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="c5120-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-171">Une ou plusieurs clés de signature pour une zone ne sont pas accessibles au serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="c5120-172">La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**l' \_ erreur \_ DNS \_ KSP \_ ne \_ prend pas en charge la \_ protection**</span><span class="sxs-lookup"><span data-stu-id="c5120-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="c5120-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-175">Le fournisseur de stockage de clés spécifié ne prend pas en charge la protection des données DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="c5120-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="c5120-176">La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**erreur DNS erreur de \_ \_ protection inattendue des \_ données \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="c5120-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-179">Une erreur DPAPI + + inattendue a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="c5120-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="c5120-180">La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**erreur DNS- \_ \_ \_ erreur CNG inattendue \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="c5120-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-183">Une erreur de chiffrement inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c5120-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="c5120-184">La signature de zone peut ne pas être opérationnelle tant que cette erreur n’est pas résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_erreur DNS \_ \_ version de paramètre de signature inconnue \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="c5120-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-187">Le serveur DNS a rencontré une clé de signature avec une version inconnue.</span><span class="sxs-lookup"><span data-stu-id="c5120-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="c5120-188">La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**le \_ KSP des erreurs DNS \_ n’est \_ pas \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="c5120-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="c5120-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-191">Le fournisseur du service de clés spécifié ne peut pas être ouvert par le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_erreur DNS \_ trop \_ de \_ SKDS**</span><span class="sxs-lookup"><span data-stu-id="c5120-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="c5120-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-194">Le serveur DNS ne peut pas accepter d’autres clés de signature avec l’algorithme spécifié et la valeur de l’indicateur KSK pour cette zone.</span><span class="sxs-lookup"><span data-stu-id="c5120-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**\_erreur DNS \_ \_ période de substitution non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-196">9114 (0x239A)</span><span class="sxs-lookup"><span data-stu-id="c5120-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-197">La période de substitution spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**erreur DNS- \_ \_ \_ décalage de substitution initial non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-199">9115 (0x239B)</span><span class="sxs-lookup"><span data-stu-id="c5120-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-200">Le décalage de substitution initial spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ substitution d’erreur DNS \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="c5120-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-202">9116 (0x239C)</span><span class="sxs-lookup"><span data-stu-id="c5120-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-203">La clé de signature spécifiée est déjà en cours de substitution des clés.</span><span class="sxs-lookup"><span data-stu-id="c5120-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_clé de secours d’erreur DNS \_ \_ \_ \_ absente**</span><span class="sxs-lookup"><span data-stu-id="c5120-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-205">9117 (0x239D)</span><span class="sxs-lookup"><span data-stu-id="c5120-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-206">La clé de signature spécifiée n’a pas de clé de secours à révoquer.</span><span class="sxs-lookup"><span data-stu-id="c5120-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ ZSK**</span><span class="sxs-lookup"><span data-stu-id="c5120-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-208">9118 (0x239E)</span><span class="sxs-lookup"><span data-stu-id="c5120-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-209">Cette opération n’est pas autorisée sur une clé de signature de zone (ZSK).</span><span class="sxs-lookup"><span data-stu-id="c5120-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ un \_ SKD actif**</span><span class="sxs-lookup"><span data-stu-id="c5120-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-211">9119 (0x239F)</span><span class="sxs-lookup"><span data-stu-id="c5120-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-212">Cette opération n’est pas autorisée sur une clé de signature active.</span><span class="sxs-lookup"><span data-stu-id="c5120-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_ \_ substitution d’erreur DNS déjà en \_ \_ file d’attente**</span><span class="sxs-lookup"><span data-stu-id="c5120-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-214">9120 (0x23A0)</span><span class="sxs-lookup"><span data-stu-id="c5120-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-215">La clé de signature spécifiée est déjà en file d’attente pour la substitution.</span><span class="sxs-lookup"><span data-stu-id="c5120-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_erreur DNS \_ non \_ autorisée \_ sur une \_ zone non signée \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-217">9121 (0x23A1)</span><span class="sxs-lookup"><span data-stu-id="c5120-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-218">Cette opération n’est pas autorisée sur une zone non signée.</span><span class="sxs-lookup"><span data-stu-id="c5120-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_erreur DNS \_ mauvais \_ maître**</span><span class="sxs-lookup"><span data-stu-id="c5120-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-220">9122 (0x23A2)</span><span class="sxs-lookup"><span data-stu-id="c5120-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-221">Impossible d’effectuer cette opération, car le serveur DNS indiqué comme maître des clés actuel pour cette zone est défaillant ou mal configuré.</span><span class="sxs-lookup"><span data-stu-id="c5120-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="c5120-222">Résolvez le problème sur le maître des clés actuel pour cette zone ou utilisez un autre serveur DNS pour prendre le rôle de maître des clés.</span><span class="sxs-lookup"><span data-stu-id="c5120-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**erreur DNS période de validité de la \_ \_ signature non valide \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-224">9123 (0x23A3)</span><span class="sxs-lookup"><span data-stu-id="c5120-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-225">La période de validité de la signature spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**Erreur DNS- \_ \_ \_ nombre d' \_ itérations NSEC3 non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-227">9124 (0x23A4)</span><span class="sxs-lookup"><span data-stu-id="c5120-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-228">Le nombre d’itérations NSEC3 spécifié est plus élevé que ce qui est autorisé par la longueur de clé minimale utilisée dans la zone.</span><span class="sxs-lookup"><span data-stu-id="c5120-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**l' \_ erreur DNS \_ DNSSEC \_ est \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="c5120-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-230">9125 (0x23A5)</span><span class="sxs-lookup"><span data-stu-id="c5120-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-231">Cette opération n’a pas pu aboutir car le serveur DNS a été configuré avec les fonctionnalités DNSSEC désactivées.</span><span class="sxs-lookup"><span data-stu-id="c5120-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="c5120-232">Activez DNSSEC sur le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ code XML non valide pour l’erreur DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-234">9126 (0x23A6)</span><span class="sxs-lookup"><span data-stu-id="c5120-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-235">Impossible d’effectuer cette opération, car le flux de données XML reçu est vide ou n’est pas valide syntaxiquement.</span><span class="sxs-lookup"><span data-stu-id="c5120-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**\_erreur DNS \_ aucune \_ \_ ancre d’approbation valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-237">9127 (0x23A7)</span><span class="sxs-lookup"><span data-stu-id="c5120-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-238">Cette opération s’est terminée, mais aucune ancre d’approbation n’a été ajoutée, car toutes les ancres d’approbation reçues n’étaient pas valides, ne sont pas prises en charge, ont expiré ou ne seraient pas valides dans moins de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="c5120-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_substitution d’erreur DNS \_ non survolée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-240">9128 (0x23A8)</span><span class="sxs-lookup"><span data-stu-id="c5120-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-241">La clé de signature spécifiée n’attend pas la mise à jour des services de domaine Active Directory parental.</span><span class="sxs-lookup"><span data-stu-id="c5120-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_Erreur DNS \_ \_ collision de nom NSEC3 \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-243">9129 (0x23A9)</span><span class="sxs-lookup"><span data-stu-id="c5120-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-244">Collision de hachage détectée au cours de la signature NSEC3.</span><span class="sxs-lookup"><span data-stu-id="c5120-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="c5120-245">Spécifiez un autre Salt fourni par l’utilisateur ou utilisez un Salt généré de manière aléatoire, puis essayez de signer à nouveau la zone.</span><span class="sxs-lookup"><span data-stu-id="c5120-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Erreur DNS \_ NSEC \_ incompatible \_ avec la fonction de \_ \_ \_ hachage RSA SHA1**</span><span class="sxs-lookup"><span data-stu-id="c5120-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-247">9130 (0x23AA)</span><span class="sxs-lookup"><span data-stu-id="c5120-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-248">NSEC n’est pas compatible avec l’algorithme NSEC3-RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="c5120-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="c5120-249">Choisissez un algorithme différent ou utilisez NSEC3.</span><span class="sxs-lookup"><span data-stu-id="c5120-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_informations DNS \_ aucun \_ enregistrement**</span><span class="sxs-lookup"><span data-stu-id="c5120-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-251">9501 (0x251D)</span><span class="sxs-lookup"><span data-stu-id="c5120-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-252">Aucun enregistrement trouvé pour la requête DNS donnée.</span><span class="sxs-lookup"><span data-stu-id="c5120-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**erreur DNS de \_ \_ paquet incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-254">9502 (0x251E)</span><span class="sxs-lookup"><span data-stu-id="c5120-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-255">Paquet DNS incorrect.</span><span class="sxs-lookup"><span data-stu-id="c5120-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**erreur DNS- \_ \_ aucun \_ paquet**</span><span class="sxs-lookup"><span data-stu-id="c5120-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-257">9503 (0x251F)</span><span class="sxs-lookup"><span data-stu-id="c5120-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-258">Aucun paquet DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_erreur DNS \_ RCODE**</span><span class="sxs-lookup"><span data-stu-id="c5120-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="c5120-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-261">Erreur DNS, vérifiez le RCODE.</span><span class="sxs-lookup"><span data-stu-id="c5120-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**\_paquet d’erreur DNS \_ non sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="c5120-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-264">Paquet DNS non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c5120-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_demande DNS \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="c5120-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="c5120-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-267">La demande de requête DNS est en attente.</span><span class="sxs-lookup"><span data-stu-id="c5120-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_erreur DNS \_ type non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-269">9551 (0x254F)</span><span class="sxs-lookup"><span data-stu-id="c5120-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-270">Type DNS non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_erreur DNS \_ \_ adresse IP non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="c5120-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-273">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_propriété erreur DNS \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="c5120-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-276">Propriété non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**\_erreur DNS \_ Réessayer \_ \_ plus tard**</span><span class="sxs-lookup"><span data-stu-id="c5120-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="c5120-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-279">Réessayez l’opération DNS ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c5120-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_erreur DNS \_ non \_ unique**</span><span class="sxs-lookup"><span data-stu-id="c5120-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="c5120-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-282">L’enregistrement pour le nom et le type donnés n’est pas unique.</span><span class="sxs-lookup"><span data-stu-id="c5120-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_erreur DNS \_ \_ nom non RFC \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="c5120-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-285">Le nom DNS n’est pas conforme aux spécifications RFC.</span><span class="sxs-lookup"><span data-stu-id="c5120-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_nom de \_ domaine complet de l’État DNS**</span><span class="sxs-lookup"><span data-stu-id="c5120-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="c5120-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-288">Le nom DNS est un nom DNS complet.</span><span class="sxs-lookup"><span data-stu-id="c5120-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_nom en \_ pointillés de l’État DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="c5120-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-291">Le nom DNS est en pointillés (étiquette multiple).</span><span class="sxs-lookup"><span data-stu-id="c5120-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**nom de la \_ \_ seule \_ partie \_ de l’État DNS**</span><span class="sxs-lookup"><span data-stu-id="c5120-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="c5120-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-294">Le nom DNS est un nom en une seule partie.</span><span class="sxs-lookup"><span data-stu-id="c5120-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_erreur DNS \_ nom de \_ nom non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="c5120-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-297">Le nom DNS contient un caractère non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nom numérique de l’erreur DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="c5120-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-300">Le nom DNS est entièrement numérique.</span><span class="sxs-lookup"><span data-stu-id="c5120-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ le \_ serveur racine**</span><span class="sxs-lookup"><span data-stu-id="c5120-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-302">9562 (0x255A)</span><span class="sxs-lookup"><span data-stu-id="c5120-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-303">L’opération demandée n’est pas autorisée sur un serveur racine DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_erreur DNS \_ non \_ autorisée \_ sous \_ délégation**</span><span class="sxs-lookup"><span data-stu-id="c5120-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-305">9563 (0x255B)</span><span class="sxs-lookup"><span data-stu-id="c5120-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-306">L’enregistrement n’a pas pu être créé, car cette partie de l’espace de noms DNS a été déléguée à un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="c5120-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_erreur DNS \_ Impossible de trouver les \_ \_ indications de racine \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-308">9564 (0x255C)</span><span class="sxs-lookup"><span data-stu-id="c5120-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-309">Le serveur DNS n’a pas pu trouver un ensemble d’indications de racine.</span><span class="sxs-lookup"><span data-stu-id="c5120-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_indications de \_ racine incohérentes d’erreur DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-311">9565 (0x255D)</span><span class="sxs-lookup"><span data-stu-id="c5120-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-312">Le serveur DNS a trouvé des indications de racine, mais elles n’étaient pas cohérentes sur tous les adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="c5120-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_valeur DWORD de l’erreur DNS \_ \_ \_ trop \_ petite**</span><span class="sxs-lookup"><span data-stu-id="c5120-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-314">9566 (0x255E)</span><span class="sxs-lookup"><span data-stu-id="c5120-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-315">La valeur spécifiée est trop petite pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="c5120-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_valeur DWORD de l’erreur DNS \_ \_ \_ trop \_ grande**</span><span class="sxs-lookup"><span data-stu-id="c5120-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-317">9567 (0x255F)</span><span class="sxs-lookup"><span data-stu-id="c5120-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-318">La valeur spécifiée est trop grande pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="c5120-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**erreur DNS lors \_ \_ du chargement en arrière-plan \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="c5120-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-321">Cette opération n’est pas autorisée pendant que le serveur DNS charge des zones en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c5120-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="c5120-322">Veuillez réessayer plus tard.</span><span class="sxs-lookup"><span data-stu-id="c5120-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ RODC**</span><span class="sxs-lookup"><span data-stu-id="c5120-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="c5120-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-325">L’opération demandée n’est pas autorisée sur un serveur DNS s’exécutant sur un contrôleur de domaine en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c5120-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_erreur DNS \_ non \_ autorisée \_ sous \_ dname**</span><span class="sxs-lookup"><span data-stu-id="c5120-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="c5120-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-328">Aucune donnée ne peut exister sous un enregistrement DNAME.</span><span class="sxs-lookup"><span data-stu-id="c5120-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_délégation d’erreurs DNS \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="c5120-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="c5120-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-331">Cette opération nécessite la délégation des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c5120-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_erreur DNS \_ \_ table de stratégie non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="c5120-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-334">La table de stratégie de résolution de noms a été endommagée.</span><span class="sxs-lookup"><span data-stu-id="c5120-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="c5120-335">La résolution DNS échouera jusqu’à ce qu’elle soit résolue.</span><span class="sxs-lookup"><span data-stu-id="c5120-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="c5120-336">Contactez votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="c5120-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**la \_ zone d’erreur DNS \_ \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="c5120-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="c5120-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-339">La zone DNS n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**\_erreur DNS \_ aucune \_ information de zone \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="c5120-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-342">Les informations de zone DNS ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="c5120-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_erreur DNS erreur de \_ zone non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="c5120-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-345">Opération non valide pour la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_erreur de \_ configuration du fuseau erreur \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="c5120-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-348">Configuration de zone DNS non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zone d’erreur DNS n' \_ \_ a \_ pas d' \_ \_ enregistrement SOA**</span><span class="sxs-lookup"><span data-stu-id="c5120-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="c5120-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-351">La zone DNS n’a pas d’enregistrement SOA (Start of Authority).</span><span class="sxs-lookup"><span data-stu-id="c5120-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zone d’erreur DNS n' \_ \_ a \_ pas d' \_ \_ enregistrements NS**</span><span class="sxs-lookup"><span data-stu-id="c5120-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="c5120-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-354">La zone DNS n’a aucun enregistrement de serveur de noms (NS).</span><span class="sxs-lookup"><span data-stu-id="c5120-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zone d’erreur DNS \_ \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="c5120-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="c5120-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-357">La zone DNS est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c5120-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**échec de la création de la \_ zone d’erreur DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="c5120-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-360">Échec de la création de la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**la \_ zone d’erreur DNS \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="c5120-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="c5120-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-363">La zone DNS existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c5120-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**une \_ erreur DNS \_ \_ existe déjà \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-365">9610 (0x258A)</span><span class="sxs-lookup"><span data-stu-id="c5120-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-366">La zone DNS automatique existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c5120-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_erreur DNS \_ \_ type de zone non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-368">9611 (0x258B)</span><span class="sxs-lookup"><span data-stu-id="c5120-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-369">Type de zone DNS non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**erreur DNS la base de données \_ \_ secondaire \_ requiert une \_ \_ adresse IP principale**</span><span class="sxs-lookup"><span data-stu-id="c5120-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-371">9612 (0x258C)</span><span class="sxs-lookup"><span data-stu-id="c5120-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-372">La zone DNS secondaire requiert une adresse IP principale.</span><span class="sxs-lookup"><span data-stu-id="c5120-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zone d’erreur DNS \_ \_ non \_ secondaire**</span><span class="sxs-lookup"><span data-stu-id="c5120-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-374">9613 (0x258D)</span><span class="sxs-lookup"><span data-stu-id="c5120-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-375">Zone DNS non secondaire.</span><span class="sxs-lookup"><span data-stu-id="c5120-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**une \_ erreur DNS \_ nécessite des \_ \_ adresses secondaires**</span><span class="sxs-lookup"><span data-stu-id="c5120-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-377">9614 (0x258E)</span><span class="sxs-lookup"><span data-stu-id="c5120-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-378">Vous avez besoin d’une adresse IP secondaire.</span><span class="sxs-lookup"><span data-stu-id="c5120-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_échec de \_ l' \_ initialisation \_ WINS de l’erreur DNS**</span><span class="sxs-lookup"><span data-stu-id="c5120-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-380">9615 (0x258F)</span><span class="sxs-lookup"><span data-stu-id="c5120-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-381">Échec de l’initialisation WINS.</span><span class="sxs-lookup"><span data-stu-id="c5120-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**une \_ erreur DNS \_ nécessite des \_ \_ serveurs WINS**</span><span class="sxs-lookup"><span data-stu-id="c5120-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="c5120-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-384">Serveurs WINS requis.</span><span class="sxs-lookup"><span data-stu-id="c5120-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_erreur DNS \_ NBSTAT \_ init \_ failed**</span><span class="sxs-lookup"><span data-stu-id="c5120-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="c5120-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-387">Échec de l’appel d’initialisation NBTSTAT.</span><span class="sxs-lookup"><span data-stu-id="c5120-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_erreur DNS \_ SOA \_ suppression \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="c5120-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="c5120-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-390">Suppression non valide du SOA (Start of Authority).</span><span class="sxs-lookup"><span data-stu-id="c5120-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**le \_ redirecteur des erreurs DNS \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="c5120-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="c5120-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-393">Il existe déjà une zone de transfert conditionnel pour ce nom.</span><span class="sxs-lookup"><span data-stu-id="c5120-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zone d’erreur DNS \_ nécessite une \_ \_ \_ adresse IP principale**</span><span class="sxs-lookup"><span data-stu-id="c5120-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="c5120-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-396">Cette zone doit être configurée avec une ou plusieurs adresses IP de serveur DNS maître.</span><span class="sxs-lookup"><span data-stu-id="c5120-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**la \_ zone d’erreur DNS \_ \_ est \_ Shutdown**</span><span class="sxs-lookup"><span data-stu-id="c5120-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="c5120-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-399">Impossible d’effectuer l’opération, car cette zone est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="c5120-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zone d’erreur DNS \_ verrouillée \_ pour la \_ signature**</span><span class="sxs-lookup"><span data-stu-id="c5120-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="c5120-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-402">Impossible d’effectuer cette opération, car la zone est actuellement signée.</span><span class="sxs-lookup"><span data-stu-id="c5120-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="c5120-403">Veuillez réessayer plus tard.</span><span class="sxs-lookup"><span data-stu-id="c5120-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**une \_ erreur DNS \_ principale \_ nécessite un fichier de \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="c5120-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-405">9651 (0x25B3)</span><span class="sxs-lookup"><span data-stu-id="c5120-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-406">La zone DNS principale nécessite un fichier de fichier.</span><span class="sxs-lookup"><span data-stu-id="c5120-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_erreur DNS \_ nom du fichier de fichier non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-408">9652 (0x25B4)</span><span class="sxs-lookup"><span data-stu-id="c5120-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-409">Nom de fichier de fichier non valide pour la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**échec de l' \_ ouverture du fichier de fichier d’erreur DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-411">9653 (0x25B5)</span><span class="sxs-lookup"><span data-stu-id="c5120-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-412">Impossible d’ouvrir le fichier de fichier pour la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_échec de \_ l' \_ écriture différée du fichier d’erreurs DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-414">9654 (0x25B6)</span><span class="sxs-lookup"><span data-stu-id="c5120-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-415">Échec de l’écriture du fichier de fichier pour la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**erreur DNS lors de l' \_ \_ analyse du fichier de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-417">9655 (0x25B7)</span><span class="sxs-lookup"><span data-stu-id="c5120-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-418">Échec lors de la lecture du fichier de fichier pour la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**l' \_ enregistrement d’erreur DNS \_ \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="c5120-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-420">9701 (0x25E5)</span><span class="sxs-lookup"><span data-stu-id="c5120-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-421">L’enregistrement DNS n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_format d' \_ enregistrement des erreurs DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-423">9702 (0x25E6)</span><span class="sxs-lookup"><span data-stu-id="c5120-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-424">Erreur de format d’enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**échec de la création du nœud d' \_ erreur DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-426">9703 (0x25E7)</span><span class="sxs-lookup"><span data-stu-id="c5120-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-427">Échec de la création du nœud dans DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_type d’enregistrement d’erreur DNS \_ inconnu \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-429">9704 (0x25E8)</span><span class="sxs-lookup"><span data-stu-id="c5120-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-430">Type d’enregistrement DNS inconnu.</span><span class="sxs-lookup"><span data-stu-id="c5120-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**expiration du délai de l' \_ enregistrement d’erreur DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-432">9705 (0x25E9)</span><span class="sxs-lookup"><span data-stu-id="c5120-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-433">Expiration du délai de l’enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nom d’erreur DNS \_ non dans la \_ \_ zone**</span><span class="sxs-lookup"><span data-stu-id="c5120-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-435">9706 (0x25EA)</span><span class="sxs-lookup"><span data-stu-id="c5120-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-436">Le nom n’est pas dans la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ boucle CNAME d’erreur DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-438">9707 (0x25EB)</span><span class="sxs-lookup"><span data-stu-id="c5120-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-439">Boucle CNAMe détectée.</span><span class="sxs-lookup"><span data-stu-id="c5120-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**le \_ nœud d’erreur DNS \_ \_ est \_ CNAME**</span><span class="sxs-lookup"><span data-stu-id="c5120-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-441">9708 (0x25EC)</span><span class="sxs-lookup"><span data-stu-id="c5120-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-442">Le nœud est un enregistrement DNS CNAMe.</span><span class="sxs-lookup"><span data-stu-id="c5120-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_erreur DNS \_ CNAME \_ collision**</span><span class="sxs-lookup"><span data-stu-id="c5120-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-444">9709 (0x25ED)</span><span class="sxs-lookup"><span data-stu-id="c5120-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-445">Un enregistrement CNAMe existe déjà pour le nom donné.</span><span class="sxs-lookup"><span data-stu-id="c5120-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_enregistrement des erreurs DNS \_ \_ uniquement à la \_ racine de la \_ zone \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-447">9710 (0x25EE)</span><span class="sxs-lookup"><span data-stu-id="c5120-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-448">Enregistrement uniquement au niveau de la racine de la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**un \_ enregistrement d’erreur DNS \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="c5120-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-450">9711 (0x25EF)</span><span class="sxs-lookup"><span data-stu-id="c5120-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-451">L’enregistrement DNS existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c5120-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ données secondaires d’erreur DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-453">9712 (0x25F0)</span><span class="sxs-lookup"><span data-stu-id="c5120-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-454">Erreur de données de la zone DNS secondaire.</span><span class="sxs-lookup"><span data-stu-id="c5120-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**erreur DNS- \_ \_ pas de création de \_ \_ données de cache \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-456">9713 (0x25F1)</span><span class="sxs-lookup"><span data-stu-id="c5120-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-457">Impossible de créer les données du cache DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**le \_ nom d’erreur DNS \_ \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="c5120-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-459">9714 (0x25F2)</span><span class="sxs-lookup"><span data-stu-id="c5120-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-460">Le nom DNS n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**échec de la création du PTR d' \_ Avertissement DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-462">9715 (0x25F3)</span><span class="sxs-lookup"><span data-stu-id="c5120-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-463">Impossible de créer un enregistrement de pointeur (PTR).</span><span class="sxs-lookup"><span data-stu-id="c5120-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**\_domaine d’avertissement DNS \_ \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="c5120-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-465">9716 (0x25F4)</span><span class="sxs-lookup"><span data-stu-id="c5120-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-466">Le domaine DNS n’a pas été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c5120-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_erreur DNS \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="c5120-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-468">9717 (0x25F5)</span><span class="sxs-lookup"><span data-stu-id="c5120-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-469">Le service d’annuaire n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c5120-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**une erreur DNS de la \_ \_ \_ zone DS \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="c5120-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-471">9718 (0x25F6)</span><span class="sxs-lookup"><span data-stu-id="c5120-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-472">La zone DNS existe déjà dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c5120-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_erreur DNS \_ non \_ BOOTFILE \_ si \_ la \_ zone DS**</span><span class="sxs-lookup"><span data-stu-id="c5120-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-474">9719 (0x25F7)</span><span class="sxs-lookup"><span data-stu-id="c5120-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-475">Le serveur DNS ne crée pas ou ne lit pas le fichier de démarrage pour la zone DNS intégrée au service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c5120-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**le \_ nœud d’erreur DNS \_ \_ est \_ dname**</span><span class="sxs-lookup"><span data-stu-id="c5120-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-477">9720 (0x25F8)</span><span class="sxs-lookup"><span data-stu-id="c5120-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-478">Le nœud est un enregistrement DNS DNAME.</span><span class="sxs-lookup"><span data-stu-id="c5120-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_erreur DNS \_ - \_ collision dname**</span><span class="sxs-lookup"><span data-stu-id="c5120-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-480">9721 (0x25F9)</span><span class="sxs-lookup"><span data-stu-id="c5120-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-481">Un enregistrement DNAME existe déjà pour le nom donné.</span><span class="sxs-lookup"><span data-stu-id="c5120-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_boucle d' \_ alias d’erreur DNS \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-483">9722 (0x25FA)</span><span class="sxs-lookup"><span data-stu-id="c5120-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-484">Une boucle d’alias a été détectée avec des enregistrements CNAMe ou DNAME.</span><span class="sxs-lookup"><span data-stu-id="c5120-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**informations de DNS \_ sur le \_ AXFR \_ terminées**</span><span class="sxs-lookup"><span data-stu-id="c5120-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="c5120-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-487">DNS AXFR (transfert de zone) terminé.</span><span class="sxs-lookup"><span data-stu-id="c5120-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_erreur DNS \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="c5120-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="c5120-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-490">Échec du transfert de la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="c5120-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**\_Ajout du \_ \_ WINS local \_ aux informations DNS**</span><span class="sxs-lookup"><span data-stu-id="c5120-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="c5120-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-493">Serveur WINS local ajouté.</span><span class="sxs-lookup"><span data-stu-id="c5120-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_État DNS \_ toujours \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="c5120-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="c5120-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-496">L’appel de mise à jour sécurisée doit continuer la demande de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c5120-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_erreur DNS \_ non \_ tcpip**</span><span class="sxs-lookup"><span data-stu-id="c5120-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-498">9851 (0x267B)</span><span class="sxs-lookup"><span data-stu-id="c5120-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-499">Le protocole réseau TCP/IP n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="c5120-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**\_erreur DNS \_ aucun \_ \_ serveur DNS**</span><span class="sxs-lookup"><span data-stu-id="c5120-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-501">9852 (0x267C)</span><span class="sxs-lookup"><span data-stu-id="c5120-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-502">Aucun serveur DNS configuré pour le système local.</span><span class="sxs-lookup"><span data-stu-id="c5120-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**l' \_ erreur \_ DNS \_ DP \_ n' \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="c5120-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-504">9901 (0x26AD)</span><span class="sxs-lookup"><span data-stu-id="c5120-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-505">La partition d’annuaire spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c5120-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**l' \_ erreur \_ DNS \_ DP \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="c5120-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-507">9902 (0x26AE)</span><span class="sxs-lookup"><span data-stu-id="c5120-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-508">La partition d’annuaire spécifiée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c5120-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_erreur DNS \_ DP \_ non \_ inscrite**</span><span class="sxs-lookup"><span data-stu-id="c5120-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-510">9903 (0x26AF)</span><span class="sxs-lookup"><span data-stu-id="c5120-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-511">Ce serveur DNS n’est pas inscrit dans la partition d’annuaire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c5120-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_erreur DNS \_ DP \_ déjà \_ inscrite**</span><span class="sxs-lookup"><span data-stu-id="c5120-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-513">9904 (0x26B0)</span><span class="sxs-lookup"><span data-stu-id="c5120-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-514">Ce serveur DNS est déjà inscrit dans la partition d’annuaire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c5120-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_DP d’erreur DNS \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="c5120-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-516">9905 (0x26B1)</span><span class="sxs-lookup"><span data-stu-id="c5120-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-517">La partition d’annuaire n’est pas disponible pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="c5120-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="c5120-518">Patientez quelques minutes et recommencez.</span><span class="sxs-lookup"><span data-stu-id="c5120-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**erreur \_ DNS \_ DP \_ FSMO \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-520">9906 (0x26B2)</span><span class="sxs-lookup"><span data-stu-id="c5120-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-521">L’opération a échoué car le rôle FSMO du maître d’opérations des noms de domaine est inaccessible.</span><span class="sxs-lookup"><span data-stu-id="c5120-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="c5120-522">Le contrôleur de domaine détenant le rôle FSMO du maître d’attribution de noms de domaine est inactif ou ne peut pas traiter la demande ou n’exécute pas Windows Server 2003 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c5120-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="c5120-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="c5120-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-525">Une opération de blocage a été interrompue par un appel à WSACancelBlockingCall.</span><span class="sxs-lookup"><span data-stu-id="c5120-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span><span class="sxs-lookup"><span data-stu-id="c5120-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="c5120-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-528">Le descripteur de fichier fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="c5120-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-530">10013 (0x271D)</span><span class="sxs-lookup"><span data-stu-id="c5120-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-531">Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.</span><span class="sxs-lookup"><span data-stu-id="c5120-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c5120-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-533">10014 (0x271E)</span><span class="sxs-lookup"><span data-stu-id="c5120-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-534">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="c5120-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="c5120-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="c5120-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-537">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="c5120-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span><span class="sxs-lookup"><span data-stu-id="c5120-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="c5120-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-540">Trop de sockets ouverts.</span><span class="sxs-lookup"><span data-stu-id="c5120-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="c5120-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="c5120-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-543">Une opération de socket non bloquante n’a pas pu être effectuée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c5120-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="c5120-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="c5120-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-546">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="c5120-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span><span class="sxs-lookup"><span data-stu-id="c5120-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="c5120-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-549">Tentative d'opération sur un socket non bloquant au niveau duquel une opération était déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="c5120-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="c5120-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="c5120-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-552">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="c5120-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="c5120-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="c5120-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-555">Une adresse requise a été omise d’une opération sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="c5120-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="c5120-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="c5120-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-558">Un message envoyé sur un socket datagramme était plus volumineux que le tampon de messages interne ou qu'une autre limite réseau ou bien le tampon utilisé pour recevoir un datagramme était plus petit que le datagramme lui-même.</span><span class="sxs-lookup"><span data-stu-id="c5120-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="c5120-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="c5120-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-561">Un protocole a été spécifié dans l’appel de fonction socket qui ne prend pas en charge la sémantique du type de socket demandé.</span><span class="sxs-lookup"><span data-stu-id="c5120-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="c5120-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-563">10042 (0x273A)</span><span class="sxs-lookup"><span data-stu-id="c5120-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-564">Une option ou un niveau inconnu, non valide ou non pris en charge a été spécifié dans un appel getsockopt ou setsockopt.</span><span class="sxs-lookup"><span data-stu-id="c5120-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="c5120-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-566">10043 (0x273B)</span><span class="sxs-lookup"><span data-stu-id="c5120-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-567">Le protocole demandé n’a pas été configuré dans le système, ou aucune implémentation de ce dernier n’existe.</span><span class="sxs-lookup"><span data-stu-id="c5120-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="c5120-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-569">10044 (0x273C)</span><span class="sxs-lookup"><span data-stu-id="c5120-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-570">La prise en charge du type de socket spécifié n'existe pas dans cette famille d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c5120-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="c5120-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-572">10045 (0x273D)</span><span class="sxs-lookup"><span data-stu-id="c5120-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-573">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="c5120-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="c5120-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-575">10046 (0x273E)</span><span class="sxs-lookup"><span data-stu-id="c5120-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-576">La famille de protocoles n’a pas été configurée dans le système ou aucune implémentation de celle-ci n’existe.</span><span class="sxs-lookup"><span data-stu-id="c5120-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="c5120-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-578">10047 (0x273F)</span><span class="sxs-lookup"><span data-stu-id="c5120-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-579">Une adresse incompatible avec le protocole demandé a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="c5120-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="c5120-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="c5120-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-582">Une seule utilisation de chaque adresse de socket (protocole/adresse réseau/port) est habituellement autorisée.</span><span class="sxs-lookup"><span data-stu-id="c5120-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="c5120-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="c5120-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-585">L’adresse demandée n’est pas valide dans son contexte.</span><span class="sxs-lookup"><span data-stu-id="c5120-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="c5120-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="c5120-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-588">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="c5120-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span><span class="sxs-lookup"><span data-stu-id="c5120-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="c5120-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-591">Une opération de socket a été tentée sur un réseau inaccessible.</span><span class="sxs-lookup"><span data-stu-id="c5120-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span><span class="sxs-lookup"><span data-stu-id="c5120-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="c5120-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-594">La connexion a été interrompue en raison d’une activité de maintien en état de la détection d’un échec pendant l’opération.</span><span class="sxs-lookup"><span data-stu-id="c5120-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="c5120-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="c5120-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-597">Une connexion établie a été abandonnée par un logiciel de votre ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="c5120-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="c5120-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="c5120-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-600">une connexion existante a dû être fermée par l’hôte distant.</span><span class="sxs-lookup"><span data-stu-id="c5120-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="c5120-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="c5120-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-603">Impossible d’effectuer une opération sur un socket en raison de l’insuffisance de l’espace de mémoire tampon du système ou de la saturation de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5120-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span><span class="sxs-lookup"><span data-stu-id="c5120-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="c5120-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-606">Une demande de connexion a été effectuée sur un socket déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="c5120-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="c5120-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="c5120-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-609">Une requête d'envoi ou de réception de données n'a pas été autorisée, car le socket n'est pas connecté et (lors de l'envoi sur un socket datagramme en utilisant un appel sendto) aucune adresse n'a été fournie.</span><span class="sxs-lookup"><span data-stu-id="c5120-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="c5120-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-611">10058 (0x274A)</span><span class="sxs-lookup"><span data-stu-id="c5120-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-612">Une demande d'envoi ou de réception de données n'a pas été autorisée car le socket avait déjà été éteint dans cette direction par un appel d'arrêt précédent.</span><span class="sxs-lookup"><span data-stu-id="c5120-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span><span class="sxs-lookup"><span data-stu-id="c5120-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-614">10059 (0x274B)</span><span class="sxs-lookup"><span data-stu-id="c5120-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-615">Trop de références à un objet de noyau.</span><span class="sxs-lookup"><span data-stu-id="c5120-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="c5120-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-617">10060 (0x274C)</span><span class="sxs-lookup"><span data-stu-id="c5120-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-618">Une tentative de connexion a échoué car le tiers connecté n’a pas répondu correctement après une certaine période, ou la connexion établie a échoué, car l’hôte connecté n’a pas pu répondre.</span><span class="sxs-lookup"><span data-stu-id="c5120-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span><span class="sxs-lookup"><span data-stu-id="c5120-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-620">10061 (0x274D)</span><span class="sxs-lookup"><span data-stu-id="c5120-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-621">Aucune connexion n’a pu être établie car l’ordinateur cible l’a refusé activement.</span><span class="sxs-lookup"><span data-stu-id="c5120-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span><span class="sxs-lookup"><span data-stu-id="c5120-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-623">10062 (0x274E)</span><span class="sxs-lookup"><span data-stu-id="c5120-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-624">Impossible de traduire le nom.</span><span class="sxs-lookup"><span data-stu-id="c5120-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span><span class="sxs-lookup"><span data-stu-id="c5120-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-626">10063 (0x274F)</span><span class="sxs-lookup"><span data-stu-id="c5120-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-627">Le nom ou le composant du nom est trop long.</span><span class="sxs-lookup"><span data-stu-id="c5120-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span><span class="sxs-lookup"><span data-stu-id="c5120-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="c5120-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-630">Une opération de socket a échoué, car l’ordinateur hôte de destination était en panne.</span><span class="sxs-lookup"><span data-stu-id="c5120-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span><span class="sxs-lookup"><span data-stu-id="c5120-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="c5120-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-633">Une opération de socket a été tentée sur un hôte impossible à atteindre.</span><span class="sxs-lookup"><span data-stu-id="c5120-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span><span class="sxs-lookup"><span data-stu-id="c5120-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="c5120-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-636">Impossible de supprimer un répertoire qui n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="c5120-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span><span class="sxs-lookup"><span data-stu-id="c5120-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="c5120-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-639">Une implémentation de Windows Sockets peut avoir une limite du nombre d’applications qui peuvent l’utiliser simultanément.</span><span class="sxs-lookup"><span data-stu-id="c5120-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span><span class="sxs-lookup"><span data-stu-id="c5120-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="c5120-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-642">Le quota est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="c5120-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span><span class="sxs-lookup"><span data-stu-id="c5120-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="c5120-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-645">Le quota de disque est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="c5120-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span><span class="sxs-lookup"><span data-stu-id="c5120-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="c5120-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-648">La référence de descripteur de fichier n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="c5120-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span><span class="sxs-lookup"><span data-stu-id="c5120-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="c5120-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-651">L’élément n’est pas disponible localement.</span><span class="sxs-lookup"><span data-stu-id="c5120-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span><span class="sxs-lookup"><span data-stu-id="c5120-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-653">10091 (0x276B)</span><span class="sxs-lookup"><span data-stu-id="c5120-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-654">WSAStartup ne peut pas fonctionner pour l’instant, car le système sous-jacent qu’il utilise pour fournir des services réseau n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="c5120-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="c5120-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-656">10092 (0x276C)</span><span class="sxs-lookup"><span data-stu-id="c5120-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-657">La version de Windows Sockets demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c5120-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span><span class="sxs-lookup"><span data-stu-id="c5120-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-659">10093 (0x276D)</span><span class="sxs-lookup"><span data-stu-id="c5120-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-660">Soit l’application n’a pas appelé WSAStartup, soit WSAStartup a échoué.</span><span class="sxs-lookup"><span data-stu-id="c5120-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span><span class="sxs-lookup"><span data-stu-id="c5120-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="c5120-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-663">Retourné par WSARecv ou WSARecvFrom pour indiquer que le tiers distant a initié une séquence d’arrêt appropriée.</span><span class="sxs-lookup"><span data-stu-id="c5120-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span><span class="sxs-lookup"><span data-stu-id="c5120-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="c5120-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-666">Aucun autre résultat ne peut être retourné par WSALookupServiceNext.</span><span class="sxs-lookup"><span data-stu-id="c5120-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span><span class="sxs-lookup"><span data-stu-id="c5120-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="c5120-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-669">Un appel à WSALookupServiceEnd a été effectué alors que cet appel était toujours en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="c5120-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="c5120-670">L’appel a été annulé.</span><span class="sxs-lookup"><span data-stu-id="c5120-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span><span class="sxs-lookup"><span data-stu-id="c5120-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="c5120-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-673">La table des appels de procédure n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span><span class="sxs-lookup"><span data-stu-id="c5120-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="c5120-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-676">Le fournisseur de services demandé n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span><span class="sxs-lookup"><span data-stu-id="c5120-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-678">10106 (0x277A)</span><span class="sxs-lookup"><span data-stu-id="c5120-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-679">Impossible de charger ou d’initialiser le fournisseur de services demandé.</span><span class="sxs-lookup"><span data-stu-id="c5120-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="c5120-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-681">10107 (0x277B)</span><span class="sxs-lookup"><span data-stu-id="c5120-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-682">Un appel système a échoué.</span><span class="sxs-lookup"><span data-stu-id="c5120-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="c5120-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-684">10108 (0x277C)</span><span class="sxs-lookup"><span data-stu-id="c5120-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-685">Aucun service de ce type n’est connu.</span><span class="sxs-lookup"><span data-stu-id="c5120-685">No such service is known.</span></span> <span data-ttu-id="c5120-686">Le service est introuvable dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="c5120-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="c5120-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-688">10109 (0x277D)</span><span class="sxs-lookup"><span data-stu-id="c5120-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-689">La classe spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c5120-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ plus \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-691">10110 (0x277E)</span><span class="sxs-lookup"><span data-stu-id="c5120-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-692">Aucun autre résultat ne peut être retourné par WSALookupServiceNext.</span><span class="sxs-lookup"><span data-stu-id="c5120-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="c5120-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-694">10111 (0x277F)</span><span class="sxs-lookup"><span data-stu-id="c5120-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-695">Un appel à WSALookupServiceEnd a été effectué alors que cet appel était toujours en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="c5120-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="c5120-696">L’appel a été annulé.</span><span class="sxs-lookup"><span data-stu-id="c5120-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span><span class="sxs-lookup"><span data-stu-id="c5120-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="c5120-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-699">Une requête de base de données a échoué car elle a été refusée activement.</span><span class="sxs-lookup"><span data-stu-id="c5120-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="c5120-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-701">11001 (0x2AF9)</span><span class="sxs-lookup"><span data-stu-id="c5120-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-702">Hôte inconnu.</span><span class="sxs-lookup"><span data-stu-id="c5120-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY \_ à nouveau**</span><span class="sxs-lookup"><span data-stu-id="c5120-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-704">11002 (0x2AFA)</span><span class="sxs-lookup"><span data-stu-id="c5120-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-705">Il s'agit habituellement d'une erreur temporaire qui se produit durant la résolution du nom d'hôte et qui signifie que le serveur local n'a pas reçu de réponse d'un serveur de référence.</span><span class="sxs-lookup"><span data-stu-id="c5120-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_récupération WSANO**</span><span class="sxs-lookup"><span data-stu-id="c5120-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-707">11003 (0x2AFB)</span><span class="sxs-lookup"><span data-stu-id="c5120-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-708">Une erreur non récupérable s’est produite lors d’une recherche de base de données.</span><span class="sxs-lookup"><span data-stu-id="c5120-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_données WSANO**</span><span class="sxs-lookup"><span data-stu-id="c5120-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-710">11004 (0x2AFC)</span><span class="sxs-lookup"><span data-stu-id="c5120-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-711">Le nom demandé est valide, mais aucune donnée du type demandé n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="c5120-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_récepteurs de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-713">11005 (0x2AFD)</span><span class="sxs-lookup"><span data-stu-id="c5120-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-714">Au moins une réserve est arrivée.</span><span class="sxs-lookup"><span data-stu-id="c5120-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_expéditeurs de la QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-716">11006 (0x2AFE)</span><span class="sxs-lookup"><span data-stu-id="c5120-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-717">Au moins un chemin d’accès est arrivé.</span><span class="sxs-lookup"><span data-stu-id="c5120-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_non- \_ \_ expéditeurs de la QoS WSA**</span><span class="sxs-lookup"><span data-stu-id="c5120-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-719">11007 (0x2AFF)</span><span class="sxs-lookup"><span data-stu-id="c5120-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-720">Il n’y a pas d’expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="c5120-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_non- \_ \_ destinataires de la QoS WSA**</span><span class="sxs-lookup"><span data-stu-id="c5120-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-722">11008 (0x2B00)</span><span class="sxs-lookup"><span data-stu-id="c5120-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-723">Il n’existe aucun destinataire.</span><span class="sxs-lookup"><span data-stu-id="c5120-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_demande de QoS WSA \_ \_ confirmée**</span><span class="sxs-lookup"><span data-stu-id="c5120-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-725">11009 (0x2B01)</span><span class="sxs-lookup"><span data-stu-id="c5120-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-726">La réserve a été confirmée.</span><span class="sxs-lookup"><span data-stu-id="c5120-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**échec d’admission de la \_ QoS WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-728">11010 (0x2B02)</span><span class="sxs-lookup"><span data-stu-id="c5120-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-729">Erreur due à un manque de ressources.</span><span class="sxs-lookup"><span data-stu-id="c5120-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**échec de la \_ stratégie de QoS WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-731">11011 (0x2B03)</span><span class="sxs-lookup"><span data-stu-id="c5120-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-732">Rejeté pour des raisons d’administration : informations d’identification incorrectes.</span><span class="sxs-lookup"><span data-stu-id="c5120-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**STYLE de qualité de service WSA non \_ \_ valide \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-734">11012 (0x2B04)</span><span class="sxs-lookup"><span data-stu-id="c5120-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-735">Style inconnu ou en conflit.</span><span class="sxs-lookup"><span data-stu-id="c5120-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objet incorrect de la QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-737">11013 (0x2B05)</span><span class="sxs-lookup"><span data-stu-id="c5120-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-738">Problème avec une partie de la mémoire tampon filterspec ou providerspecific en général.</span><span class="sxs-lookup"><span data-stu-id="c5120-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_erreur de \_ Ctrl pour le trafic de QoS WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-740">11014 (0x2B06)</span><span class="sxs-lookup"><span data-stu-id="c5120-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-741">Problème avec une partie du flowspec.</span><span class="sxs-lookup"><span data-stu-id="c5120-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ erreur générique de la QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-743">11015 (0x2B07)</span><span class="sxs-lookup"><span data-stu-id="c5120-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-744">Erreur QOS générale.</span><span class="sxs-lookup"><span data-stu-id="c5120-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-746">11016 (0x2B08)</span><span class="sxs-lookup"><span data-stu-id="c5120-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-747">Un type de service non valide ou non reconnu a été trouvé dans le flowspec.</span><span class="sxs-lookup"><span data-stu-id="c5120-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-749">11017 (0x2B09)</span><span class="sxs-lookup"><span data-stu-id="c5120-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-750">Un flowspec non valide ou incohérent a été trouvé dans la structure QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-752">11018 (0x2B0A)</span><span class="sxs-lookup"><span data-stu-id="c5120-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-753">Mémoire tampon spécifique au fournisseur QOS non valide.</span><span class="sxs-lookup"><span data-stu-id="c5120-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-755">11019 (0x2B0B)</span><span class="sxs-lookup"><span data-stu-id="c5120-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-756">Un style de filtre QOS non valide a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5120-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-758">11020 (0x2B0C)</span><span class="sxs-lookup"><span data-stu-id="c5120-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-759">Un type de filtre QOS non valide a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5120-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-761">11021 (0x2B0D)</span><span class="sxs-lookup"><span data-stu-id="c5120-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-762">Un nombre incorrect de FILTERSPECs QOS a été spécifié dans le FLOWDESCRIPTOR.</span><span class="sxs-lookup"><span data-stu-id="c5120-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-764">11022 (0x2B0E)</span><span class="sxs-lookup"><span data-stu-id="c5120-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-765">Un objet avec un champ ObjectLength non valide a été spécifié dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-767">11023 (0x2B0F)</span><span class="sxs-lookup"><span data-stu-id="c5120-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-768">Un nombre incorrect de descripteurs de workflow a été spécifié dans la structure QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-770">11024 (0x2B10)</span><span class="sxs-lookup"><span data-stu-id="c5120-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-771">Un objet non reconnu a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-773">11025 (0x2B11)</span><span class="sxs-lookup"><span data-stu-id="c5120-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-774">Un objet de stratégie non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-776">11026 (0x2B12)</span><span class="sxs-lookup"><span data-stu-id="c5120-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-777">Un descripteur de workflow QOS non valide a été trouvé dans la liste des descripteurs de Flow.</span><span class="sxs-lookup"><span data-stu-id="c5120-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-779">11027 (0x2B13)</span><span class="sxs-lookup"><span data-stu-id="c5120-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-780">Un flowspec non valide ou incohérent a été trouvé dans la mémoire tampon spécifique du fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-782">11028 (0x2B14)</span><span class="sxs-lookup"><span data-stu-id="c5120-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-783">Un FILTERSPEC non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-785">11029 (0x2B15)</span><span class="sxs-lookup"><span data-stu-id="c5120-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-786">Un objet de mode de suppression de forme non valide a été trouvé dans la mémoire tampon spécifique du fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de qualité de service WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-788">11030 (0x2B16)</span><span class="sxs-lookup"><span data-stu-id="c5120-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-789">Un objet de taux de mise en forme non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE réservée de la QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-791">11031 (0x2B17)</span><span class="sxs-lookup"><span data-stu-id="c5120-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-792">Un élément de stratégie réservée a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.</span><span class="sxs-lookup"><span data-stu-id="c5120-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**l' \_ hôte sécurisé WSA est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="c5120-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-794">11032 (0x2B18)</span><span class="sxs-lookup"><span data-stu-id="c5120-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-795">Aucun hôte de ce type n’est connu en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="c5120-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5120-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_erreur de \_ stratégie de nom d’IPSec WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5120-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5120-797">11033 (0x2B19)</span><span class="sxs-lookup"><span data-stu-id="c5120-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="c5120-798">Impossible d’ajouter la stratégie IPSEC basée sur le nom.</span><span class="sxs-lookup"><span data-stu-id="c5120-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="c5120-799">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5120-799">Requirements</span></span>



| <span data-ttu-id="c5120-800">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5120-800">Requirement</span></span> | <span data-ttu-id="c5120-801">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5120-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5120-802">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5120-802">Minimum supported client</span></span><br/> | <span data-ttu-id="c5120-803">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5120-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5120-804">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5120-804">Minimum supported server</span></span><br/> | <span data-ttu-id="c5120-805">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5120-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5120-806">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5120-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5120-807"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5120-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5120-808">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5120-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5120-809">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="c5120-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




