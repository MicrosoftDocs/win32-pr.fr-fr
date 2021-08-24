---
description: Représente les paramètres pour l’allocation du port Ethernet, en plus des paramètres fournis par la classe CIM \_ EthernetPort. Ces paramètres sont utilisés pour fournir des informations spécifiques à la ressource elle-même.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Classe CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7546af167a6e13712119a081e7dbfaee118dc0c8a4912b8411d898a4ad90bc7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695799"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a>\_Classe CIM EthernetPortAllocationSettingData

Représente les paramètres pour l’allocation du port Ethernet, en plus des paramètres fournis par la classe [**CIM \_ EthernetPort**](cim-ethernetport.md) . Ces paramètres sont utilisés pour fournir des informations spécifiques à la ressource elle-même.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ EthernetPortAllocationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ EthernetPortAllocationSettingData** possède les propriétés suivantes.

<dl> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")
</dt> </dl>

Mode VLAN demandé. Cette propriété est utilisée pour définir la valeur de la propriété **OperationalEndpointMode** initiale dans l’instance de **\_ VLANEndpoint CIM** associée au port Ethernet.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Accès** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Automatique dynamique** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Désirable dynamique** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Tunnel Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")
</dt> </dl>

Type de modèle de point de terminaison VLAN pris en charge par ce point de terminaison VLAN, lorsque la valeur de la propriété mode est définie sur « 1 » (autre). Cette propriété doit être définie sur **null** lorsque la propriété mode est toute valeur autre que « 1 ».

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

