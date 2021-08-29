---
description: Représente la configuration d’un commutateur de Fibre Channel virtuel.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Classe Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 75991b0efe412d53fab421d8518cc8fa35d2fb37cd1bda21a6d38186d9874cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426319"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a>MSVM \_ VirtualFcSwitchSettingData, classe

Représente la configuration d’un commutateur de Fibre Channel virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualFcSwitchSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualFcSwitchSettingData** possède les propriétés suivantes.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Délai avant le démarrage automatique de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte. Un nombre inférieur indique une activation antérieure. Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation. La valeur 0 indique que la séquence dépend de l’implémentation. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Fichier ConfigurationFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** . Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique de la configuration. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création des paramètres. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les notes fournies par l’utilisateur sont liées à la machine virtuelle. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de machine virtuelle que les données de paramètre représentent. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

