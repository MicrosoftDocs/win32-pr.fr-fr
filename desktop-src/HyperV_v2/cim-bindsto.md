---
description: Représente une association dans laquelle un \_ objet SERVICEACCESSPOINT CIM demande des services de protocole à partir d’un \_ objet ProtocolEndpoint CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Classe CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519365"
---
# <a name="cim_bindsto-class"></a>\_Classe CIM BindsTo

Représente une association dans laquelle un objet [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) demande des services de protocole à partir d’un objet [**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ BindsTo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ BindsTo** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ ProtocolEndpoint CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Point de terminaison de niveau inférieur auquel accède le point d’accès au service.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Point d’accès ou point de terminaison de protocole qui est dépendant du point de terminaison de niveau inférieur.

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

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

