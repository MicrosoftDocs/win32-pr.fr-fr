---
description: Point de terminaison de communication qui peut se connecter à un réseau local pour envoyer et recevoir des trames de données. Les points de terminaison LAN incluent les interfaces Ethernet, Token Ring et FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Classe CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545184"
---
# <a name="cim_lanendpoint-class"></a>\_Classe CIM LANEndpoint

Point de terminaison de communication qui peut se connecter à un réseau local pour envoyer et recevoir des trames de données. Les points de terminaison LAN incluent les interfaces Ethernet, Token Ring et FDDI.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LANEndpoint** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LANEndpoint** possède les propriétés suivantes.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient d’autres adresses monodiffusion qui peuvent être utilisées pour communiquer avec le point de terminaison LAN.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient les adresses de multidiffusion sur lesquelles le point de terminaison LAN écoute.

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LANID, CIM \_ LANSegment. LANID")
</dt> </dl>

Étiquette ou identificateur du segment LAN auquel le point de terminaison est connecté. Si le point de terminaison n’est pas actuellement connecté ou si ces informations sont inconnues, **LANID** a la valeur null.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")
</dt> </dl>

> [!Note]  
> Description déconseillée : type de technologie utilisée sur le réseau local.

 

Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons d’utiliser la propriété **ProtocolType** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Adresse de monodiffusion principale utilisée par le point de terminaison LAN.

L’adresse MAC doit être mise en forme avec les caractéristiques suivantes :

-   L’adresse se compose de douze chiffres hexadécimaux.
-   Chaque paire de chiffres représente l’un des six octets de l’adresse MAC.
-   Chaque paire de chiffres doit être dans l’ordre des bits canoniques conformément à la norme RFC 2469.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)
</dt> </dl>

Taille maximale, en octets, des champs de données envoyés ou reçus par le point de terminaison LAN.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Description déconseillée : type de technologie utilisée sur le réseau local lorsque la propriété **LANType** est définie sur « 1 » (autre).

 

Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons d’utiliser la propriété **OtherTypeDescription** .

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

[**\_PROTOCOLENDPOINT CIM**](cim-protocolendpoint.md)
</dt> </dl>

 

