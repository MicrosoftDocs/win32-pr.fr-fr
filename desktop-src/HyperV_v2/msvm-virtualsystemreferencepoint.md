---
description: Représente un point de référence pour un système virtuel.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Classe Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522751"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a>MSVM \_ VirtualSystemReferencePoint, classe

Représente un point de référence pour un système virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemReferencePoint** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemReferencePoint** possède les propriétés suivantes.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Niveau de cohérence du point de référence.

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)


</dt> <dd>

Le point de référence indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)


</dt> <dd>

Le point de référence indique un point dans le temps où le système virtuel se trouvait dans un état de cohérence en cas d’incident.

</dd> </dl>

</dd> <dt>

**HasAssociatedData**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

A la valeur **true** si le point de référence a des données associées. Cela est valide uniquement pour les points de référence basés sur un journal. Pour les points de référence basés sur RCT, **HasAssociatedData** est défini sur **false**. Pour les points de référence basés sur un journal, une fois le journal ignoré, **HasAssociatedData** prend la **valeur false**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identification unique d’un objet de point de référence.

</dd> <dt>

**ReferencePointType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique le type du point de référence.

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basé sur le journal** (1)


</dt> <dd>

Suivi du journal de réplication Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basé sur RCT** (2)


</dt> <dd>

Basé sur une Change Tracking résiliente des disques virtuels.

</dd> </dl>

</dd> <dt>

**ResilientChangeTrackingIdentifiers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’ID RCT correspondant aux disques virtuels de la machine virtuelle au moment de la création de ce point de référence. Ce champ est valide uniquement pour les points de référence basés sur RCT.

</dd> <dt>

**VirtualDiskIdentifiers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’ID d’instance WMI correspondant aux disques virtuels de la machine virtuelle au moment de la création de ce point de référence. Ces disques virtuels sont associés à des ID RCT.

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ CIM**](cim-computersystem.md).**Name**»)
</dt> </dl>

Nom du [**\_ ComputerSystem CIM**](cim-computersystem.md) auquel ce point de référence appartient

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> </dl>

 

