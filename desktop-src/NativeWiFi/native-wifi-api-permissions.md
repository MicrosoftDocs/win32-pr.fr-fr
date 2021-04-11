---
description: Autorisations de l’API WiFi Native
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Autorisations de l’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202738"
---
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="d77e0-103">Autorisations de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="d77e0-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="d77e0-104">Un appel de l’API WiFi Native peut échouer avec quand un appelant ne dispose pas des autorisations adéquates pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="d77e0-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="d77e0-105">Les autorisations sont stockées dans des [listes de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control Lists)](../secauthz/access-control-lists.md) associées à un [**\_ \_ objet sécurisable WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span><span class="sxs-lookup"><span data-stu-id="d77e0-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="d77e0-106">Pour plus d’informations sur les DACL et les objets sécurisables, consultez [Comment les DACL contrôlent l’accès à un objet](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="d77e0-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="d77e0-107">Le tableau suivant présente les fonctions WiFi natives qui utilisent des objets sécurisables pour déterminer si l’appelant dispose des autorisations suffisantes pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="d77e0-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="d77e0-108">Il montre également les objets sécurisables utilisés par chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="d77e0-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d77e0-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="d77e0-109">Function</span></span></th>
<th><span data-ttu-id="d77e0-110">Objet sécurisable</span><span class="sxs-lookup"><span data-stu-id="d77e0-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d77e0-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="d77e0-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="d77e0-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="d77e0-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d77e0-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="d77e0-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d77e0-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="d77e0-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d77e0-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="d77e0-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="d77e0-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="d77e0-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="d77e0-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="d77e0-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="d77e0-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="d77e0-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="d77e0-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="d77e0-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="d77e0-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="d77e0-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d77e0-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="d77e0-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="d77e0-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="d77e0-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d77e0-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="d77e0-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d77e0-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="d77e0-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d77e0-130">Avant que l’une des fonctions nommées ci-dessus ne termine son opération, la fonction récupère la liste DACL stockée dans l’objet sécurisable approprié.</span><span class="sxs-lookup"><span data-stu-id="d77e0-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="d77e0-131">La fonction vérifie ensuite la liste DACL pour voir si l’appelant dispose des autorisations suffisantes.</span><span class="sxs-lookup"><span data-stu-id="d77e0-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="d77e0-132">Les \* fonctions WlanGet et WlanQuery \* requièrent que la liste DACL contienne une [entrée de contrôle d’accès (ACE)](../secauthz/access-control-entries.md) qui accorde au [jeton d’accès](../secauthz/access-tokens.md) du thread appelant un \_ accès en lecture WLAN \_ à la fonction.</span><span class="sxs-lookup"><span data-stu-id="d77e0-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="d77e0-133">Les \* fonctions WlanSet nécessitent une entrée du contrôle d’accès qui accorde au jeton d’accès du thread appelant un \_ accès en écriture WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="d77e0-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="d77e0-134">Si l’appelant ne dispose pas des autorisations suffisantes, l’appel de fonction échoue avec l’erreur erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="d77e0-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="d77e0-135">Chaque objet sécurisable est associé par défaut à une liste DACL.</span><span class="sxs-lookup"><span data-stu-id="d77e0-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="d77e0-136">Les autorisations par défaut stockées dans la liste DACL peuvent être modifiées à l’aide de la fonction [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="d77e0-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="d77e0-137">Pour déterminer les droits d’utilisateur effectifs requis pour effectuer une opération sur un système particulier, appelez [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="d77e0-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="d77e0-138">Tous les profils utilisateur ont des autorisations supplémentaires associées au profil lui-même.</span><span class="sxs-lookup"><span data-stu-id="d77e0-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="d77e0-139">Les autorisations sur un profil utilisateur sont établies lorsque le profil est créé ou modifié à l’aide de [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) ou [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span><span class="sxs-lookup"><span data-stu-id="d77e0-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="d77e0-140">Le paramètre *strAllUserProfileSecurity* spécifie les autorisations requises pour modifier un profil, supprimer un profil ou se connecter à un réseau à l’aide d’un profil.</span><span class="sxs-lookup"><span data-stu-id="d77e0-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="d77e0-141">La suppression ou la modification d’un profil requiert une \_ autorisation d’accès en écriture WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="d77e0-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="d77e0-142">La connexion à un réseau à l’aide d’un profil requiert l' \_ autorisation d’accès WLAN Execute \_ .</span><span class="sxs-lookup"><span data-stu-id="d77e0-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="d77e0-143">\* \* Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 : \* \* les fonctions [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) et [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d77e0-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="d77e0-144">Le paramètre *strAllUserProfileSecurity* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d77e0-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d77e0-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d77e0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d77e0-146">Comment les DACL contrôlent l’accès à un objet</span><span class="sxs-lookup"><span data-stu-id="d77e0-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="d77e0-147">**\_objet sécurisable \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="d77e0-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
