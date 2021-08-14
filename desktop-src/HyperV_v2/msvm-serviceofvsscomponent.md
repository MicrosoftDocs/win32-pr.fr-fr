---
description: Association entre une instance de MSVM \_ VssComponent et une instance de MSVM \_ VssService qui représente un service pour l’exécution d’opérations sur le composant VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a96c59a2e483080293ece2281ddb64fc9a7b43b425e5b508fe7ec209d1144dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950538"
---
# <a name="msvm_serviceofvsscomponent-class"></a>MSVM \_ ServiceOfVssComponent, classe

Association entre une instance de [**MSVM \_ VssComponent**](msvm-vsscomponent.md) et une instance de [**MSVM \_ VssService**](msvm-vssservice.md) qui représente un service pour l’exécution d’opérations sur le composant VSS.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ServiceOfVssComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ServiceOfVssComponent** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ VssComponent**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

[**MSVM \_ VssComponent**](msvm-vsscomponent.md) qui représente le composant VSS.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ VssService**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")
</dt> </dl>

[**MSVM \_ VssService**](msvm-vssservice.md) qui représente le service VSS IC.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

