---
description: L' \_ Association CIM PackageCooling représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: Classe CIM_PackageCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dcb6727e909936e08ba8506c1a99855136c0a9725c746503dbf7fd7626515df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820629"
---
# <a name="cim_packagecooling-class"></a>\_Classe CIM PackageCooling

L’Association **CIM \_ PackageCooling** représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ PackageCooling** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ PackageCooling** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ CoolingDevice**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ CoolingDevice CIM**](cim-coolingdevice.md) qui décrit l’appareil de refroidissement pour le package.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalPackage**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le package physique dont l’environnement est refroidi.

</dd> </dl>

## <a name="remarks"></a>Remarques

**CIM \_ PackageCooling** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).

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

 

