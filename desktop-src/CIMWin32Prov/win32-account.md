---
description: Contient des informations sur les comptes d’utilisateur et les comptes de groupe connus du système informatique exécutant Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Classe Win32_Account
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc98f826ddae09bd507517e564ec2d9387d6bf17147d5eac36596bdb9d1e81ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918119"
---
# <a name="win32_account-class"></a>\_Classe de compte Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) du **\_ compte Win32** contient des informations sur les comptes d’utilisateurs et les comptes de groupe connus du système informatique exécutant Windows. les noms d’utilisateurs ou de groupes reconnus par un domaine de Windows sont des descendants (ou membres) de cette classe.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Membres

La classe de **\_ compte Win32** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ compte Win32** possède ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Brève description de l’objet.

Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

</dd> <dt>

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Network Management Functions \| Domain »)
</dt> </dl>

nom du domaine Windows auquel appartient un groupe ou un utilisateur.

Exemple : « NA-SALES »

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Si la **valeur est true**, le compte est défini sur l’ordinateur local. Pour récupérer uniquement les comptes définis sur l’ordinateur local, créez une requête qui comprend la condition « LocalAccount =**true**».

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management structures \| Name")
</dt> </dl>

nom du compte système Windows sur le domaine spécifié par la propriété de **domaine** de cette classe. Cette propriété remplace la propriété **Name** héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| identificateurs de sécurité (SID)")
</dt> </dl>

Identificateur de sécurité (SID) pour ce compte. Un SID est une valeur de chaîne de longueur variable utilisée pour identifier un tiers de confiance. chaque compte possède un SID unique émis par une autorité (par exemple, un domaine Windows), stocké dans une base de données de sécurité. Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données et le place dans le jeton d’accès de l’utilisateur. le système utilise le SID dans le jeton d’accès de l’utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec Windows la sécurité. Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut pas être réutilisé pour identifier un autre utilisateur ou groupe.

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Access Control types énumération types \| sid \_ \_ use")
</dt> </dl>

Valeurs énumérées qui spécifient le type d’identificateur de sécurité (SID).

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

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédit une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

Les valeurs sont :

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

## <a name="remarks"></a>Remarques

La classe de **\_ compte Win32** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).

## <a name="examples"></a>Exemples

Le code PowerShell suivant récupère les comptes locaux.


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



Le code PowerShell suivant récupère les comptes de domaine.


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

