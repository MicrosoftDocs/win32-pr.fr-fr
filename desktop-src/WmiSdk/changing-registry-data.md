---
description: 'La classe de fournisseur de Registre système StdRegProv pour WMI a des méthodes qui effectuent les opérations suivantes :'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Modification des données de Registre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106545198"
---
# <a name="changing-registry-data"></a>Modification des données de Registre

La classe de [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) pour WMI a des méthodes qui effectuent les opérations suivantes :

-   Créez ou supprimez des clés de registre.

    Utilisez [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) ou [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).

-   Créez ou supprimez des valeurs nommées, appelées entrées lorsqu’elles sont sous clés.

    Utilisez le nom d’une nouvelle valeur et [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)ou [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) pour créer une valeur nommée. Utilisez [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) pour supprimer une valeur nommée.

-   Modifiez les valeurs nommées.

    Utilisez le nom d’une valeur et les méthodes définies (identifiées dans l’élément à puce précédent) pour modifier les valeurs nommées existantes sous une clé. Vous devez connaître le nom d’une valeur pour la modifier. Si vous ne connaissez pas les noms de valeur sous une clé, utilisez la méthode [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) pour obtenir les noms.

Les sections suivantes sont présentées dans cette rubrique :

-   [Création d’une clé de Registre à l’aide de VBScript](#creating-a-registry-key-using-vbscript)
-   [Création d’une valeur de Registre nommée à l’aide de PowerShell et VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Création d’une clé de Registre à l’aide de VBScript

Étant donné que le Registre est la base de données de configuration centrale pour le système d’exploitation, les applications et les services, soyez prudent lorsque vous écrivez des modifications apportées à des valeurs de registre ou supprimez des clés.

> [!Note]  
> Vous ne pouvez pas surveiller la sous-clé **\_ \_ racine HKEY classes** de **HKEY \_ Current \_ User (HKCU)**. La surveillance des **\_ utilisateurs HKEY** n’est pas recommandée, car les sous-clés apparaissent et disparaissent au fur et à mesure que les ruches sont chargées.

 

Les exemples de code suivants montrent comment créer une nouvelle clé de Registre et une sous-clé.


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Création d’une valeur de Registre nommée à l’aide de PowerShell et VBScript

L’exemple de code suivant montre comment créer une valeur nommée appelée **MultiStringValue** sous la clé **HKEY \_ local \_ machine** \\ **Software** \\ **MyKey** \\ **MySubKey** créée par le script précédent. Le script appelle [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) pour écrire des valeurs de chaîne dans une nouvelle valeur nommée.


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

À l’aide de WMI, vous ne pouvez pas définir la sécurité d’accès sur une clé de registre. Toutefois, la méthode [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compare les paramètres de sécurité de l’utilisateur actuel au descripteur de sécurité sur une clé de Registre pour déterminer si l’utilisateur dispose d’une autorisation spécifique, telle que la **valeur du \_ jeu \_ de clés**.
