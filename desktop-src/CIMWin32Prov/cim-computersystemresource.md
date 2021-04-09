---
description: La \_ classe CIM ComputerSystemResource représente une association entre un système informatique et les ressources système disponibles.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033715"
---
# <a name="cim_computersystemresource-class"></a>\_Classe CIM ComputerSystemResource

La classe **CIM \_ ComputerSystemResource** représente une association entre un système informatique et les ressources système disponibles.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ComputerSystemResource** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ComputerSystemResource** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SystemResource**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ SystemResource CIM**](cim-systemresource.md) qui décrit une ressource système du système informatique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ ComputerSystemResource** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

WMI n’implémente pas cette classe. Pour plus d’informations sur les classes dérivées de **CIM \_ ComputerSystemResource**, consultez [classes Win32](win32-provider.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

