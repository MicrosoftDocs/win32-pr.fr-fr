---
description: La \_ classe CIM ElementCapacity associe un \_ objet PhysicalCapacity CIM à un ou plusieurs éléments physiques. Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483376"
---
# <a name="cim_elementcapacity-class"></a>\_Classe CIM ElementCapacity

La classe **CIM \_ ElementCapacity** associe un objet [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md) à un ou plusieurs éléments physiques. Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ElementCapacity** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ElementCapacity** possède les propriétés suivantes.

<dl> <dt>

**Capacité**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalCapacity**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à la classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) qui décrit les exigences minimales et maximales et la capacité à prendre en charge différents types de matériel pour un élément physique.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Référence à l’élément physique qui est décrit.

</dd> </dl>

## <a name="remarks"></a>Notes

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



 

