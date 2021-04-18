---
description: La méthode AdvertiseScript de l’objet installer publie un package d’installation.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: 'Installer :: AdvertiseScript, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7e4ec5afae8d870511c6f91502f8b5844ce135bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533067"
---
# <a name="installeradvertisescript-method"></a>Installer :: AdvertiseScript, méthode

La méthode **AdvertiseScript** de l’objet [**installer**](installer-object.md) publie un package d’installation.

## <a name="syntax"></a>Syntaxe


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*scriptPath* 
</dt> <dd>

Chemin d’accès complet au fichier de script généré par la méthode [**CreateAdvertiseScript**](installer-createadvertisescript.md) .

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Indicateurs qui contrôlent la publication. Ce paramètre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**msiAdvertiseScriptCacheInfo**</dt> <dt>0x001</dt> </dl>                                                                 | Incluez cet indicateur si les icônes doivent être créées ou supprimées.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiAdvertiseScriptShortcuts**</dt> <dt>0x004</dt> </dl>                                                                 | Incluez cet indicateur si les raccourcis doivent être créés ou supprimés.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiAdvertiseScriptMachineAssign**</dt> <dt>0x008</dt> </dl>                                                 | Incluez cet indicateur si le produit doit être attribué à un ordinateur.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptConfigurationRegistration**</dt> <dt>0x020</dt> </dl> | Incluez cet indicateur si les informations de configuration et de gestion des données du Registre doivent être écrites ou supprimées.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**msiAdvertiseScriptValidateTransformList**</dt> <dt>0x040</dt> </dl>                 | Incluez cet indicateur pour forcer la validation des transformations répertoriées dans le script par rapport aux transformations précédemment inscrites pour ce produit. Notez que les conflits de transformation sont détectés à l’aide d’une comparaison de chaînes qui ne respecte pas la casse et sont évaluées entre les installations par utilisateur et par ordinateur dans tous les [contextes d’installation](installation-context.md).<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptClassInfoRegistration**</dt> <dt>0x080</dt> </dl>                 | Incluez cet indicateur si les informations de publication dans le Registre liées aux classes COM doivent être écrites ou supprimées.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptExtensionInfoRegistration**</dt> <dt>0x100</dt> </dl> | Incluez cet indicateur si les informations de publication dans le Registre relatives à une extension doivent être écrites ou supprimées.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**msiAdvertiseScriptAppInfo**</dt> <dt>0x180</dt> </dl>                                                                         | Incluez cet indicateur si les informations sur la publication dans le registre doivent être écrites ou supprimées.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**msiAdvertiseScriptRegData**</dt> <dt>0x1A0</dt> </dl>                                                                         | Incluez cet indicateur si les informations sur la publication dans le registre doivent être écrites ou supprimées.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE si les éléments spécifiés doivent être supprimés au lieu d’être créés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **AdvertiseScript** utilise la fonction [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) . L’utilisation de la méthode **AdvertiseScript** nécessite que le script s’exécute dans un processus de système local.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **AdvertiseScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
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

 

 




