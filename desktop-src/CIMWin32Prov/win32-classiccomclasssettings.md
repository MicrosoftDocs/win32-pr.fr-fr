---
description: La \_ classe WMI de l’Association Win32 ClassicCOMClassSettings lie une classe com (Component Object Model) et les paramètres utilisés pour configurer des instances de la classe com.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860698"
---
# <a name="win32_classiccomclasssettings-class"></a>\_Classe ClassicCOMClassSettings Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **Win32 \_ CLASSICCOMCLASSSETTINGS** lie une classe com (Component Object Model) et les paramètres utilisés pour configurer des instances de la classe com.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ClassicCOMClassSettings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ClassicCOMClassSettings** a ces propriétés.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ClassicCOMClass**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

[**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) qui représente la classe com dans laquelle les paramètres sont appliqués.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ClassicCOMClassSetting**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")
</dt> </dl>

[**\_ ClassicCOMClassSetting Win32**](win32-classiccomclasssetting.md) qui représente les paramètres de configuration associés à la classe com.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ ClassicCOMClassSettings** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

