---
description: Représente une entrée dans la base de données de transfert associée à la \_ classe CIM TransparentBridgingService.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Classe CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5c53d39ff56bfe36f49ed9e224508e013a5f17977355145d316da147c266a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812566"
---
# <a name="cim_dynamicforwardingentry-class"></a>\_Classe CIM DynamicForwardingEntry

Représente une entrée dans la base de données de transfert associée à la classe [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ DynamicForwardingEntry** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ DynamicForwardingEntry** possède les propriétés suivantes.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée pour créer l’instance. Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.

</dd> <dt>

**DynamicStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")
</dt> </dl>

État de l’entrée.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

**Non valide** (2)


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

**Appris** (3)


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

**Self** (4)


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

**Mgmt** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")
</dt> </dl>

Adresse MAC de monodiffusion pour laquelle le service de pontage filtre les informations. L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux, par exemple 010203040506, chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques, conformément à la RFC 2469.

</dd> <dt>

**ServiceCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ service CIM**](cim-service.md).**CreationClassName**»)
</dt> </dl>

Valeur **CreationClassName** de l’objet de service d’étendue.

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ service CIM**](cim-service.md).**Name**»)
</dt> </dl>

Nom du service d’étendue.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)
</dt> </dl>

Valeur **CreationClassName** de l’objet système d’étendue.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)
</dt> </dl>

Nom du système d’étendue.

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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> </dl>

 

