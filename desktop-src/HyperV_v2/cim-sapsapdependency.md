---
description: Représente une association entre deux points d’accès de service (SAP), dans laquelle un SAP dépend de l’autre pour utiliser un service ou s’y connecter.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: Classe CIM_SAPSAPDependency (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526781"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a>Classe CIM_SAPSAPDependency (gestion Hyper-V)

Représente une association entre deux points d’accès de service (SAP), dans laquelle un SAP dépend de l’autre pour utiliser un service ou s’y connecter. Par exemple, pour imprimer sur une imprimante réseau, les points d’accès d’impression locaux doivent utiliser des SAP liés au réseau sous-jacents pour envoyer la demande d’impression.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SAPSAPDependency** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SAPSAPDependency** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Une référence au SAP requis.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à la fonction SAP dépendante.

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

