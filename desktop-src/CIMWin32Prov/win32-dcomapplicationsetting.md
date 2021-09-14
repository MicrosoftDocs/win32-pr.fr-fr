---
description: Le \_ DCOMApplicationSetting Win32&\# 8194 ; La classe WMI représente les paramètres d’une application DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921896"
---
# <a name="win32_dcomapplicationsetting-class"></a>\_Classe DCOMApplicationSetting Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ DCOMApplicationSetting** représente les paramètres d’une application DCOM. Il contient les options de configuration DCOM associées à la clé **AppID** dans le registre. Ces options sont valides sur les composants regroupés logiquement sous la classe d’application donnée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ DCOMApplicationSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ DCOMApplicationSetting** possède ces méthodes.



| Méthode                                                                                                                        | Description                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAccessSecurityDescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Obtient le descripteur de sécurité qui contrôle les personnes autorisées à accéder à une application DCOM.<br/>                                                                                                                              |
| [**GetConfigurationSecurityDescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Obtient le descripteur de sécurité qui contrôle les personnes autorisées à configurer une application DCOM.<br/>                                                                                                                           |
| [**GetLaunchSecurityDescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Obtient le descripteur de sécurité qui contrôle les personnes autorisées à lancer une application DCOM.<br/>                                                                                                                              |
| [**SetAccessSecurityDescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Met à jour le descripteur de sécurité d’accès de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |
| [**SetConfigurationSecurityDescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Met à jour le descripteur de sécurité de configuration de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/> |
| [**SetLaunchSecurityDescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Met à jour le descripteur de sécurité de lancement de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ DCOMApplicationSetting** a ces propriétés.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] »)
</dt> </dl>

Identificateur global unique (GUID) de cette application DCOM.

</dd> <dt>

**AuthenticationLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")
</dt> </dl>

Niveau minimal d’authentification du client requis par ce serveur COM. Si la **valeur est null**, les valeurs par défaut sont utilisées.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (1)


</dt> <dd>

Aucun (aucune authentification n’est effectuée)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connecter** (2)


</dt> <dd>

Connecter (l’authentification est effectuée uniquement lorsque le client établit une relation avec l’application)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Appel** (3)


</dt> <dd>

Appel (l’authentification est effectuée uniquement au début de chaque appel lorsque l’application reçoit la demande)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paquet** (4)


</dt> <dd>

Paquet (l’authentification est effectuée sur toutes les données reçues du client)

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)


</dt> <dd>

PacketIntegrity (toutes les données transférées entre le client et l’application sont authentifiées et vérifiées)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)


</dt> <dd>

PacketPrivacy (les propriétés des autres niveaux d’authentification sont utilisées et toutes les données sont chiffrées)

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**CustomSurrogate**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

Nom du substitut personnalisé dans lequel l’application DCOM in-process est activée. Si cette valeur est **null** et que la clé **UseSurrogate** est **true**, le système fournit un processus de substitution.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")
</dt> </dl>

L’application DCOM récupère l’état enregistré de l’application ou commence à l’État dans lequel l’application est initialisée pour la première fois.

</dd> <dt>

**LocalService**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Nom des services fournis par l’application DCOM.

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")
</dt> </dl>

Nom du serveur distant sur lequel l’application est activée.

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ runas \] ")
</dt> </dl>

Compte d’utilisateur spécifique sous lequel l’application doit être exécutée lors de l’activation.

</dd> <dt>

**ServiceParameters**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")
</dt> </dl>

Paramètres de ligne de commande passés à l’application DCOM. cela est valide uniquement si l’application est écrite en tant que service Windows.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

L’application DCOM peut être activée en tant que serveur hors processus à l’aide d’un fichier exécutable de substitution.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ DCOMApplicationSetting** est dérivée de la [**\_ comdéfinition Win32**](win32-comsetting.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Configuration de Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

