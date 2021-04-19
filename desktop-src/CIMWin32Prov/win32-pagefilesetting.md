---
description: Le \_ PageFileSetting Win32&\# 8194 ; La classe WMI représente les paramètres d’un fichier d’échange.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Classe Win32_PageFileSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515794"
---
# <a name="win32_pagefilesetting-class"></a>\_Classe PageFileSetting Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PageFileSetting** représente les paramètres d’un fichier d’échange. Les informations contenues dans les objets instanciés à partir de cette classe spécifient les paramètres du fichier d’échange utilisés lors de la création du fichier au démarrage du système. Les propriétés de cette classe peuvent être modifiées et différées jusqu’au démarrage. Ces paramètres sont différents de l’état d’exécution d’un fichier d’échange exprimé via la classe associée [**Win32 \_ PageFileUsage**](win32-pagefileusage.md).

Pour créer une instance de cette classe, activez le privilège **SeCreatePagefilePrivilege** . Pour plus d’informations, consultez [**constantes de privilège**](../wmisdk/privilege-constants.md) et [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PageFileSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PageFileSetting** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| PagingFiles »), [**Units**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)
</dt> </dl>

Taille initiale du fichier d’échange.

Exemple : 139

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| PagingFiles »), [**Units**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)
</dt> </dl>

Taille maximale du fichier d’échange.

Exemple : 178

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Chemin d’accès et nom de fichier du fichier d’échange.

Exemple : « C : \\PAGEFILE.SYS »

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ PageFileSetting** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

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

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
