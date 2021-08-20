---
description: Représente une association dans laquelle les points de terminaison de protocole dépendent d’un service de transfert pour transférer des données.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Classe CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa6f3782407f57f999117b83918460adae307c962336386301592d3408e6490d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014647"
---
# <a name="cim_forwardsamong-class"></a>\_Classe CIM ForwardsAmong

Représente une association dans laquelle les points de terminaison de protocole dépendent d’un service de transfert pour transférer des données.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ForwardsAmong** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ForwardsAmong** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ ProtocolEndpoint CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Les points de terminaison de protocole envoient et reçoivent les données transférées.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ ForwardingService**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Service de transfert qui transfère les données.

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

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> </dl>

 

