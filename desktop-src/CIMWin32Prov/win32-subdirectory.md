---
description: La \_ classe WMI d’association de sous-répertoires Win32 lie un répertoire (dossier) et l’un de ses sous-répertoires (sous-dossiers).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111199"
---
# <a name="win32_subdirectory-class"></a>\_Classe de sous-répertoire Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) d’association de **\_ sous-répertoires Win32** lie un répertoire (dossier) et l’un de ses sous-répertoires (sous-dossiers).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe de **\_ sous-répertoire win32** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ sous-répertoire win32** possède ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| répertoire Win32 WMI \_ ")
</dt> </dl>

Référence à l’instance représentant les propriétés du répertoire parent (dossier) dans cette association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« PartComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| répertoire win32 Win32 \_ »)
</dt> </dl>

Référence à l’instance représentant le sous-répertoire (sous-dossier) qui fait partie de l’Association.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ sous-répertoire win32** est dérivée du [**\_ composant CIM**](cim-component.md).

Pour retourner une collection de sous-dossiers d’un dossier, créez une requête d’association qui définit *ResultRole* sur *PartComponent*. Cela indique que tous les éléments de la collection retournée doivent jouer le rôle d’un PartComponent, ou sous-dossier, de l’objet Folder. Pour retourner le dossier parent d’un dossier, affectez à *ResultRole* la valeur *GroupComponent*.

La classe de **\_ sous-répertoire win32** fonctionne uniquement au niveau du système de fichiers juste au-dessus ou immédiatement au-dessous du dossier spécifié.

## <a name="examples"></a>Exemples

L’exemple VBScript suivant retourne une liste de tous les sous-dossiers dans le dossier C : \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



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

[**\_Composant CIM**](cim-component.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
