---
title: Méthode ModifyPermissions de la classe Win32_TSAccount
description: Définit une autorisation pour le compte spécifié.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ModifyPermissions
- Services Bureau à distance de la méthode ModifyPermissions, classe Win32_TSAccount
- Win32_TSAccount de la classe Services Bureau à distance, méthode ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511758"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Méthode ModifyPermissions de la \_ classe Win32 TSAccount

Définit une autorisation pour le compte spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PermissionMask* \[ dans\]
</dt> <dd>

Autorisation de l' [hôte de Session Bureau à distance](terminal-services-permissions.md) pour définir.

Les valeurs possibles sont les suivantes :

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

*Autoriser* \[ dans\]
</dt> <dd>

Spécifie si l’autorisation dans le paramètre *PermissionMask* est autorisée ou refusée.

Les valeurs possibles sont les suivantes :

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

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



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

 

