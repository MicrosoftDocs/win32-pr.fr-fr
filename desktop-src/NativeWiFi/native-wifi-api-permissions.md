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
# <a name="native-wifi-api-permissions"></a>Autorisations de l’API WiFi Native

Un appel de l’API WiFi Native peut échouer avec quand un appelant ne dispose pas des autorisations adéquates pour effectuer l’opération demandée.

Les autorisations sont stockées dans des [listes de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control Lists)](../secauthz/access-control-lists.md) associées à un [**\_ \_ objet sécurisable WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object). Pour plus d’informations sur les DACL et les objets sécurisables, consultez [Comment les DACL contrôlent l’accès à un objet](../secauthz/how-dacls-control-access-to-an-object.md).

Le tableau suivant présente les fonctions WiFi natives qui utilisent des objets sécurisables pour déterminer si l’appelant dispose des autorisations suffisantes pour effectuer l’opération demandée. Il montre également les objets sécurisables utilisés par chaque fonction.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonction</th>
<th>Objet sécurisable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Avant que l’une des fonctions nommées ci-dessus ne termine son opération, la fonction récupère la liste DACL stockée dans l’objet sécurisable approprié. La fonction vérifie ensuite la liste DACL pour voir si l’appelant dispose des autorisations suffisantes. Les \* fonctions WlanGet et WlanQuery \* requièrent que la liste DACL contienne une [entrée de contrôle d’accès (ACE)](../secauthz/access-control-entries.md) qui accorde au [jeton d’accès](../secauthz/access-tokens.md) du thread appelant un \_ accès en lecture WLAN \_ à la fonction. Les \* fonctions WlanSet nécessitent une entrée du contrôle d’accès qui accorde au jeton d’accès du thread appelant un \_ accès en écriture WLAN \_ . Si l’appelant ne dispose pas des autorisations suffisantes, l’appel de fonction échoue avec l’erreur erreur \_ accès \_ refusé.

Chaque objet sécurisable est associé par défaut à une liste DACL. Les autorisations par défaut stockées dans la liste DACL peuvent être modifiées à l’aide de la fonction [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . Pour déterminer les droits d’utilisateur effectifs requis pour effectuer une opération sur un système particulier, appelez [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Tous les profils utilisateur ont des autorisations supplémentaires associées au profil lui-même. Les autorisations sur un profil utilisateur sont établies lorsque le profil est créé ou modifié à l’aide de [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) ou [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). Le paramètre *strAllUserProfileSecurity* spécifie les autorisations requises pour modifier un profil, supprimer un profil ou se connecter à un réseau à l’aide d’un profil. La suppression ou la modification d’un profil requiert une \_ autorisation d’accès en écriture WLAN \_ . La connexion à un réseau à l’aide d’un profil requiert l' \_ autorisation d’accès WLAN Execute \_ .

* * Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 : * * les fonctions [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) et [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) ne sont pas prises en charge. Le paramètre *strAllUserProfileSecurity* n’est pas utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment les DACL contrôlent l’accès à un objet](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_objet sécurisable \_ WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
