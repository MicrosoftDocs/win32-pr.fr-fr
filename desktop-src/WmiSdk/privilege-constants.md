---
description: Le paramètre strPrivilege de la méthode SWbemPrivilegeSet. AddAsString et le paramètre iPrivilege pour SWbemPrivilegeSet. Add requièrent des chaînes de privilège de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilège (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759766"
---
# <a name="privilege-constants"></a>Constantes de privilège

Le *paramètre strPrivilege* de la [**méthode SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) et le paramètre *iPrivilege* pour [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) requièrent des chaînes de privilège de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Pour plus d’informations sur l’utilisation des constantes de privilège, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).

Les constantes suivantes sont définies dans [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). La liste suivante comprend les constantes équivalentes pour C++ et les chaînes pour les scripts. Pour former le nom abrégé de script, supprimez le « se » et le « privilège » du nom de la constante C++.

L’exemple de code VBScript suivant montre comment activer le privilège RemoteShutdown dans un script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



De nombreuses méthodes WMI requièrent l’activation d’une ou de plusieurs autorisations. Si aucun privilège n’a été accordé à un compte, il ne peut pas être activé pour l’appel de méthode.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Constante C++ : **se créer une chaîne de \_ \_ \_ nom de jeton** : **SeCreateTokenPrivilege**

Nom abrégé du script : **Okta**

Requis pour créer un objet de jeton principal.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Constante C++ : **SeAssignPrimaryTokenPrivilege** chaîne : **SeAssignPrimaryTokenPrivilege**

Nom abrégé du script : **AssignPrimaryToken**

Requis pour remplacer un jeton au niveau du processus.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Constante C++ : **\_ Delock \_ Memory \_ Name** String : **SeLockMemoryPrivilege**

Nom abrégé du script : **LockMemory**

Requis pour verrouiller des pages en mémoire.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Constante C++ : **se augmente la chaîne de \_ \_ \_ nom de quota** : **SeIncreaseQuotaPrivilege**

Nom abrégé du script : **IncreaseQuotaPrivilege**

Requis pour ajuster les quotas de mémoire d’un processus.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ \_ nom de compte de se** -même : **SeMachineAccountPrivilege**

Nom abrégé du script : **MachineAccount**

Requis pour ajouter des stations de travail à un domaine.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ nom TCB** de la se : **SeTcbPrivilege**

Nom abrégé du script : **TCB**

Requis pour agir en tant que partie du système d’exploitation. Le détenteur fait partie de la base de l’ordinateur approuvé.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ nom de sécurité de se** : **SeSecurityPrivilege**

Nom abrégé du script : **sécurité**

Requis pour gérer l’audit et le journal de sécurité NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Constante C++ : **se \_ prendre \_ possession \_** de la chaîne de nom : **SeTakeOwnershipPrivilege**

Nom abrégé du script : **TakeOwnership**

Obligatoire pour assumer la propriété des fichiers ou d’autres objets sans avoir d' [*entrée de Access Control*](/windows/desktop/SecGloss/a-gly) dans la liste de contrôle d’accès discrétionnaire (DACL, *Discretionary Access Control List* ).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Constante C++ : **se \_ charger \_** la chaîne du pilote : **SeLoadDriverPrivilege**

Nom abrégé du script : **LoadDriver**

Requis pour charger ou décharger un pilote de périphérique.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ \_ nom de profil système se** : **SeSystemProfilePrivilege**

Nom abrégé du script : **SystemProfile**

Requis pour collecter des informations de profil sur les performances du système.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Constante C++ : chaîne de nom **\_ SystemTime de se** \_ : **SeSystemTimePrivilege**

Nom abrégé du script : **SystemTime**

Requis pour modifier l’heure système.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ \_ \_ nom de processus unique de se Prof** : **SeProfileSingleProcessPrivilege**

Nom abrégé du script : **ProfileSingleProcess**

Requis pour collecter des informations de profil pour un seul processus.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Constante C++ : chaîne de **nom de priorité de \_ \_ base se \_ \_ Inc** . : **SeIncreaseBasePriorityPrivilege**

Nom abrégé du script : **IncreaseBasePriority**

Requis pour augmenter la priorité de planification.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Constante C++ : **se créer une chaîne de \_ nom de fichier d' \_ échange \_** : **SeCreatePagefilePrivilege**

Nom abrégé du script : **CreatePagefile**

Requis pour créer un fichier d’échange.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Constante C++ : **se créer une chaîne de \_ \_ \_ nom permanente** : **SeCreatePermanentPrivilege**

Nom abrégé du script : **CreatePermanent**

Requis pour créer des objets partagés permanents.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ nom** de la sauvegarde de se : **SeBackupPrivilege**

Nom abrégé du script : **sauvegarde**

Requis pour sauvegarder des fichiers et des répertoires, quelle que soit la liste de contrôle d’accès spécifiée pour le fichier.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Constante C++ : **se \_ Restore \_ Name** String : **SeRestorePrivilege**

Nom abrégé du script : **restauration**

Requis pour restaurer des fichiers et des répertoires, quelle que soit la liste de contrôle d’accès spécifiée pour le fichier.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Constante C++ : **se \_ arrêter \_** chaîne de nom : **SeShutdownPrivilege**

Nom abrégé du script : **Shutdown**

Requis pour arrêter le système local.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ nom de débogage de se** : **SeDebugPrivilege**

Nom abrégé du script : **débogage**

Requis pour déboguer et ajuster la mémoire d’un processus appartenant à un autre compte.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ nom d’audit** de la se : **SeAuditPrivilege**

Nom abrégé du script : **audit**

Requis pour générer des entrées d’audit dans le journal de sécurité NT. Seuls les serveurs sécurisés doivent disposer de ce privilège.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Constante C++ : chaîne de nom de l' **\_ \_ environnement \_ système se** : **SeSystemEnvironmentPrivilege**

Nom abrégé du script : **SystemEnvironment**

Requis pour modifier la mémoire RAM non volatile des systèmes qui utilisent ce type de mémoire pour stocker les données de configuration.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Constante C++ : nom de la chaîne de notification de modification de la **se \_ \_ \_** : **SeChangeNotifyPrivilege**

Nom abrégé du script : **ChangeNotify**

Requis pour recevoir des notifications des modifications apportées aux fichiers ou aux répertoires et contourner les vérifications d’accès Traversal. Ce privilège est activé par défaut pour tous les utilisateurs.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Constante C++ : chaîne de **\_ \_ \_ nom d’arrêt à distance de se** : **SeRemoteShutdownPrivilege**

Nom abrégé du script : **RemoteShutdown**

Requis pour arrêter un ordinateur distant.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Constante C++ : **se \_ \_ détacher** la chaîne de nom : **SeUndockPrivilege**

Nom abrégé du script : **détacher**

Requis pour retirer un ordinateur portable d’une station d’accueil.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Constante C++ : nom de la chaîne de **\_ \_ l’agent \_ de synchronisation se** : **SeSyncAgentPrivilege**

Nom abrégé du script : **SyncAgent**

Requis pour synchroniser les données du service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Constante C++ : **se activer la chaîne de \_ \_ \_ nom de délégation** : **SeEnableDelegationPrivilege**

Nom abrégé du script : **EnableDelegation**

Requis pour permettre aux comptes d’ordinateurs et d’utilisateurs d’être approuvés pour la délégation.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Constante C++ : **se gérer la chaîne de \_ \_ \_ nom de volume** : **SeManageVolumePrivilege**

Nom abrégé du script : **ManageVolume**

Requis pour effectuer des tâches de maintenance de volume.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’API de script](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

