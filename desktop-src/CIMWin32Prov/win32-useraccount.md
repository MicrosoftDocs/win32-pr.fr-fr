---
description: Le \_ UserAccount Win32&\# 32 ; La classe WMI contient des informations sur un compte d’utilisateur sur un système informatique exécutant Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033625"
---
# <a name="win32_useraccount-class"></a>\_Classe UserAccount Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ UserAccount** WMI contient des informations sur un compte d’utilisateur sur un système informatique exécutant Windows.

> [!Note]  
> Étant donné que le **nom** et le **domaine** sont tous les deux des propriétés de clé, l’énumération de **\_ UserAccount Win32** sur un réseau de grande taille peut avoir un impact négatif sur les performances. L’appel de **GetObject** ou l’interrogation d’une instance spécifique a moins d’impact.

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ UserAccount** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ UserAccount** possède ces méthodes.



| Méthode                                                     | Description                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**Renommer**](rename-method-in-class-win32-useraccount.md) | Autorise l’attribution d’un nouveau nom au compte d’utilisateur.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ UserAccount** a ces propriétés.

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags »)
</dt> </dl>

Indicateurs qui décrivent les caractéristiques d’un compte d’utilisateur Windows.

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Compte dupliqué temporaire** (256)


</dt> <dd>

**\_ \_ compte DUPLIQUÉ temporaire \_ uf**

Compte d’utilisateur local pour les utilisateurs qui ont un compte principal dans un autre domaine. Ce compte fournit un accès utilisateur à ce domaine uniquement, et non à un domaine qui approuve ce domaine.

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Compte normal** (512)


</dt> <dd>

**\_compte standard \_ uf**

Type de compte par défaut qui représente un utilisateur standard.

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Compte de confiance interdomaine** (2048)


</dt> <dd>

**\_compte de confiance interdomaine UF \_ \_**

Compte d’un domaine système qui approuve d’autres domaines.

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Compte de confiance de station de travail** (4096)


</dt> <dd>

**compte d’approbation de station de \_ travail UF \_ \_**

Compte d’ordinateur pour un système d’ordinateur exécutant Windows qui est membre de ce domaine.

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Compte de confiance du serveur** (8192)


</dt> <dd>

**\_compte de \_ confiance du serveur uf \_**

Compte d’un contrôleur de domaine de sauvegarde du système qui est membre de ce domaine.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Domaine et nom d’utilisateur du compte.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description du compte.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Désactivé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| \_ info utilisateur \| UF \_ ACCOUNTDISABLE »)
</dt> </dl>

Le compte d’utilisateur Windows est désactivé.

</dd> <dt>

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APId \| Network Management Functions \| nom_domaine")
</dt> </dl>

Nom du domaine Windows auquel appartient un compte d’utilisateur, par exemple : « NA-SALES ».

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**»)
</dt> </dl>

Nom complet d’un utilisateur local, par exemple : « Dan Wilson ».

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Date d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Si la **valeur est true**, le compte est défini sur l’ordinateur local.

Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).

</dd> <dt>

**Verrouillage.**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ lockout**»)
</dt> </dl>

Si la **valeur est true**, le compte d’utilisateur est verrouillé sur le système d’exploitation Windows.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| Name")
</dt> </dl>

Nom du compte d’utilisateur Windows sur le domaine que la propriété de **domaine** de cette classe spécifie.

Exemple : « danwilson ».

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PasswordChangeable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF passwd impossibilité \_ \_ \_ change**»)
</dt> </dl>

Si la **valeur est true**, le mot de passe de ce compte d’utilisateur peut être modifié.

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info utilisateur \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)uf ne pas faire \| **\_ \_ expirer \_ passwd**»)
</dt> </dl>

Si la **valeur est true**, le mot de passe de ce compte d’utilisateur expire.

</dd> <dt>

**PasswordRequired**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd passwd \_ NOTREQD**»)
</dt> </dl>

Si la **valeur est true**, un mot de passe est requis sur un compte d’utilisateur Windows. Si la **valeur est false**, ce compte ne requiert pas de mot de passe.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| identificateurs de sécurité (SID)")
</dt> </dl>

Identificateur de sécurité (SID) pour ce compte. Un SID est une valeur de chaîne de longueur variable qui est utilisée pour identifier un tiers de confiance. Chaque compte possède un SID unique qu’une autorité, comme un domaine Windows, émet. Le SID est stocké dans la base de données de sécurité. Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données, place le SID dans le jeton d’accès utilisateur, puis utilise le SID dans le jeton d’accès utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows. Chaque SID est un identificateur unique pour un utilisateur ou un groupe, et un autre utilisateur ou groupe ne peut pas avoir le même SID.

Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Access Control types énumération types \| [**sid \_ \_ use**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")
</dt> </dl>

Valeur énumérée qui spécifie le type de SID.

Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**SidTypeAlias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel d’un objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prédit », qui est un élément tel qu’un lecteur de disque dur intelligent qui peut fonctionner correctement, mais prédit une défaillance dans un avenir proche. Les États non opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service », qui peuvent s’appliquer pendant la réargentation miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ UserAccount** est dérivée [**du \_ compte Win32**](win32-account.md).

> [!Note]  
> Une erreur n’est pas retournée pour une tentative d’écriture dans une propriété en lecture seule, et la valeur de la propriété reste inchangée.

 

## <a name="examples"></a>Exemples

L’exemple de code [répertorier les comptes d’utilisateurs locaux à l’aide](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) de code WMI VBScript sur la Galerie TechNet utilise **Win32 \_ UserAccount** pour renvoyer des informations sur les comptes d’utilisateurs locaux détectés sur un ordinateur.

[Traduire le SID en compte d’utilisateur et le compte d’utilisateur en sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) L’exemple de code PowerShell sur la Galerie TechNet utilise **Win32 \_ UserAccount** pour convertir un SID en compte d’utilisateur et/ou un compte d’utilisateur en sid.

L’exemple de code VBScript suivant vous montre comment obtenir le nom complet d’un utilisateur sur un ordinateur local. Le nom complet est le nom de la langue humaine. par exemple, une personne peut avoir le nom d’utilisateur « kensanchez » et le nom complet peut être « Ken Sanchez ». vous devez donc remplacer le nom de domaine réel et le nom d’utilisateur par « MyDomainName » et « MyUserName ». Pour une requête efficace, vous devez spécifier les propriétés Domain et User Name.

Si vous êtes un administrateur sur un ordinateur distant, vous pouvez attribuer le nom de l’ordinateur distant pour strComputer (au lieu de « . »), puis utiliser le type de script suivant pour obtenir le nom complet d’un compte d’utilisateur sur un ordinateur local, à partir d’un ordinateur distant.


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Compte Win32**](win32-account.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
