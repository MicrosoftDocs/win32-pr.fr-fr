---
title: Indicateurs de méthode EAP (Eaptypes. h)
description: Les indicateurs de méthode EAP sont utilisés dans les fonctions du demandeur, de l’authentificateur et de l’homologue pour spécifier les comportements d’une session d’authentification EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464178"
---
# <a name="eap-method-flags"></a><span data-ttu-id="a8508-103">Indicateurs de méthode EAP</span><span class="sxs-lookup"><span data-stu-id="a8508-103">EAP Method Flags</span></span>

<span data-ttu-id="a8508-104">Les indicateurs de méthode EAP sont utilisés dans les fonctions du demandeur, de l’authentificateur et de l’homologue pour spécifier les comportements d’une session d’authentification EAP.</span><span class="sxs-lookup"><span data-stu-id="a8508-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="a8508-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Indicateur EAP \_ Reserved1**</span><span class="sxs-lookup"><span data-stu-id="a8508-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8508-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="a8508-107">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-107">Do not use.</span></span> <span data-ttu-id="a8508-108">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_indicateur EAP \_ non \_ interactif**</span><span class="sxs-lookup"><span data-stu-id="a8508-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a8508-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="a8508-111">N’affiche pas d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8508-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**connexion de l' \_ indicateur EAP \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a8508-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="a8508-114">Les données utilisateur ont été obtenues à partir de l’ouverture de session Windows.</span><span class="sxs-lookup"><span data-stu-id="a8508-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**Aperçu de l' \_ indicateur EAP \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a8508-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="a8508-117">Affiche l’interface utilisateur des informations d’identification avant l’authentification, même si des informations d’identification mises en cache sont présentes.</span><span class="sxs-lookup"><span data-stu-id="a8508-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**Protocole EAP \_ INDICATEUR \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="a8508-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8508-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="a8508-120">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-120">Do not use.</span></span> <span data-ttu-id="a8508-121">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**authentification de machine de l' \_ indicateur EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a8508-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="a8508-124">Utiliser l’authentification au niveau de l’ordinateur ; Si vous ne définissez pas cet indicateur, l’authentification au niveau de l’utilisateur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a8508-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_indicateur EAP \_ \_ accès invité**</span><span class="sxs-lookup"><span data-stu-id="a8508-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="a8508-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a8508-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="a8508-127">Indique une demande de fourniture d’un accès invité.</span><span class="sxs-lookup"><span data-stu-id="a8508-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Indicateur EAP \_ Reserved3**</span><span class="sxs-lookup"><span data-stu-id="a8508-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a8508-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="a8508-130">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-130">Do not use.</span></span> <span data-ttu-id="a8508-131">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**Protocole EAP \_ INDICATEUR \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="a8508-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="a8508-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="a8508-134">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-134">Do not use.</span></span> <span data-ttu-id="a8508-135">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_ \_ reprise de la \_ \_ mise en veille de l’indicateur EAP**</span><span class="sxs-lookup"><span data-stu-id="a8508-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="a8508-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="a8508-138">Indique qu’il s’agit du premier appel après la reprise de l’activité de l’ordinateur à partir d’une période de mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="a8508-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**Protocole EAP \_ INDICATEUR \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="a8508-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="a8508-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="a8508-141">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-141">Do not use.</span></span> <span data-ttu-id="a8508-142">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Indicateur EAP \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="a8508-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="a8508-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="a8508-145">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-145">Do not use.</span></span> <span data-ttu-id="a8508-146">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ authentification complète de l’indicateur EAP \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="a8508-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-149">Indique que les méthodes de tunnel doivent effectuer une authentification complète au lieu d’une version abrégée, telle que la [reconnexion rapide PEAP (Protected EAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="a8508-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**l' \_ indicateur EAP \_ préfère les \_ \_ informations d’identification Alt**</span><span class="sxs-lookup"><span data-stu-id="a8508-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="a8508-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-152">Indique que les informations d’identification passées dans [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) sont préférées à toutes les autres formes de récupération des informations d’identification, même si les données de configuration transmises à la fonction actuelle demandent un mode de récupération des informations d’identification différent.</span><span class="sxs-lookup"><span data-stu-id="a8508-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="a8508-153">Cet indicateur est utilisé uniquement par [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="a8508-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Indicateur EAP \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="a8508-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="a8508-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-156">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-156">Do not use.</span></span> <span data-ttu-id="a8508-157">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**changement d’état d’intégrité de l' \_ indicateur d’homologue EAP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="a8508-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-160">Indique que la nouvelle authentification est un rappel de [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP); La protection d’accès réseau a initié la session d’authentification car l’état d’intégrité a changé.</span><span class="sxs-lookup"><span data-stu-id="a8508-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="a8508-161">Cet indicateur doit être envoyé uniquement lorsque cette fonction est appelée par un rappel [*NotificationHandler*](/previous-versions/windows/desktop/api) spécifique à la protection d’accès réseau fourni par un appel précédent à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a8508-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ \_ interface utilisateur supprimer l’indicateur EAP**</span><span class="sxs-lookup"><span data-stu-id="a8508-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="a8508-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-164">Continuer l’authentification avec les informations disponibles.</span><span class="sxs-lookup"><span data-stu-id="a8508-164">Continue authentication with available information.</span></span> <span data-ttu-id="a8508-165">Si l’authentification ne peut pas se poursuivre, échoue.</span><span class="sxs-lookup"><span data-stu-id="a8508-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_pré- \_ ouverture de \_ session de l’indicateur EAP**</span><span class="sxs-lookup"><span data-stu-id="a8508-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="a8508-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-168">Indique qu’EAPHost doit fournir une authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="a8508-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="a8508-169">Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="a8508-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**authentification de l’utilisateur de l' \_ indicateur EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8508-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="a8508-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-172">Indique l’authentification au niveau de l’utilisateur pour les méthodes héritées qui ne peuvent pas définir l’authentification de l' **\_ \_ ordinateur \_ indicateur EAP**.</span><span class="sxs-lookup"><span data-stu-id="a8508-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_indicateur EAP \_ CONFG \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="a8508-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="a8508-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="a8508-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-175">Indique que la configuration peut être affichée mais pas mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a8508-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8508-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Indicateur EAP \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="a8508-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8508-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="a8508-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="a8508-178">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8508-178">Do not use.</span></span> <span data-ttu-id="a8508-179">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8508-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8508-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8508-180">Requirements</span></span>



| <span data-ttu-id="a8508-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8508-181">Requirement</span></span> | <span data-ttu-id="a8508-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8508-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8508-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8508-183">Minimum supported client</span></span><br/> | <span data-ttu-id="a8508-184">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8508-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8508-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8508-185">Minimum supported server</span></span><br/> | <span data-ttu-id="a8508-186">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8508-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8508-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8508-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8508-188"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8508-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8508-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8508-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8508-190">Constantes EAPHost communes</span><span class="sxs-lookup"><span data-stu-id="a8508-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

