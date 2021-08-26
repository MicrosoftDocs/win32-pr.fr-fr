---
description: La \_ classe WMI d’association CIMLogicalDeviceCIMDataFile Win32 associe des périphériques logiques et des fichiers de données, indiquant les fichiers de pilote utilisés par l’appareil. Cette classe est utilisée pour détecter les pilotes de périphérique utilisés par un périphérique.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Classe Win32_CIMLogicalDeviceCIMDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8124031c07091399241ce355eef0a499235892bff3875e4248641f0454671540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917979"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a>\_Classe CIMLogicalDeviceCIMDataFile Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) d’association **\_ CIMLogicalDeviceCIMDataFile Win32** associe des périphériques logiques et des fichiers de données, indiquant les fichiers de pilote utilisés par l’appareil. Cette classe est utilisée pour détecter les pilotes de périphérique utilisés par un périphérique.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique utilisé par le fichier de données.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ fichier** de données CIM
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier de \| fichier CIM CIM \_ »)
</dt> </dl>

Fichier de données [**CIM \_**](cim-datafile.md) qui représente les propriétés du fichier de données affecté à l’unité logique.

</dd> <dt>

**Objectif**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Rôle joué par le fichier de données en ce qui concerne son appareil logique associé.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

**Pilote** (2)


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

**Logiciel de configuration** (3)


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

**Logiciel d’application** (4)


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

**Instrumentation** (5)


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

**Microprogramme** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Étend la valeur de la propriété **Purpose** de cette classe.

Exemple : « lecteur de disquette »

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** est dérivée de la [**\_ dépendance CIM**](cim-logicaldevice.md).

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

