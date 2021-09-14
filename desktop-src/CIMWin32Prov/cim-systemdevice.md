---
description: L' \_ Association CIM SystemDevice représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: CIM_SystemDevice, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225305"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a>CIM_SystemDevice, classe (fournisseurs WMI CIMWin32)

L’Association **CIM \_ SystemDevice** représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SystemDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SystemDevice** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ système CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Système CIM**](cim-system.md) qui décrit le système parent dans l’Association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil logique qui est un composant d’un système.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ SystemDevice** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

WMI n’implémente pas cette classe. Pour les classes WMI dérivées de **CIM \_ SystemDevice**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Spécifications



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

 

