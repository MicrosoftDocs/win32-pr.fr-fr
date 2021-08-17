---
description: La \_ classe CIM InstalledSoftwareElement associe un système informatique à un élément logiciel installé.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: Classe CIM_InstalledSoftwareElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33670db4836b193135786363f961ce7809eeaefa2eb9886a5f46e2a97889dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438709"
---
# <a name="cim_installedsoftwareelement-class"></a>\_Classe CIM InstalledSoftwareElement

La classe **CIM \_ InstalledSoftwareElement** associe un système informatique à un élément logiciel installé.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ InstalledSoftwareElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ InstalledSoftwareElement** possède les propriétés suivantes.

<dl> <dt>

**Logiciels**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SoftwareElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)
</dt> </dl>

Référence à l’élément logiciel installé sur le système informatique.

</dd> <dt>

**Système**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)
</dt> </dl>

Référence au système informatique hébergeant un élément logiciel particulier.

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe. Pour les classes dérivées de **CIM \_ InstalledSoftwareElement**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

