---
title: Constantes d’informations et d’erreurs liées à EAP (Eaphosterror. h)
description: Groupes individuels de constantes d’informations et d’erreurs liées à EAP communes à toutes les technologies d’API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032950"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="4a7fb-103">Constantes d’informations et d’erreurs liées à EAP</span><span class="sxs-lookup"><span data-stu-id="4a7fb-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="4a7fb-104">Groupes individuels de constantes d’informations et d’erreurs liées à EAP communes à toutes les technologies d’API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="4a7fb-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST en \_ premier**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-107">Définit la limite des rapports d’erreurs ; toute erreur associée à EAPHost se produira entre **EAP \_ e \_ EAPHost en \_ premier** et **EAP \_ e \_ EAPHost en \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST en \_ dernier**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-110">Définit la limite des rapports d’erreurs ; toute erreur associée à EAPHost se produira entre **EAP \_ e \_ EAPHost en \_ premier** et **EAP \_ e \_ EAPHost en \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST en \_ premier**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-113">Définit la limite des rapports d’informations ; tout enregistrement d’événement d’information lié à EAPHost aura lieu entre le **\_ \_ \_ premier** et **le \_ \_ \_ dernier EAP i EAPHost**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHOST en \_ dernier**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-116">Définit la limite des rapports d’informations ; tout enregistrement d’événement d’information lié à EAPHost aura lieu entre le **\_ \_ \_ premier** et **le \_ \_ \_ dernier EAP i EAPHost**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_magasin de certificats EAP E \_ \_ \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="4a7fb-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-119">Ni l’authentificateur, ni l’homologue ne peuvent accéder au magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ méthode EAPHost E \_ EAPHost \_ non \_ installée**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="4a7fb-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-122">La méthode EAP demandée n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**réinitialisation de l’hôte de la \_ \_ \_ \_ méthode THIRDPARTY \_ EAP E EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="4a7fb-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-125">L’hôte de la méthode tierce ne répond pas et a été redémarré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ EAPQEC \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="4a7fb-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-128">EAPHost n’est pas en mesure de communiquer avec le [client de contrainte de mise en quarantaine](/windows/desktop/NAP/nap-client-architecture) EAP (QEC) sur un client de protection d' [accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP) compatible.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identité EAP \_ E \_ EAPHOST \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="4a7fb-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-131">EAPHost retourne cette erreur si l’authentificateur ne parvient pas à s’authentifier après l’envoi de l’identité d’homologue.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_échec de \_ l’authentification EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="4a7fb-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="4a7fb-134">EAPHost retourne cette erreur en cas d’échec de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_échec de \_ la \_ \_ négociation EAP \_ du protocole EAP I EAPHOST**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="4a7fb-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-137">EAPHost enregistre cet événement d’informations lorsque le client et le serveur ne sont pas configurés avec des types EAP compatibles.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ paquet non valide pour la méthode EAPHost EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="4a7fb-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-140">Une méthode EAP a reçu un paquet EAP qui ne peut pas être traité.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="4a7fb-141">Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide EAP E EAPHOST** est un paquet non valide de la **\_ méthode EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ \_ \_ paquet non valide distant EAP E EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="4a7fb-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-144">EAPHost a reçu un paquet qui ne peut pas être traité.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="4a7fb-145">Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide distant EAP E EAPHOST** est le **\_ \_ paquet EAP non valide**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ XML EAPHost non \_ \_ conforme**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="4a7fb-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-148">Échec de la validation du schéma de configuration EAPHost.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**la \_ configuration de la méthode EAP E \_ \_ \_ ne \_ \_ prend pas en charge l' \_ authentification unique**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="4a7fb-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-151">Windows 7 ou version ultérieure : la méthode EAP ne prend pas en charge l’authentification unique (SSO) pour la configuration fournie.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_opération de \_ méthode EAPHOST EAP E \_ \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="4a7fb-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-154">EAPHost retourne cette erreur lorsqu’une méthode EAP configurée ne prend pas en charge une opération demandée (appel de procédure).</span><span class="sxs-lookup"><span data-stu-id="4a7fb-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_utilisateur EAP \_ E \_ First**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-157">Définit la limite des rapports d’erreurs ; toute erreur liée à l’utilisateur se produira entre l’utilisateur **EAP \_ e \_ User \_ First** et l' **\_ utilisateur EAP e \_ \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_utilisateur EAP \_ E \_ Last**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-160">Définit la limite des rapports d’erreurs ; toute erreur liée à l’utilisateur se produira entre l’utilisateur **EAP \_ e \_ User \_ First** et l' **\_ utilisateur EAP e \_ \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**d' \_ \_ abord l’utilisateur I EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-163">Définit la limite des rapports d’informations ; toute journalisation des événements d’information liée à EAP se produira entre le **\_ \_ \_ premier utilisateur EAP i** et l' **\_ utilisateur i EAP en \_ \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_utilisateur I EAP en \_ \_ dernier**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-166">Définit la limite des rapports d’informations ; toute journalisation des événements d’information liée à EAP se produira entre le **\_ \_ \_ premier utilisateur EAP i** et l' **\_ utilisateur i EAP en \_ \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ certificat utilisateur EAP \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="4a7fb-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-169">EAPHost n’a pas pu trouver de certificat d’utilisateur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ certificat utilisateur EAP \_ E \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="4a7fb-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-172">Le certificat utilisateur pour lequel l’authentification n’est pas définie n’a pas l’utilisation de clé étendue (EKU) appropriée.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**le \_ \_ certificat utilisateur EAP E \_ \_ a expiré**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="4a7fb-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-175">EAPhost a trouvé un certificat utilisateur arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ certificat utilisateur EAP \_ E \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="4a7fb-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-178">Le certificat utilisateur utilisé pour l’authentification a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_ \_ \_ \_ autre erreur du certificat utilisateur EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="4a7fb-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-181">Une erreur inconnue s’est produite lors de l’utilisation de la certification d’utilisateur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ certificat utilisateur EAP \_ E \_ rejeté**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="4a7fb-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-184">L’authentificateur a rejeté la certification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ \_ autre erreur du compte d’utilisateur EAP I \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="4a7fb-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-187">Une erreur EAP a été reçue après un échange d’identité, indiquant la probabilité d’un problème avec le compte d’utilisateur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ informations d’identification de l’utilisateur EAP E \_ \_ rejetées**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="4a7fb-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-190">L’authentificateur a rejeté les informations d’identification de l’utilisateur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_ \_ \_ mot de passe du nom d’utilisateur E EAP \_ \_ rejeté**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="4a7fb-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-193">Windows 7 ou version ultérieure : échec de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="4a7fb-194">L’authentificateur a rejeté les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ pas \_ de \_ lecteur de carte à puce \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="4a7fb-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-197">Windows 7 ou version ultérieure : aucun lecteur de carte à puce n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_serveur EAP \_ E \_ First**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-200">Définit la limite des rapports d’erreurs ; toute erreur liée au serveur se produit entre le **\_ serveur EAP e \_ \_** et le serveur **e EAP en \_ \_ \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_dernier E \_ serveur \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-203">Définit la limite des rapports d’erreurs ; toute erreur liée au serveur se produit entre le **\_ serveur EAP e \_ \_** et le serveur **e EAP en \_ \_ \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_certificat de serveur EAP E \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="4a7fb-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-206">EAPHost n’a pas pu trouver le certificat de serveur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_certificat du serveur EAP E \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="4a7fb-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-209">Le certificat de serveur qui est l’utilisateur pour l’authentification ne dispose pas d’un ensemble d’utilisation de clé étendue (EKU) approprié.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**le \_ certificat du serveur EAP E \_ \_ \_ a expiré**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="4a7fb-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-212">EAPhost a trouvé un certificat de serveur expiré.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_certificat de \_ serveur EAP E \_ \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="4a7fb-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-215">Le certificat de serveur utilisé pour l’authentification a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ autre erreur de certificat de serveur EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="4a7fb-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-218">Une erreur inconnue s’est produite avec le certificat de serveur.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ certificat racine d’utilisateur EAP E \_ \_ \_ First**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-221">Définit la limite des rapports d’erreurs ; toute erreur liée au certificat racine de l’utilisateur se produit entre le **\_ \_ \_ \_ \_ premier** et le certificat racine de l' **utilisateur EAP e \_ \_ \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ dernier certificat racine d’utilisateur EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-224">Définit la limite des rapports d’erreurs ; toute erreur liée au certificat racine de l’utilisateur se produit entre le **\_ \_ \_ \_ \_ premier** et le certificat racine de l' **utilisateur EAP e \_ \_ \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ certificat racine utilisateur EAP E \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="4a7fb-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-227">EAPHost n’a pas pu trouver de certificat dans un magasin de certificats racines de confiance pour la validation de la certification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ certificat racine utilisateur EAP E \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="4a7fb-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-230">L’authentification a échoué car le certificat racine utilisé pour ce réseau n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**le \_ certificat racine de l’utilisateur EAP E \_ \_ \_ \_ a expiré**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="4a7fb-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-233">Le certificat racine approuvé requis pour la validation du certificat de l’utilisateur a expiré.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ First**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="4a7fb-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-236">Définit la limite des rapports d’erreurs ; toute erreur liée à un certificat racine du serveur se produit entre le certificat **\_ racine du serveur EAP e \_ \_ \_ \_** et le certificat racine du **\_ \_ serveur \_ \_ \_ EAP** e d’abord.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ dernier certificat racine du serveur EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="4a7fb-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-239">Définit la limite des rapports d’erreurs ; toute erreur liée à un certificat racine du serveur se produit entre le certificat **\_ racine du serveur EAP e \_ \_ \_ \_** et le certificat racine du **\_ \_ serveur \_ \_ \_ EAP** e d’abord.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="4a7fb-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-242">EAPHost n’a pas pu trouver de certificat racine dans un magasin de certificats racines de confiance pour la validation de la certification du serveur.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="4a7fb-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-245">L’authentification a échoué car le certificat de serveur requis pour ce réseau sur l’ordinateur serveur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a7fb-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_nom du \_ certificat racine du serveur EAP E \_ \_ \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7fb-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="4a7fb-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="4a7fb-248">L’authentification a échoué car le certificat sur l’ordinateur serveur n’a pas de nom de serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a7fb-249">Notes</span><span class="sxs-lookup"><span data-stu-id="4a7fb-249">Remarks</span></span>

<span data-ttu-id="4a7fb-250">Il existe d’autres noms pour certaines erreurs :</span><span class="sxs-lookup"><span data-stu-id="4a7fb-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="4a7fb-251">Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide EAP E EAPHOST** est un paquet non valide de la **\_ méthode EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="4a7fb-252">Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide distant EAP E EAPHOST** est le **\_ \_ paquet EAP non valide**.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7fb-253">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a7fb-253">Requirements</span></span>



| <span data-ttu-id="4a7fb-254">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a7fb-254">Requirement</span></span> | <span data-ttu-id="4a7fb-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a7fb-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7fb-256">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7fb-256">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7fb-257">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7fb-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4a7fb-258">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7fb-258">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7fb-259">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7fb-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a7fb-260">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a7fb-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7fb-261"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7fb-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7fb-262">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a7fb-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7fb-263">Constantes EAPHost communes</span><span class="sxs-lookup"><span data-stu-id="4a7fb-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

