---
description: Représente une association dans laquelle un \_ objet CIM ou un \_ objet ProtocolEndpoint CIM dépend d’un objet LANEndpoint CIM sous-jacent \_ sur le même système.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Classe CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520072"
---
# <a name="cim_bindstolanendpoint-class"></a>\_Classe CIM BindsToLANEndpoint

Représente une association dans laquelle un objet [**CIM ou un \_**](cim-serviceaccesspoint.md) objet [**\_ ProtocolEndpoint**](cim-protocolendpoint.md) CIM dépend d’un objet [**\_ LANEndpoint CIM**](cim-lanendpoint.md) sous-jacent sur le même système.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ BindsToLANEndpoint** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ BindsToLANEndpoint** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LANEndpoint**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Objet [**\_ LANEndpoint CIM**](cim-lanendpoint.md) sous-jacent.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

L’objet [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**CIM CIM \_**](cim-protocolendpoint.md) qui est dépendant de la [**\_ LANEndpoint CIM**](cim-lanendpoint.md).

</dd> <dt>

**Frame**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Méthode de tramage pour le point d’accès du service de couche supérieure ou le point de terminaison de protocole.

> [!Note]  
> La valeur 802.3 brute est uniquement connue pour être utilisée avec le protocole IPX.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802,2** (2)


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**Alignement** (3)


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**802.3 brut** (4)


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

[**\_BINDSTO CIM**](cim-bindsto.md)
</dt> </dl>

 

