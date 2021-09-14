---
title: Méthode ModifyAuditPermissions de la classe Win32_TSAccount
description: Prépare la définition d’un jeu d’autorisations d’audit plus granulaire pour le compte spécifié.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ModifyAuditPermissions
- Services Bureau à distance de la méthode ModifyAuditPermissions, classe Win32_TSAccount
- Win32_TSAccount de la classe Services Bureau à distance, méthode ModifyAuditPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919584"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Méthode ModifyAuditPermissions de la \_ classe Win32 TSAccount

La méthode **ModifyAuditPermissions** prépare la définition d’un jeu d’autorisations d’audit plus granulaire pour le compte spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PermissionMask* \[ dans\]
</dt> <dd>

Ensemble d' [Bureau à distance autorisations d’hôte de session](terminal-services-permissions.md) à associer au compte spécifié. La valeur de ce paramètre est une image bitmap, et tout ou partie des valeurs suivantes peuvent être sélectionnées.

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Station \_ de REQUÊTE** (0)


</dt> <dd>

Autorisation d’interroger les informations relatives à une session.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Station \_ de SET** (1)


</dt> <dd>

Autorisation de modifier les paramètres de connexion.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Station \_ de RÉINITIALISER** (6)


</dt> <dd>

Autorisation de réinitialiser ou de mettre fin à une session ou à une connexion.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Station \_ de \| Droits standard \_ virtuels \_ requis** (3)


</dt> <dd>

Autorisation d’utiliser des canaux virtuels. Les canaux virtuels fournissent un accès à partir d’un programme serveur sur les périphériques clients.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Station \_ de OMBRE** (4)


</dt> <dd>

Autorisation d’ombrer ou de contrôler à distance la session d’un autre utilisateur.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Station \_ de Ouverture de session** (5)


</dt> <dd>

Autorisation de se connecter à une session sur le serveur.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Station \_ de Fermeture de session** (2)


</dt> <dd>

Autorisation de fermer la session d’un utilisateur à partir d’une session.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Station \_ de MSG** (7)


</dt> <dd>

Autorisation d’envoyer un message à la session d’un autre utilisateur.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Station \_ de SE connecter** (8)


</dt> <dd>

Autorisation de se connecter à une autre session.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Station \_ de Déconnexion** (9)


</dt> <dd>

Autorisation de déconnecter une session.

</dd> </dl> </dd> <dt>

*Opération réussie* \[ dans\]
</dt> <dd>

Spécifie si le jeu d’autorisations spécifié par la valeur du paramètre *PermissionMask* est autorisé ou refusé.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Le jeu d’autorisations spécifié est autorisé.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Le jeu d’autorisations spécifié est refusé.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 

