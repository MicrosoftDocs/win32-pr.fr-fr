---
Description: Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Chaque privilège d’utilisateur inclut ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilège (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327154"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilège (autorisation)

Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Les privilèges de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.

Les fonctions qui obtiennent et ajustent les privilèges dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) utilisent le type d' [*identificateur unique local*](/windows/desktop/SecGloss/l-gly) (LUID) pour identifier les privilèges. Utilisez la fonction [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) pour déterminer le [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) sur le système local qui correspond à une constante de privilège. Utilisez la fonction [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) pour convertir un **LUID** en sa constante de chaîne correspondante.

Le système d’exploitation représente un privilège à l’aide de la chaîne qui suit « utilisateur droit » dans la colonne Description du tableau suivant. Le système d’exploitation affiche les chaînes de droite de l’utilisateur dans la colonne **stratégie** du nœud **attribution des droits utilisateur** du composant logiciel enfichable MMC (Microsoft Management Console) paramètres de sécurité locale.

## <a name="example"></a>Exemple

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) sur GitHub.

## <a name="constants"></a>Constantes


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_ASSIGNPRIMARYTOKEN_NAME ( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour assigner le <a href="/windows/desktop/SecGloss/p-gly"><em>jeton principal</em></a> d’un processus. <br/> Droit de l’utilisateur : remplacez un jeton au niveau du processus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_AUDIT_NAME ( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour générer des entrées de journal d’audit. Accordez ce privilège à des serveurs sécurisés. <br/> Droit d’utilisateur : générer des audits de sécurité.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_BACKUP_NAME ( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour effectuer des opérations de sauvegarde. Ce privilège force le système à accorder tout contrôle d’accès en lecture à n’importe quel fichier, quelle que soit la <a href="/windows/desktop/SecGloss/a-gly"><em>liste de contrôle d’accès</em></a> (ACL) spécifiée pour le fichier. Toute demande d’accès autre que Read est toujours évaluée avec la liste de contrôle d’accès. Ce privilège est requis par les fonctions <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> et <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>. Les droits d’accès suivants sont accordés si ce privilège est détenu :<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Droit d’utilisateur : sauvegarde des fichiers et des répertoires.<br/>Si le fichier se trouve sur un lecteur amovible et que l’option « auditer le stockage amovible » est activée, le SE_SECURITY_NAME doit avoir ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CHANGE_NOTIFY_NAME ( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour recevoir des notifications des modifications apportées aux fichiers ou aux répertoires. Ce privilège oblige également le système à ignorer toutes les vérifications d’accès Traversal. Il est activé par défaut pour tous les utilisateurs. <br/> Droit d’utilisateur : contourner la vérification de parcours.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CREATE_GLOBAL_NAME ( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer des objets de mappage de fichiers nommés dans l’espace de noms global pendant les sessions des services Terminal Server. Ce privilège est activé par défaut pour les administrateurs, les services et le compte système local.<br/> Droit de l’utilisateur : créer des objets globaux.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CREATE_PAGEFILE_NAME ( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer un fichier d’échange. <br/> Droit d’utilisateur : créer un fichier d’échange.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CREATE_PERMANENT_NAME ( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer un objet permanent. <br/> Droit d’utilisateur : créez des objets partagés permanents.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CREATE_SYMBOLIC_LINK_NAME ( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer un lien symbolique.<br/> Droit d’utilisateur : créez des liens symboliques.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_CREATE_TOKEN_NAME ( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer un jeton principal. <br/> Droit d’utilisateur : créez un objet de jeton.<br/> Vous ne pouvez pas ajouter ce privilège à un compte d’utilisateur avec la &quot; stratégie créer un objet jeton &quot; . En outre, vous ne pouvez pas ajouter ce privilège à un processus détenu à l’aide des API Windows. <strong>Windows Server 2003 et Windows XP avec SP1 et versions antérieures :</strong> Les API Windows peuvent ajouter ce privilège à un processus détenu.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_DEBUG_NAME ( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour déboguer et ajuster la mémoire d’un processus appartenant à un autre compte. <br/> Droit de l’utilisateur : déboguer les programmes.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME ( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour obtenir un jeton d’emprunt d’identité pour un autre utilisateur au cours de la même session. <br/> Droit d’utilisateur : emprunter l’identité d’autres utilisateurs.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_ENABLE_DELEGATION_NAME ( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour marquer les comptes d’utilisateurs et d’ordinateurs comme approuvés pour la délégation.<br/> Droit d’utilisateur : activez les comptes d’ordinateur et d’utilisateur pour qu’ils soient approuvés pour la délégation.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_IMPERSONATE_NAME ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour emprunter l’identité.<br/> Droit d’utilisateur : emprunter l’identité d’un client après l’authentification.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_INC_BASE_PRIORITY_NAME ( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour augmenter la priorité de base d’un processus. <br/> Droit de l’utilisateur : augmenter la priorité de planification.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_INCREASE_QUOTA_NAME ( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour augmenter le quota affecté à un processus. <br/> Droit d’utilisateur : ajuster les quotas de mémoire pour un processus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_INC_WORKING_SET_NAME ( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour allouer davantage de mémoire pour les applications qui s’exécutent dans le contexte des utilisateurs.<br/> Droit d’utilisateur : augmenter une plage de travail de processus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_LOAD_DRIVER_NAME ( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour charger ou décharger un pilote de périphérique. <br/> Droit de l’utilisateur : charger et décharger les pilotes de périphérique.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_LOCK_MEMORY_NAME ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour verrouiller des pages physiques en mémoire. <br/> Droit de l’utilisateur : verrouiller les pages en mémoire.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_MACHINE_ACCOUNT_NAME ( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour créer un compte d’ordinateur. <br/> Droit d’utilisateur : ajouter des stations de travail au domaine.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_MANAGE_VOLUME_NAME ( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour activer les privilèges de gestion du volume. <br/> Droit de l’utilisateur : gérez les fichiers sur un volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_PROF_SINGLE_PROCESS_NAME ( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour collecter des informations de profilage pour un seul processus. <br/> Droit de l’utilisateur : profiler un processus unique.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_RELABEL_NAME ( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour modifier le niveau d’intégrité obligatoire d’un objet.<br/> Droit de l’utilisateur : modifier l’étiquette d’un objet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_REMOTE_SHUTDOWN_NAME ( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour arrêter un système à l’aide d’une demande réseau. <br/> Droit de l’utilisateur : forcer l’arrêt à partir d’un système distant.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_RESTORE_NAME ( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour effectuer des opérations de restauration. Ce privilège force le système à accorder tout contrôle d’accès en écriture à n’importe quel fichier, quelle que soit la liste ACL spécifiée pour le fichier. Toute demande d’accès autre que l’écriture est toujours évaluée avec la liste de contrôle d’accès. En outre, ce privilège vous permet de définir un SID d’utilisateur ou de groupe valide comme propriétaire d’un fichier. Ce privilège est requis par la fonction <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> . Les droits d’accès suivants sont accordés si ce privilège est détenu :<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Droit de l’utilisateur : restaurez les fichiers et les répertoires.<br/>Si le fichier se trouve sur un lecteur amovible et que l’option « auditer le stockage amovible » est activée, le SE_SECURITY_NAME doit avoir ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SECURITY_NAME ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour effectuer un certain nombre de fonctions liées à la sécurité, telles que le contrôle et l’affichage des messages d’audit. Ce privilège identifie son détenteur comme un opérateur de sécurité. <br/> Droit d’utilisateur : gérer le journal d’audit et de sécurité.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SHUTDOWN_NAME ( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour arrêter un système local. <br/> Droit de l’utilisateur : Arrêtez le système.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SYNC_AGENT_NAME ( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour qu’un contrôleur de domaine utilise les services de synchronisation d’annuaires <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access Protocol</em></a> . Ce privilège permet au détenteur de lire tous les objets et propriétés de l’annuaire, quelle que soit la protection sur les objets et les propriétés. Par défaut, il est affecté aux comptes administrateur et LocalSystem sur les contrôleurs de domaine. <br/> Droit de l’utilisateur : synchroniser les données du service d’annuaire.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SYSTEM_ENVIRONMENT_NAME ( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour modifier la mémoire RAM non volatile des systèmes qui utilisent ce type de mémoire pour stocker les informations de configuration. <br/> Droit de l’utilisateur : modifier les valeurs de l’environnement du microprogramme.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SYSTEM_PROFILE_NAME ( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour collecter des informations de profilage pour l’ensemble du système. <br/> Droit de l’utilisateur : profiler les performances du système.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_SYSTEMTIME_NAME ( &quot; SeSystemTimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour modifier l’heure système. <br/> Droit de l’utilisateur : modifier l’heure système.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_TAKE_OWNERSHIP_NAME ( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour prendre possession d’un objet sans disposer d’un accès discrétionnaire. Ce privilège permet de définir la valeur owner uniquement sur les valeurs que le détenteur peut légitimement attribuer en tant que propriétaire d’un objet. <br/> Droit d’utilisateur : appropriation de fichiers ou d’autres objets.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_TCB_NAME ( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Ce privilège identifie son détenteur dans le cadre de la base de l’ordinateur approuvé. Certains sous-systèmes protégés approuvés bénéficient de ce privilège. <br/> Droit de l’utilisateur : agir en tant que partie du système d’exploitation.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_TIME_ZONE_NAME ( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour ajuster le fuseau horaire associé à l’horloge interne de l’ordinateur.<br/> Droit de l’utilisateur : modifiez le fuseau horaire.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_TRUSTED_CREDMAN_ACCESS_NAME ( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour accéder au gestionnaire d’informations d’identification en tant qu’appelant approuvé.<br/> Droit de l’utilisateur : accédez au gestionnaire des informations d’identification en tant qu’appelant approuvé.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_UNDOCK_NAME ( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour déconnecter un ordinateur portable.<br/> Droit d’utilisateur : supprimer l’ordinateur de la station d’accueil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong></strong></dt> <dt>Texte SE_UNSOLICITED_INPUT_NAME ( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requis pour lire une entrée non sollicitée à partir d’un périphérique <a href="/windows/desktop/SecGloss/t-gly"><em>Terminal</em></a> .<br/> Droit de l’utilisateur : non applicable.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

Les constantes de privilège sont définies en tant que chaînes dans Winnt. h. Par exemple, la \_ constante de nom d’audit se \_ est définie en tant que « SeAuditPrivilege ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Privilèges](privileges.md)
</dt> </dl>

