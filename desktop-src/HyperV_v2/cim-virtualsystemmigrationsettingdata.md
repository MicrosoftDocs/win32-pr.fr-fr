---
description: Définit les paramètres de migration du système virtuel qui est géré par une instance de la \_ classe CIM VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Classe CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24a48877a4195d17398457912314186d0220ace8016a4c9cc3edd3e06c378ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950668"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>\_Classe CIM VirtualSystemMigrationSettingData

Définit les paramètres de migration du système virtuel qui est géré par une instance de la classe [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ VirtualSystemMigrationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ VirtualSystemMigrationSettingData** possède les propriétés suivantes.

<dl> <dt>

**Bande passante**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

Bande passante affectée à une opération de migration de système virtuel ou demandée pour celle-ci. « 0 » est la bande passante par défaut pour les demandes de migration.

Les propriétés de la **bande passante** et de la **priorité** peuvent être utilisées conjointement. Les processus de migration ayant les valeurs de **priorité** les plus élevées partagent la bande passante disponible en fonction de la bande passante demandée. Si la bande passante n’est pas consommée par cet ensemble de processus, les processus de migration avec les valeurs de **priorité** inférieure égale suivantes partagent la bande passante restante. Si davantage de bande passante subsistent, les processus de migration avec les valeurs de **priorité** inférieure égale suivante sont pris en compte.

L’unité utilisée dans la propriété **Bandwidth** est spécifiée par la valeur de la propriété **BandwidthUnit** .

Si la valeur de la propriété **BandwidthUnit** est « percent », les règles suivantes s’appliquent :

-   La valeur de la propriété de **bande passante** doit être comprise entre « 0 » et « 100 », avec des valeurs supérieures indiquant une bande passante plus élevée.
-   La valeur « 100 » indique toute la bande passante disponible pour effectuer les opérations de migration du système virtuel.
-   Les valeurs comprises entre « 1 » et « 100 » sont corrélées de façon linéaire avec la plage de bande passante disponible. Par exemple, la valeur 50 demande la moitié de la bande passante disponible.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Bande passante**»), **IsPUnit**
</dt> </dl>

Unité utilisée par la propriété de **bande passante** . La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.

> [!Note]  
> Les profils tels que DMTF DSP1081 définissent la façon dont les clients peuvent découvrir l’ensemble d’unités pris en charge par une implémentation, ainsi que les plages et les incréments pour les valeurs de la propriété **Bandwidth** .

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’opération de migration à effectuer.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

En **direct** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**Reprendre** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Redémarrer** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")
</dt> </dl>

Type de transport à appliquer si la valeur de **TransportType** est « 1 » (autre).

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’importance de la migration relative que l’implémentation de la migration du système virtuel peut utiliser pour ordonner ou attribuer une préférence entre plusieurs demandes de migration en attente. Plus la valeur est faible, plus la priorité est élevée. « 0 » est la bande passante par défaut pour les demandes de migration.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

Type de transport à appliquer à une opération de migration de système virtuel.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768...)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

