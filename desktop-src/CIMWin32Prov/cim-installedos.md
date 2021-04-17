---
description: La \_ classe d’association CIM installos représente un lien entre le système de l’ordinateur et le système d’exploitation installé.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Classe CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523764"
---
# <a name="cim_installedos-class"></a>\_Classe CIM installée

La classe d’association **CIM \_ installos** représente un lien entre le système de l’ordinateur et le système d’exploitation installé. Un système d’exploitation est installé lorsqu’il se trouve dans l’extension de stockage d’un système d’ordinateur (par exemple, copié sur un lecteur de disque ou téléchargé en mémoire).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ installed** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ installed** possède ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) décrivant le système informatique.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ OperatingSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) qui décrit le système d’exploitation installé sur le système informatique.

</dd> <dt>

**Serveur primaire**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Système d’exploitation DMTF \| 001,4»)
</dt> </dl>

Si la **valeur est true**, le système d’exploitation installé est le système d’exploitation par défaut pour le système informatique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ installed** est dérivée de [**la \_ SystemComponent CIM**](cim-systemcomponent.md).

WMI n’implémente pas cette classe. Pour les classes dérivées de **CIM \_ installed**, consultez [classes Win32](win32-provider.md).

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

 

