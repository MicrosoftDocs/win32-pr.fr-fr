---
description: Connecte un port commuté au point de terminaison LAN auquel le port est connecté.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693609"
---
# <a name="msvm_activeconnection-class"></a>MSVM, \_ classe ActiveConnection

Connecte un port commuté au point de terminaison LAN auquel le port est connecté. L’existence de cet objet signifie que le port commuté et le point de terminaison LAN sont activement connectés et que le port Ethernet associé au point de terminaison LAN peut communiquer avec le réseau via le port commuté.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ActiveConnection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ActiveConnection** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) qui représente le point d’accès au service (SAP) qui est configuré pour communiquer ou qui communique activement avec le SAP dépendant. Dans une connexion unidirectionnelle, ce SAP est celui qui transmet.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) qui représente le SAP configuré pour communiquer ou qui communique activement avec l’antécédent SAP. Dans une connexion unidirectionnelle, ce SAP est celui qui reçoit.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si cette propriété a la **valeur true**, cette connexion est unidirectionnelle ; dans le cas contraire, cette connexion est bidirectionnelle. Lorsqu’une connexion est unidirectionnelle, la « Speaker » doit être définie comme référence **Antecedent** . Dans une connexion bidirectionnelle, il n’est pas important de savoir si le point d’accès sélectionné est l' **antécédent** ou le **dépendant**. Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ActiveConnection** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ACTIVECONNECTION CIM**](cim-activeconnection.md)
</dt> <dt>

[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

