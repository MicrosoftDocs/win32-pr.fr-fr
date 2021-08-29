---
description: La \_ classe d’association CIM SoftwareElementChecks associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2912f17b35ce3134a7ba66df7fa8630720aa755ae75eb4923863e3f541fbf9a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919219"
---
# <a name="cim_softwareelementchecks-class"></a>\_Classe CIM SoftwareElementChecks

La classe d’association **CIM \_ SoftwareElementChecks** associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.

Étant donné que les éléments logiciels dans un état prêt à être en cours d’exécution ne peuvent pas passer à un autre État, la valeur de la propriété **phase** est limitée à in-State pour les objets [**CIM \_ SoftwareElement**](cim-softwareelement.md) dans un état prêt à être exécuté.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SoftwareElementChecks** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SoftwareElementChecks** possède les propriétés suivantes.

<dl> <dt>

**Vérification**
</dt> <dd> <dl> <dt>

Type de données **: \_ vérification CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à la vérification.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SoftwareElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à l’élément.

</dd> <dt>

**Phase**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le contrôle référencé est un contrôle à l’État ou un contrôle d’état suivant.

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**In-State** (0)


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**État suivant** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe. Pour les classes WMI dérivées de **CIM \_ SoftwareElementChecks**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

