---
description: Utilisé dans la méthode GetSummaryInformation de la \_ classe MSVM VirtualSystemManagementService pour récupérer rapidement les informations communes relatives à un système virtuel ou à un instantané.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd99ec5a0a9f3bd4bd07fa88cfc15139c69a442b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886578"
---
# <a name="msvm_summaryinformationbase-class"></a>MSVM \_ SummaryInformationBase, classe

Utilisé dans la méthode [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pour récupérer rapidement les informations communes relatives à un système virtuel ou à un instantané.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SummaryInformationBase** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SummaryInformationBase** possède les propriétés suivantes.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le système virtuel ou l’instantané a été créé.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. ElementName")
</dt> </dl>

Nom convivial du système virtuel ou de l’instantané.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel du système virtuel ou de l’instantané.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les connexions en mode étendu sont autorisées par l’hôte et, le cas échéant, si elles sont disponibles pour la machine virtuelle.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Autorisé et disponible** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Non autorisé** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Autorisé mais non disponible** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État d’intégrité actuel du système virtuel. Cette propriété n’est pas valide pour les instances de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représentent un instantané de système virtuel.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur hébergeant cet ordinateur virtuel.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. InstanceId"), [**clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID est une propriété facultative qui peut être utilisée pour identifier de manière opaque et unique une instance de cette classe dans l’étendue de l’espace de noms d’instanciation. Plusieurs sous-classes de cette classe peuvent substituer cette propriété pour la rendre obligatoire ou une clé. Ces sous-classes peuvent également modifier les algorithmes préférés pour garantir l’unicité définie ci-dessous.

Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant :

&lt;Identifiant OrgID &gt; : &lt; LocalID&gt;

Où &lt; identifiant OrgID &gt; et &lt; LocalID &gt; sont séparés par un signe deux-points ( :), et où &lt; identifiant OrgID &gt; doit inclure un nom de droits d’auteur, de marque ou d’autre nom unique qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier par une autorité globale reconnue. (Cette spécification est semblable à la <Schema Name> \_ <Class Name> suivante : structure des noms de classes de schéma.) En outre, pour garantir l’unicité, &lt; identifiant OrgID &gt; ne doit pas contenir de deux-points ( :). Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre &lt; identifiant OrgID &gt; et &lt; LocalID &gt; .

&lt;LocalID &gt; est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels). Si la valeur n’est pas null et que l’algorithme « préféré » ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.

Si vous ne définissez pas la valeur null pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le &lt; identifiant OrgID &gt; défini sur CIM.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom unique du système virtuel ou de l’instantané.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Remarques associées au système virtuel ou à l’instantané.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de processeurs virtuels alloués au système virtuel ou à la capture instantanée.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

État actuel de l’élément.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »). Cette propriété doit avoir la valeur NULL quand **EnabledState** a une valeur autre que 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .

</dd> <dt>

**Activité**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée écoulée depuis le dernier démarrage du système virtuel. Cette propriété n’est pas valide pour les instances de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représentent un instantané de système virtuel.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La version du système virtuel dans un format « majeure. mineure »; par exemple, « 2,0 ».

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Chaînes qui répertorient les noms conviviaux des commutateurs virtuels auxquels la machine virtuelle est connectée.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Sous-type du système virtuel.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft : Hyper-v : sous-type : 1** (« Microsoft : Hyper-v : SubType : 1 »)


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft : Hyper-v : sous-type : 2** (« Microsoft : Hyper-v : SubType : 2 »)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Vue CIM**](cim-view.md)
</dt> </dl>

 

