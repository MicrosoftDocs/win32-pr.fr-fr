---
Description: Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Chaque privilège d’utilisateur inclut ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilège (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118898"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilège (autorisation)

Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Les privilèges de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.

Les fonctions qui obtiennent et ajustent les privilèges dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) utilisent le type d' [*identificateur unique local*](/windows/desktop/SecGloss/l-gly) (LUID) pour identifier les privilèges. Utilisez la fonction [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) pour déterminer le [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) sur le système local qui correspond à une constante de privilège. Utilisez la fonction [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) pour convertir un **LUID** en sa constante de chaîne correspondante.

Le système d’exploitation représente un privilège à l’aide de la chaîne qui suit « utilisateur droit » dans la colonne Description du tableau suivant. le système d’exploitation affiche les chaînes de droite de l’utilisateur dans la colonne **stratégie** du nœud **attribution des droits utilisateur** du composant logiciel enfichable sécurité locale Paramètres la console MMC (Microsoft Management Console).

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
exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) sur GitHub.

## <a name="constants"></a>Constantes



| Constante/valeur | Description | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl>Texte <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>(« SeAssignPrimaryTokenPrivilege »)</dt></dl> | Requis pour assigner le <a href="/windows/desktop/SecGloss/p-gly"><em>jeton principal</em></a> d’un processus. <br /> Droit de l’utilisateur : remplacez un jeton au niveau du processus.<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl>Texte <dt><strong>SE_AUDIT_NAME</strong></dt><dt>(« SeAuditPrivilege »)</dt></dl> | Requis pour générer des entrées de journal d’audit. Accordez ce privilège à des serveurs sécurisés. <br /> Droit d’utilisateur : générer des audits de sécurité.<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl>Texte <dt><strong>SE_BACKUP_NAME</strong></dt><dt>(« SeBackupPrivilege »)</dt></dl> | Requis pour effectuer des opérations de sauvegarde. Ce privilège force le système à accorder tout contrôle d’accès en lecture à n’importe quel fichier, quelle que soit la <a href="/windows/desktop/SecGloss/a-gly"><em>liste de contrôle d’accès</em></a> (ACL) spécifiée pour le fichier. Toute demande d’accès autre que Read est toujours évaluée avec la liste de contrôle d’accès. Ce privilège est requis par les fonctions <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> et <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>. Les droits d’accès suivants sont accordés si ce privilège est détenu :<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>Droit d’utilisateur : sauvegarde des fichiers et des répertoires.<br />si le fichier se trouve sur un lecteur amovible et que l’option « Audit des Stockage amovibles » est activée, les SE_SECURITY_NAME doivent avoir ACCESS_SYSTEM_SECURITY. | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl>Texte <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>(« SeChangeNotifyPrivilege »)</dt></dl> | Requis pour recevoir des notifications des modifications apportées aux fichiers ou aux répertoires. Ce privilège oblige également le système à ignorer toutes les vérifications d’accès Traversal. Il est activé par défaut pour tous les utilisateurs. <br /> Droit d’utilisateur : contourner la vérification de parcours.<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl>Texte <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>(« SeCreateGlobalPrivilege »)</dt></dl> | Requis pour créer des objets de mappage de fichiers nommés dans l’espace de noms global pendant les sessions des services Terminal Server. Ce privilège est activé par défaut pour les administrateurs, les services et le compte système local.<br /> Droit de l’utilisateur : créer des objets globaux.<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl>Texte <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>(« SeCreatePagefilePrivilege »)</dt></dl> | Requis pour créer un fichier d’échange. <br /> Droit d’utilisateur : créer un fichier d’échange.<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl>Texte <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>(« SeCreatePermanentPrivilege »)</dt></dl> | Requis pour créer un objet permanent. <br /> Droit d’utilisateur : créez des objets partagés permanents.<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl>Texte <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>(« SeCreateSymbolicLinkPrivilege »)</dt></dl> | Requis pour créer un lien symbolique.<br /> Droit d’utilisateur : créez des liens symboliques.<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl>Texte <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>(« SeCreateTokenPrivilege »)</dt></dl> | Requis pour créer un jeton principal. <br /> Droit d’utilisateur : créez un objet de jeton.<br /> Vous ne pouvez pas ajouter ce privilège à un compte d’utilisateur avec la stratégie « créer un objet jeton ». en outre, vous ne pouvez pas ajouter ce privilège à un processus détenu à l’aide d’api Windows. <strong>Windows Server 2003 et Windows XP avec SP1 et versions antérieures :</strong> les api Windows peuvent ajouter ce privilège à un processus détenu.<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl>Texte <dt><strong>SE_DEBUG_NAME</strong></dt><dt>(« SeDebugPrivilege »)</dt></dl> | Requis pour déboguer et ajuster la mémoire d’un processus appartenant à un autre compte. <br /> Droit de l’utilisateur : déboguer les programmes.<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl>Texte <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>(« SeDelegateSessionUserImpersonatePrivilege »)</dt></dl> | Requis pour obtenir un jeton d’emprunt d’identité pour un autre utilisateur au cours de la même session. <br /> Droit d’utilisateur : emprunter l’identité d’autres utilisateurs.<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl>Texte <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>(« SeEnableDelegationPrivilege »)</dt></dl> | Requis pour marquer les comptes d’utilisateurs et d’ordinateurs comme approuvés pour la délégation.<br /> Droit d’utilisateur : activez les comptes d’ordinateur et d’utilisateur pour qu’ils soient approuvés pour la délégation.<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl>Texte <dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>(« SeImpersonatePrivilege »)</dt></dl> | Requis pour emprunter l’identité.<br /> Droit d’utilisateur : emprunter l’identité d’un client après l’authentification.<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl>Texte <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>(« SeIncreaseBasePriorityPrivilege »)</dt></dl> | Requis pour augmenter la priorité de base d’un processus. <br /> Droit de l’utilisateur : augmenter la priorité de planification.<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl>Texte <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>(« SeIncreaseQuotaPrivilege »)</dt></dl> | Requis pour augmenter le quota affecté à un processus. <br /> Droit d’utilisateur : ajuster les quotas de mémoire pour un processus.<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl>Texte <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>(« SeIncreaseWorkingSetPrivilege »)</dt></dl> | Requis pour allouer davantage de mémoire pour les applications qui s’exécutent dans le contexte des utilisateurs.<br /> Droit d’utilisateur : augmenter une plage de travail de processus.<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl>Texte <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>(« SeLoadDriverPrivilege »)</dt></dl> | Requis pour charger ou décharger un pilote de périphérique. <br /> Droit de l’utilisateur : charger et décharger les pilotes de périphérique.<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl>Texte <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>(« SeLockMemoryPrivilege »)</dt></dl> | Requis pour verrouiller des pages physiques en mémoire. <br /> Droit de l’utilisateur : verrouiller les pages en mémoire.<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl>Texte <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>(« SeMachineAccountPrivilege »)</dt></dl> | Requis pour créer un compte d’ordinateur. <br /> Droit d’utilisateur : ajouter des stations de travail au domaine.<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl>Texte <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>(« SeManageVolumePrivilege »)</dt></dl> | Requis pour activer les privilèges de gestion du volume. <br /> Droit de l’utilisateur : gérez les fichiers sur un volume.<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl>Texte <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>(« SeProfileSingleProcessPrivilege »)</dt></dl> | Requis pour collecter des informations de profilage pour un seul processus. <br /> Droit de l’utilisateur : profiler un processus unique.<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl>Texte <dt><strong>SE_RELABEL_NAME</strong></dt><dt>(« SeRelabelPrivilege »)</dt></dl> | Requis pour modifier le niveau d’intégrité obligatoire d’un objet.<br /> Droit de l’utilisateur : modifier l’étiquette d’un objet.<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl>Texte <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>(« SeRemoteShutdownPrivilege »)</dt></dl> | Requis pour arrêter un système à l’aide d’une demande réseau. <br /> Droit de l’utilisateur : forcer l’arrêt à partir d’un système distant.<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl>Texte <dt><strong>SE_RESTORE_NAME</strong></dt><dt>(« SeRestorePrivilege »)</dt></dl> | Requis pour effectuer des opérations de restauration. Ce privilège force le système à accorder tout contrôle d’accès en écriture à n’importe quel fichier, quelle que soit la liste ACL spécifiée pour le fichier. Toute demande d’accès autre que l’écriture est toujours évaluée avec la liste de contrôle d’accès. En outre, ce privilège vous permet de définir un SID d’utilisateur ou de groupe valide comme propriétaire d’un fichier. Ce privilège est requis par la fonction <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> . Les droits d’accès suivants sont accordés si ce privilège est détenu :<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>Suppression</li></ul>Droit de l’utilisateur : restaurez les fichiers et les répertoires.<br />si le fichier se trouve sur un lecteur amovible et que l’option « Audit des Stockage amovibles » est activée, les SE_SECURITY_NAME doivent avoir ACCESS_SYSTEM_SECURITY.<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl>Texte <dt><strong>SE_SECURITY_NAME</strong></dt><dt>(« SeSecurityPrivilege »)</dt></dl> | Requis pour effectuer un certain nombre de fonctions liées à la sécurité, telles que le contrôle et l’affichage des messages d’audit. Ce privilège identifie son détenteur comme un opérateur de sécurité. <br /> Droit d’utilisateur : gérer le journal d’audit et de sécurité.<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl>Texte <dt><strong>SE_SHUTDOWN_NAME</strong></dt><dt>(« SeShutdownPrivilege »)</dt></dl> | Requis pour arrêter un système local. <br /> Droit de l’utilisateur : Arrêtez le système.<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl>Texte <dt><strong>SE_SYNC_AGENT_NAME</strong></dt><dt>(« SeSyncAgentPrivilege »)</dt></dl> | Requis pour qu’un contrôleur de domaine utilise les services de synchronisation d’annuaires <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access Protocol</em></a> . Ce privilège permet au détenteur de lire tous les objets et propriétés de l’annuaire, quelle que soit la protection sur les objets et les propriétés. Par défaut, il est affecté aux comptes administrateur et LocalSystem sur les contrôleurs de domaine. <br /> Droit de l’utilisateur : synchroniser les données du service d’annuaire.<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl>Texte <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt><dt>(« SeSystemEnvironmentPrivilege »)</dt></dl> | Requis pour modifier la mémoire RAM non volatile des systèmes qui utilisent ce type de mémoire pour stocker les informations de configuration. <br /> Droit de l’utilisateur : modifier les valeurs de l’environnement du microprogramme.<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl>Texte <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt><dt>(« SeSystemProfilePrivilege »)</dt></dl> | Requis pour collecter des informations de profilage pour l’ensemble du système. <br /> Droit de l’utilisateur : profiler les performances du système.<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl>Texte <dt><strong>SE_SYSTEMTIME_NAME</strong></dt><dt>(« SeSystemTimePrivilege »)</dt></dl> | Requis pour modifier l’heure système. <br /> Droit de l’utilisateur : modifier l’heure système.<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl>Texte <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt><dt>(« SeTakeOwnershipPrivilege »)</dt></dl> | Requis pour prendre possession d’un objet sans disposer d’un accès discrétionnaire. Ce privilège permet de définir la valeur owner uniquement sur les valeurs que le détenteur peut légitimement attribuer en tant que propriétaire d’un objet. <br /> Droit d’utilisateur : appropriation de fichiers ou d’autres objets.<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl>Texte <dt><strong>SE_TCB_NAME</strong></dt><dt>(« SeTcbPrivilege »)</dt></dl> | Ce privilège identifie son détenteur dans le cadre de la base de l’ordinateur approuvé. Certains sous-systèmes protégés approuvés bénéficient de ce privilège. <br /> Droit de l’utilisateur : agir en tant que partie du système d’exploitation.<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl>Texte <dt><strong>SE_TIME_ZONE_NAME</strong></dt><dt>(« SeTimeZonePrivilege »)</dt></dl> | Requis pour ajuster le fuseau horaire associé à l’horloge interne de l’ordinateur.<br /> Droit de l’utilisateur : modifiez le fuseau horaire.<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl>Texte <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt><dt>(« SeTrustedCredManAccessPrivilege »)</dt></dl> | Requis pour accéder au gestionnaire d’informations d’identification en tant qu’appelant approuvé.<br /> Droit de l’utilisateur : accédez au gestionnaire des informations d’identification en tant qu’appelant approuvé.<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl>Texte <dt><strong>SE_UNDOCK_NAME</strong></dt><dt>(« SeUndockPrivilege »)</dt></dl> | Requis pour déconnecter un ordinateur portable.<br /> Droit d’utilisateur : supprimer l’ordinateur de la station d’accueil.<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl>Texte <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt><dt>(« SeUnsolicitedInputPrivilege »)</dt></dl> | Requis pour lire une entrée non sollicitée à partir d’un périphérique <a href="/windows/desktop/SecGloss/t-gly"><em>Terminal</em></a> .<br /> Droit de l’utilisateur : non applicable.<br /> | 




## <a name="remarks"></a>Notes

Les constantes de privilège sont définies en tant que chaînes dans Winnt. h. par exemple, la \_ constante SE AUDIT \_ NAME est définie sur « SeAuditPrivilege ».

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Privilèges](privileges.md)
</dt> </dl>

