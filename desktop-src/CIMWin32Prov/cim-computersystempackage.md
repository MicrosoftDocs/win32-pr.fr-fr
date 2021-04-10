---
description: La \_ classe CIM ComputerSystemPackage représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950697"
---
# <a name="cim_computersystempackage-class"></a>\_Classe CIM ComputerSystemPackage

La classe **CIM \_ ComputerSystemPackage** représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques. L’Association est semblable à la façon dont les unités logiques sont réalisées par les éléments physiques.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ComputerSystemPackage** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ComputerSystemPackage** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalPackage**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le ou les packages physiques qui réalisent un système informatique unitaire.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ UnitaryComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

[**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) qui décrit le système informatique unitaire.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ ComputerSystemPackage** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

 

