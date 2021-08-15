---
description: Représente des catégories et des sous-catégories d’événements de stratégie d’audit.
ms.assetid: e3b12139-947d-4922-91fd-f9833c069011
title: Constantes d’audit (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316dcd969ebba3cf571c7851a6d628617e4a261aea83c26b2524e3edcc0e4b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784307"
---
# <a name="auditing-constants"></a>Audit des constantes

Les constantes suivantes représentent des catégories et des sous-catégories d’événements de stratégie d’audit.

Les constantes suivantes représentent des catégories d’événements de stratégie d’audit. Ces constantes sont définies en tant que structures **GUID** dans Ntsecapi. h.

<dl> <dt>

<span id="Audit_System"></span><span id="audit_system"></span><span id="AUDIT_SYSTEM"></span>**Système d’audit \_**
</dt> <dd> <dl> <dt>

69979848-797a-11d9-bed3-505054503030
</dt> <dt>



L’audit tente d’arrêter ou de redémarrer l’ordinateur. En outre, les événements d’audit qui affectent la sécurité du système ou le journal de sécurité.


</dt> </dl> </dd> <dt>

<span id="Audit_Logon"></span><span id="audit_logon"></span><span id="AUDIT_LOGON"></span>**Auditer la \_ connexion**
</dt> <dd> <dl> <dt>

69979849-797a-11d9-bed3-505054503030
</dt> <dt>



Les tentatives d’audit pour se connecter ou se déconnecter du système. En outre, l’audit tente d’établir une connexion réseau.


</dt> </dl> </dd> <dt>

<span id="Audit_ObjectAccess"></span><span id="audit_objectaccess"></span><span id="AUDIT_OBJECTACCESS"></span>**Auditer \_ ObjectAccess**
</dt> <dd> <dl> <dt>

6997984a-797a-11d9-bed3-505054503030
</dt> <dt>



Audite les tentatives d’accès aux objets sécurisables.


</dt> </dl> </dd> <dt>

<span id="Audit_PrivilegeUse"></span><span id="audit_privilegeuse"></span><span id="AUDIT_PRIVILEGEUSE"></span>**Auditer \_ PrivilegeUse**
</dt> <dd> <dl> <dt>

6997984b-797a-11d9-bed3-505054503030
</dt> <dt>



Audite les tentatives d’utilisation [*des privilèges*](/windows/desktop/SecGloss/p-gly).


</dt> </dl> </dd> <dt>

<span id="Audit_DetailedTracking"></span><span id="audit_detailedtracking"></span><span id="AUDIT_DETAILEDTRACKING"></span>**Auditer \_ DetailedTracking**
</dt> <dd> <dl> <dt>

6997984c-797a-11d9-bed3-505054503030
</dt> <dt>



Événements spécifiques à l’audit, tels que l’activation de programme, certaines formes de duplication de handle, l’accès indirect à un objet et la sortie de processus.


</dt> </dl> </dd> <dt>

<span id="Audit_PolicyChange"></span><span id="audit_policychange"></span><span id="AUDIT_POLICYCHANGE"></span>**Auditer \_ PolicyChange**
</dt> <dd> <dl> <dt>

6997984d-797a-11d9-bed3-505054503030
</dt> <dt>



Les tentatives d’audit de modification des règles d’objet de [**stratégie**](/windows/desktop/SecMgmt/the-policy-object-type) .


</dt> </dl> </dd> <dt>

<span id="Audit_AccountManagement"></span><span id="audit_accountmanagement"></span><span id="AUDIT_ACCOUNTMANAGEMENT"></span>**Audit \_ AccountManagement**
</dt> <dd> <dl> <dt>

6997984e-797a-11d9-bed3-505054503030
</dt> <dt>



Les tentatives d’audit pour créer, supprimer ou modifier des comptes d’utilisateur ou de groupe. En outre, auditer les modifications de mot de passe.


</dt> </dl> </dd> <dt>

<span id="Audit_DirectoryServiceAccess"></span><span id="audit_directoryserviceaccess"></span><span id="AUDIT_DIRECTORYSERVICEACCESS"></span>**Auditer \_ DirectoryServiceAccess**
</dt> <dd> <dl> <dt>

6997984f-797a-11d9-bed3-505054503030
</dt> <dt>



Audite les tentatives d’accès au service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="Audit_AccountLogon"></span><span id="audit_accountlogon"></span><span id="AUDIT_ACCOUNTLOGON"></span>**Auditer \_ AccountLogon**
</dt> <dd> <dl> <dt>

69979850-797a-11d9-bed3-505054503030
</dt> <dt>



Auditez les tentatives de connexion par compte privilégié qui se connecte au contrôleur de domaine. Ces événements d’audit sont générés lorsque le [*Centre de distribution de clés*](/windows/desktop/SecGloss/k-gly) Kerberos (KDC) ouvre une session sur le contrôleur de domaine.


</dt> </dl> </dd> </dl>

Les constantes suivantes représentent des sous-catégories d’événements de stratégie d’audit. Ces constantes sont définies en tant que structures **GUID** dans Ntsecapi. h.

<dl> <span id="Audit_System_SecurityStateChange"></span><span id="audit_system_securitystatechange"></span><span id="AUDIT_SYSTEM_SECURITYSTATECHANGE"></span>**Audit \_ System \_ SecurityStateChange** (0cce9210-69ae-11d9-bed3-505054503030) <span id="Audit_System_SecuritySubsystemExtension"></span> <span id="audit_system_securitysubsystemextension"></span> <span id="AUDIT_SYSTEM_SECURITYSUBSYSTEMEXTENSION"></span> **audit \_ System \_ SecuritySubsystemExtension** (0cce9211-69ae-11d9-bed3-505054503030) audit System <span id="Audit_System_Integrity"></span> <span id="audit_system_integrity"></span> <span id="AUDIT_SYSTEM_INTEGRITY"></span> **\_ \_ Integration** (0cce9212-69ae-11d9-bed3-505054503030) audit System <span id="Audit_System_IPSecDriverEvents"></span> <span id="audit_system_ipsecdriverevents"></span> <span id="AUDIT_SYSTEM_IPSECDRIVEREVENTS"></span> **\_ \_ IPSecDriverEvents** (0cce9213-69ae-11d9-bed3-505054503030) audit <span id="Audit_System_Others"></span> <span id="audit_system_others"></span> <span id="AUDIT_SYSTEM_OTHERS"></span> **\_ System \_ others** (0cce9214-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_Logon"></span> <span id="audit_logon_logon"></span> <span id="AUDIT_LOGON_LOGON"></span> **audit Logon \_ \_ Logon** (0cce9215-69ae-11d9-bed3-505054503030) audit Logon <span id="Audit_Logon_Logoff"></span> <span id="audit_logon_logoff"></span> <span id="AUDIT_LOGON_LOGOFF"></span> **\_ \_ Logoff** (0cce9216-69ae-11d9-bed3-505054503030) audit Logon <span id="Audit_Logon_AccountLockout"></span> <span id="audit_logon_accountlockout"></span> <span id="AUDIT_LOGON_ACCOUNTLOCKOUT"></span> **\_ \_ AccountLockout** (0cce9217-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecMainMode"></span> <span id="audit_logon_ipsecmainmode"></span> <span id="AUDIT_LOGON_IPSECMAINMODE"></span> **audit \_ Logon \_ IPSecMainMode** (0cce9218-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecQuickMode"></span> <span id="audit_logon_ipsecquickmode"></span> <span id="AUDIT_LOGON_IPSECQUICKMODE"></span> **Audit \_ Logon \_ IPSecQuickMode** (0cce9219-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecUserMode"></span> <span id="audit_logon_ipsecusermode"></span> <span id="AUDIT_LOGON_IPSECUSERMODE"></span> **audit \_ Logon \_ IPSecUserMode** (0cce921a-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_SpecialLogon"></span> <span id="audit_logon_speciallogon"></span> <span id="AUDIT_LOGON_SPECIALLOGON"></span> **audit \_ Logon \_ SpecialLogon** (0cce921b-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_Others"></span> <span id="audit_logon_others"></span> <span id="AUDIT_LOGON_OTHERS"></span> **audit \_ Logon \_ other** (0cce921c-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FileSystem"></span> <span id="audit_objectaccess_filesystem"></span> <span id="AUDIT_OBJECTACCESS_FILESYSTEM"></span> **audit \_ ObjectAccess \_ FileSystem** (0cce921d-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Registry"></span> <span id="audit_objectaccess_registry"></span> <span id="AUDIT_OBJECTACCESS_REGISTRY"></span> **audit \_ ObjectAccess \_ Registry** (0cce921e-69ae-11d9-bed3-505054503030) audit ObjectAccess <span id="Audit_ObjectAccess_Kernel"></span> <span id="audit_objectaccess_kernel"></span> <span id="AUDIT_OBJECTACCESS_KERNEL"></span> **\_ \_ kernel** (0cce921f-69ae-11d9-bed3-505054503030) audit ObjectAccess <span id="Audit_ObjectAccess_Sam"></span> <span id="audit_objectaccess_sam"></span> <span id="AUDIT_OBJECTACCESS_SAM"></span> **\_ \_ Sam** (0cce9220-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_CertificationServices"></span> <span id="audit_objectaccess_certificationservices"></span> <span id="AUDIT_OBJECTACCESS_CERTIFICATIONSERVICES"></span> **audit \_ ObjectAccess \_ CertificationServices** ( 0cce9221-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_ApplicationGenerated"></span> <span id="audit_objectaccess_applicationgenerated"></span> <span id="AUDIT_OBJECTACCESS_APPLICATIONGENERATED"></span> **audit \_ ObjectAccess \_ ApplicationGenerated** (0cce9222-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Handle"></span> <span id="audit_objectaccess_handle"></span> <span id="AUDIT_OBJECTACCESS_HANDLE"></span> **audit \_ ObjectAccess \_ handle** (0cce9223-69ae-11d9-bed3-505054503030) audit <span id="Audit_ObjectAccess_Share"></span> <span id="audit_objectaccess_share"></span> <span id="AUDIT_OBJECTACCESS_SHARE"></span> **\_ ObjectAccess \_ share** (0cce9224-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FirewallPacketDrops"></span> <span id="audit_objectaccess_firewallpacketdrops"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLPACKETDROPS"></span> **audit \_ ObjectAccess \_ FirewallPacketDrops** (0cce9225-69ae-11d9-bed3-505054503030) audit <span id="Audit_ObjectAccess_FirewallConnection"></span> <span id="audit_objectaccess_firewallconnection"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLCONNECTION"></span> **\_ ObjectAccess \_ FirewallConnection** (0cce9226-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Other"></span> <span id="audit_objectaccess_other"></span> <span id="AUDIT_OBJECTACCESS_OTHER"></span> **audit \_ ObjectAccess \_ other** (0cce9227-69ae-11d9-bed3-505054503030) audit PrivilegeUse <span id="Audit_PrivilegeUse_Sensitive"></span> <span id="audit_privilegeuse_sensitive"></span> <span id="AUDIT_PRIVILEGEUSE_SENSITIVE"></span> **\_ \_ sensitive** (0cce9228-69ae-11d9-bed3-505054503030 <span id="Audit_PrivilegeUse_NonSensitive"></span> <span id="audit_privilegeuse_nonsensitive"></span> <span id="AUDIT_PRIVILEGEUSE_NONSENSITIVE"></span> **\_ ) \_ audit PrivilegeUse** Audit 0cce9229-69ae-11d9-bed3-505054503030 (non sensible) audit <span id="Audit_PrivilegeUse_Others"></span> <span id="audit_privilegeuse_others"></span> <span id="AUDIT_PRIVILEGEUSE_OTHERS"></span> **\_ PrivilegeUse \_ others** (0cce922a-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessCreation"></span> <span id="audit_detailedtracking_processcreation"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSCREATION"></span> **audit \_ DetailedTracking \_ ProcessCreation** (0cce922b-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessTermination"></span> <span id="audit_detailedtracking_processtermination"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSTERMINATION"></span> **audit \_ DetailedTracking \_ ProcessTermination** (0cce922c-69ae-11d9-bed3-505054503030) audit DetailedTracking <span id="Audit_DetailedTracking_DpapiActivity"></span> <span id="audit_detailedtracking_dpapiactivity"></span> <span id="AUDIT_DETAILEDTRACKING_DPAPIACTIVITY"></span> **\_ \_ DpapiActivity** (0cce922d-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_RpcCall"></span> <span id="audit_detailedtracking_rpccall"></span> <span id="AUDIT_DETAILEDTRACKING_RPCCALL"></span> **audit \_ DetailedTracking \_ RpcCall** (0cce922e-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuditPolicy"></span> <span id="audit_policychange_auditpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUDITPOLICY"></span> **audit \_ PolicyChange \_ Auditpolicy** (0cce922f-69ae-11d9-bed3-505054503030) audit PolicyChange AuthenticationPolicy <span id="Audit_PolicyChange_AuthenticationPolicy"></span> <span id="audit_policychange_authenticationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHENTICATIONPOLICY"></span> (0cce9230-69ae-11d9-bed3-505054503030) **\_ \_** <span id="Audit_PolicyChange_AuthorizationPolicy"></span> <span id="audit_policychange_authorizationpolicy"></span> Audit <span id="AUDIT_POLICYCHANGE_AUTHORIZATIONPOLICY"></span> **\_ PolicyChange \_ AuthorizationPolicy** (0cce9231-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_MpsscvRulePolicy"></span> <span id="audit_policychange_mpsscvrulepolicy"></span> <span id="AUDIT_POLICYCHANGE_MPSSCVRULEPOLICY"></span> **audit \_ PolicyChange \_ MpsscvRulePolicy** (0cce9232-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_WfpIPSecPolicy"></span> <span id="audit_policychange_wfpipsecpolicy"></span> <span id="AUDIT_POLICYCHANGE_WFPIPSECPOLICY"></span> **audit \_ PolicyChange \_ WfpIPSecPolicy** (0cce9233-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_Others"></span> <span id="audit_policychange_others"></span> <span id="AUDIT_POLICYCHANGE_OTHERS"></span> **audit \_ PolicyChange \_ others** (0cce9234-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_UserAccount"></span> <span id="audit_accountmanagement_useraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_USERACCOUNT"></span> **audit \_ AccountManagement \_ UserAccount** (0cce9235-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ComputerAccount"></span> <span id="audit_accountmanagement_computeraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_COMPUTERACCOUNT"></span> **audit \_ AccountManagement \_ compteordinateur** (0cce9236-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_SecurityGroup"></span> <span id="audit_accountmanagement_securitygroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_SECURITYGROUP"></span> **audit \_ AccountManagement \_ SecurityGroup** (0cce9237-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_DistributionGroup"></span> <span id="audit_accountmanagement_distributiongroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_DISTRIBUTIONGROUP"></span> **audit \_ AccountManagement \_ DistributionGroup**(0cce9238-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ApplicationGroup"></span> <span id="audit_accountmanagement_applicationgroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_APPLICATIONGROUP"></span> **audit \_ AccountManagement \_ ApplicationGroup** (0cce9239-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_Others"></span> <span id="audit_accountmanagement_others"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_OTHERS"></span> **audit \_ AccountManagement \_ others** (0cce923a-69ae-11d9-bed3-505054503030) <span id="Audit_DSAccess_DSAccess"></span> <span id="audit_dsaccess_dsaccess"></span> <span id="AUDIT_DSACCESS_DSACCESS"></span> **audit \_ DSAccess \_ DSAccess** (0cce923b-69ae-11d9-bed3-505054503030) <span id="Audit_DsAccess_AdAuditChanges"></span> <span id="audit_dsaccess_adauditchanges"></span> <span id="AUDIT_DSACCESS_ADAUDITCHANGES"></span> **audit \_ DSAccess \_ AdAuditChanges** (0cce923c-69ae-11d9-bed3-505054503030) audit DS <span id="Audit_Ds_Replication"></span> <span id="audit_ds_replication"></span> <span id="AUDIT_DS_REPLICATION"></span> **\_ \_ Replication** (0cce923d-69ae-11d9-bed3-505054503030) audit <span id="Audit_Ds_DetailedReplication"></span> <span id="audit_ds_detailedreplication"></span> <span id="AUDIT_DS_DETAILEDREPLICATION"></span> **\_ DS \_ DetailedReplication** (0cce923e-69ae-11d9-bed3-505054503030) audit <span id="Audit_AccountLogon_CredentialValidation"></span> <span id="audit_accountlogon_credentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_CREDENTIALVALIDATION"></span> **\_ AccountLogon \_ CredentialValidation** (0cce923f-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Kerberos"></span> <span id="audit_accountlogon_kerberos"></span> <span id="AUDIT_ACCOUNTLOGON_KERBEROS"></span> **audit \_ \_ AccountLogon Kerberos** (0cce9240-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Others"></span> <span id="audit_accountlogon_others"></span> <span id="AUDIT_ACCOUNTLOGON_OTHERS"></span> **audit \_ AccountLogon \_ others** (0cce9241-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_KerbCredentialValidation"></span> <span id="audit_accountlogon_kerbcredentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_KERBCREDENTIALVALIDATION"></span> **audit \_ AccountLogon \_ KerbCredentialValidation** (0cce9242-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_NPS"></span> <span id="audit_logon_nps"></span> <span id="AUDIT_LOGON_NPS"></span> **audit \_ Logon \_ NPS** (0cce9243-69ae-11d9-bed3-505054503030)
</dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

