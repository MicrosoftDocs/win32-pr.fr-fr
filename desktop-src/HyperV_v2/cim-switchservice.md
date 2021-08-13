---
description: Représente un service de commutateur.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: Classe CIM_SwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cae4f157073721dc7cdd87585b39e1dbdb4c73b03a4aaf82a8ffd26796cbc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646781"
---
# <a name="cim_switchservice-class"></a>\_Classe CIM SwitchService

Représente un service de commutateur.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SwitchService** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SwitchService** possède les propriétés suivantes.

<dl> <dt>

**BridgeAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")
</dt> </dl>

Adresse du service de commutateur, qui est une partie de l’identificateur unique du service.

</dd> <dt>

**BridgeAddressType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")
</dt> </dl>

Format d’adressage utilisé pour le pont et la propriété **BridgeAddress** .

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (3)


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

**Mac** (4)


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

**Mac + priorité d’arborescence étendue** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**BridgeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseType ")
</dt> </dl>

Type de service de commutation à effectuer.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (1)


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

**Transparent uniquement** (2)


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

**SourceRoute uniquement** (3)


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

**SRT** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**NumPorts**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseNumPorts ")
</dt> </dl>

Nombre de ports de commutateur contrôlés par ce service de commutation.

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

[**\_FORWARDINGSERVICE CIM**](cim-forwardingservice.md)
</dt> </dl>

 

