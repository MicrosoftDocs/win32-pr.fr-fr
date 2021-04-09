---
description: Le \_ StartupCommand Win32&\# 8194 ; La classe WMI représente une commande qui s’exécute automatiquement lorsqu’un utilisateur ouvre une session sur le système informatique.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Classe Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861581"
---
# <a name="win32_startupcommand-class"></a>\_Classe StartupCommand Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand** WMI représente une commande qui s’exécute automatiquement lorsqu’un utilisateur ouvre une session sur le système informatique.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ StartupCommand** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ StartupCommand** a ces propriétés.

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

**Commande**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run »)
</dt> </dl>

Commande exécutée par la commande de démarrage.

WMI obtient ces données à partir de la clé de Registre

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**

Exemple : « C : \\ Windows \\notepad.exe myfile.txt »

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

**Lieu**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows »)
</dt> </dl>

Chemin d’accès où la commande de démarrage réside sur le système de fichiers du disque.

Par exemple : HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Startup** (« Startup »)


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Démarrage commun** (« démarrage commun »)


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\ LOGICIEL \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** (« HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run »)


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de fichiers win32api \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")
</dt> </dl>

Nom de fichier de la commande de démarrage.

Exemple : « FindFast »

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

</dd> <dt>

**Utilisateur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Nom d’utilisateur pour lequel cette commande de démarrage s’exécutera.

Exemple : « MyDomain \\ myname »

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

La propriété UserSID indique le SID de l’utilisateur pour lequel cette commande de démarrage s’exécutera. Cette propriété d’utilisateur peut être vide, mais UserSID a toujours une valeur si le nom d’utilisateur ne peut pas être résolu (comme dans le cas d’un utilisateur supprimé). La propriété permet de faire la distinction entre les commandes associées à w/deux utilisateurs avec des noms non résolus. Il peut s’agir de la valeur NULL lorsque la commande est associée à des éléments qui n’identifient pas réellement un utilisateur comme tous les utilisateurs.

Exemple : S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ StartupCommand** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

Le démarrage de l’ordinateur ne se termine pas après le chargement du système d’exploitation. Au lieu de cela, le système d’exploitation Windows peut être configuré de sorte que les commandes de démarrage soient exécutées à chaque démarrage de Windows. Les commandes de démarrage sont stockées dans le registre ou dans le cadre du profil utilisateur et sont utilisées pour démarrer automatiquement des scripts ou des applications spécifiés à chaque fois que Windows est chargé.

Dans la plupart des cas, les programmes AutoStart sont utiles. ils garantissent que certaines applications, telles que les outils antivirus, sont automatiquement démarrées et exécutées chaque fois que Windows est chargé. Toutefois, les programmes de démarrage automatique peuvent également être responsables des problèmes tels que :

-   Les ordinateurs qui prennent beaucoup de temps à démarrer. Cela peut être dû à un grand nombre d’applications qui doivent être démarrées à chaque démarrage de Windows.
-   Applications qui sont représentées dans la barre des tâches ou dans le gestionnaire des tâches, même si l’utilisateur ne les a pas démarrées. Bien que ces applications ne causent pas nécessairement des problèmes, elles peuvent entraîner des appels au support technique émis par des utilisateurs qui se sont déconcertés en ce qui concerne l’origine de ces programmes et pourquoi ils sont en cours d’exécution.
-   Ordinateurs rencontrant des problèmes même lorsqu’ils semblent inactifs. Ces problèmes sont souvent suivis dans des commandes de démarrage qui s’exécutent lorsque personne n’est conscient qu’elles sont en cours d’exécution.

L’identification des applications et des scripts qui s’exécutent automatiquement au démarrage est une tâche administrative importante mais difficile, car les commandes de démarrage peuvent être stockées dans différents emplacements :

-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   \\Logiciel HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   \\Logiciel HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   \\fichiers du lecteur_système et paramètres \\ tous les utilisateurs \\ démarrage des \\ programmes du menu démarrer \\
-   lecteur_système \\ Documents and Settings \\ NomUtilisateur \\ menu démarrer \\ programmes \\ démarrage

Vous pouvez utiliser la classe WMI Win32 \_ StartupCommand pour énumérer les programmes de démarrage automatique, quel que soit l’emplacement de stockage des informations.

Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre. Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège. Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).

Vous pouvez modifier les valeurs de Registre dans lesquelles **Win32 \_ StartupCommand** obtient des données en appelant les méthodes de [fournisseur du Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI dans un script ou en C++. Pour plus d’informations, consultez [modification du Registre système](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Exemples

Le code VBScript suivant énumère les commandes de démarrage sur un ordinateur.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
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

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
