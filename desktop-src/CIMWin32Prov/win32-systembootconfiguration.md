---
description: La \_ classe WMI de l’Association SystemBootConfiguration Win32 associe un système informatique et sa configuration de démarrage.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Classe Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad5b30d42e94391163a4a54836877f90415225d0ae697e719e6c088f432430cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416752"
---
# <a name="win32_systembootconfiguration-class"></a>\_Classe SystemBootConfiguration Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemBootConfiguration Win32** associe un système informatique et sa configuration de démarrage.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemBootConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemBootConfiguration** a ces propriétés.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Référence à l’instance de qui représente le système informatique à l’aide de la configuration de démarrage.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ BootConfiguration**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")
</dt> </dl>

Référence à l’instance représentant la configuration de démarrage pour le système informatique.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ SystemBootConfiguration** est dérivée de [**Win32 \_ SystemSetting**](win32-systemsetting.md).

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

[**\_SystemSetting Win32**](win32-systemsetting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
