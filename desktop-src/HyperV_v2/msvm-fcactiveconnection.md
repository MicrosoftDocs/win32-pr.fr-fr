---
description: Connecte un port de commutateur au point de terminaison Fibre Channel auquel le port est connecté.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516901"
---
# <a name="msvm_fcactiveconnection-class"></a>MSVM \_ FcActiveConnection, classe

Connecte un port de commutateur au point de terminaison Fibre Channel auquel le port est connecté. L’existence de cet objet signifie que le port de commutateur et le point de terminaison Fibre Channel sont connectés activement, et que le port Fibre Channel associé au point de terminaison Fibre Channel peut communiquer avec le réseau via le port commuté.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ FcActiveConnection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ FcActiveConnection** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ FcEndpoint**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le point d’accès au service (SAP) qui est configuré pour communiquer ou qui communique activement avec le SAP dépendant. Dans une connexion unidirectionnelle, ce SAP est celui qui transmet.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ FcEndpoint**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le SAP configuré pour communiquer ou qui communique activement avec l’antécédent SAP. Dans une connexion unidirectionnelle, ce SAP est celui qui reçoit.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

