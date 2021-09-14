---
description: La \_ classe DesktopWMI Win32 représente les caractéristiques courantes du Bureau d’un utilisateur. Les propriétés de cette classe peuvent être modifiées par l’utilisateur pour personnaliser le bureau.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Classe Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921884"
---
# <a name="win32_desktop-class"></a>\_Classe de bureau Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) du **\_ Bureau Win32** représente les caractéristiques courantes du Bureau d’un utilisateur. Les propriétés de cette classe peuvent être modifiées par l’utilisateur pour personnaliser le bureau.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Membres

La **classe \_ Desktop Win32** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ Bureau Win32** possède ces propriétés.

<dl> <dt>

**BorderWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Bureau \\ \\ WindowMetrics \| BorderWidth»)
</dt> </dl>

Largeur des bordures autour de toutes les fenêtres avec des bordures réglables.

Exemple : 3

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**CoolSwitch**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| panneau de configuration \\ \\ Desktop \| CoolSwitch »)
</dt> </dl>

Le changement rapide de tâches est activé. Le changement rapide de tâches permet à l’utilisateur de basculer entre les fenêtres à l’aide de la combinaison de touches **Alt + Tab** .

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| panneau de configuration \\ \\ \| CursorBlinkRate"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondes")
</dt> </dl>

Durée entre les clignotements successifs du curseur.

Exemple : 530

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

**DragFullWindows**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| panneau de configuration \\ \\ Desktop \| DragFullWindows »)
</dt> </dl>

Le contenu d’une fenêtre s’affiche lorsqu’un utilisateur déplace la fenêtre.

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| panneau de configuration \\ \\ \| GridGranularity"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")
</dt> </dl>

Espacement de la grille à laquelle les fenêtres sont liées sur le bureau. Cela facilite l’Organisation des fenêtres. L’espacement est généralement suffisamment précis pour que l’utilisateur ne le remarque pas.

Exemple : 1

</dd> <dt>

**IconSpacing**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")
</dt> </dl>

Espacement entre les icônes.

Exemple : 75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconFont»)
</dt> </dl>

Police utilisée pour les noms des icônes.

Exemple : « MS San Serif »

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| font and Text structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")
</dt> </dl>

Taille de police de l’icône.

Exemple : 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap»)
</dt> </dl>

Le texte du titre de l’icône revient à la ligne suivante.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Nom qui identifie le profil de bureau actuel.

Exemple : « MainProf »

</dd> <dt>

**Modèle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Modèle de bureau du panneau de configuration par défaut \\ \\ \| ")
</dt> </dl>

Nom du modèle utilisé comme arrière-plan du bureau.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaveActive ")
</dt> </dl>

L’économiseur d’écran est actif.

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\SCRNSAVE.EXE de bureau \| »)
</dt> </dl>

Nom du fichier exécutable de l’économiseur d’écran actuel.

Exemple : «LOGON. SCR

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaverIsSecure ")
</dt> </dl>

Le mot de passe est activé pour l’économiseur d’écran.

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaveTimeOut "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ")
</dt> </dl>

Durée écoulée avant le démarrage de l’économiseur d’écran.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**Papier peint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ \| Papier peint du bureau ")
</dt> </dl>

Nom de fichier pour la conception du papier peint sur l’arrière-plan du bureau.

Exemple : « WINNT.BMP »

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| WallpaperStyle ")
</dt> </dl>

Le papier peint est étiré pour remplir tout l’écran. Microsoft plus ! doit être installé pour que cette option soit disponible. Si la **valeur est false**, le papier peint conserve ses dimensions d’origine sur l’arrière-plan du bureau.

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| TileWallpaper ")
</dt> </dl>

Le papier peint est en mosaïque ou centré.

</dd> </dl>

## <a name="remarks"></a>Notes

La **classe \_ Bureau Win32** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

le processus appelant qui utilise cette classe doit avoir le privilège **SE \_ restore \_ NAME** sur l’ordinateur où se trouve le registre. Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège. Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Exemples

L’exemple de code suivant décrit comment récupérer des informations sur le bureau.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



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

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

