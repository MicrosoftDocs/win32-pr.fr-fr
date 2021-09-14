---
description: La \_ classe CIM SoftwareFeatureSAPImplementation représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095102"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>\_Classe CIM SoftwareFeatureSAPImplementation

La classe **CIM \_ SoftwareFeatureSAPImplementation** représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel. Un SAP peut être fourni par plusieurs fonctionnalités logicielles pour fonctionner conjointement. En outre, une fonctionnalité logicielle peut fournir plusieurs SAP. Lorsque de nombreuses fonctionnalités logicielles sont associées à un seul SAP, il est supposé que les éléments fonctionnent conjointement pour fournir le point d’accès. Si différentes implémentations d’un SAP existent, chaque implémentation entraînerait des instanciations individuelles de l’objet SAP. Les instanciations individuelles ont alors des associations avec les implémentations uniques.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SoftwareFeatureSAPImplementation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SoftwareFeatureSAPImplementation** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SoftwareFeature**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ SoftwareFeature CIM**](cim-softwarefeature.md) qui décrit la fonctionnalité de logiciel antécédent.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service dépendant.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ SoftwareFeatureSAPImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

