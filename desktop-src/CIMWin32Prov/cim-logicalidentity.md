---
description: La \_ classe LOGICALIDENTITY CIM est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950495"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>CIM_LogicalIdentity, classe (fournisseurs WMI CIMWin32)

La **classe \_ LogicalIdentity CIM** est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente. L’Association transmet ce qui peut être défini avec un héritage multiple et est limité aux aspects logiques d’un élément système géré. Dans la plupart des scénarios, la relation d’identité est déterminée par l’équivalence des clés, ou d’autres propriétés d’identification des éléments associés.

L’Association doit être utilisée uniquement dans les scénarios bien compris, ce qui permet une définition et une clarification plus concrètes dans les sous-classes. Un scénario dans lequel la relation est raisonnable, par exemple, représente un appareil qui est à la fois une entité de bus et une entité fonctionnelle où l’appareil est une entité USB (bus) et un clavier (fonctionnel).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LogicalIdentity** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LogicalIdentity** possède les propriétés suivantes.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un autre aspect de l’entité système.

</dd> <dt>

**SYSTEME**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un aspect de l’élément logique.

</dd> </dl>

## <a name="remarks"></a>Notes

WMI n’implémente pas cette classe. Pour les classes dérivées de **CIM \_ LogicalIdentity**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




