---
description: L' \_ Association de composants CIM représente les parties d’une relation entre les MSEs.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: CIM_Component, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7b47aa88c7cf1238f74a9cb359ddb5f499c2a77b34de0f89023c83bd67420722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065179"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a>CIM_Component, classe (fournisseurs WMI CIMWin32)

L’Association de **\_ composants CIM** représente les parties d’une relation entre les MSEs.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe de **\_ composant CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ composant CIM** possède ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément parent dans l’Association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément enfant dans l’Association.

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe. Pour plus d’informations sur les classes dérivées du **\_ composant CIM**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

