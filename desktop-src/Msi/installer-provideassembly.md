---
description: La méthode ProvideAssembly de l’objet installer retourne le chemin d’accès installé d’un assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Programme d’installation ::P méthode rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542727"
---
# <a name="installerprovideassembly-method"></a>Programme d’installation ::P méthode rovideAssembly

La méthode **ProvideAssembly** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès installé d’un assembly.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*assembly* 
</dt> <dd>

Nom fort de l’assembly installé à interroger.

</dd> <dt>

*appContext* 
</dt> <dd>

Affectez la valeur null pour les assemblys globaux. Pour les assemblys privés, définissez *appContext* sur le chemin d’accès complet du fichier de configuration de l’application ou sur le chemin d’accès complet du fichier exécutable de l’application dans laquelle l’assembly a été rendu privé.

</dd> <dt>

*installMode* 
</dt> <dd>

Définit le mode d’installation. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                                                                              | Signification                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | Fournissez le composant et effectuez toute installation nécessaire pour fournir le composant. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | Fournissez le composant uniquement si la fonctionnalité existe. Cette option permet de vérifier l’existence de l’assembly.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | Fournissez le composant uniquement si la fonctionnalité existe. Cette option ne vérifie pas l’existence de l’assembly.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | Fournit l’assembly uniquement si l’assembly est installé en local.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Combinaison des indicateurs utilisés par [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt> </dl> | Appelle la méthode [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour *ReinstallMode*, puis retourne le chemin d’accès de l’assembly.<br/> |



 

</dd> <dt>

*assemblyInfo* 
</dt> <dd>

Informations d’assembly et type d’assembly. Définissez l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                       | Signification                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | Assembly .NET.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Assembly côte à côte Win32.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chemin d’accès à l’assembly installé.

## <a name="remarks"></a>Notes

La méthode **ProvideAssembly** utilise la fonction [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .

## <a name="examples"></a>Exemples

L’exemple de script suivant illustre l’utilisation de la méthode ProvideAssembly.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 et Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Programme d’installation**](installer-object.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




