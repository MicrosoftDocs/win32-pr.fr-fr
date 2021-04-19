---
title: Classe Win32_TSAccount
description: Autorise la suppression d’un compte qui existe sur le \_ Terminal Win32 et la modification des autorisations existantes.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount de la classe Services Bureau à distance
- Win32_TSAccount de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511392"
---
# <a name="win32_tsaccount-class"></a>\_Classe TSAccount Win32

La classe WMI **\_ TSAccount** WMI autorise la suppression d’un compte qui existe sur [**le \_ Terminal Win32**](win32-terminal.md) et la modification des autorisations existantes.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSAccount** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSAccount** possède ces méthodes.



| Méthode                                                                   | Description                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Supprimer**](win32-tsaccount-delete.md)                                 | Supprime l’utilisateur, le groupe ou le compte d’ordinateur spécifié.<br/>                           |
| [**ModifyAuditPermissions**](win32-tsaccount-modifyauditpermissions.md) | Modifie la granularité de l’ensemble des autorisations d’audit du compte spécifié.<br/> |
| [**ModifyPermissions**](win32-tsaccount-modifypermissions.md)           | Définit un jeu d’autorisations plus granulaire pour le compte spécifié.<br/>                     |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSAccount** a ces propriétés.

<dl> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom actuel du compte. Le nom de domaine est inclus.

</dd> <dt>

**AuditFail**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les [autorisations des services d’hôte de Session Bureau à distance](terminal-services-permissions.md) qui sont auditées pour une condition d’échec. La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**Station \_ de REQUÊTE = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**Station \_ de SET = 0X2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**Station \_ de LOGOFF = 0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**Station \_ de \| Droits standard \_ virtuels \_ requis = 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**Station \_ de SHADOW = 0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**Station \_ de LOGON = 0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**Station \_ de MSG = 0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**Station \_ de CONNECT = 0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**Station \_ de Disconnect = 0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**AuditSuccess**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les autorisations spécifiques au serveur hôte de session Bureau à distance qui sont auditées pour une condition de réussite. La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**Station \_ de REQUÊTE = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**Station \_ de SET = 0X2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**Station \_ de LOGOFF = 0x4WINSTATION \_ les \| droits standard virtuels \_ \_ requis = 0xF008** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**Station \_ de SHADOW = 0x10** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**Station \_ de LOGON = 0x20** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**Station \_ de MSG = 0x80** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**Station \_ de CONNECT = 0x100** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**Station \_ de Disconnect = 0x200** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Brève description (chaîne d’une ligne) de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Date à laquelle l’objet a été installé. L’absence d’une valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l'objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PermissionsAllowed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les [autorisations de services Bureau à distance](terminal-services-permissions.md) autorisées pour le compte. La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs suivantes.

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**Station \_ de REQUÊTE = 0x1** (1)


</dt> <dd>

Autorisation d’interroger les informations relatives à une session.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Station \_ de DÉFINIR** (2)


</dt> <dd>

Autorisation de modifier les paramètres de connexion.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Station \_ de Réinitialisation** (64)


</dt> <dd>

Autorisation de réinitialiser ou de mettre fin à une session ou à une connexion.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Station \_ de \| Droits standard \_ virtuels \_ requis** (983048)


</dt> <dd>

Autorisation d’utiliser des canaux virtuels. Les canaux virtuels fournissent un accès à partir d’un programme serveur sur les périphériques clients.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Station \_ de OMBRE** (16)


</dt> <dd>

Autorisation d’ombrer ou de contrôler à distance la session d’un autre utilisateur.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Station \_ de Ouverture de session** (32)


</dt> <dd>

Autorisation de se connecter à une session sur le serveur.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Station \_ de Fermeture de session** (4)


</dt> <dd>

Autorisation de fermer la session d’un utilisateur à partir d’une session.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Station \_ de MSG** (128)


</dt> <dd>

Autorisation d’envoyer un message à la session d’un autre utilisateur.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Station \_ de SE connecter** (256)


</dt> <dd>

Autorisation de se connecter à une autre session.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Station \_ de Se déconnecter** (512)


</dt> <dd>

Autorisation de déconnecter une session.

</dd> </dl>

</dd> <dt>

**PermissionsDenied**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les autorisations spécifiques au serveur hôte de session Bureau à distance qui ne sont pas autorisées pour le compte. La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**Station \_ de REQUÊTE = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**Station \_ de SET = 0X2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**Station \_ de LOGOFF = 0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**Station \_ de \| Droits standard \_ virtuels \_ requis = 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**Station \_ de SHADOW = 0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**Station \_ de LOGON = 0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**Station \_ de MSG = 0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**Station \_ de CONNECT = 0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**Station \_ de Disconnect = 0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les [identificateurs de sécurité](/windows/desktop/SecAuthZ/security-identifiers) du compte.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 (« OK »)


</dt> <dd></dd> <dt>



 (« Erreur »)


</dt> <dd></dd> <dt>



 (« Détérioré »)


</dt> <dd></dd> <dt>



 ("Inconnu")


</dt> <dd></dd> <dt>



 (« Échec prédit »)


</dt> <dd></dd> <dt>



 (« Démarrage »)


</dt> <dd></dd> <dt>



 (« Arrêt »)


</dt> <dd></dd> <dt>



 (« Service »)


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du terminal.

Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6. L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



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

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

