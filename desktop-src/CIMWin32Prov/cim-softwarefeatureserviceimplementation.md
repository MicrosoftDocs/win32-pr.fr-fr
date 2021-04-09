---
description: La \_ classe CIM SoftwareFeatureServiceImplementation représente une association entre un service et la manière dont il est implémenté dans le logiciel.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110178"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a>\_Classe CIM SoftwareFeatureServiceImplementation

La classe **CIM \_ SoftwareFeatureServiceImplementation** représente une association entre un service et la manière dont il est implémenté dans le logiciel. Un service peut être fourni par plusieurs fonctionnalités logicielles, qui fonctionnent conjointement les unes avec les autres. En outre, une fonctionnalité logicielle peut fournir plusieurs services. Lorsque plusieurs fonctionnalités logicielles sont associées à un seul service, il est supposé que les éléments fonctionnent conjointement pour fournir le service. Si différentes implémentations d’un service existent, chaque implémentation entraînerait des instanciations individuelles de l’objet de service. Les instanciations individuelles ont alors des associations avec les implémentations uniques.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SoftwareFeatureServiceImplementation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SoftwareFeatureServiceImplementation** possède les propriétés suivantes.

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

Type de données **: \_ service CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

[**\_ Service CIM**](cim-service.md) qui décrit le service dépendant.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ SoftwareFeatureServiceImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



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

 

