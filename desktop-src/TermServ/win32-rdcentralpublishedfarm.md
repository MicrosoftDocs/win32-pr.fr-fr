---
title: Classe Win32_RDCentralPublishedFarm
description: Liste des batteries de serveurs à partir desquelles les ordinateurs de bureau ou les applications ont été publiés.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFarm de la classe Services Bureau à distance
- Win32_RDCentralPublishedFarm de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217228"
---
# <a name="win32_rdcentralpublishedfarm-class"></a>\_Classe RDCentralPublishedFarm Win32

Liste des batteries de serveurs à partir desquelles les ordinateurs de bureau ou les applications ont été publiés.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDCentralPublishedFarm** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDCentralPublishedFarm** a ces propriétés.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de la batterie de serveurs à partir de laquelle les ordinateurs de bureau ou les applications ont été publiés.

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

**FarmType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Type de batterie de serveurs :

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

**Hôte** de la (0)


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

**TempVM** (1)


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

**ManualPersonalVM** (2)


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

**AutoPersonalVM** (3)


</dt> <dd></dd> </dl>

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

**IsUserAdmin**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**true** si un utilisateur doit être ajouté au groupe administrateur local lors de la connexion ; Sinon, **false**. S’applique uniquement aux types de batterie ManualPersonalVm et AutoPersonalVM.

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

**RollbackEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**true** pour restaurer automatiquement la machine virtuelle vers un instantané après la fermeture de session de l’utilisateur ; Sinon, **false**. S’applique uniquement aux types de batterie TempVm.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom du descripteur de sécurité contrôlant l’accès à l’application, au format SDDL. L’utilisation d’une chaîne vide implique l’autorisation de tous les accès.

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

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Paramètres de la batterie de serveurs virtuels.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

