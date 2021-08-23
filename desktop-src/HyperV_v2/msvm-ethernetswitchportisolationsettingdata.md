---
description: Représente les données de paramètre d’isolation.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Classe Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 33ddf01fb7df5787fc35c073472987aa9a170e62086cd6c127f874cb2360b38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681529"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a>MSVM \_ EthernetSwitchPortIsolationSettingData, classe

Représente les données de paramètre d’isolation.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchPortIsolationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchPortIsolationSettingData** possède les propriétés suivantes.

<dl> <dt>

**AllowUntaggedTraffic**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (2), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indique si le port est autorisé à envoyer/recevoir du trafic non marqué.

</dd> <dt>

**DefaultIsolationId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (3), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

VirtualSubnetId ou VLAN par défaut qui sera défini sur tout le trafic d’envoi/réception si **AllowedUntaggedTraffic** a la **valeur true**.

</dd> <dt>

**EnableMultiTenantStack**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (4), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Si la **valeur est true**, la pile réseau de la machine virtuelle peut accéder à la configuration d’isolation. La valeur par défaut est **false**.

</dd> <dt>

**IsolationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (1), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indique si le port utilise **VLAN** ou **VirtualSubnetId** pour l’isolation. **NativeVirtualSubnetId** est utilisé pour les réseaux wnv VirtualSubnetId.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

**NativeVirtualSubnetId** (1)


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

**ExternalVirtualSubnetId** (2)


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

**Réseau local virtuel** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

