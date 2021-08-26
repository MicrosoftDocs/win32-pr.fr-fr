---
description: Cette classe représente l’association entre un système d’exploitation et les paramètres Autochk qui s’appliquent aux disques sur l’ordinateur. Notez que le paramètre est associé au système d’exploitation plutôt qu’au système informatique, car il peut y avoir un ou plusieurs systèmes d’exploitation installés sur l’ordinateur, chacun avec ses propres paramètres Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972539"
---
# <a name="win32_operatingsystemautochksetting-class"></a>\_Classe OperatingSystemAutochkSetting Win32

Cette classe représente l’association entre un système d’exploitation et les paramètres Autochk qui s’appliquent aux disques sur l’ordinateur. Notez que le paramètre est associé au système d’exploitation plutôt qu’au système informatique, car il peut y avoir un ou plusieurs systèmes d’exploitation installés sur l’ordinateur, chacun avec ses propres paramètres Autochk.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ OperatingSystemAutochkSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ OperatingSystemAutochkSetting** a ces propriétés.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ OperatingSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ AutochkSetting**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> </dl>

 

 
