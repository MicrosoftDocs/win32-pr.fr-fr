---
description: Représente des données de configuration pour un point de terminaison de réseau local virtuel.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Classe CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443d7b50ae8fe727a95464ec4e7fa589d7a08db770ce4c5090f37e5c988bfa4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682609"
---
# <a name="cim_vlanendpointsettingdata-class"></a>\_Classe CIM VLANEndpointSettingData

Représente des données de configuration pour un point de terminaison de réseau local virtuel.

## <a name="syntax"></a>Syntaxe

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ VLANEndpointSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ VLANEndpointSettingData** possède les propriétés suivantes.

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

VLAN d’accès pour le point de terminaison.

</dd> <dt>

**DefaultVLAN**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Valeur par défaut pour le VLAN natif sur le point de terminaison Trunk.

> [!Note]  
> Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .

 

</dd> <dt>

**NativeVLAN**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

ID de réseau local virtuel utilisé pour baliser le trafic non marqué reçu sur le point de terminaison Trunk.

> [!Note]  
> Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **SwitchEndpointMode** .

 

</dd> <dt>

**PruneEligibleVLANList**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Tableau qui contient les ID des réseaux locaux virtuels que le système peut supprimer du point de terminaison Trunk.

> [!Note]  
> Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Tableau qui contient les ID des points de terminaison de réseau local virtuel avec le Trunking activé.

> [!Note]  
> Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .

 

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

